---
title: Setup Server Admins
permalink: /Setup_Server_Admins
layout: page
author: Wilson
date: 2009-09-12T13:33:25Z
category: 
---
In DarkestHour.ini

1\. Look for the section called '\[UWeb.WebServer\]' and in that section
look for 'bEnabled=' and edit it to say the following:

`bEnabled=True`

2\. Look for the section called '\[Engine.GameInfo\]' and in that
section look for 'AccessControlClass=' and edit it to say the following:

`AccessControlClass=XAdmin.AccessControlIni`

3\. Then save the file and upload it back into your RO server FTP and
restart the server...this will then create a file in the 'system' folder
called 'xadmin.ini '

4\. Browse to your web administration at

<http://><YourServerIP>`:8075/ServerAdmin`

5\. Login to your web administration using either the default
Username/Password which is Admin/Admin (case sensitive) or you can just
make a copy of the 'xadmin.ini ' file to your desktop and edit it and
give yourself your own Username/Password...

6\. Once you login there is a new section on the web administration
called ' Admins & Groups ' near the top...

7\. Click that and then you can edit yourself and add more admins and
set privileges as well....

Sources and More Info:

  - <http://forums.gameservers.com/viewtopic.php?t=8431>
  - <http://forums.gameservers.com/viewtopic.php?t=8460>

