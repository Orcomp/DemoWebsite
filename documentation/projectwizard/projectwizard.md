---
layout: page-with-navigation
title: Project Wizard
permalink: /documentation/projectwizard/
navigation-bar:
    - Reference: project-wizard
      Title: Project Wizard
---
Introduction
============

In order to use the Rantt application (both desktop and web versions), you will need to first create a project file (.rprj file).

The Rantt Project Creator is a small utility wizard that will help you set up a project file easily.

Icon

A .rprj file is simply an xml file which can be constructed manually, however the wizard provides a simple user interface to facilitate this task.

Once a project file has been created it can be opened in the Rantt application to display the data.

The project can be created by starting the "Rantt Management Viewer". And clicking on the "create project" tool button.

![](/wiki/download/attachments/7897116/createprj.png?version=1&modificationDate=1385963042955&api=v2)

Project File Structure
======================

A project file can contain multiple datasets.

A dataset is made up of a (compulsory) "operation" data source, an (optional) "Operationsrelationship" and an (optional) "calendar" data source. These data sources can come from either a csv file or a database table.

Using the Project Creator Wizard
================================

The first screen you will see when you start the wizard is the General Information screen.

General Information
-------------------

![](/wiki/download/attachments/7897116/GeneralInformation.png?version=1&modificationDate=1374457136628&api=v2)

This screen contains the following fields:

1.  Name - The project name
2.  Culture - Select your culture
3.  First day of the week - Select the first day of the week
4.  Start Date - Optional
5.  End Date - Optional
    

Large database tables

Icon

The Start and End dates are generally used to filter the data coming from large database tables. Only the data contained in within the start and end dates will be retreived.

Operation Dataset
-----------------

![](/wiki/download/attachments/7897116/OperationsDataset.png?version=1&modificationDate=1374457148102&api=v2)

The inputs required for this screen include:

1.  Name – The dataset name which will be used in the Gantt chart if multiple datasets are defined.
2.  Data Source type – Can either be:
    1.  CSV (file)
    2.  DB (table)
    3.  XML (Not implemented yet)
    4.  Json (Not implemented yet)

3.  Date Representation – Can either be:
    1.  Absolute: For fixed start and end times
    2.  Relative: For start and end times that are defined in terms of numbers (either integers or floats). If this option is selected a "Start Date" field will appear, from which the relative time will start, as well as a "Unit of time" field, which corresponds to the unit of time used in the start and end time fields. 
        Relative time is generally used for simulation data.
        ![](/wiki/download/attachments/7897116/RelativeDates.png?version=1&modificationDate=1374458642832&api=v2)

4.  File – The location and name of the operation file. If a database source is selected instead of a CSV file, you will be prompted for a connection string and database table name:
    ![](/wiki/download/attachments/7897116/DbOptions.png?version=1&modificationDate=1374458853386&api=v2)
    The "Table Name" can either be physical database table or a view.
5.  Default Attribute – This field is not critical. Generally the attribute that is the most significant to the user should be set as default.
6.  Field Mappings – The wizard will try and automatically match the column or fields names to the required attributes. If it is unsuccessful the user will need to map the attributes manually.
    1.  Resource
    2.  Start Time
    3.  End TIme

The wizard will validate the data source. If successful the next screen will capture calendar information.

If the validation fails the wizard will prompt you to fix the relevant input fields.

Calendar Information
--------------------

Calendar information is optional, therefore in order to include such information please tick the "Include calendar periods" option.

![](/wiki/download/attachments/7897116/CalendarInformation.png?version=1&modificationDate=1374457143560&api=v2)

There is an option at the bottom of the screen to include another dataset. Please tick this option in order to create multiple datasets.

The next screen will prompt for the optional "Operation Relationships" file.

 

Operation Relationships Information
-----------------------------------

Operation relationship information is optional, therefore in order to include such information please tick the "Include operation relationships" option.

You can define the file name and other details as shown below.

![](/wiki/download/attachments/7897116/or.png?version=1&modificationDate=1386147624425&api=v2)

 

There is an option at the bottom of the screen to include another dataset. Please tick this option in order to create multiple datasets.

 

Viewing Operations
------------------

 

The default view for the operations like, "all the operations" or a range based on dates can be set in the next screen.

![](/wiki/download/attachments/7897116/view.png?version=1&modificationDate=1386147823928&api=v2)

 

Refresh Data
------------

The timer for refreshing the data can be set in the next screen. You need to check the "Enable Timer" check box to get this to effect.

![](/wiki/download/attachments/7897116/timer.png?version=1&modificationDate=1386148043235&api=v2)

 

Summary

This screen will provide a summary of the project name as well as the datasets that have been defined.

![](/wiki/download/attachments/7897116/ProjectSummary.png?version=1&modificationDate=1374457151800&api=v2)

 

You will only be able to save the project if all the required fields have been filled in and the data was successfully validated.