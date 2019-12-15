---
title: Recompile With Batch File
permalink: /Recompile_With_Batch_File
layout: page
author: Wilson
date: 2011-06-18T20:36:16Z
category: 
---
1.  Open notepad and paste the below contents into it.
2.  Change the path on line 2 to your DH system directory. If it's on
    another hard drive, add a line above it containing the drive letter
    only (i.e. D:)
3.  Save the file as filename.bat (whatever filename you like, but with
    a .bat extension)

`@echo off`  
`cd C:\program files\steam\steamapps\common\red orchestra\darkesthour\system`  
`if not (%1) == () GOTO :provided`  
`echo Enter Package Name`  
`set /p PackageName=`  
`del %PackageName%.u`  
`echo %PackageName%.u deleted`  
`GOTO :compile`  
`:provided`  
`del %1.u`  
`echo %1.u deleted`  
`:compile`  
`cd ..\..\system`  
`ucc make -mod=darkesthour`  
`pause`

There are two ways to recompile using this batch file.

Option 1: Simply click on the file to open it. It will prompt you for
the package name you wish to recompile. Type it in \*\*without the
.u\*\*

![Rcmp1.png](images/Rcmp1.png "Rcmp1.png")

Option 2: Open command prompt (Start\>Run\>cmd) and browse to the
directory you saved the batch file in. Then type the batch file's name
with the package name you wish to recompile (without the .u) as a
parameter, as shown below. The advantage of this method is that if you
are recompiling the same package over-and-over (for debugging), you can
keep the command prompt window open and just press the up-arrow and
enter to repeat the last command.

![Rcmp2.png](images/Rcmp2.png "Rcmp2.png")

