---
layout: page-with-navigation
title: Sharing Workspaces
permalink: /documentation/sharingworkspaces/

---

This is a guide on how to share workspaces between the web and desktop version of Rantt.

Essentially the web and desktop version of Rantt need to share the same folder in which the workspaces are saved.

Because of permission issues with IIS it is often easier to change the desktop configuration.

Open the **Rant.Release.exe.config** file located in "**C:\Program Files (x86)\Wild Gums\Rantt for Desktop**"

![](images/config.png)

Then add the line:

    <add key="ConfigurationFolder" value="C:\RanttWeb\App_Data\Configuration" />

**Note:**

> You may have to change the "C:\RanttWeb" to match the correct folder on your server.

<img src="images/configFile.png" alt="Drawing" style="width: 720px;"/> 

 

 
                    