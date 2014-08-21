---
layout: page-with-navigation
title: Default Colours
permalink: /documentation/defaultcolours/

---

    Rantt will automatically assign colors to operations based on the attribute selected in the legend control and their corresponding values.

![](images/LegendControl.png)

 

You can manually change the colors by clicking on the disks:

![](images/ColorPicker.png)

 

You can also create a Colors.csv file and save it in the same folder as your Rantt project.

The Colors.csv file needs 3 columns:

-   AttributeName
-   AttributeValue
-   Color

Example.

![](images/colorsCsvFile.png)

When Rantt loads a project it will automatically check for the existence of a **Colors.csv** file. If there is one it will use the colors supplied for the attribute name/values.

The "Color" column in the csv file can specify colors in three formats:

-   English
-   Hexadecimal
-   RGB

For a list of supported English color codes please visit this page: [http://www.rapidtables.com/web/color/RGB_Color.htm](http://www.rapidtables.com/web/color/RGB_Color.htm)

 

**NOTE:** When using English color codes, do not include spaces. e.g. "light steel blue" should be written "lightsteelblue".
