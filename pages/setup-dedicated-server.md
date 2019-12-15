---
title: Setup Dedicated Server
permalink: /Setup_Dedicated_Server
layout: page
author: Wilson
date: 2010-05-07T20:39:08Z
category: 
---
1\. Find **steam\_appid.txt** in your [Red Orchestra System
Directory](Game_Paths "wikilink") and open it in a text editor such as
notepad. By default, its contents are **1200**. Change its contents to
**1280** then save and close. This tells the game to run a *Darkest
Hour* server instead of a *Red Orchestra* server.

2\. Open a text editor and paste the following line:

`ucc server DH-Brecourt.rom?game=DH_Engine.DarkestHourGame?MaxPlayers=32 -mod=DarkestHour -log=DH_Server.log -ini=DarkestHour.ini`

You are welcome to change the map or max players on this line.

3\. Save the text file in your [Red Orchestra System
Directory](Game_Paths "wikilink") as **myserver.bat** *Please note the
file extension should be .bat and not .txt*

4\. Double-click on your newly saved batch (.bat) file to start your
server. It should bring up a DOS window that stays running. You should
then be able to join your own server by going to the LAN window in
Darkest Hour.

Note: If the DOS window opens and immediately disappears, that probably
means you put the batch file in the wrong directory. Make sure it is in
your [Red Orchestra System Directory](Game_Paths "wikilink") and not
your [Darkest Hour System Directory](Game_Paths "wikilink")

