---
layout: page-with-navigation
title: Getting Started
permalink: /documentation/gettingstarted/
navigation-bar:
    - Reference: prerequisites
      Title: Prerequisites
    - Reference: installation
      Title: Installation
    - Reference: required-data
      Title: Required Data
      SubItems:
        - Reference: operation-csv-file
          Title: Operation csv file
        - Reference: calendar-periods-csv-file
          Title: Calendar Periods csv file
        - Reference: operation-relationships-csv-file
          Title: Operation relationships csv file
---

Prerequisites
--------------

- Framework: .NET 4.5
- CPU:  1.7 GHz
- RAM: 2 GB


Installation
------------

Double click on the executable and follow through the prompts.

The program will be installed in `C:\Program Files (x86)\Wild Gums\Rantt for Desktop`

Sample project files can also be found in this installation folder under the following folder names:

- ActualPlanned (two datasets are defined in the same project)
- Elsinore (Operations and Calendar)
- FinoFlex (Operations and Calendar)
- Globex (Operations and Relationships)
- MultiDataset (Multiple Datasets)
- CurrentTime (only Operations)

More details (and screen shots) about the sample data can be found on [this page](http://www.resourcegantt.com/documentation/sampledata/).

Workspaces and settings files are saved in `%AppData%/Wild Gums/Rantt`


Required Data
-------------

The Rantt application needs a project file (.rprj) file in order to know where to get its data from. Data can either be stored in csv, Excel files or database tables (or views).

A project can include multiple datasets.

A dataset is made up of:

- An operations file (compulsory)
- A calendar file (optional)
- An Operation Relationships file (optional)

For more information on how to create a project file, please visit the [Project Wizard](http://www.resourcegantt.com/documentation/projectwizard/) page.


### Operation csv file

The minimum required fields in order to display operations on the Gantt chart are:

- Resource
- Start time
- End time

![Operations csv file](img/rantt_operations.png)
 
The wording in the column header is insignificant but will need to mapped to the required fields during the project creation.

**Note:**

> - The start and end time values must have valid values (i.e. Rantt does not accept NULL or blank values)
> - The end time must be equal or greater than the start time.


More columns can be included and will be available as contextual information associated with the operation. 
The visibility of these additional fields can be fully customized. An example of a csv file with multiple fields is shown below.

![More details](img/rantt_operations2.png)

These additional fields will be used by Rantt to facilitate the analysis of your data by:

- Being visible as tooltips when hovering over the operation:

![Tooltips](img/rantt_tooltip.png)

- Allowing you to colour operations by the value of these fields via the legend control:

![Legend Control](img/rantt_legendControl.png)


### Calendar Periods csv file

This file is optional and contains a row for each period of time you want to display on the Gantt.

Generally "Off Shift" periods are worth displaying in order to provide a better understanding of the schedule.

A calendar period is defined by:

- Resource
- Calendar state name
- Start time
- End time

This data file will look like the picture shown below:

![Calendar Periods](img/rantt_calendarPeriods.png)

Each calendar period will by default be displayed as a grey rectangle. The colour for a particular calendar state can be changed from the "Legend Control" as shown below:

![Calendar Legend](img/rantt_calendarLegend.png)

**Note:**

> - The start and end time values must have valid values (i.e. Rantt does not accept NULL or blank values)
> - The end time must be equal or greater than the start time.

### Operation Relationships csv file

The fields required in this file are:

- From
- To
 
These fields will hold a unique identifier number for each operation.
In order for this file to work with Rantt, the Operations.csv file will need an extra "Reference" column, which will contain the unique identifier for each operation.

![Operation with reference](img/rantt_operations3.png)

![Operation with reference](img/rantt_relationships.png)
 
When you right click an operation and if this operation is mentioned in the OperationRelationships csv file, then three right click options are shown.

- Show Parent Relationships
- Show child Relationships
- Show All Relationships
 
![Relationship Conext Menu](img/rantt_relationshipContextMenu.png)

The result will be:

![Relationship Lines](img/rantt_relationshipLines.png)

**Note:**

> In order to make the relationship lines disappear simply double click anywhere on the Gantt chart.
 
 