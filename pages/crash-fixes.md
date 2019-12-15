---
title: Crash Fixes
permalink: /Crash_Fixes
layout: page
author: Olson
date: 2011-03-30T16:44:05Z
category: 
---
# First Things First

There are a number of measures that you can take for yourself if
something goes wrong with Red Orchestra, Darkest Hour, or Mare Nostrum.
The steps listed below will solve the problem 80% of the time, so try
these before reinstalling your game

## Software Checks

  - In an Explorer window, right-click on each drive and select . Select
    the  tab and click on  Check off , then click . If it says that it
    can't and asks if you want to schedule one for the next time you
    start your computer, say 'Yes'. Once you have done this with each
    one of your hard drives, reboot your computer (if necessary) and let
    it check the drive(s).
  - Run Windows Update and see if any secondary update might apply to
    you.
  - Install the latest video drivers
    ([nVidia](http://www.nvidia.com/Download/index.aspx?lang=en-us)/[ATI](http://support.amd.com/us/gpudownload/Pages/index.aspx))
    and
    [DirectX](http://www.microsoft.com/downloads/en/results.aspx?DisplayLang=en&nr=10&freetext=DirectX+Redistributable&sortCriteria=Date&categoryid=2&sortOrder=Decending&stype=ss_rr&period=500).
  - Make sure to [secure your
    system](http://29th.org/wiki/index.php?title=Securing_Your_System).
  - Update [common
    runtimes](http://ninite.com/air-dotnet-flash-flashie-java-quicktime-reader-silverlight/).
    (Adding it as a nightly task will ensure that they are always kept
    up-to-date.)

## Hardware Checks

  - Make sure that your surge protector is rated to at least 1500 Joules
    (3000 is better), and its protection light is still on.
  - To check for overheating components, do in-depth CPU and GPU tests
    with [OCCT](http://www.ocbase.com/perestroika_en/).
  - To check for failing RAM, download, burn, then boot an [Ubuntu
    LiveCD](http://www.ubuntu.com), then run the memory check on the
    first menu. After it is finished, start up Ubuntu itself and see how
    stable your system is.

## RO/DH/MN Specifics

  - Delete  or  if it exists.
  - Validate RO/DH/MN by clicking on these links:

[`Red`` 
 ``Orchestra`](http://steam.opencoding.net/?url=steam://validate/1200/)  
[`Darkest`` 
 ``Hour`](http://steam.opencoding.net/?url=steam://validate/1280/)  
[`Mare`` 
 ``Nostrum`](http://steam.opencoding.net/?url=steam://validate/1230/)

  - Shut down Steam, then delete all of the files (**NOT FOLDERS UNLESS
    SPECIFICALLY TOLD TO BY A TECH\!\!\!**) in the Steam folder except
    for . Restart Steam and see if the problems have been solved.
  - If that doesn't work, temporarily rename  to  (or w/e) to trigger
    the creation of a factory default version.
  - If that doesn't work, temporarily rename  to  (or w/e) to trigger
    the creation of a factory default version.
  - If that doesn't work, post a help request in the Medical Office,
    containing your  using this:

`[collapsible=Click Here to Expand]This is the content that pops out when you click on the title[/collapsible]`

-----

-----

# Keyboard Movement Lag

Some users have described a "movement lag" that involves pressing a
movement button and experiencing a delay before your player actually
moves, or your player continuing to move for a short time after you let
go of the movement key (greater delay than a realistic stop). Following
the instructions in the [Decrease Load
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

-----

-----

# Video Problems

Sometimes a problem is serious enough that you can't even start DH up,
so the video driver needs to be changed manually.

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
different driver.

-----

-----

# Karma Crash

This bug causes a crash very frequently - on some maps with many
players, even once every 15 minutes or so. The game closes and gives the
following error:

`General protection fault!`  
  
`History: KBodyGetActor <- BodyGetDoubleRate <- KBuildPartitions <- KWorldStepSafeTime <- KTickLevelKarma <-`  
`TickAllActors <- ULevel::Tick <- (NetMode=3) <- TickLevel <- UGameEngine::Tick <- Level D-Day 0830hrs -`  
`Brécourt Manoir <- UpdateWorld <- MainLoop <- FMallocWindows::Free <- FMallocWindows::Realloc <- 0012FEF8 0`  
`FArray <- FArray::Realloc <- 0*2 <- FMallocWindows::Free`

This is fixed by editing your main  files. You can download an
[automatic patch](http://29th.org/uploads/crashfix.zip) or do it
manually, as described below.

1.  Find your  file and open it in Notepad. It is located in your
    [DarkestHour System folder](Game_Paths "wikilink").
2.  Scroll down to the  section and notice the first line, . You will
    need to change the number *32* to coordinate with the [amount of RAM
    you have](RAM "wikilink").
    1.  If you have 256MB of RAM or less, 
    2.  If you have 512MB of RAM, 
    3.  If you have 768MB of RAM, 
    4.  If you have 1GB of RAM or More, 
3.  Scroll down to the  section and locate the line that reads . Change
    this to .
4.  Scroll down to the  section and match the first few lines to these:
    1.  
    2.  
    3.  
    4.  
    5.  
5.  Browse to your [Red Orchestra System folder](Game_Paths "wikilink")
    and open  in notepad. Repeat Steps 2-4 on this file (just in case,
    as the author put it).

-----

-----

# Memory Crash

Certain maps (like DogGreen) use a lot more memory than others, and can
cause the engine to attempt to use up more than is available
[Olson](User:Olson "wikilink"): To be finished

-----

-----

# Sound Crash

This bug causes you to crash as you before you get to the menu of the
game, providing the below error message:

`General protection fault!`  
  
`History: alcOpenDevice <- UALAudioSubsystem::Init <- UEngine::InitAudio <- UGameEngine::Init <- InitEngine`  
`<- FMallocWindows::Free <- FMallocWindows::Free`

This problem can be fixed with the below solution. If you are not
experiencing this problem, there is no need to apply this fix.

1.  Find your  file and open it in Notepad. It is located in your
    [DarkestHour System folder](Game_Paths "wikilink").
2.  Scroll down to the  section and locate the line that reads . Change
    this to .

-----

-----

# "Failed to load 'Entry': Can't find file 'Entry'"

1.  Delete  then revalidate your DH cache.
2.  Open up the following files in Notepad, and change (|) every
    instance of **DarkestHourDev** with **DarkestHour**.

