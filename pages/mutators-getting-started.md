---
title: Mutators:Getting Started
permalink: /Mutators:Getting_Started
layout: page
author: Wilson
date: 2011-01-01T20:48:06Z
category: 
---
It is recommended that you read [tutorials](Making_Mutators "wikilink")
to get a foundational understanding of UnrealScript and how the engine
works (particularly the 3D Buzz Video Tutorials), but it is even more
important to browse existing code and see 'how they do it.' Once you
have an objective for your first mutator, you can search around existing
code to try to figure out how to do it.

## Install a Text Editor

As Windows does not come with a decent text editor, you will need to
install one if you have not already. We recommend using
[Notepad++](Installing_Notepad++ "wikilink"), which was rated the \#1
Text Editor by
[Lifehacker](http://lifehacker.com/5708503/best-text-editor-notepad).

## Decompiling RO Source Code

The first thing to do is [Install Red Orchestra
SDK](Installing_the_SDK "wikilink"). Apart from giving you the editing
software, doing this will automatically decompile all of the Red
Orchestra code packages from the system directory, allowing you to view
the source code and see how things are done. After doing this, you will
notice several new folders in your [Red Orchestra Game
Directory](Game_Paths "wikilink") that correspond to **.u** files in
your [Red Orchestra System Directory](Game_Paths "wikilink") (e.g. \\Red
Orchestra\\RO\_Engine\\ is the decompiled classes from the \\Red
Orchestra\\System\\RO\_Engine.u package). Inside these new folders (in
the Classes subfolder) you will find **.uc** files, which can be opened
in a text editor and contain the actual code that makes the game work.

## Decompiling DH Source Code

The process for viewing the Darkest Hour source code is not as easy -
you have to manually decompile each package. If you browse to your
[Darkest Hour System Directory](Game_Paths "wikilink"), you will find
the following **.u** files, which are compiled code packages.

  - DH\_ATWeapons
  - DH\_BritishPlayers
  - DH\_Effects
  - DH\_Engine
  - DH\_Equipment
  - DH\_Game
  - DH\_GerPlayers
  - DH\_Guns
  - DH\_Interface
  - DH\_USPlayers
  - DH\_Vehicles
  - DH\_Weapons

These packages can be decompiled using the instructions found
[here](Modifying_Packages "wikilink"). While it would be possible to
create a batch file that automates this decompiling process, learning
how to decompile is a vital part of getting started.

## Decompiling Other Mutators

If you come across [other mutators](Existing_Mutators "wikilink") that
do something and you'd like to know how, you can decompile it and find
out. Just place the **.u** file in your [Darkest Hour System
Directory](Game_Paths "wikilink") and [decompile
it](Modifying_Packages "wikilink"). If it is a Red Orchestra mutator,
put it in your [Red Orchestra System Directory](Game_Paths "wikilink")
and [decompile it](Modifying_Packages "wikilink") by changing the path
(no need for ..\\DarkestHour\\) and removing the **-mod=darkesthour**
suffix.

You should be able to decompile **Unreal Tournament 2004** mutators as
well, but sometimes they have dependencies on Unreal maps/textures, etc.
that we do not have with Red Orchestra. If you're feeling determined,
you can [download the Unreal Tournament 2004
Demo](http://download.cnet.com/Unreal-Tournament-2004-demo/3000-7441_4-10262824.html)
to get the packages and decompile it.

