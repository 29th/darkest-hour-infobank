---
title: Parachute Mutator Tutorial
permalink: /Parachute_Mutator_Tutorial
layout: page
author: Wilson
date: 2011-01-01T21:23:32Z
category: 
---
## Introduction

This tutorial will teach you to create a very simple mutator that gives
a parachute to every player when they spawn, so that when they jump off
a building, they 'float' down.

We will call this mutator **DH\_MyParachute**

## Creating the File

The first thing we have to do is create the **Package** and the
**Class** (aka the directory and the file). Browse to your [Darkest Hour
Game Directory](Game_Paths "wikilink") and create a folder called
**DH\_MyParachute**. This is the name of our new **Package**. Inside
your new folder, create a subfolder called **Classes**.

Inside the **Classes** folder, create a file called
**DH\_MyParachuteMut.uc** and open it in your favourite text editor.
(Note that it is optional to include the name of your **Package** in the
name of your Mutator file, but it is recommended for organisational
purposes.)

## The Class Declaration

The first thing we want to do in our file is declare that we are
creating a new **Class**, name it and base it off of a **Parent Class**.

``` cpp
class DH_MyParachuteMut extends Mutator;
```

We named the class **DH\_MyParachuteMut**, like the filename. We then
based it off of **Mutator**, which is a class that already exists in the
Game's code. You can view it in *Engine\\Classes\\Mutator.uc*. The
Mutator class is already linked into the Game and has several functions
and properties already made in it. Rather than starting completely from
scratch, we will base our **DH\_MyParachuteMut** class of of the
**Mutator** class, and *inherit* those functions and properties.

## The Default Properties

Now we'll go over the **Default Properties**, which are always written
at the bottom of the class file. Notice there are no semicolons used in
defaultproperties.

``` cpp
defaultproperties
{
    GroupName="DH_MyParachute"
    FriendlyName="My Parachute Mutator"
    Description="This is my first mutator"
    RemoteRole=ROLE_SimulatedProxy
    bAlwaysRelevant=true
}
```

The first line declares the **GroupName**. I'm not entirely sure what
purpose this serves, but I'm pretty sure it's required, so I always just
put the package name.

The **FriendlyName** and **Description** are what are displayed in the
**Mutator Window** when you are starting a server so you know which
mutators you are selecting.

The **RemoteRole** and **bAlwaysRelevant** do something very important,
but I don't remember what it is, so I always include them just in case.
You should too.

So now your file should look like this:

``` cpp
class DH_MyParachuteMut extends Mutator;


defaultproperties
{
    GroupName="DH_MyParachute"
    FriendlyName="My Parachute Mutator"
    Description="This is my first mutator"
    RemoteRole=ROLE_SimulatedProxy
    bAlwaysRelevant=true
}
```

It is technically a working mutator, and it will load in-game. Of
course, it doesn't actually *do anything* yet.

## The Main Function

Now that we have the template for the Mutator setup, it's time to make
it *do* something. One of the functions that all classes which extend
**Mutator** have access to is **ModifyPlayer()**, because it is declared
in the **Mutator** class. When we add it to our class, we essentially
override the one in the **Mutator** class. This is a basic concept of
*Object-Oriented Programming*.

The **ModifyPlayer()** function is called by the game every time a
player spawns. By overriding it, the engine is basically asking *our
class* if we have anything extra we want to do when a player spawns. So
we will copy over the function declaration from the parent **Mutator**
class to override it in *our* class:

``` cpp
function ModifyPlayer(Pawn Other)
{
}
```

Now we are overriding it and doing nothing - basically we are just
stopping the parent **Mutator** class from doing whatever it was going
to do in this function. How do we know that we're actually getting here
in-game? Let's add a log to make sure.

``` cpp
function ModifyPlayer(Pawn Other)
{
    Log("Successfully Overrode ModifyPlayer()");
}
```

If you try this in-game right now, the log will show this every time a
player spawns.

So let's give our spawning player that parachute. Notice that in the
function declaration, the only parameter is **Other**, which is a
**Pawn**. This means that we have access to the **Pawn** of the player
that is spawning, thus access to any of the properties and functions
inside the **Pawn** class (view this by opening
**Engine\\Classes\\Pawn.uc**).

One of the functions in the Pawn class that we now have access to is
**GiveWeapon()** which gives a weapon or item to the Pawn. All we need
to specify in the parameters is the class name of the weapon/item we
want to give. The parachute requires 2 items be given:

  - DH\_Equipment.DH\_ParachuteStaticLine
  - DH\_Equipment.DH\_ParachuteItem

<!-- end list -->

``` cpp
function ModifyPlayer(Pawn Other)
{
    Log("Successfully Overrode ModifyPlayer()");

    Other.GiveWeapon("DH_Equipment.DH_ParachuteStaticLine");
    Other.GiveWeapon("DH_Equipment.DH_ParachuteItem");
}
```

Using the **Other** variable, which is the actual Pawn that just
spawned, we called the **GiveWeapon()** function on the Pawn, and
specified the items we wanted to give in each line.

One last thing - it is good practise to allow the Parent class (in this
case the **Mutator** class) to do whatever it was going to do in the
function you're extending, unless you are intentionally trying to block
what it was going to do. In this case we are not, so we'll call the
**ModifyPlayer()** function of the **Parent** class using **Super**, and
pass on the parameter **Other**.

``` cpp
function ModifyPlayer(Pawn Other)
{
    Log("Successfully Overrode ModifyPlayer()");

    Other.GiveWeapon("DH_Equipment.DH_ParachuteStaticLine");
    Other.GiveWeapon("DH_Equipment.DH_ParachuteItem");

    Super.ModifyPlayer(Other);
}
```

## The Final Product

``` cpp
class DH_MyParachuteMut extends Mutator;

function ModifyPlayer(Pawn Other)
{
    Log("Successfully Overrode ModifyPlayer()");

    Other.GiveWeapon("DH_Equipment.DH_ParachuteStaticLine");
    Other.GiveWeapon("DH_Equipment.DH_ParachuteItem");
    
    Super.ModifyPlayer(Other);
}

defaultproperties
{
    RemoteRole=ROLE_SimulatedProxy
    bAlwaysRelevant=true
    GroupName="DH_MyParachute"
    FriendlyName="My Parachute Mutator"
    Description="This is my first mutator"
}
```

Now [Compile It](Modifying_Packages "wikilink"), generate the **.ucl**
file, and [Enable it In-Game](Mutators:Enabling_In-Game "wikilink")\!

