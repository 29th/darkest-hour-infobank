---
title: Eliminating Map Re-Downloads
permalink: /Eliminating_Map_Re-Downloads
layout: page
author: Smithp
date: 2010-03-14T14:15:27Z
category: 
---
This fix will either prevent, or delay for a very long time, a map
you've played again and again from re-downloading itself.

# Editing the .ini file

1\. First, open this folder: steam/steamapps/common/red
orchestra/darkesthour/system. The file you are looking for is named
DarkestHour and it's is a Configuration Settings type of file. To be
sure it's the correct file, when you open it, it begins with:

`   Protocol=RedOrchestra`  
`   ProtocolDescription=RedOrchestra Protocol`

2\. When the file is open, press key F3, and a search window will open.
Type "Purge" and hit enter. You will find this part:

`   [Core.System]`  
`   PurgeCacheDays=30`

3\. Change 30 to 0 (zero),

`   PurgeCacheDays=0`

4\. Save & close. No more annoying map downloads for maps you already
have.

# Editing Preferences from the Console

If you're not comfortable editing the .ini file, this is an alternate
method that increases the \# of days, from 30 to 999, until a map
re-download occurs.

1.  Open console using the (\~) tilde key.
2.  Type: "preferences" in the console window and hit enter. This should
    open the Preferences box.
3.  Look for Advanced/File System. Then change the value in
    'purgecachedays' to 999.

