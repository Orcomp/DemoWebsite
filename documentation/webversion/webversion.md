---
layout: page-with-navigation
title: Web Version
permalink: /documentation/webversion/

---


This page will contain documentation on how to install and use the stand alone web (Silverlight 5) application.
The web application shares a lot of the same features as the desktop version, except:

- Shortcut keys


Prerequisites
==============

- IIS
- .NET 4.5

Installation
=============

The installation package will create a new folder in "C:\SMS Software\RanttWebSetup" and will automatically register itself with IIS.
Once the installation is complete, you can test the installation was successful by pointing your browser to the following address:  http://localhost/???

If IIS is configured properly you should be able to see a page with some links on it, as shown int the picture below. Click on any of hose links to open a sample project:

![Projects](img/webRantt0.png)

IIS can sometimes be tricky to setup so if you have a problem displaying the page, please send us an email.

If you click on one of the links you should see a page like the picture below:

![Projects](img/webRantt.png)

![Projects](img/webRantt2.png)

Notes
------

The system expects new project folders to be located in the "C:\????" sub-directory.

The name of the project folder must be the same as name of the project file. (e.g. C:\SMS Software\RanttWebSetup\App_Data\ABC\ABC.rprj)

The project is then accessible from http://localhost/sms/Rantt/ABC

To find out how to create a project file please visit the Rantt Project Creator page.


Workspaces
==========

Workspaces for the Desktop and Web version can be shared with each other.

In fact you can force the webRantt to open a workspace directly by appending the workspace name to the URL

TODO: Show example