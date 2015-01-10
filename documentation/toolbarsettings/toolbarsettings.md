---
layout: page-with-navigation
title: Toolbar Settings
permalink: /documentation/toolbarsettings/
navigation-bar:
    - Reference: toolbar-settings
      Title: Toolbar Settings

---
# Toolbar Settings

![Toolbar Settings](img/ToolbarSettings.png)

Here is a description of the buttons as seen in the toolbar from left to right:

### Horizontal

Display horizontal lines between the resources.

### Vertical

Display vertical lines between the time intervals as defined by the date-time axis.

### Past

Highlight the past region.

### Current

Show current time

### Time Format

If the operations data comes from a simulation model that uses "0" as the beginning of time you can select relative time and set a new date origin.

### Show Data Rows

![Data Rows](img/DataRows.png)

With data rows enabled you will see a new row for each resource which will give you some statistical information about the operations contained within a time interval.

The Data row has a few options:

- Hide operations: will hide all the operations and only the data rows will be shown
- Align: The numbers can either be left or right aligned
- Include Count: will display the number of operations contained within a time interval (or part thereof)
- Include Duration: will display the total duration of all operations contained within a time interval (or part thereof)

**Note:**

> Any attributes can be included in the data row cells if they contain numeric values

![Data Row Workspace](/img/DataRowWorkspace.png)

### Show Plot Rows


### Show Tooltips

Enable of disbale tooltips.

### Hide Empty Resource

When enabled Rantt will hide resources that have empty resources (i.e. a resource that has no operations on it)
