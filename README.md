# MobileDeviceDetection C# library
It is a helper library to:
- Get information of all mobile devices which currently plugin in USB
- Raise events whenever a mobile device is pluged or unpluged in USB

# Getting Started
<p>1. To search mobile devices, use class MobileDeviceSearcher</p>
``` C#
var searcher = new MobileDeviceSearcher();
var devices = searcher.SearchAllDevices();
```

<p>2. To detect device plug / unplug, use class MobileDeviceDetection</p>
``` C#
var watcher = new MobileDeviceDetection();
deviceDetection.DevicePlugDetected += (sender, e) => { // TODO };
deviceDetection.DeviceUnplugDetected += (sender, e) => { // TODO };
deviceDetection.Start();
```
<p>Remember to stop it after using, by deviceDetection.Stop() method.</p>
<p>In e parameter, there is a property DeviceID.</p>
<p>To get mobile device informtation based on DeviceID:</p>
``` C#
var searcher = new MobileDeviceSearcher();
var device = searcher.SearchByDeviceId(e.DeviceID);
```
