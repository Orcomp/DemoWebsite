---
layout: page-with-navigation
title: Preactor Views
permalink: /documentation/preactorviews/
---

Rantt can be used to view [Preactor](http://preactor.com/Home.aspx) data.

In order to display Preactor data in Rantt you will need to create some views.

Please download the following [zip file](https://drive.google.com/file/d/0B5SM6iAQ6u64RjZSZmF4VTc3bkU/view?usp=sharing).

Instructions
=============

The zip file contains two scripts:
	- FunctionsAndProcedures.sql 
	- CreateViews.sql

These scripts will create two views, one for **operations** and the other for **calendar periods**, which can then be imported into Rantt easily.

Step 1: Run FunctionsAndProcedures.sql
Step 2: CreateViews.sql
Step 3: Create a new Rantt project and include the newly created views

**Note:**

> The operation view only contains a few fields. You can add more fields to the operation view by editing the FunctionsAndProcedures.sql script. (Advanced SQL knowledge is required.)
 