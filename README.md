# MobileDeviceDetection C# library
It is a helper library to
- Get information of all mobile devices which currently plugin in USB
- Raise events whenever a mobile device is pluged or unpluged in USB

# Getting Started
1. To search mobile devices, use class MobileDeviceSearcher
var searcher = new MobileDeviceSearcher();
var devices = searcher.SearchAllDevices();

2. To detect device plug / unplug, use class MobileDeviceDetection
var watcher = new MobileDeviceDetection();
deviceDetection.DevicePlugDetected += (sender, e) => { // TODO };
deviceDetection.DeviceUnplugDetected += (sender, e) => { // TODO };

In e parameter, there is a property DeviceID.
To get mobile device informtation based on DeviceID, use MobileDeviceSearcher.SearchDeviceById().
