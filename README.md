# fablab-octoprint

Octoprint installation and deployment for our 3D printers
*Octoprint installation guide*

Version 1.0

24.08.2020

TABLE OF CONTENTS

[1 Introduction ](#introduction) 
=================================

[2 Installation on ultimaker 2+ ](#installation-on-ultimaker-2)
================================================================

[2.1 BOM ](#bom)

[2.2 Parts to 3d print ](#parts-to-3d-print)

[2.3 Hardware installation ](#hardware-installation)

[2.3.1 Raspberry pi 3 or 4 installation
](#raspberry-pi-3-or-4-installation)

[2.3.2 Camera installation ](#camera-installation)

[2.4 Software intallation ](#software-intallation)

[2.5 Octoprint configuration ](#octoprint-configuration)

[2.6 Create a octoprint printer profile on cura
12](#create-a-octoprint-printer-profile-on-cura)

[3 Installation on Prusa I3 MK3S ](#installation-on-prusa-i3-mk3s) 
====================================================================

[3.1 BOM ](#bom-1)

[3.2 Parts to 3d print ](#parts-to-3d-print-1)

[3.3 Hardware installation ](#hardware-installation-1)

[3.3.1 Camera installation ](#camera-installation-1)

[3.3.2 Raspberry pi installation ](#raspberry-pi-installation)

[3.4 Software intallation ](#software-intallation-1)

[3.5 Octoprint configuration ](#octoprint-configuration-1)

[4 Installation of the octroprint plugin ](#installation-of-the-octroprint-plugin) 
====================================================================================

[4.1 List of the plugins](#list-of-the-plugins)

 Introduction
============

This document explains how to install octoprint for the Ultimaker 2+ and
for the Prusa I3 MK3S.

Installation on ultimaker 2+
============================

BOM
---


| N° |              Materiel              | Quantity |                                                                    link                                                                    |   
|:--:|:----------------------------------:|:--------:|:------------------------------------------------------------------------------------------------------------------------------------------:|
|  1 |      Raspberry Pi 3 B+ or   4      |     1    |                                                https://www.pi-shop.ch/raspberry-pi-3-model-b                                               |   
|  2 |         Raspberry Pi Camera        |     1    |                                          https://www.pi-shop.ch/raspberry-pi-noir-camera-module-v2                                         |   
|  3 |  Raspberry Pi Camera   Cable 610m  |     1    | https://www.distrelec.ch/fr/cable-flexible-pour-camera-raspberry-pi-ou-raspberry-pi-display-adafruit-1731/p/30133569?queryFromSuggest=true |   
|  4 | Type A to type b USB   cable 162mm |     1    |                      https://www.mouser.ch/ProductDetail/TE-Connectivity-AMP/1487586-3?qs=8nBuXIG0xJCnrEJlF8nvyQ%3D%3D                     |   
|  5 |              Cable tie             |     3    |                                                                                                                                            |   
|  6 |            Power supply            |     1    |                                           https://www.pi-shop.ch/steckernetzteil-microusb-5v-25a                                           |   
|  7 |           Srew M6 x 25 mm          |     4    |                                                                                                                                            |   
|  8 |               M6 nut               |     3    |                                                                                                                                            |   
|  9 |              M3 x 16mm             |     4    |                                                                                                                                            |   
| 10 |              M3 x 12mm             |     2    |                                                                                                                                            |          

Parts to 3d print
-----------------

 | N° |                 Parts                 | Quantity |                    link                   |   
|:--:|:-------------------------------------:|:--------:|:-----------------------------------------:|
|  1 | Support.STL or   SupportRpi3_HEIG.STL |     1    | https://www.thingiverse.com/thing:1726120 |  
|  2 |              picam_holder             |     1    | https://www.thingiverse.com/thing:2702779 | 

Hardware installation
---------------------

### Raspberry pi 3 or 4 installation

Put the tie Cable Wire holder in place as the picture.

![2](https://user-images.githubusercontent.com/69343914/91181582-6ab16300-e6e9-11ea-9409-560b965efa54.jpg)

Use the M2.5 screws and screw the raspberry pi on the 3d support part
(support.stl) and screw it below the Ultimaker 2+ with the M3 screws and
nuts.

![3](https://user-images.githubusercontent.com/69343914/91181584-6b49f980-e6e9-11ea-9c01-34dcf64b5e24.jpg)
![4](https://user-images.githubusercontent.com/69343914/91181586-6b49f980-e6e9-11ea-883f-db26fdd9608f.jpg)

Connect the raspberry to the Ultimaker 2+ via USB and connect the power
supply to the raspberry.

![5](https://user-images.githubusercontent.com/69343914/91181587-6be29000-e6e9-11ea-9f2f-63644955ab98.jpg)

### Camera installation

Connect the camera with the raspberry pi camera cable 1m and put the
camera on the 3d printed part "picam_holder.stl". Move the extruder in
the right front corner. With the double side tape put in place the
camera. Be careful to let a small gap below the extruder and the camera.


![6](https://user-images.githubusercontent.com/69343914/91181590-6be29000-e6e9-11ea-9a81-50eaf667915f.jpg)
![7](https://user-images.githubusercontent.com/69343914/91181591-6c7b2680-e6e9-11ea-84a5-7cde543a78de.jpg)

Manage the rest of the camera cable as the picture below. Connect the
camera to the raspberry pi.

![8](https://user-images.githubusercontent.com/69343914/91181595-6c7b2680-e6e9-11ea-8b4a-9fa00f2c4866.jpg)

Software intallation
--------------------

For the raspberry pi 3 installation follow this
[tutorial](https://help.prusa3d.com/fr/article/octoprint-building-an-image-for-raspberry-pi-zero-w_5556)
until the step V:

Use the "HEIG-Devices" wifi network, for the password ask the fablab
supervisor.

Connect to the raspberry pi on ssh.

Change the default password of the raspberry pi.

Change the host name of the raspberry pi. (UltimakerXfablab)

With a web browser access to the octoprint server.

![9](https://user-images.githubusercontent.com/69343914/91181598-6d13bd00-e6e9-11ea-890e-d370ee22df8a.jpg)

Octoprint configuration
-----------------------

1.  Set a user name and a password

![10](https://user-images.githubusercontent.com/69343914/91181599-6d13bd00-e6e9-11ea-8b0e-f2dc185e3b77.jpg)

2.  Disable anonymous tracking

![11](https://user-images.githubusercontent.com/69343914/91181600-6d13bd00-e6e9-11ea-850f-69c65402507c.jpg)

3.  Disable connectivity check

![12](https://user-images.githubusercontent.com/69343914/91181602-6dac5380-e6e9-11ea-88c6-59eee68f9010.jpg)

4.  Enable plugin Blacklist processing

![13](https://user-images.githubusercontent.com/69343914/91181603-6dac5380-e6e9-11ea-8207-3a58fb932e0f.jpg)

5.  Create a printer Ultimaker 2 + profile with this values

> For the print bed and build volume

![14](https://user-images.githubusercontent.com/69343914/91181605-6e44ea00-e6e9-11ea-8ade-869f880f579e.jpg)

For the Hotend & extruder

![15](https://user-images.githubusercontent.com/69343914/91181607-6e44ea00-e6e9-11ea-8c96-088e0786d6c1.jpg)

And for the axes

![16](https://user-images.githubusercontent.com/69343914/91181608-6edd8080-e6e9-11ea-835d-87e303eb2c2e.jpg)

Don't forgot to invert the Z Axis control !

6.  Disable those two options (model size detection and SD support)

![17](https://user-images.githubusercontent.com/69343914/91181611-6edd8080-e6e9-11ea-8a0f-93b93902eb8d.jpg)

Create a octoprint printer profile on cura
------------------------------------------

For using octoprint you need a special printer profile in Cura slicer.

1.  Create a new Ultimaker 2+ printer profile

![18](https://user-images.githubusercontent.com/69343914/91181612-6f761700-e6e9-11ea-98f0-2c4e5e07bd2a.jpg)

2.  In the menu preference select the new Ultimaker 2+ printer profile
    and click on "Machine setting".

![19](https://user-images.githubusercontent.com/69343914/91181613-6f761700-e6e9-11ea-9e8c-30f26ce41056.jpg)

3.  Change the G-code Falvor for Marlin.

![20](https://user-images.githubusercontent.com/69343914/91181614-6f761700-e6e9-11ea-8ef7-25a1d8f00994.jpg)

When you want print with an Ultimaker 2+ via octoprint use the Ultimaker
2+ octoprint printer profile.

![21](https://user-images.githubusercontent.com/69343914/91181616-700ead80-e6e9-11ea-870c-375205c7f615.jpg)

You can now use octoprint, you just have to upload your gcode file on
the octoprint server and you are ready to go !

Installation on Prusa I3 MK3S
=============================

BOM
---

 | N° |              Materiel              | Quantity |                                                                    link                                                                    |   
|:--:|:----------------------------------:|:--------:|:------------------------------------------------------------------------------------------------------------------------------------------:|
|  1 |      Raspberry Pi 3 B+ or   4      |     1    |                                                https://www.pi-shop.ch/raspberry-pi-3-model-b                                               |   
|  2 |         Raspberry Pi Camera        |     1    |                                          https://www.pi-shop.ch/raspberry-pi-noir-camera-module-v2                                         |   
|  3 |  Raspberry Pi Camera   Cable 610m  |     1    | https://www.distrelec.ch/fr/cable-flexible-pour-camera-raspberry-pi-ou-raspberry-pi-display-adafruit-1731/p/30133569?queryFromSuggest=true |   
|  4 | Type A to type b USB   cable 162mm |     1    |                      https://www.mouser.ch/ProductDetail/TE-Connectivity-AMP/1487586-3?qs=8nBuXIG0xJCnrEJlF8nvyQ%3D%3D                     |   
|  5 |              Cable tie             |     3    |                                                                                                                                            |   
|  6 |            Power supply            |     1    |                                           https://www.pi-shop.ch/steckernetzteil-microusb-5v-25a                                           |   
|  7 |           Srew M6 x 25 mm          |     4    |                                                                                                                                            |   
|  8 |               M6 nut               |     3    |                                                                                                                                            |   
|  9 |              M3 x 16mm             |     4    |                                                                                                                                            |   
| 10 |              M3 x 12mm             |     2    |                                                                                                                                            |   

Parts to 3d print
-----------------

  | N° |           Parts           | Quantity |                       link                      |
|:--:|:-------------------------:|:--------:|:-----------------------------------------------:|
|  1 |        BallNut.stl        |     1    |    https://www.thingiverse.com/thing:3114849    |  
|  2 |   ffLink_90_support.stl   |     1    |                                                 |   
|  3 |   mfLink_90_support.stl   |     2    |                                                 |  
|  4 |     mfLink_support.stl    |     1    |                                                 |   
|  5 |      raspiCamBack.stl     |     1    |                                                 |   
|  6 | raspiCamCover_NoLense.stl |     1    |                                                 |   
|  7 |      xAxisBracket.stl     |     1    |                                                 |  
|  8 |        FullCase.stl       |     1    | https://www.thingiverse.com/thing:3004038/files |   

Hardware installation
---------------------

### Camera installation

With all the 3d printed parts excepted the "FullCase.stl", the M6 screws
and the m3x16mm screw, mount the camera support as the picture below.

![22](https://user-images.githubusercontent.com/69343914/91181617-700ead80-e6e9-11ea-9e6f-742f25295e13.jpg)

Mount the camera in the support, fix the camera cable with the cable
ties and connect the camera to the raspberry pi.

![23](https://user-images.githubusercontent.com/69343914/91181618-70a74400-e6e9-11ea-9723-8efbae5dcf80.jpg)

### Raspberry pi installation

Insert the raspberry pi into the 3dprinter part "FullCase.stl". screw
the cover with the four M3x16mm screws. Set the assembly to the Prusa I3
MK3S with the two M3x12mm screws.

![24](https://user-images.githubusercontent.com/69343914/91181621-70a74400-e6e9-11ea-8c9c-b018a76ef692.jpg)

Connect the power supply and the 3d printer to the raspberry pi.

Software intallation
--------------------

For the raspberry pi 3 installation follow this
[tutorial](https://help.prusa3d.com/fr/article/octoprint-building-an-image-for-raspberry-pi-zero-w_5556)
until the step V:

Use the "HEIG-Devices" wifi network, for the password ask the fablab
supervisor.

Connect to the raspberry pi on ssh.

Change the default password of the raspberry pi.

Change the host name of the raspberry pi. (PrusaXfablab)

With a web browser access to the octoprint server.

![25](https://user-images.githubusercontent.com/69343914/91181622-70a74400-e6e9-11ea-80ad-1e631c1fd8e9.jpg)

Octoprint configuration
-----------------------

1.  Set a user name and password

2.  Disable anonymous tracking

![26](https://user-images.githubusercontent.com/69343914/91181623-713fda80-e6e9-11ea-87b1-ca4bb4fb1282.jpg)

3.  Disable connectivity check

![27](https://user-images.githubusercontent.com/69343914/91181626-713fda80-e6e9-11ea-8599-a4c922ac61c9.jpg)

4.  Enable plugin Blacklist processing

![28](https://user-images.githubusercontent.com/69343914/91181627-71d87100-e6e9-11ea-81bf-5666888862a5.jpg)

5.  Create a printer Prusa I3 MK3S profile with this values

> For the print bed and build volume

![29](https://user-images.githubusercontent.com/69343914/91181629-71d87100-e6e9-11ea-801f-e6f5f0ba4d98.jpg)

For the Hotend & extruder

![30](https://user-images.githubusercontent.com/69343914/91181631-71d87100-e6e9-11ea-852a-069402b6b12f.jpg)

And for the axes

![31](https://user-images.githubusercontent.com/69343914/91181633-72710780-e6e9-11ea-901f-f49d3595f18f.jpg)

Don't forgot to invert the Z Axis control!

6.  Disable those two options

![32](https://user-images.githubusercontent.com/69343914/91181634-72710780-e6e9-11ea-9f4b-1fd6224a30f9.jpg)

You can now use octoprint, you just have to upload your gcode file on
the octoprint server and you are ready to go !

Installation of the octroprint plugin
=====================================

With octoprint it is possible to install plugin. To install a plugin, go
on the octoprint settings and click on plugin manager and click on "get
more".

![33](https://user-images.githubusercontent.com/69343914/91181635-73099e00-e6e9-11ea-9caf-0bd94f8bea82.jpg)

You can research the plugin with research bar.

![34](https://user-images.githubusercontent.com/69343914/91181636-73099e00-e6e9-11ea-99b3-36e2980ea945.jpg))

When you have find the plugin you want click "install", finish the
installation and reboot the octoprint.

![35](https://user-images.githubusercontent.com/69343914/91181638-73099e00-e6e9-11ea-91a5-b35ce790313b.jpg)

List of the plugins
-------------------

List of the added plugins

|     Name                   |     Function                                                                   |
|----------------------------|--------------------------------------------------------------------------------|
|     Custom   Background    |     Simple   plugin that replaces the temperature graph's background image.    |
|     Fullscreen   Plugin    |     Open webcam   in fullscreen mode                                           |
