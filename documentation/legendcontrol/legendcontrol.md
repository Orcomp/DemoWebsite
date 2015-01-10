---
layout: page-with-navigation
title: Legend Control
permalink: /documentation/legendcontrol/
navigation-bar:
---

The legend control allows you to quickly identify operations on the Gantt chart by their associated attribute value.

![Legend Control](img/RanttLegendControl.png)

All the field names from the operations data source will be available in the "Colour Attribute" combo box.

Once you select an attribute, each distinct value associated with it will be shown in the list box beneath it and will be associated with a distinct colour. 

Selecting a row will "highlight" these values on the Gantt chart and gray out all others.

![Highlights](img/Highlights.png)

**Note:** 

> - Select one or multiple rows by holding the "Ctrl" or "Shift" key down as you make your selection.
> - Clicking on the "x" button on the bottom right corner will reset the legend control.
> - The number (or count) of each operation having the specified value is shown in brackets on the right hand side.

With this tool you can also:

- Hide rectangles with a give attribute value by un-ticking the tick box. (Compare the image below with the images above.) 
	![Hidden Operations](img/Hidden.png)
- Change the color of an attribute by double clicking on a color disk.
	![Colour Picker](img/ColourPicker.png)
- Search for attribute values using the search box (The search box will accept wild cards, and the "Settings" drop down window will allow you to select "Regex" for more advanced searches.)
