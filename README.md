iOS Open GPX Tracker
====================

Open GPX Tracker is an app for iOS devices (iPhone, iPad, iPod). It allows you to create GPX files and send them by email. 

This app has no time restrictions when creating the gpx files, no ads, no in-app-purchases. 

Requires iOS 7.0 or above. Open GPX tracker is an open source app.


![My image](https://merlos.github.io/iOS-Open-GPX-Tracker/images/open-gpx-tracker-4-screenshots.png)

You can use Open GPX tracker for: 

 - Creating routes and waypoints for editing Open Street Map.
 - Publishing Open Street Map Traces.
 - Creating real GPX files for testing your iOS apps in Xcode.

# Main Features

 - Displays tracking information in a map
 - Support Open Street Maps, MapBox and Open Cycle Maps as map sources
 - Pause / Resume tracking
 - Add waypoint to user location
 - Add waypoint to any place in the map with a long press
 - Edit waypoint name
 - Drag & Drop waypoint pin
 - Remove waypoints
 - Send by email saved session (track + waypoints)
 - Load on map a saved session and continue tracking

# Install

Please note, that because it is still in the early stages of development the app is **NOT AVAILABLE on the App Store**. In order try it you need to download the source code and compile it by yourself using Xcode. 

If you want to run it on a device, you also need an Apple developer account.


# Download Source code
This application is written in Swift. To download the code run this command in a console:

``` 
 git clone https://github.com/merlos/iOS-Open-GPX-Tracker.git
```

Then, to test it open the file `OpenGpxTracker.xcworkspace` with XCode.

Please note that this source code was released under the GPL license.  So any change on the code shall be made publicly available and distributed under the GPL license (this does not apply to the pods included in the project which have their own license)


## Selecting the tile server
**Open GPX Tracker** supports using different map sources (Apple Mapkit, Open Street Maps, MapBox, Open Cycle Maps). That is, you can view the maps generated by Open Street Maps.

Tiles provided by Apple Mapkit are displayed by default. To change the tile server you need to edit the file `ViewController.swift`, and modify the line:

```swift
 //Default
 map.tileServer = GPXTileServer.Apple
 
 //Setting OpenStreetMaps
 map.tileServer = GPXTileServer.OpenStreetMaps
       
``` 

The list of available tile servers is defined in `GPXTileServer.swift`.


Please note the [limitations of using Open Street Maps Tile Servers](http://wiki.openstreetmap.org/wiki/Tile_usage_policy)

### Adding another tile server
Adding a tile server is easy, just edit the file `GPXTileServer.swift`, uncomment the lines with `AnotherMap` and modify the templateUrl to point to the new tile server.

You have a list of tile servers in [Open Street Maps Wiki](http://wiki.openstreetmap.org/wiki/Tile_servers)

# TODO

- Do not request user location while not tracking and in background (to save battery)
- Add user interface to change the tile server as well as copyright 


License
====================

Open GPX Tracker app for iOS.  Copyright (C) 2014  Juan M. Merlos (@merlos)

This program is free software: you can redistribute it and/or modify
it under the terms of the **GNU General Public License** as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.

----

This app uses:
 - [iOS GPX Framework](https://github.com/merlos/ios-gpx-framework) created by Watanabe Toshinori and podified by  [@Pierre-Loup](https://github.com/Pierre-Loup/)


