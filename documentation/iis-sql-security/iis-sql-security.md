---
layout: page-with-navigation
title: IIS & SQL Security
permalink: /documentation/iis-sql-security/
navigation-bar:
    - Reference: simplified-security
      Title: Simplified security
    - Reference: secure-calls-to-sql
      Title: Secure calls to SQL
    - Reference: individual-security
      Title: Individual security
---


There are a number of ways to secure your SQL data. No method is perfect for everyone, each has pros and cons; use these options as a guide to help determine the best solution for you:

Simplified security
-------------------

####Simplified security / Standalone or trusted environment

If you are hosting the web server and SQL server on a single PC and have a single user, then you may find it convenient to use many out-of-the-box defaults and to secure your data through standard windows logon.

In other words, you rely on your existing windows logon to access the PC, and in turn the data. The Rantt Web Host and SQL data are secured in the same way as say an Excel spread sheet on your PC; if you can log on to your PC, then you provide access to the data on your PC.

If this level of security is sufficient, and you wish to "hide" the web host and SQL data, then you set IIS and SQL for local access only, and set Windows Firewall to block incoming web requests and SQL access across the network/LAN

The connection string used in the Rantt project file would typically be like this (change server, SQL instance and database to suit), if using Windows Authentication:

    <ConnectionString Data Source=SERVERSQLEXPRESS;Initial Catalog=DATABASENAME;Integrated Security=True</ConnectionString>

or if using SQL authentication, similar to this:

    <ConnectionString>Data Source=SERVERSQLEXPRESS;Initial Catalog=DATABASENAME;User Id=MYSQLUSER;Password=MYSQLPASSWORD</ConnectionString>



Secure calls to SQL
-------------------

#####Access Rantt Web Host with secure calls to SQL - without exposing passwords

If all staff are allowed unrestricted access to Rantt Web Host, but you would like to secure SQL without adding many individual user accounts, then consider creating a special user account that is just used for Rantt Web Host to query SQL server.

Advantages:

-   simple; requires just one user account to be created
-   secure; password is not required when setting up new Rantt Web Host projects
-   easy to setup; one user account + password needs to be entered in two places into IIS

Disadvantages:

-   none

To set up this system of security:

1. Create a new user account; if IIS and SQL are on the same PC/server, then this can be a local account

2. Add the new user to SQL Server Security/Logins, under "Server Roles" check "public, under "User Mapping" check the box beside the SQL database(es) required, and then check "public" in the lower pane, click OK.

3. Create a new Application Pool. In IIS Manager, highlight "Application Pools", click "Add Application Pool", create a name such as "RanttWebHost", choose .Net 40 and Integrated pipeline mode, click OK Right click this newly created App Pool, click Advanced Settings, scroll down to Process Model/Identity, click the   [ . ] button, change from Built-in Account to Custom Account, click Set button, choose the user account you created in (A) above You will need to enter the password and then again to verify, then click OK

4. Change the identify of the IIS web process In IIS Manager, highlight the Rantt Web Host website "SMS", double click "Authentication", right click Anonymous Authentication (normally the only entry enabled), click Edit. Change from "Specific User" (normally IUSR) to  "Application Pool Identity", click OK

Now any user visiting the Rantt Web Host website will be able to use a Rantt project file to access SQL The username is not exposed outside of the Rantt project file, and the password is not exposed at all to end users.

 

The connection string used in the Rantt project file would typically be like this (change server, SQL instance and database to suit). The username does not need to be specified, as it relies on Windows Authentication between IIS and SQL:


    <ConnectionString>Data Source=SERVERSQLEXPRESS;Initial Catalog=DATABASENAME;Integrated Security=True</ConnectionString>
 

Individual security
-------------------

#####Individual security / fine grained control over access

If you have a small number of users who are to be provided access to Rantt Web Host, or you have already added these user accounts into SQL server security, then you might consider setting IIS to provide authentication pass-through to SQL.

Advantages:

-   users already granted access to SQL can access data using Rantt Web Host.
-   users without SQL access could still browse Rantt Web Host website and use other Rantt projects using, say CSV files or other data sources (depending on security), but will not be able to view any projects accessing SQL
-   security is configured in one location, in SQL

Disadvantages:

-   if there are many users, IIS can be less efficient; for IIS to use "SQL connection pooling" it relies on a single user account accessing SQL
-   adding or changing user access requires changes to SQL security, administration effort required.
-   setting up can be quite complex, particularly if you have active directory; may require extensive knowledge of Kerberos and SPNs


                    