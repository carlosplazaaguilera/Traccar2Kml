# Traccar2Kml
I love Traccar project!! but since 2015 nobody has publish how to show Traccar data in Google Earth (https://www.traccar.org/forums/topic/traccar-on-google-earth/ ).
So here we go! 
IMPORTANT NOTE: This is UNOFICIAL Traccar complement!!. PLEASE, Do not disturb Traccar project!!. 
Thanks a lot. Traccar2Kml - WIP 0.0 (Work in Progress)

Objetive
With Traccar2Kml, you will see your Traccar devices in 3D, in Google Earth near real time, with autorefreshing positions each X seconds.
Also you will see your Traccar info with your own Google Earth GIS information like; Pois, Links, Photos, Streetview and anymore interactive items in you map.
This PHP code will read Traccar MySQL database and create a .KML file with the position of each Device enable.

Requirements
A working LAMP amd Traccar server running over MySQL database and bidirectionals comunications between LAMP server (URL/IP) and Google Earth.

Structure files:
 - Traccar2Kml.php   Main executable file
 - Traccar2Kml.conf  ServerName, DatabaseName, DataBasePassword, RefreshTime, ServerUrl, IconsPath, OutPutPath, OutFilename, HTMLDeBugOutput, IconPixels (default 64), IconScalePixel... 
 - Traccar2Kml.kml   This file may be opened by Google Earth, which will read each X seconds Traccar2KmlOut.kml.
 - Traccar2KmlOut.kml This file cotains the devices data.
 - Traccar2KmlOut.html Html chart for Debuging outout file data.
 - T2KrenderIcons.php This file convert each .svg categories files icon to .png Google Earth valid icon 64x64 pixels. This function will not be implemented until Traccar2Kml V2.0.


RoadMap

- v0.1. Read Config file
- v0.2. Read tc_devices table and print in screen Traccar active decvices.
- v0.3. Read tc_positions table of each active devices and print in screen, Traccar active decvices, DeviceName, DeviceLastTime, DeviceLat, DeviceLong.
- v0.4. Read extra info from any table like category icon (filename.png), attributes... and show it as description field. 
- v0.5. Same as point 4. showing .png icon, 
(At this point every Traccar categories icons will be converted manually to .png file)
- v0.6. Create a DeBug mode which print results in a HTML chart Traccar2KmlOut.html.
- v07. Write a Traccar2KmlOut.kml with one device.
- v08. Write a Traccar2KmlOut.kml with all devices.
- v09. Traccar2KmlOut.kml description field will use HTML rich text,
- v1.0 All Traccar info appear correctly in Google Earth.
- v1.5 Debug and Refine code
- v2.0 T2KrenderIcons.php Automatic categories icons render
- v3.0 Other format export .CSV, .JSON, .GPX, GeoServer/Mapserver valid format in order to render a TileMap for OsmAnd realtime AVL.


Last update.
 29th October 2020, Carlos Plaza Aguilera hidrantescpa@gmail.com 
 
 This code is under development and no working version exist. Help needed.
 
 Carlos Plaza Aguilera
