---
layout: page-with-navigation
title: Project Wizard
permalink: /documentation/projectwizard/
navigation-bar:
    - Reference: introduction
      Title: Introduction
    - Reference: project-file-structure
      Title: Project File Structure
    - Reference: using-the-project-creator-wizard
      Title: Using the Project Creator Wizard
    - Reference: general-information
      Title: General Information
    - Reference: operation-dataset
      Title: Operation Dataset
    - Reference: calendar-information
      Title: Calendar Information
    - Reference: operation-relationships-information
      Title: Operation Relationships Information
    - Reference: viewing-operations
      Title: Viewing Operations
    - Reference: refresh-data
      Title: Refresh Data
    - Reference: summary
      Title: Summary
---
Introduction
============

In order to use the Rantt application (both desktop and web versions), you will need to first create a project file (.rprj file).

The Rantt Project Creator is a small utility wizard that will help you set up a project file easily.


> A .rprj file is simply an xml file which can be constructed manually, however the wizard provides a simple user interface to facilitate this task.


Once a project file has been created it can be opened in the Rantt application to display the data.

The project can be created by starting the "Rantt Management Viewer". And clicking on the "create project" tool button.

![](images/createprj.png)

Project File Structure
======================

A project file can contain multiple datasets.

A dataset is made up of a (compulsory) "operation" data source, an (optional) "Operationsrelationship" and an (optional) "calendar" data source. These data sources can come from either a csv file or a database table.

Using the Project Creator Wizard
================================

The first screen you will see when you start the wizard is the General Information screen.

General Information
-------------------

![](images/GeneralInformation.png)

This screen contains the following fields:

1.  Name - The project name
2.  Culture - Select your culture
3.  First day of the week - Select the first day of the week
4.  Start Date - Optional
5.  End Date - Optional
    

> **Large database tables**
> 
> The Start and End dates are generally used to filter the data coming from large database tables. Only the data contained in within the start and end dates will be retreived.


Operation Dataset
-----------------

![](images/OperationsDataset.png)

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
        ![](images/RelativeDates.png)

4.  File – The location and name of the operation file. If a database source is selected instead of a CSV file, you will be prompted for a connection string and database table name:
    ![](images/DbOptions.png)
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

![](images/CalendarInformation.png)

There is an option at the bottom of the screen to include another dataset. Please tick this option in order to create multiple datasets.

The next screen will prompt for the optional "Operation Relationships" file.

 

Operation Relationships Information
-----------------------------------

Operation relationship information is optional, therefore in order to include such information please tick the "Include operation relationships" option.

You can define the file name and other details as shown below.

![](images/or.png)

 

There is an option at the bottom of the screen to include another dataset. Please tick this option in order to create multiple datasets.

 

Viewing Operations
------------------

 

The default view for the operations like, "all the operations" or a range based on dates can be set in the next screen.

![](images/view.png)

 

Refresh Data
------------

The timer for refreshing the data can be set in the next screen. You need to check the "Enable Timer" check box to get this to effect.

![](images/timer.png)

 

Summary
-------
This screen will provide a summary of the project name as well as the datasets that have been defined.

![](images/ProjectSummary.png)

 

You will only be able to save the project if all the required fields have been filled in and the data was successfully validated.