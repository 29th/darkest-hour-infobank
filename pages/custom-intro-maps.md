---
title: Custom Intro Maps
permalink: /Custom_Intro_Maps
layout: page
author: Wilson
date: 2010-12-31T15:44:47Z
category: 
---
## Disable The Darkest Hour Intro

To disable the DH-Intro, you will first need to download the custom map
[No Intro](http://29th.org/eng/NoIntro.zip)

Extract the map to the **Maps** folder in your [Darkest Hour Game
Directory](Game_Paths "wikilink").

Next, open the **DarkestHour.ini** which is located in your [Darkest
Hour System Directory](Game_Paths "wikilink").

Under the \[URL\] section at the top, change

`LocalMap=DHintro.rom`

to

`LocalMap=NoIntro.rom`

and save your .ini.

## Connect To Lan (Or Any Server) On DH Startup

To connect to a server automatically on DH startup, you will first need
to download the custom map [Open Lan](http://29th.org/eng/OpenLan.zip)

Extract the map to the **Maps** folder in your [Darkest Hour Game
Directory](Game_Paths "wikilink").

Open **OpenLan.rom** with the **Red Orchestra SDK Beta** and locate the
**Scripted Trigger** on the map.

Open the **Properties** for the Scripted Trigger by double-clicking it.

1.  Expand the **AIScript** Tab.
2.  Expand **Actions**
3.  Expand **\[1\]**
4.  Expand **Action\_ConsoleCommand'myLevel.Action\_ConsoleCommand0**
5.  Change the **CommandStr** to: **open xxx.xxx.xxx.xxx** ←*(IP Address
    you wish to join)*

Save your map.

Next, open the **DarkestHour.ini** which is located in your [Darkest
Hour System Directory](Game_Paths "wikilink").

Under the \[URL\] section at the top, change

`LocalMap=DHintro.rom`

to

`LocalMap=OpenLan.rom`

and save your .ini.

