---
title: Compressing Files
permalink: /Compressing_Files
layout: page
author: Wilson
date: 2009-10-19T15:25:41Z
category: 
---
Darkest Hour allows clients to connect to an HTTP server to download
custom content instead of downloading it directly form the server. This
provides a much faster download for the client and less stress on the
server. In addition, the engine on which Darkest Hour runs has a built
in compressor/decompressor, so the files that clients download can be in
a compressed format, thus increasing the download speed even more.

## UCC Commands

The program that handles compression and several other functions is
known as **ucc**, and is located in your [Red Orchestra System
Directory](Game_Paths "wikilink"). Unfortunately you cannot simply open
this program and run it - you must use it through a command prompt. To
learn how to use UCC, see the article called [Using
UCC](Using_UCC "wikilink")

To compress your file, use the *compress* command

`ucc compress ..\DarkestHour\Maps\DH-filename.rom`

Note the ..\\ at the beginning, as you will have to browse up from the
*\\System\\* directory and into the *\\DarkestHour\\Maps\\* directory.

This should output the following on success:

`Compressed ..\DarkestHour\Maps\DH-filename.rom -> ..\DarkestHour\Maps\DH-filename.rom.uz2 (26%)`

Note that the percentage is some random number usually less than 100% -
this is normal and does not mean it was incomplete.

You should now have your new compressed (.uz2) file in your Maps
directory. You can also do this with Textures, Sounds, etc. and they can
all be uploaded to the same HTTP directory for fast downloading.

## Troubleshooting

#### Wrong Directory

`'ucc' is not recognized as an internal or external command,`  
`operable program or batch file.`

This error is given when you are not currently in the proper directory.
Make sure that your command prompt is in your red orchestra\\System
directory when you type *ucc*. For example:

`C:\Program Files\Steam\steamapps\common\red orchestra\System>`

#### Forward Slashes

`Error occured opening DH-filename.rom`

This error is given when you use forward slashes instead of backslashes.
Remember, the path should read:

`..\DarkestHour\Maps\DH-filename.rom`

#### Misspelled

`Source ..\DarkestHour\Maps\DH-filename.rom not found`

This error is given if the file name you typed does not exist. Check
your spelling and ensure the map is present in your Darkest Hour Maps
directory.

#### Forgot Compress

`Commandlet ..\DarkestHour\Maps\DH-filename.rom not found`

This error is given when you forget to add *compress* to your command
line. Your command should read:

`ucc `**`compress`**` ..\DarkestHour\Maps\DH-filename.rom`

