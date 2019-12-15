---
title: Server Admin
permalink: /Server_Admin
layout: page
author: Wilson
date: 2011-09-17T22:08:20Z
category: 
---
## Web Admin

The easy way to alter server variables and kick/ban people is to use the
server control panel.

  - [Battalion Server](http://bn.29th.org:8075/ServerAdmin/)
  - [Company Server](http://co.29th.org:8075/ServerAdmin/)
  - [Euro Server](http://eu.29th.org:8075/ServerAdmin/)
  - [Platoon Server](http://plt.29th.org:8075/ServerAdmin/)
  - [Squad Server](http://sqd.29th.org:8075/ServerAdmin/)

## Console Admin

Alternatively, you can use the following [console](console "wikilink")
commands after logging in.

**adminlogin username password**  
Logs you in.

**admin set Engine.AccessControl GamePassword passhere**  
Sets server password. Leave 'passhere' blank to remove password.

**admin set ROEngine.ROTeamGame MaxTeamDifference 99**  
Turns off team balancing and allows all members to join the same team.
Set to 2 by default.

**listplayers**  
Gets a list of all players currently in the game, numbers are assigned
to each player which can be used in replace of their name.

**admin kick playername**  
Kicks player.

**admin kickban playername**  
Kicks & Bans player.

**admin kick session playername**  
Kicks & Session Bans player.

## Match Admin

The below commands are used for realism matches and most of them require
the server to have [Realism
Match](http://forums.darkesthourgame.com/viewtopic.php?f=72&t=4427)
installed.

**mutate enablematch**  
Begins the match and restarts the round

**mutate disablematch**  
Ends the match and restarts the round, setting everything back to normal

**mutate respawn**  
Respawns player

**admin resetgame**  
Restarts the round

**Type in chat: /ready**  
Sets your team as 'ready' (admin not required)

**Type in chat: /notready**  
Sets your team as 'not ready' (admin not required)

**mutate matchlive**  
Admin command to force match to live, regardless of 'ready' states

**Round Duration**  
To change the round duration to unlimited, go to the Web Admin of the
server, click 'Defaults' at the top-centre, click 'Realism Match' on the
left, and change the 'Round Duration' setting to 999. After doing this,
you must reset the level (can be done on the left-hand panel) or change
the map for it to take effect. When you are done, set it back to 0 and
reset the level\!\!

