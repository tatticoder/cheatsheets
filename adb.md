---
title: ADB (Android Debug Bridge)
description: Android Debug Bridge command-line tool helps us to interact with connected Android device/ Emulator. We can install, debug apps using ADB
created: 2019-06-17
updated: 2019-06-17
---

## Selecting Device

|Command|Description|
|---|---|
|`adb devices`|This command is used to retrieve all devices by serial number|
|`adb devices -l`|List of devices by product/model|

## App installation & uninstallation
|Command|Description|
|---|---|
|`adb install <apk>`|Install app|
|`adb shell pm install <path_from_phone>`|Install app from phone path|
|`adb shell pm install -r <path_from_phone>`|Reinstall app from phone path|
|`adb uninstall <com.test.package.name>`|Remove the app|

## App info 
|Command|Description|
|---|---|
|`adb shell pm list packages`|List package names|
|`adb shell pm list packages -f`|as above + path tp APks|
|`adb shell pm -3`| only third party packages|
|`adb shell pm -s`|only system packages|
|`adb shell pm -u`|also uninstalled packages|
|`adb shell dumpsys package packages`|List info on all apps|
|`adb shell pm dump name`|List info on one package|
|`adb shell pm path package`|path to the APK file|


## Permissions
|Command|Description|
|---|---|
|`adb shell pm permission groups`|Permission groups definitions|
|`adb shell pm list permissions -g -f`|List permissions details|


## Common actions
|Command|Description|
|---|---|
|`am start -a android.intent.action.VIEW -d URL`|To open the URL|


## Miscellaneous
|Command|Description|
|---|---|
|`screencap -p .png`|Screenshot (saved on device)|
|`screenrecord .mp4`|Screen capture (path on device)|

## ADB daemon
|Command|Description|
|---|---|
|`adb kill-server`|Kill the server if it is running|
|`adb start-server`|Ensure that there is a server running|
|`adb root`|Restarts the adbd with root permissions|



