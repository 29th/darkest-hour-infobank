---
title: Using a Joystick
permalink: /Using_a_Joystick
layout: page
author: Olson
date: 2008-11-25T21:17:44Z
category: 
---
You will have to add these to be able to setup your joystick right, but
its not much of a problem.

Open up **Steam\\SteamApps\\common\\red
orchestra\\DarkestHour\\System\\darkesthourUser.ini** in Notepad.

Somewhere between \[Engine.Input\] and \[Engine.Controller\] there
should be multiple lines starting with "joy(Number)=". If they are
there, look if you also have some that start with "joy(letter)=".

If you don't have the letter-ones already, add the following lines below
the "joy(number)=" lines:

`JoyX=`  
`JoyY=`  
`JoyZ=`  
`JoyR=`  
`JoyU=`  
`JoyV=`  
`JoySlider1=`  
`JoySlider2=`

The ones with the numbers define which button on the joystick does what,
and the ones with the letters define which if the joystick's axes do
what.

You can assign the joystick's buttons in the game's menu, just like you
would assign keyboard keys. After that, the game writes the action you
bound to that key into the User.ini. You can write it in there by
yourself too, if you know what its called. The "joy(letter)=" lines
should be empty after the "=", so there is no action defined for them.

And here are the "codes" for various actions you might need, that you
have to assign to the axes in the User.ini. I don't know what axis is
what on your joystick, because I have a gamepad with two joysticks so my
setup is different from yours. You might have to experiment a bit.

Here are the codes:

Strafing:

`Axis aStrafe SpeedBase=300.0 DeadZone=0.1`

Moving Forward/Backward:

`Axis aBaseY SpeedBase=300.0 DeadZone=0.1`

Turning Left/Right:

`Axis aBaseX SpeedBase=30.0 DeadZone=0.1`

Look Up/Down:

`Axis aLookUp SpeedBase=30.0 DeadZone=0.1`

This is used to look up or down.

Now add these lines behind the "joy(Axis/Letter)=" you want to assign
the action to. For example, if you want to turn around with the X-Axis,
and you want to look up with the Y-Axis, you would have create the
following lines:

`JoyX=Axis aBaseX SpeedBase=30.0 DeadZone=0.1`  
`JoyY=Axis aLookUp SpeedBase=30.0 DeadZone=0.1`

If you want to invert an axis you can simply add "Invert=-1" to the end
of the line.

Don't mess with the values for the strafing and the forwards movement,
because I don't know what happens if you do.

You can change the SpeedBase value for the look-around-lines if you feel
that the joystick is to sensitive or not sensitive enough in-game. If
you want to turn around faster, increase the value, if you want to turn
slower, decrease it. I think that twice the value is twice as fast.

You can edit the
[dead-zone](http://answers.yahoo.com/question/index?qid=1006031104229)
if this one doesn't work for you.

You also have to edit the *darkesthour.ini*' which is found in the same
folder and change all of the lines **UseJoystick=False** to
**UseJoystick=True**.

As an example, here is the setup I use to be able to use the pedals from
my steering wheel setup to rotate the tank turret:

`JoyX=`  
`JoyY=Axis aStrafe SpeedBase=32768.0 DeadZone=0.2 Invert=-1`  
`JoyZ=`  
`JoyR=`  
`JoyU=`  
`JoyV=`  
`JoySlider1=`  
`JoySlider2=`

It also works for regular strafing, though its response time is too
slow.

