---
title: Advanced Binding Guide
permalink: /Advanced_Binding_Guide
layout: page
author: Olson
date: 2010-03-09T05:16:02Z
category: 
---
This article was written by
[o0|REDRUM|0o](http://www.redorchestragame.com/forum/member.php?u=3602)
at Red Orchestra's Forums.

## The Basics

First of all, to bind keys you have to find the correct file to do so.
In your typical installation this file will be located like so..

`C:\Program Files\Steam\steamapps\common\red orchestra\DarkestHour\System\user.ini`

*User.ini* is the file we are looking for.

Within this file we will mainly be dealing with the topmost section
which has lines like this..

`Aliases[8]=(Command="Jump | Axis aUp Speed=+300.0",Alias="Jump")`  
`Aliases[9]=(Command="Crouch | Axis aUp Speed=-300.0| OnRelease UnCrouch",Alias="Duck")`  
`Aliases[18]=(Command="Button bRun",Alias="Walking")`

Aliases are just that, an alias. As you can see in the above example,
Button bRun is the same as Walking. When you bind a key to walking,
G=Walking, you are essentially telling the game to do Button bRun

It appears that the game only allows for 39 Aliases so you will have to
choose carefully on which you want to replace - more on that later.

## Keybinds

Keybinding is as simple as it gets. As you can see below, a letter
simply equals a command.

`C=ToggleDuck`  
`D=StrafeRight`  
`E=LeanRight`  
`F=use`

## Advanced

Alright, now for what some symbols mean within the .ini.

### Semicolon

This symbol (;) is used in front of a line will comment it out. That
means the game will not read this line, for example,

`;C=ToggleDuck This line will now not be read and will be rendered useless.`

Another example would be to add notes to your user.ini If you wanted to
organize your user.ini and say put your speech binds in a section.

`;Speech Binds`  
`p=speech SUPPORT 4`  
`l=speech ENEMY 1`

### Pipe

This symbol (|) just basically allows a further command to be set, a
comma if you will. For example,

`RightMouse=ROIronSights`**`|`**`set Engine.PlayerInput MouseSensitivity 0.5`**`|`**`Onrelease `  
`ROironsights`**`|`**`Onrelease set Engine.PlayerInput MouseSensitivity 2.5`

In this example by holding down the rightmouse it will bring up your
ironsights and lower your mouse sensitivity, then on release it lowers
your ironsights and returns your sensitivity to normal.

***NOTE***  
*This bind, specifically the ironsights is buggy at best. You must hold
the button down to allow the ironsight animation to finish or you will
get stuck with your mouse speed reversed. Unfortunately there isn’t any
way to have an ironsight holdon any other way for now.*

### Onrelease

This performs an action when the key is released. Check the above
example.

### Toggle

This will *sometimes* work to toggle an action. One keypress will do an
action, the second keypress will stop the action. By sometimes I mean
this will not work with all commands, you will just have to try it and
see if it works.

`C=ToggleDuck`

### SET \[class variable value\]

Sets a specified class and specified variable with the specified value

## Multiple binds

\[KEY\]= speech SUPPORT 0| speech ALERT 8| teamsay I am down to %H This
would produce in speech *We need help\!  
Under attack at..  
I am down to 30 Health*  
More on % binds in the speech section

## Creating Aliases/Scripting

`Aliases[32]=(Command="ROIronSights|set Engine.PlayerInput MouseSensitivity 0.5|set input p`  
`Newsightoff",Alias="Newsighton")`  
`Aliases[33]=(Command="ROIronSights|set Engine.PlayerInput MouseSensitivity 2.5|set input p`  
`Newsighton",Alias="Newsightoff")`  
`P= Newsighton`

In the above example we are raising our ironsights and turning down the
sensitivity, and hitting it again to reverse those actions. We are
creating a toggle to do this versus an onrelease command. We are also
creating a script. A script allows us to have a key do a specific
command or commands, then allows us to assign the key to do something
else on the next keypress. We are also assigning a key to do the next
command. In alias 32 you see the phrase “set input p Newsightoff” Alias
33 is newsightoff. When you press P in 32 it does the specified action,
then assigns the key to alias 33, newsighton.

`P= Newsighton`

You must then put this line in your binds section to start the script
using alias 32, and after that were done.

***NOTE***  
*You may only have one alias assigned to a \#.It is believed you can
only have 39 aliases so choose wisely. Further testing is required*

## EXEC and multiple keyboard layouts

The exec command can be very useful. Here is one example but use your
imagination. Like map specific configs or settings

`Alt=exec Vehiclebinds.txt|OnRelease exec Defaultbinds.txt`

These are a little more complex... What it does, is execute a .txt file
that contains lines of commands, and execute another file that contains
another file which should inculde you default binds. That means that you
can make a bind for, lets say X, and another bind for Alt+X

**IMPORTANT**  
You need to make a .txt file containing the binds for Alt+Button and
another file for you default binds or you will loose your originals...
like this:

`Vehiclebinds.txt:`  
`NumPad6=speech VEH_ALERTS 0`  
`NumPad6=speech VEH_ALERTS 0`  
`NumPad6=speech VEH_ALERTS 0`  
`NumPad6=speech VEH_ALERTS 0`  
`NumPad6=speech VEH_ALERTS 0`  
`NumPad6=speech VEH_ALERTS 0`

`Defaultbinds.txt:`  
`NumPad6=speech VEH_ALERTS 0`  
`NumPad5=speech VEH_ORDERS 0`  
`NumPad4=speech ALERT 0`  
`NumPad3=speech ENEMY 0`  
`NumPad2=speech ACK 0`  
`NumPad1=speech SUPPORT 0`

NOTE: You can not make complex bindings with this... a complex binding
is a bind containing more than one action... like the other binds here\!

NOTE2: The more binds executed in one .txt file, the longer screen
freezeup... so instead of filling one file with a lot of binds, try
making more button combos... Shift+Button, Ctrl+Button, Caps+Button

## Some commands you can bind

### Stat commands

  - MEM STAT - Displays Windows memory usage
  - STAT ALL - Shows all stats
  - STAT AUDIO - Shows audio stats
  - STAT FPS - Displays your frames per second
  - STAT GAME - Displays game stats
  - STAT HARDWARE - Shows hardware stats
  - STAT NET - Shows network game play stats
  - STAT NONE - Turns off all stats
  - STAT RENDER - Displays rendering statistics

### Demo Commands

  - DEMOPLAY \[demoname\] - Plays the specified demo
  - DEMOREC \[demoname\] - Records a demo using the demoname you type
  - STOPDEMO - Stop recording a demo

### Other Commands

  - BRIGHTNESS \[number\] - Changes the brightness level to the
    specified number
  - CONFIGHASH - Displays configuration info
  - CONTRAST \[number\] - Changes the contrast level to the specified
    number
  - DEBUG CRASH - Test crashes the game with an error
  - DEBUG EATMEM - Tests memory allocation until full
  - DEBUG GPF - Test crashes the game with a general protection fault
    error
  - DEBUG RECURSE - Test crashes the game by infinite recursion
  - DUMPCACHE - Displays the memory gcache contents
  - EXEC \[filename\] - Executes a file in the UT2003 /system/ directory
    by default
  - EXIT Exits the game entirely
  - FLUSH - Flushes all caches and relights
  - GAMMA \[number\] - Changes the gamma level to the specified number
  - GETCURRENTRES - Displays your current resolution
  - GETCURRENTTICKRATE - Displays your current tick rate
  - GETMAXTICKRATE - Displays the maximum allowed tick rate
  - NETSPEED \[number\] - Sets the net speed, default is 10000
  - OBJ GARBAGE - Collects and purges objects no longer in use
  - PAUSESOUNDS - Pauses all sounds
  - RELAUNCH - Relaunches the engine
  - REPORT - Copies a report of the current game to clipboard
  - Engine.PlayerInput MouseSensitivity \[number\] - Sets the mouse
    sensitivity to the specified number
  - SETRES \[WxHxD\] - Sets your screen resolution to the specified
    width, height, and color depth
  - SOCKETS - Displays a list of sockets in use
  - TOGGLEFULLSCREEN - Toggles fullscreen mode
  - TYPE \[text\] - Displays the specified text on the console
  - UNPAUSESOUNDS - Un-pauses all sounds

### Weapon Binds

#### Non-toggleable Iron Sights

Scroll down the binds at the top of the .ini until you find the button
you use for iron sights. Paste this on to the line:

`RightMouse=ROIronsights | Onrelease ROironsights`

There is some problems with this tweak in that the gun doesnt always
release when you let go of the button. Its rough but its the only option
as of now.

#### Ironsights with a sensitivity change

`Aliases[32]=(Command="ROIronSights|set Engine.PlayerInput MouseSensitivity 0.5|set input p`  
`Newsightoff",Alias="Newsighton")`  
`Aliases[33]=(Command="ROIronSights|set Engine.PlayerInput MouseSensitivity 2.5|set input p`  
`Newsighton",Alias="Newsightoff")`

Change the sensitivity to your liking

I used P in my example, for your key, change it to yours in both lines
above "set input p" Then add this to your desired key

`p=Newsighton`

If you want the ironsights toggle along with the mouse toggle. If thats
the case then here...

`RightMouse=ROIronSights|set Engine.PlayerInput MouseSensitivity 0.5|Onrelease ROironsights|Onrelease set`  
`Engine.PlayerInput MouseSensitivity 2.5`

#### Grenade Throw

`KEY=SwitchWeapon 2|Fire|OnRelease SwitchToBestWeapon`

Hit the button and hold it down until you wanna throw(distance) your
grenade and when you release, it will switch to your best weapon.

### Movement Binds

#### Mouse sensitivity

`set Engine.PlayerInput MouseSensitivity 0.8 | onrelease set Engine.PlayerInput MouseSensitivity 2.0`

#### Toggle Sprint

`key=Toggle bSprint`

#### Toggle Walk

`Z=Toggle bRun`

#### Toggle Lean

`Aliases[34]=(Command="leanleft|set input q leanleftoff",Alias="leanlefton")`  
`Aliases[35]=(Command="LeanLeftReleased|set input q leanlefton",Alias="leanleftoff")`  
`Aliases[36]=(Command="leanRight|set input e leanrightoff",Alias="leanRighton")`  
`Aliases[37]=(Command="LeanRightReleased|set input e leanRighton",Alias="leanrightoff")`  
  
`q=leanlefton`  
`e=leanRighton`

### Miscelaneous Binds

#### Combat Photographer Binds

For those who want to be able to get a clean screen on the fly and not
have to remove the hud by going to the menu and wasting time, possibly
missing the shot, type this in the console (x is just an exampe for the
key you want):

`set input x togglescreenshotmode`  
` or`  
`set input x showhud 0`

For a single-key solution, try this:

`set input x showhud|OnRelease shot|OnRelease showhud`

As long as you hold the key down, the HUD stays turned off. As soon as
you release it, the shot is taken and the HUD is turned back on. That
should help with timing those perfect shots.

#### Voice Binds

  - Say = Global chat
  - Teamsay = teamchat

<!-- end list -->

  - %w Weapon
  - %h Health
  - %Ll Location (doesn’t work very well, its redundant information)
  - \* ^NOTE only works in team chat^

Examples

`[KEY]=Say GG all im out for the night`  
`[KEY]=Teamsay Get your asses over here, im in trouble`  
`t=speech SUPPORT 0| Im at %L and down to %H`

This would produce

*We need help  
Im at The Ruins and down to 20 Health*

#### Speech binds

\[KEY\]=speech SUPPORT \[\#\]

  - \[0\]="We need help\!"
  - \[1\]="Need help at"
  - \[2\]="I need ammo\!"
  - \[3\]="Get a sniper over here\!"
  - \[4\]="We need MG support\!"
  - \[5\]="We need an AT Rifle\!" OR "We need a Panzerfaust\!"
  - \[6\]="Someone blow this\!"
  - \[7\]="We need a tank\!"
  - \[8\]="Give us artillery\!"
  - \[9\]="I need transport\!"

\[KEY\]=speech ENEMY \[\#\]

  - \[0\]="Infantry spotted\!"
  - \[1\]="MG position\!"
  - \[2\]="Sniper\!"
  - \[3\]="Sapper\!" OR "Pionier\!"
  - \[4\]="Anti-tank soldiers\!"
  - \[5\]="Small vehicle\!"
  - \[6\]="Tank\! Tank\!" OR "Achtung, panzer\!"
  - \[7\]="Heavy tank\!"
  - \[8\]="Artillery\!"

\[KEY\]=speech ALERT \[\#\]

  - \[0\]="Grenade\!"
  - \[1\]="Go go go\!"
  - \[2\]="Take cover\!"
  - \[3\]="Stop\!"
  - \[4\]="Follow me\!"
  - \[5\]="Satchel planted\!"
  - \[6\]="Covering fire\!"
  - \[7\]="Friendly fire\!"
  - \[8\]="Under attack at"
  - \[9\]="Retreat\!"

\[KEY\]=speech VEH\_ORDERS \[\#\]

  - \[0\]="Go to"
  - \[1\]="Move forward"
  - \[2\]="Stop"
  - \[3\]="Move back"
  - \[4\]="Go left"
  - \[5\]="Go right"
  - \[6\]="Forward 5 metres\!"
  - \[7\]="Back 5 metres\!"
  - \[8\]="Turn left a little\!"
  - \[9\]="Turn right a little\!"

\[KEY\]=speech VEH\_ALERTS \[\#\]

  - \[0\]="Enemy in front\!"
  - \[1\]="Enemy left flank\!"
  - \[2\]="Enemy right flank\!"
  - \[3\]="Enemy behind us\!"
  - \[4\]="Enemy infantry close\!"
  - \[5\]="Yes, sir\!"
  - \[6\]="No, no\!"
  - \[7\]="We're burning\!"
  - \[8\]="Get out\!"
  - \[9\]="Loaded."

\[KEY\]=speech TAUNT \[\#\]

  - \[0\]="I will kill you\!"
  - \[1\]="No retreat\!"
  - \[2\]="\*insult\*"

\[KEY\]=speech ACK \[\#\]

  - \[0\]="Yes sir\!"
  - \[1\]="No, no\!"
  - \[2\]="Thanks"
  - \[3\]="Sorry"

\[KEY\]=speech ORDER \[\#\]

  - \[0\]="Attack"
  - \[1\]="Defend"
  - \[2\]="Hold this position\!"
  - \[3\]="Follow me\!"
  - \[4\]="Attack at will\!"
  - \[5\]="Retreat\!"
  - \[6\]="Fire at will\!"
  - \[7\]="Cease fire\!"

