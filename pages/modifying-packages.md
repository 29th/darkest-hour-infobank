---
title: Modifying Packages
permalink: /Modifying_Packages
layout: page
author: Wilson
date: 2011-01-01T21:15:04Z
category: 
---
This article is intended for learning purposes, such as modifying
mutators or *reading* default game packages.

**NOTE:** Recompiling default game packages such as DH\_Engine,
DH\_Game, etc. will prevent you from joining a standard game server. You
are welcome to *decompile* them but do not *recompile* them (basically
do not delete their **.u** files from the System directories).

## Decompiling a Package

This page will explain how to decompile a **.u** package using an
example.

To decompile **\\DarkestHour\\System\\DH\_MutatorExample.u**, [Using
UCC](Using_UCC "wikilink"), enter:

`ucc batchexport ..\DarkestHour\System\DH_MutatorExample.u class uc ..\DarkestHour\DH_MutatorExample\Classes -mod=DarkestHour`

You should now have a folder called **DH\_MutatorExample** inside your
**DarkestHour** directory, with a **Classes** folder inside that. The
**Classes** folder will now contain all of the **.uc** files included in
the **.u** package. The **.uc** files can be opened and modified with a
text editor.

## Compiling a Package

With the **\\DarkestHour\\DH\_MutatorExample\\Classes\\** folder created
and containing '.uc' files, the package can be re-compiled by the
following process.

1.  Delete the original **DH\_MutatorExample.u** file from the
    **\\DarkestHour\\System\\** directory (if it exists)
2.  Open the file **\\DarkestHour\\System\\DarkestHour.ini**
3.  Search the file for **EditPackages**
4.  Add a line to the list, **EditPackages=DH\_MutatorExample**

Then, [Using UCC](Using_UCC "wikilink"), enter:

`ucc make -mod=DarkestHour`

You will now see a new **DH\_MutatorExample.u** in the
**\\DarkestHour\\System** directory. This contains your modified code.

### Creating the .ucl File

(Optional) The .ucl file contains text variables such as those necessary
to add a Mutator the Mutator Menu. [Using UCC](Using_UCC "wikilink"),
enter:

`ucc exportcache DH_MutatorExample.u -mod=darkesthour`

You will now see a new **DH\_MutatorExample.ucl** in the
**\\DarkestHour\\System** directory.

### Creating the .int File

(Optional, Rarely Needed) The .int file contains setup data necessary
for using a new Game Type. [Using UCC](Using_UCC "wikilink"), enter:

`ucc dumpint DH_MutatorExample.u -mod=darkesthour`

You will now see a new **DH\_MutatorExample.int** in the
**\\RedOrchestra\\System** directory. You will have to move this to your
**\\DarkestHour\\System\\** directory.

