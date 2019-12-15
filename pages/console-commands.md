---
title: Console Commands
permalink: /Console_Commands
layout: page
author: Wilson
date: 2010-12-30T07:47:29Z
category: 
---
These console commands were copied from [Planet
Unreal](http://da.planetunreal.gamespy.com/2/help/UnrealTournament2004ConsoleCommands.asp).
They are commands for the UT2004 engine, on which Red Orchestra runs,
and should all apply to Darkest Hour.

## Useful Commands

|                     |                                                                                                                     |
| ------------------- | ------------------------------------------------------------------------------------------------------------------- |
| **Command**         | **Description**                                                                                                     |
| stat fps            | Shows average and current frames per second                                                                         |
| reconnect           | Reconnects to last server                                                                                           |
| suicide             | Kills self                                                                                                          |
| setname <name_here> | Changes name. To include spaces, [read this page](Name_Changing "wikilink").                                        |
| demorec <name>      | Records a demo                                                                                                      |
| demoplay <name>     | Plays a demo                                                                                                        |
| togglefullscreen    | Switches between fullscreen and window modes. Alternatively, press \[Alt\]+\[Enter\]                                |
| shot                | saves a **.bmp** screenshot to **Steam\\SteamApps\\common\\red orchestra\\ScreenShots** - Usually bound to **<F9>** |

## Admin Commands

<table>
<tbody>
<tr class="odd">
<td><p><strong>Command</strong></p></td>
<td><p><strong>Description</strong></p></td>
</tr>
<tr class="even">
<td><p>Adminlogin <user> <pass></p></td>
<td><p>Logs admin onto server</p></td>
</tr>
<tr class="odd">
<td><p>Adminlogout</p></td>
<td><p>Logs off admin</p></td>
</tr>
<tr class="even">
<td><p>Admin servertravel <mapname></p></td>
<td><p>Changes server to specific map/game type/mutator<br />
Optional Params ?game=gametype?mutator=mutator</p></td>
</tr>
<tr class="odd">
<td><p>Admin <command></p></td>
<td><p>Executes a command</p></td>
</tr>
<tr class="even">
<td><p>Kick <playername></p></td>
<td><p>Kicks player from server</p></td>
</tr>
<tr class="odd">
<td><p>Kickban <playername></p></td>
<td><p>Kicks and Bans player from server</p></td>
</tr>
<tr class="even">
<td><p>Kick Session <playername></p></td>
<td><p>Kicks and Bans player from server only for the duration of the map</p></td>
</tr>
</tbody>
</table>

## Statistics

|               |                                             |
| ------------- | ------------------------------------------- |
| **Command**   | **Description**                             |
| Mem stat      | Show Windows memory usage                   |
| Stat all      | Displays all stats                          |
| Stat audio    | Shows audio stats                           |
| Stat fps      | Shows average and current frames per second |
| Stat game     | Displays game stats                         |
| Stat hardware | Shows hardware stats                        |
| Stat net      | Displays net stats (ping etc)               |
| Stat none     | Removes stat displays                       |
| Stat render   | Displays rendering stats                    |

## Player Commands / Bot Controls

|                       |                             |
| --------------------- | --------------------------- |
| **Command**           | **Description**             |
| Add bots <number>     | Add X number of bots        |
| Behindview 1          | Switches to 3rd person view |
| Behindview 0          | Switches to 1st person view |
| Disconnect            | Disconnects from server     |
| Reconnect             | Reconnects to last server   |
| Quit                  | Quits game                  |
| Exit                  | Closes UT2003               |
| Killbots              | Eliminates bots             |
| Switchlevel <mapname> | Changes to level named      |
| Open <mapname>        | Opens named map             |
| Switchteam            | Changes players team        |
| Suicide               | Kills player                |
| Teamsay <text>        | Talk to team-mates only     |
| Playersonly           | Freezes bots                |
| Say <text>            | Message to all players      |
| Setname <name>        | Changes name                |

## Misc. Commands

|                                  |                                                                      |
| -------------------------------- | -------------------------------------------------------------------- |
| **Command**                      | **Description**                                                      |
| Demorec <demoname>               | Records a demo                                                       |
| Demoplay <demoname>              | Plays a demo                                                         |
| Stopdemo                         | Stops playing a demo (n/a until patch)                               |
| Showhud                          | Shows the HUD toggled on/off - added by Dudeguy                      |
| Brightness <number>              | Increases/Decreases brightness based on number                       |
| Contrast <number>                | Increases/Decreases contrast based on number - added by MacNiel      |
| Gamma <number>                   | Changes gamma level to certain number - added by MacNiel             |
| Cdtrack <number>                 | Plays named CD track number                                          |
| Confighash                       | Shows configuration information                                      |
| Contrast <number>                | Increases/Decreases contrast based on number                         |
| Debug crash                      | Test crash the game with an error                                    |
| Debug eatmem                     | Tests memory allocation until filled                                 |
| Debug GPF                        | Produces a general protection fault error                            |
| Debug recurse                    | Test crash via infinite recursion                                    |
| Exec <filename>                  | Runs a file in the UT2003/system directory                           |
| Flush                            | Cleans all caches and relights                                       |
| FOV <number>                     | Changes field of view to certain number                              |
| Dumpcache                        | Clears memory cache contents                                         |
| Getcolodepths                    | Displays maximum colour depth supported by hardware                  |
| Getcurrentcolordepths            | Displays current colour depth                                        |
| Getcurrentres                    | Displays current resolution                                          |
| Getcurrenttickrate               | Displays current tick rate                                           |
| Getmaxtickrate                   | Displays maximum tick rate                                           |
| Musicorder <number>              | Changes to certain track in the song (0=ambient 1=action 2=suspense) |
| Netspeed <number>                | Set net speed (default=10000)                                        |
| Obj classes                      | Displays a list of object classes                                    |
| Obj garbage                      | Collects and purges objects not in use                               |
| Obj hash                         | Displays object hashing stats                                        |
| Obj linkers                      | Displays list of active linkers                                      |
| Unpausesounds                    | Un pauses all sounds                                                 |
| Preferences                      | Opens advanced settings (Disabled in Retail Game)                    |
| Relaunch                         | Copies report of current game to clipboard                           |
| Set <class variable value>       | Sets specified class and variable with named value                   |
| Setsensitivity <number>          | Sets mouse sensitivity to X                                          |
| Setres <WidthxHeightxColordepth> | Sets screen resolution to specific width/height/colour depth         |
| Slomo 1                          | Sets game speed to normal                                            |
| Slomo 2                          | Sets game speed to double - Increase number to go faster             |
| Slomo .5                         | Sets game speed to half - Decrease number to go slower               |
| Sockets                          | Displays the list of in use sockets                                  |
| Togglefullscreen                 | Changes full screen mode (in Windows hit ALT + ENTER as well)        |
| Type <text>                      | Displays specified text in console                                   |

