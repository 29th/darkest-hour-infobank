---
title: Unofficial Tweak Guide
permalink: /Unofficial_Tweak_Guide
layout: page
author: Olson
date: 2008-09-18T04:08:39Z
category: 
---
''This guide was written for Red Orchestra by Divinehammer at [Red
Orchestra's
Forums](http://www.redorchestragame.com/forum/showthread.php?t=10701).
When it refers to *RedOrchestra.ini* or other files in the Red Orchestra
directory, you should also apply these to the Darkest Hour directory.''

-----

For those of you interested in getting the very best out of RO and
exploring some options you may never knew to exist I have started this
thread. Most tweaks listed are from Koroush Ghazi from
<http://www.tweakguides.com/> and his UT2004 tweak guide (RO runs on
almost the exact engine). He has done all the hard work finding and
compiling the threads for UT2004 so all credit goes to him and his
sources. I just simply reiterate them and add some RO-specific tweaks.
The purpose of the thread is to compile any known tweaks into one thread
to be supplemented by new ones so, by all means, post yours as well\!

Also be aware that I am not posting tweaks that make the game have any
less quality for performance increase. All tips either increase graphics
at slight performance loss, no performance loss, or just increase
performance with no loss of eye candy.

All tweaks done are at your own risk.

## Basic Ingame Tweaks

### Disable Reduce Mouse Lag

Go into configuration and go in under the menu "Input" at the top. Then
untick Reduce Mouse Lag. This feature is known to take up a lot of CPU
and do absolutely nothing to the average user. If you, however, got
problems with your mouse moving in odd ways, tick it back on.  
Listed under \[WinDrv.WindowsClient\]. This tip was taken from
StrangFrik so Ill just post his original words:

`“Long load times or laggy keyboard response?`  
`I played around with my redorchestra.ini file which is located here:`  
`SteamApps\red orchestraSystemredorchestra.ini`  
`The two things changed in the redorchestra.ini are:`  
`UsePrecache=True - bNeverPrecache=False.`  
`They are now UsePrecache=False - bNeverPrecache=True”`

### Disable Mouse Smoothing

Turn off mouse-smoothing- This has been known to actually cause more lag
than smoothing. Unless it has changed from the mod to Ostfront, go ahead
and disable this feature.

### Disable HDR Bloom

(For ATI Users) Turn off HDR Bloom- If your textures seem blurred and
you have an ATI card, it is most likely from the Bloom effect RO uses.
There is a problem with ATI cards at lower resolutions. If you fit into
this category turn it off.

## RedOrchestra.ini Tweaks

You can find the .ini by going to C:/Program
Files/Valve/steam/SteamApps/common/red orchestra/system/RedOrchestra.ini

Open with notepad.

### Change Cache Size

This controls the amount of RAM used for caching models and other game
related data. Helps alleviate the stutter associated with loading of new
models and other game data. May help with FPS if your game stutters due
to loading game data. Defaults to 32.

