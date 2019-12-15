---
title: Known Problems and Fixes
permalink: /Known_Problems_and_Fixes
layout: page
author: Olson
date: 2011-01-18T09:08:23Z
category: 
---
This page describes known problems and fixes for Darkest Hour/Red
Orchestra, excluding crashes. For crash fixes, see [this
page](Crash_Fixes "wikilink").

# Validating Caches

Click on the links to validate your [Red
Orchestra](http://steam.opencoding.net/?url=steam://validate/1200/) and
[Darkest Hour](http://steam.opencoding.net/?url=steam://validate/1280/)
caches.  
  
\= Keyboard Movement Lag = Some users have described a "movement lag"
that involves pressing a movement button and experiencing a delay before
your player actually moves, or your player continuing to move for a
short time after you let go of the movement key (greater delay than a
realistic stop). Following the instructions in the [Decrease Load
Times](Decrease_Load_Times "wikilink") tutorial helps eliminate keyboard
movement lag.

In addition, background services such as *Avast Antivirus* or other CPU
hogs are [known to cause keyboard
lag](http://www.redorchestragame.com/forum/showthread.php?t=25958). To
check your background services, press \[CTRL\] + \[ALT\] + \[DEL\] to
start the *Task Manager* (In Windows Vista, you will have to click
*Start Task Manager* after pressing those keys).

Select the *Processes* tab at the top to view what processes are running
in the background. This window also displays how much memory and CPU is
being used by each process. Clicking on a process and clicking the *End
Process* button will end the process, but you should consult someone in
the [Medical Office](http://www.29th.org/forums/index.php?board=28.0)
before ending a process with a name you do not recognise.  
  
\= Video Problems = Sometimes a problem is serious enough that you can't
even start DH up, so the video driver needs to be changed manually.

Open up  in Notepad. (Immediately save a copy as , in case something
goes wrong.) You will see a section that starts with this:  that
contains these lines:  

Each line that has a semicolon in front of it has been commented out
(i.e. turned from a command to a line that the program ignores). The
single line without one is the currently used driver. To switch video
drivers, simply remove the semicolon from one of the other lines that
start with  and place one in front of the current one that doesn't. **It
is very important that only one line is uncommented; no more, no less.**
There are also other lines that start with , but don't try to uncomment
them.

Save the file and try to restart DH. If it won't start up, try a
different driver. If it doesn't work with any of them, post your problem
in the [Medical
Office](http://www.29th.org/forums/index.php?board=109.0).

