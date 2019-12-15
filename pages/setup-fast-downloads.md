---
title: Setup Fast Downloads
permalink: /Setup_Fast_Downloads
layout: page
author: Wilson
date: 2008-08-20T16:37:23Z
category: 
---
Darkest Hour allows clients to connect to an HTTP server to download
custom content instead of downloading it directly form the server. This
provides a much faster download for the client and less stress on the
server. Assuming you have a web host to host your files, it is very
simple to configure your server to route clients there to download
files. All downloading will take place in-game and the client will never
know he was routed elsewhere.

## Your Server Configuration

1.  Open your server's DarkestHour.ini file. It is located in the
    [Darkest Hour System Directory](Game_Paths "wikilink").
2.  Fine the line containing *\[IpDrv.HTTPDownload\]*. You can use
    CTRL+F to find it quicker.
3.  On the line below it, *RedirectToURL=*, add your web site's Darkest
    Hour file directory.
    1.  For example, *RedirectToURL=<http://mywebsite.com/dhfiles/>*
    2.  Remember to include *<http://>*

In addition, the engine on which Darkest Hour runs has a built in
compressor/decompressor, so the files that clients download can be in a
compressed format, thus increasing the download speed even more. You
will have to compress the files on your own if you would like to use
this feature (Read the guide [here](Compressing_Files "wikilink")).

To use compressed files, ensure that the *UseCompression=* property is
set to *True* - otherwise ensure it is set to *False*.

## Your Files Directory

Inside of your HTTP server's designated Darkest Hour file directory, you
do not have to set up a folder-tree structure. Simply put every single
file in it. To clarify, this folder will contain maps, textures, sounds,
etc. -- Any custom content that needs to be downloaded.

<http://mywebsite.com/dhfiles/DH-mapname.rom.uz2>  
<http://mywebsite.com/dhfiles/Texturepack.utx.uz2>  
`etc.`

*(.uz2 is the file extension that the files take once they are
compressed)*

