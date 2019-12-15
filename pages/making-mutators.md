---
title: Making Mutators
permalink: /Making_Mutators
layout: page
author: Olson
date: 2011-01-15T21:13:55Z
category: 
---
  - [Getting Started](Mutators:Getting_Started "wikilink")
  - [Parachute Mutator Tutorial](Parachute_Mutator_Tutorial "wikilink")
    by Lt. Col. Wilson
  - [Jeep MG Mutator Tutorial](Jeep_MG_Mutator_Tutorial "wikilink") by
    Lt. Col. Wilson
  - [Enabling In-Game](Mutators:Enabling_In-Game "wikilink")

## Tutorials

  - [Modifying Packages](Modifying_Packages "wikilink")
  - [Existing Mutators](Existing_Mutators "wikilink")
  - [3D Buzz Video
    Tutorials](http://www.3dbuzz.com/vbforum/sv_videonav.php?fid=c4db699e6a9ffcb7cbcaa428747668bf)
    Requires free registration, well worth it
  - [BeyondUnreal Wiki:
    Mutator](http://wiki.beyondunreal.com/Legacy:Mutator)
  - [BeyondUnreal Wiki: Useful Mutator
    Functions](http://wiki.beyondunreal.com/Legacy:Useful_Mutator_Functions)
  - [BeyondUnreal Wiki: Mutator
    Topics](http://wiki.beyondunreal.com/Legacy:Mutator_Topics)
  - [BeyondUnreal Wiki: Adding Config to
    GUI/WebAdmin](http://wiki.beyondunreal.com/Legacy:Mutator_Config_GUI_\(UT2004\))
  - [BeyondUnreal Wiki: UnrealScript
    Lessons](http://wiki.beyondunreal.com/Legacy:UnrealScript_Lessons)
  - [Tactical Gamer Forums: Your First
    Mutator](http://www.tacticalgamer.com/red-orchestra-map-mod-development/70568-modding-ro-mutators-gametypes-etc.html)
    A basic, functionless mutator as well as how to compile it (not the
    best instructions)
  - [UnrealScript Tutorials](http://stuvel.eu/unrealtower/tutorials) A
    list of 9 basic tutorials
  - [BeyondUnreal Wiki: Code
    Optimization](http://wiki.beyondunreal.com/Legacy:Code_Optimization)
    (Advanced)

## Utilities

  - [UMake](http://mb.link-m.de/umake/)
  - [WOTGreal](http://www.wotgreal.com/)
  - [Recompile With Batch File](Recompile_With_Batch_File "wikilink")
  - [Custom Intro Maps](Custom_Intro_Maps "wikilink")

## Misc. Tips & Tricks

  - Iterating through all Pawns is a bad idea. Avoid using ForEach
    AllActors(class'Pawn', P) on the server.
    <span style="color:#000080">**`For (P = Level.PawnList; P != None; P
    = P.NextPawn)`**</span> does the same and is much more efficient.
    Always look for a linked list that contains the actors you want to
    access before using ForEach AllActors(...).

