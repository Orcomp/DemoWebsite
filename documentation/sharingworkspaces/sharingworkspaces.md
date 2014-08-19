---
layout: page-with-navigation
title: Sharing Workspaces
permalink: /documentation/sharingworkspaces/
navigation-bar:
    - Reference: toolbar-settings
      Title: Toolbar Settings

---

This is a guide on how to share workspaces between the web and desktop version of Rantt.

Essentially the web and desktop version of Rantt need to share the same folder in which the workspaces are saved.

Because of permission issues with IIS it is often easier to change the desktop configuration.

Open the **Rant.Release.exe.config** file located in "**C:\Program Files (x86)\Simulation Modelling Services\Rantt**"

![](/wiki/download/attachments/21692425/config.png?version=1&modificationDate=1397456696337&api=v2)

Then add the line:

<add key="ConfigurationFolder" value="C:\RanttWeb\App_Data\Configuration" />

**NOTE: **You may have to change the "C:\RanttWeb" to match the correct folder on your server.

![](/wiki/download/attachments/21692425/configFile.png?version=1&modificationDate=1397456696425&api=v2)

 

 
                    