CacheSizeMegs=32 (tweak taken from
<http://ucguides.savagehelp.com/Tribe>...FPSVisuals.htm)

Listed under \[Engine.GameEngine\].

`256 Megabytes of RAM or less`  
`CacheSizeMegs=32`  
  
`512 Megabytes of RAM`  
`CacheSizeMegs=64`  
  
`768 Megabytes of RAM`  
`CacheSizeMegs=128`  
  
`1 Gigabyte of RAM or more`  
`CacheSizeMegs=256`  
  
`2 Gigabyte of RAM or more`  
`CacheSizeMegs=512`  
*`(This``   ``tweak``   ``entered``   ``by``   ``Divinehammer,`` 
 ``there``   ``seems``   ``to``   ``be``   ``some``   ``debate`` 
 ``over``   ``whether``   ``you``   ``should``   ``use``   ``more`` 
 ``than``   ``256.``   ``This``   ``is``   ``the``   ``setting`` 
 ``though``   ``that``   ``I``   ``use.)`*

### Turn off PreCaching

Also in your redorchestra.ini under \[ALAudio.ALAudioSubsystem\]

`Change UsePrecache=True to UsePrecache=False`  
`and under [Engine.LevelInfo]`  
`Change bNeverPrecache=false to bNeverPrecache=true`  
`and under [Engine.NullRenderDevice]`  
`Change UsePrecaching=True to UsePrecaching=False`  
`and under [D3DDrv.D3DRenderDevice]`  
`Change UsePrecaching=True to UsePrecaching=False`  
`and under [D3D9Drv.D3D9RenderDevice]`  
`Change UsePrecaching=True to UsePrecaching=False`  
`and under [OpenGLDrv.OpenGLRenderDevice]`  
`Change UsePrecaching=True to UsePrecaching=False`  
`and under [PixoDrv.PixoRenderDevice]`  
`Change UsePrecaching=True to UsePrecaching=False`

### Change Brightness

Brightness=.8, Contrast=.7, Gamma=.8  
"...the best video config is Brightness = .70 , gamma = 1.00 , and
Contrast = .70"

Now, this may not look as good as it would in the mod because some
settings may have been changed when the transition was made to Ostfront.
I havent tested it enough to be definite about better quality but its
listed here nonetheless. Edit: After some testing, the default settings
actually look better imo. Different monitors will give different results
so theres no harm in testing out your own configuration.

\=== DesiredRefreshRate=60 ===

Found under \[D3DDrv.D3D9renderDevice\]. Set to the highest refresh rate
your monitor supports at the resolution you play at. You can check by
right clicking and going to properties/settings/advanced and then
looking in the monitor section. While some have reported they cant tell
the difference, anything less than 75hz bothers my eyes. Prolonged use
of 60hz can damage the eyes supposedly. This may be the cause of
headaches or other such annoyance while playing games for a long time so
make sure this setting is right. Update: 60hz is fine for LCD monitors
and should not cause irritation. The above applies to CRT.

\=== LevelOfAnisotropy=1 ===

Found under \[D3DDrv.D3D9renderDevice\]. This is just a built in
anistropic filtering settings. Unfortunately there is no setting for
anti-aliasing so there really is no point in using this over your video
card control center settings. Leave it to 1 unless you want to disable
your video card settings and use this instead.

\=== OverrideDesktopRefreshRate=False ===

Found under \[D3DDrv.D3D9renderDevice\]. Set to true.

\=== Compressedlightmaps=True ===

Found under \[D3DDrv.D3D9renderDevice\]. Set to false for better
lighting.

These Tweaks were found at the RaidersForum, much thanks.

\=== UsePrecaching=True ===

This preloads graphics textures into memory before you actually see them
to reduce in-game jerkiness when textures load "on the fly". If you have
a newer video card with more video memory (64MB or more) then set this
to True for smoother gameplay. Otherwise set to False for older video
cards.

\=== UseTripleBuffering=True === Set this option to True to reduce
screen "tearing" (when VSync is off) and improve overall graphics
performance. Using Triple Buffering may cause problems and glitches for
those with less graphics memory (32MB or less), so turn off if you’re
experiencing problems and/or you have an older card.

\=== UseHardwareTL=True === If your graphics card has onboard Transform
and Lighting (T\&L) set this to True. Most recent graphics cards do
feature T\&L, so unless you have an older card don't set this to False
for best graphics performance.

\=== UseHardwareVS=True === Similar to T\&L above, this option makes use
of the hardware Vertex Shader on modern graphics cards. The most recent
graphics cards feature VS, such as the GeForce3 and GeForce4 Ti cards
(but not the GeForce4MX). If you have an older card set this to False,
otherwise leave at True for best graphics performance.

\=== UseCubemaps=True === This is a trick used to make some reflective
surfaces (like the water puddles in DM-Antalus for example) look like
they’re actually reflecting what’s around them in 3D. Turning it off
(set to False) can improve graphics performance without any noticeable
drop in image quality. If you have a faster system, set it to True for
best visual quality at the cost of minimal fps.

\=== DesiredRefreshRate=60 === If you have VSync enabled (See UseVsync
setting below for more info) then your refresh rate will be limited to
whatever this setting is. However, to reduce monitor flickering and
eyestrain, you should set this value to the highest refresh rate
supported by your monitor at the desired resolution. For example, your
monitor may support a maximum refresh rate of 85Hz (85fps) at 1280x1024
resolution. This setting is at 60 by default, but you could set it to 85
to make full use of your monitor's capabilities and ease the strain on
your eyes.

\=== UseCompressedLightmaps=True === Using compressed lightmaps can
improve your graphics performance quite noticeably, however the colors
and shadows in the game (based on these "lightmaps") will not be quite
as nice or crisp. If you have a fast system with 128MB of VRAM or more,
set this option to False for best image quality and slightly quicker
loading times, but at the cost of a few fps.

\=== Use16bitTextures=False === UT2003 can be run in either 16-bit or
32-bit (See In-game Settings section). While you can determine this in
the settings screens, if you choose to run at 16-bit, there's no point
in 32-bit quality textures being loaded for each game. Set this option
to True to use the lower quality 16-bit textures to match the 16-bit
color depth you've chosen. This will improve fps at the cost of visual
quality and color banding.

\=== UseVSync=False === Without going into too much detail, Video
Synchronization (VSync) is the synchronization of your graphics card and
monitors' abilities to redraw the screen a number of times each second.
This is measured in Hz (which is the same as frames per second), and
your monitor will have a maximum rating in Hz for each resolution – e.g
1280x1024 at 85Hz. When set to False, your fps will improve slightly,
however, you may see some image "tearing" as your monitor and graphics
card go slightly out of synchronization when the refresh rate exceeds
the monitor's abilities. Turn off VSync (set to False) for best graphics
performance, however if the image tearing is annoying then set to True.
Setting TripleBuffering to True (See TripleBuffering above) will help
reduce any tearing. (If you have at least midrange equipment then try
UseVSync = true and TripleBuffering = true then edit if you want more
FPS, but tearing)

The only way to get rid of visual tearing is to turn VSync ON.

If you turn VSync ON, however, setting "usetriplebuffer=true" will help
uncap your framrate which would normally be stuck at your refresh rate
speed when using simple double buffering. In effect, it should help
things run more smoothly when VSync is enabled but it will use more
video memory.  
[Click here for more
information](http://www.ocworkbench.com/2006/articles/DXtweaker)

\=== LevelOfAnisotropy=1 === This setting controls the amount of
Anisotropic Filtering in UT2003. Basically Anisotropic Filtering
improves texture and general image quality, however it comes at the cost
of some performance, particularly on older (e.g. pre-GeForce4 and Radeon
9500) cards. Setting this to 0 will improve performance on most machines
without a noticeable drop in image quality. Of course increasing the
value will improve image quality at a variable rate of performance loss
based on your hardware.

\=== AvoidHitches=False === Setting this to True might help those with
graphics cards which have 64MB of VRAM and who have chosen high detail
settings. It significantly reduces the occurrence of substantial
hitches, but can reduce average framerate, so leave this option at
default unless you have problems.

\=== DecompressTextures=False === Just as with compressed lightmaps,
compressed textures reduce image quality slightly, however they improve
graphics performance dramatically (especially with Precaching set to
True) as more textures can be loaded into video memory when compressed.
Set this option to True only if you have a very fast machine and a
graphics card with 128MB of VRAM or more, and you want the absolute
highest quality of textures showing. Setting this option to True will
cripple most machines' performance.

## DarkestHourUser.ini Settings

### Screenshot Tweaks

By default, the screenshot command **shot** is bound to **<F9>**. The
resulting screenshot is saved as a **.bmp** file in the
**Steam\\SteamApps\\common\\red orchestra\\ScreenShots** folder as
**shot\#\#\#\#\#.bmp**. However, you can change both how the screenshot
is named and where it is saved by changing the following variables in
the **Steam\\SteamApps\\common\\red
orchestra\\DarkestHour\\System\\darkesthourUser.ini** section,
**'\[Screenshots\]**:

`ShotMask=Shot%c                   `  
`ShotCount=87                      `  
`ShotDir=..\DarkestHour\Screenshots`

**ShotMask** is made up of characters you directly insert, like *Shot*,
and variable name, like:

`%p = Player name > Player name`  
`%c = Count > consecutively numbers screenshots`  
`%d = Date > Date screenshot taken`  
`%m = Map name > Current map name`  
`%t = Time > Time in some long format, eight digits`

**ShotCount** is pretty obvious; is incremented every time a screenshot
is taken.

**ShotDir** is where the screenshot is saved.

For example,

`[Screenshots]`  
`ShotMask=DH-%p-%m-%d-%c`  
`ShotCount=50`  
`ShotDir=..\DarkestHour\Screenshots`

will result in

`"DH-DHPlayer-8-24-2008-00050.bmp" `

## Display Settings

These are found in the Main Menu's Configuration \> Display section.

### Resolution

This setting determines how many pixels (the individual dots which make
up a computer image) are displayed on the screen. A resolution of
800x600 implies 800 pixels wide by 600 pixels high on your monitor.
Obviously the higher the resolution (the more pixels), the more detailed
and clearer the game image, but it takes more graphics card and CPU
power and hence you will see less Frames Per Second (FPS). The highest
resolution available in this list of resolutions is limited to what your
graphics card and monitor are actually capable of rendering (drawing on
screen). The resolution alone will have the biggest impact on your
framerate, along with texture settings.

### Color Depth

This determines how many different colors can be displayed on screen.
The two options are 16-bit and 32-bit, with 32-bit only shown if your
graphics card supports it. 32-bit color looks the nicest, with 16-bit
color showing more color "banding" – that is, the gradation between
colors is more apparent. 32-bit color also resolves a lot of problems
with flickering and missing textures, especially in OpenGL mode. However
32-bit color requires a bit more power than 16-bit, so if you need more
FPS, switch to 16-bit.

### Full Screen

Tick this option to run UT2004 in full screen mode, for the least
likelihood of errors or crashes. If unticked, UT2004 will run in a
window on your Windows desktop and this may cause problems.

### Gamma, Brightness, Contrast

These three settings affect how bright/dark and crisp/soft your image
looks. Set these to taste, using the picture provided in the Gamma Test
window below these settings as a guide to how it will impact on the
in-game images. It really depends on your monitor's brightness/contrast
settings as well. For reference, my monitor's Brightness is 70% and
Contrast 100%, while my UT2004 settings are: Gamma of 0.90, Brightness
of 0.70, and Contrast of 0.70.

### Texture Detail

This determines how detailed the in-game textures (the images that cover
the surface of every 3D object) will look. The options range from Lowest
to Highest. The higher the setting, the crisper and more detailed the
textures around you will look. Higher texture settings primarily impact
on loading times and loading pauses in-game, and less on FPS. The more
Video RAM your graphics card has (ideally 128MB or more), and the more
system RAM you have (ideally 512MB or more) the less stuttering and
freezing you will get with higher texture settings, as these are loaded
into and out of RAM from your hard drive.

### Character Detail

Similar to the Texture Detail setting above, from Lowest to Highest this
determines how detailed the textures on all the characters look. The
higher the setting combined with the number of players in a match
determines the performance impact, particularly on loading times.

### World Detail

Options are Low, Normal and High. The higher this setting the richer
your surroundings, as more optional 3D objects are loaded onto the
landscape, but the higher the computing power required (and hence the
lower your FPS) especially on levels where you can see further and/or
there are more optional objects to see. If you have a slower graphics
card and/or CPU lower this setting to improve your FPS.

### Physics Detail

Options are Low, Normal and High. This setting changes the level of
detail for the simulation of physics in the UT2004 gaming world. The
higher the setting the more CPU effort required to crunch the numbers to
show more realistic effects ranging from the basic "ragdoll" effects
through to effects such as water ripples. I would recommend that the
slower your CPU (i.e the closer to the 1GHz minimum spec), the lower
your Physics setting, as this can really affect your FPS.

### Dynamic Mesh LOD

This setting controls the degree to which the Level of Detail (LOD) on
Dynamic Mesh objects (i.e. animated objects like characters and
vehicles) is affected by distance. The higher this setting, the less
quickly the level of detail (number of polygons) on such objects is
removed as they move into the distance. Put another way, the higher the
setting, the better the visual quality but the greater the impact on
your FPS depending on how many dynamic objects are on screen. A setting
of Normal is recommended for most people.

### Decal Stay

This setting, if the Decal option is ticked (and Projectors is also
ticked), will determine how long decals (scorch marks and the like) will
remain on surfaces. The three settings are Low, Normal and High, and
unless you are a stickler for detail, Normal or even Low should be just
fine. Setting it to High may negatively impact your FPS, especially with
lots of weapons fire on screen.

### Character Shadows

This setting determines the type of shadows cast by animated characters,
and can have a major impact on performance. When set to None, characters
do not cast a shadow. This provides the fastest performance. When set to
Blob, characters cast a generic, low detailed 'blob-like' shadow. This
setting is recommended for most people. Setting Character Shadows to
Full provides full-detailed shadows but can impact FPS quite noticeable,
especially when there are many characters onscreen.

### Decals

Decals are the dynamic marks left on surfaces by weapons fire,
explosions and the like. Ticking this option turns them on to improve
the realism of the game, but may affect FPS negatively, especially on
levels where there are lots of players firing lots of weapons. I
recommend leaving Decals on unless you're really struggling for FPS.

### Dynamic Lighting

Ticking this option allows the various lights in the game to react
realistically with objects, shining at different angles off weapons,
characters and walls based on the light's position. This makes for great
effects but can decrease your framerate, so untick it if you need more
FPS.

### Detail Textures

Adds a level of fine detail or "grain" to certain textures (such as
pitted or brushed metallic surfaces) when examined close up. However
this can reduce your FPS and use up more RAM, so untick it if you need
better performance.

### Coronas

A corona is the halo of glare given off from light sources, such as
lamps and shock-combo explosions. Unticking this option will give you
slightly more FPS, especially if you also have Dynamic Lighting ticked.

### Trilinear Filtering

This rendering method makes the graphics and colors seem smoother and
cleaner, but can reduce performance noticeably if you have an old (e.g
GeForce2) video card. Most newer systems should notice little if any
performance drop from having this enabled. If you're unsure about this
setting, or are struggling for performance then leave it unticked.

### Projectors

Projectors covers a range of images projected onto textures, such as
shadows from characters and objects (like tree shadows) and Decals (see
above). The noticeable effects of unticking this option include removal
of such shadows and decals, even if Character Shadows are enabled and
the Decals option is ticked. Only untick Projectors if you really need a
few extra FPS, as it makes things look fairly unrealistic.

### Foliage

As the setting name suggests, ticking this option enables grass and
other decorative foliage. Unticking it will improve your FPS by reducing
foliage details, particularly on maps like ONS-Prim\#eval\#si which have
a lot of trees and grassland.

### Weather Effects

Ticking this option enables the various weather effects found on several
maps, like raindrops, lightning, etc. Unticking this option will improve
FPS on such maps by reducing the load on your CPU and graphics card.

\=== Mindesiredframerate = 0 === If you are not seeing any blood effects
etc, then you might need to change this in the RedOrchestra.ini file, it
keeps all the gore effects even if your FPS drops low.

## Optimal Graphics Quality (ATI Users)

What you will need:

  - Omega Drivers
  - ATI Tray Tools (included with Omega install)

### Red Orchestra Settings

1.  Obviously all ingame settings should be set at the highest option
    (except for bloom if it makes textures look blurry).
2.  Resolution should be set to highest possible with a refresh rate of
    at least 75hz unless you are using an lcd monitor in which case hz
    does not matter.
3.  Compressedlightmaps should be set to false as detailed above in the
    guide.
4.  HUD- This is more preference than anything but I like my screen to
    be clear of all useles information. I have the compass off (who
    needs to kno north, south...you arent going on a trek across
    country), the clip count off (i just count as i spend them), the
    personal info off (its cool to kno where ur hit but id rather have
    it empty), and hints off. Basically i have no hud besides death
    messages and chat messages and those upper left hand messages. This
    is nice because nothing is fixed so I can have the pleasure of no
    hud unless alot is going on and then I only have the bare minimum. I
    like to spend more time surveying the battlefield than staring at
    some useless icons. All of these options are available from the
    ingame menu.

### ATI Tray Tools Settings

Right click on the Tray Tools in the system tray when its loaded up and
then proceed to Direct3D. Here you will have an array of options.

1.  Under Antialiasing, set it to 4x or 6x.
2.  Under Antisotropic Filtering, set it to 4x or higher (4x recommended
    as it looks virtually the same as anything higher yet performs
    leagues better) and check "Enable High Quality AF".
3.  Under Optimizations, check both options which are "Enable
    Antisotropic Filtering Optimization" and "Enable Trilinear Filtering
    Optimization"
4.  Disable Catalyst A.I. This attempts to tweak games by itself to make
    them perform better. There is no real definite conclusion of whether
    it reduces image quality or improves performance with no difference.
    However, if you want to make absolutely sure that you are getting
    the best image quality, disable this.

ATI Tray Tools does not have to be left in the system tray for the
settings to work. Of course the amount of quality you are able to get
depends on your system, especially the video card. I hope this helps.
Any further graphical upgrade is up to the devs\! Thanks for taking the
time to read the guide.

### Example Sections of RedOrchestra.ini

`[D3DDrv.D3DRenderDevice]`  
`DetailTextures=True`  
`HighDetailActors=True`  
`SuperHighDetailActors=False`  
`UsePrecaching=True`  
`UseTrilinear=True`  
`AdapterNumber=-1`  
`ReduceMouseLag=False`  
`UseTripleBuffering=True`  
`UseHardwareTL=True`  
`UseHardwareVS=True`  
`UseCubemaps=True`  
`DesiredRefreshRate=60`  
`UseCompressedLightmaps=False`  
`UseStencil=False`  
`Use16bit=False`  
`Use16bitTextures=False`  
`MaxPixelShaderVersion=255`  
`UseVSync=True`  
`LevelOfAnisotropy=1`  
`DetailTexMipBias=0.0`  
`DefaultTexMipBias=-0.5`  
`UseNPatches=False`  
`TesselationFactor=1.0`  
`CheckForOverflow=False`  
`AvoidHitches=False`  
`OverrideDesktopRefreshRate=False`  
`ReportUnusedTextures=False`

`[D3D9Drv.D3D9RenderDevice]`  
`DetailTextures=True`  
`HighDetailActors=True`  
`SuperHighDetailActors=True`  
`UsePrecaching=True`  
`UseTrilinear=True`  
`AdapterNumber=-1`  
`ReduceMouseLag=False`  
`UseTripleBuffering=True`  
`UseHardwareTL=True`  
`UseHardwareVS=True`  
`UseCubemaps=True`  
`DesiredRefreshRate=60`  
`UseCompressedLightmaps=False`  
`UseStencil=False`  
`Use16bit=False`  
`Use16bitTextures=False`  
`MaxPixelShaderVersion=255`  
`UseVSync=True`  
`LevelOfAnisotropy=1`  
`DetailTexMipBias=0.000000`  
`DefaultTexMipBias=-0.500000`  
`UseNPatches=False`  
`TesselationFactor=1.000000`  
`CheckForOverflow=False`  
`OverrideDesktopRefreshRate=False`  
`DecompressTextures=False`  
`TerrainLOD=0`  
`SkyboxHack=False`  
`LowQualityTerrain=False`

### User.ini

You can find the .ini by going to C:/Program
Files/Valve/steam/SteamApps/common/red orchestra/system/User.ini

\==== ConfiguredInternetSpeed=10000 ====

Found under \[Engine.Player\]. Set between 6000-8000 if you have a cable
(or similar speed) modem. I find 7000 or 8000 works best. For 56k use
between 2400 and 3000.

#### Non-toggleable Iron Sights

Courtesy of o0|REDRUM|0o from [this
thread](http://www.redorchestragame.com/forum/showthread.php?t=4598)

Scroll down the binds at the top of the .ini until you find the button
you use for iron sights. Paste this on to the line:
RightMouse=ROIronsights | Onrelease ROironsights

There is some problems with this tweak in that the gun doesnt always
release when you let go of the button. Its rough but its the only option
as of now.

#### Non-toggleable Objectives Map

Scroll down the binds at the top of the .ini until you find the button
you use for iron sights. Paste this on to the line: O=ShowObjectives |
Onrelease ShowObjectives Where O= the button you use to show objectives.

#### Toggleable Mouse Sensitivity

Courtesy of Mortisrose

A nice little tweak to make aiming smoother is to toggle mouse
sensitivity. In the User ini. file choose a button (ie. Mouse4= or any
button) Right after the equal sign type:

`set Engine.PlayerInput MouseSensitivity 0.8 | onrelease set Engine.PlayerInput MouseSensitivity 2.0`

The first number (0.8) is the desired sensitivity with the button
pressed and the last number (2.0) is your default mouse sensitivity when
not pressing the button. Make sure the last number is the same with your
own mouse sensitivity.

To do the ironsights and mouse sensitivity would be difficult as one is
a toggle and one is an onrelease. But this should work... Copy and paste
this into your user ini over aliases 32 & 33....

`;Aliases[32]=(Command="Axis aBaseX SpeedBase=100.0 DeadZone=0.1",Alias="SpaceFighter_JoyX")`  
`;Aliases[33]=(Command="Axis aLookUp SpeedBase=100.0 DeadZone=0.1",Alias="SpaceFighter_JoyY")`  
`Aliases[32]=(Command="ROIronSights|set Engine.PlayerInput MouseSensitivity 0.5|set input p Newsightoff",Alias="Newsighton")`  
`Aliases[33]=(Command="ROIronSights|set Engine.PlayerInput MouseSensitivity 2.5|set input p Newsighton",Alias="Newsightoff")`

Change the sensitivity to your liking. I used P in my example, for your
key, change it to yours in both lines above "set input p". Then add this
to your desired key:

`p=Newsighton`

Personally i just use a seperate key for both, but if this works for
some then cool. Actually just tested it and works as advertised.

#### Edit

Just reread the toggle question and it sounds like you want the
ironsights toggle along with the mouse toggle. If thats the case then
here... RightMouse=ROIronSights|set Engine.PlayerInput MouseSensitivity
0.5|Onrelease ROironsights|Onrelease set Engine.PlayerInput
MouseSensitivity 2.5

Lean toggle same deal as above....

`;Aliases[34]=(Command="Axis aUp Speed=+300.0 | Axis aStrafe SpeedBase=300.0 DeadZone=0.1",Alias="SpaceFighter_JoyV")`  
`;Aliases[35]=(Command="Axis aBaseY SpeedBase=300.0 DeadZone=0.1 Invert=-1",Alias="SpaceFighter_JoySlider1")`  
`;Aliases[36]=(Command="leanleft | OnRelease LeanLeftReleased",Alias="LeanLeft")`  
`;Aliases[37]=(Command="leanright | OnRelease leanrightreleased",Alias="LeanRight")`  
`Aliases[34]=(Command="leanleft|set input q leanleftoff",Alias="leanlefton")`  
`Aliases[35]=(Command="LeanLeftReleased|set input q leanlefton",Alias="leanleftoff")`  
`Aliases[36]=(Command="leanRight|set input e leanrightoff",Alias="leanRighton")`  
`Aliases[37]=(Command="LeanRightReleased|set input e leanRighton",Alias="leanrightoff")`  
  
`q=leanlefton`  
`e=leanRighton`

Lean script doesn't work for me. Left is good, right doesn't work.

#### Edit

FIXED\!

You had an extra "t" in Alias \[37\], at the very end where you define
the alias. leanrightoff, not leanrighttoff.

  -   
    \-)

Should be:

`;Aliases[34]=(Command="Axis aUp Speed=+300.0 | Axis aStrafe SpeedBase=300.0 DeadZone=0.1",Alias="SpaceFighter_JoyV")`  
`;Aliases[35]=(Command="Axis aBaseY SpeedBase=300.0 DeadZone=0.1 Invert=-1",Alias="SpaceFighter_JoySlider1")`  
`;Aliases[36]=(Command="leanleft | OnRelease LeanLeftReleased",Alias="LeanLeft")`  
`;Aliases[37]=(Command="leanright | OnRelease leanrightreleased",Alias="LeanRight")`  
`Aliases[34]=(Command="leanleft|set input q leanleftoff",Alias="leanlefton")`  
`Aliases[35]=(Command="LeanLeftReleased|set input q leanlefton",Alias="leanleftoff")`  
`Aliases[36]=(Command="leanRight|set input e leanrightoff",Alias="leanRighton")`  
`Aliases[37]=(Command="LeanRightReleased|set input e leanRighton",Alias="leanrightoff")`  
  
`q=leanlefton`  
`e=leanRighton`

#### Robot Voice Reads Text

`bNoTextToSpeechVoiceMessages=true`

Change that to false in the User.ini

### Miscellaneous

#### Level of Detail

EDIT: No longer available in latest version of Tray Tools

Unfortunately I can only provide this tweak to ATI users who have ATI
Tray Tools. Load up Tray Tools, right click the icon and go to Direct3D,
additional options, and click on Texture LOD 0. Change it to -2 to
increase texture quality. Remember this applies to all games. You will
find that scratches, cuts, etc. on player models are clearly visible and
there is overall much more detail in the RO textures. However, probably
moreso than any other tweak, it comes at the price of fps drop. I saw
about a 10-20fps drop. The worst part is that you get a kind of texture
"sparkling" effect on certain maps. It doesnt look that bad but it can
be noticeable. If you really notice texture quality though this is a
very good tweak to squeeze all you can out of the textures. Tray Tools
does not have to be left in the system tray for this tweak to work.

#### Console Commands

Courtesy of Redrum

Some console commands that may be helpful..

**Stat commands**

  - MEMSTAT - Displays Windows memory usage
  - STAT ALL - Shows all stats
  - STAT AUDIO - Shows audio stats
  - STAT FPS - Displays your frames per second
  - STAT GAME - Displays game stats
  - STAT HARDWARE - Shows hardware stats
  - STAT NET - Shows network game play stats
  - STAT NONE - Turns off all stats
  - STAT RENDER - Displays rendering statistics

**Demo Commands**

  - DEMOPLAY \[demoname\] - Plays the specified demo
  - DEMOREC \[demoname\] - Records a demo using the demoname you type
  - STOPDEMO - Stop recording a demo

*Other Commands*'

  - BRIGHTNESS \[number\] - Changes the brightness level to the
    specified number
  - CONFIGHASH - Displays configuration info
  - CONTRAST \[number\] - Changes the contrast level to the specified
    number
  - DEBUG CRASH - Test crashes the game with an error
  - DEBUG EATMEM - Tests memory allocation until full
  - DEBUG GPF - Test crashes the game with a general protection fault
    error
  - DEBUG RECURSE - Test crashes the game by infinite recursion
  - DUMPCACHE - Displays the memory gcache contents
  - EXEC \[filename\] - Executes a file in the UT2003 /system/ directory
    by default
  - EXIT Exits the game entirely
  - FLUSH - Flushes all caches and relights
  - GAMMA \[number\] - Changes the gamma level to the specified number
  - GETCURRENTRES - Displays your current resolution
  - GETCURRENTTICKRATE - Displays your current tick rate
  - GETMAXTICKRATE - Displays the maximum allowed tick rate
  - NETSPEED \[number\] - Sets the net speed, default is 10000
  - OBJ GARBAGE - Collects and purges objects no longer in use
  - PAUSESOUNDS - Pauses all sounds
  - PREFERENCES - Opens advanced settings
      - THERE MAY BE SETTINGS IN THIS MENU THAT MIGHT HELP THE PEOPLE
        STRUGGELING TO GET RO TO RUN SMOOTHLY. I HAVE NOT DONE A
        COMPARISON BETWEEN THE ACTUAL GAME SETTINGS AND THESE. I ALSO DO
        NOT HAVE EXPLANATIONS OF THOSE SETTINGS USE AT YOUR OWN RISK\!
  - RELAUNCH - Relaunches the engine
  - REPORT - Copies a report of the current game to clipboard
  - SET \[class variable value\] - Sets a specified class and specified
    variable with the specified value
  - Engine.PlayerInput MouseSensitivity \[number\] - Sets the mouse
    sensitivity to the specified number
  - SETRES \[WxHxD\] - Sets your screen resolution to the specified
    width, height, and color depth
  - SOCKETS - Displays a list of sockets in use
  - TOGGLEFULLSCREEN - Toggles fullscreen mode
  - TYPE \[text\] - Displays the specified text on the console
  - UNPAUSESOUNDS - Un-pauses all sounds

#### Combat Photographer Binds

For those who want to be able to get a clean screen on the fly and not
have to remove the hud by going to the menu and wasting time, possibly
missing the shot, type this in the console (x is just an exampe for the
key you want):

`set input x togglescreenshotmode`  
`or`  
`set input x showhud 0`

