---
layout: page-with-navigation
title: Independent Plots
permalink: /documentation/independentplots/
navigation-bar:
---

Rantt allows you to visualise plots that are totally independent from the gantt chart, but share the same date range.

File Structure
==============

If a Plots.csv file is found in the same folder as the project file it will automatically be loaded when you click on the "Plots" button.

You can also have plot files with different names, which you can load afterwards.

The plot files need at least 2 columns. The first column will hold values for the x-axis and the second column will hold values for the y-axis. Any subsequent columns filled with data will represent a new plot.

![Plot File](img/PlotFile.png)

Rules
------

An independent plot file must have:

- At least two columns
- First column always contains the x-axis values
- First row always contains the plot legends (If a plot does not have a legend, leave the first cell blank and a legend will automatically be assigned to the column)
- A column can have blank cells at the top and/or the bottom but not in the middle.


Highlight Columns
==================

