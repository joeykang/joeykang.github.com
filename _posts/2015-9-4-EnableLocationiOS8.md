---
layout: post
title: Enable location service in iOS 8
---


### In iOS 8, fist call either:

```
// For use in background
requestAlwaysAuthorization (on the instance)
```

```
// For use in foreground
requestWhenInUseAuthorization (on the instance)
```
### ADD a key to your project's *Info.plist*

```
<key>NSLocationAlwaysUsageDescription</key>
<string>Your message goes here</string>
```
```
<key>NSLocationWhenInUseUsageDescription</key>
<string>Your message goes here</string>
```


[Reference](http://matthewfecher.com/app-developement/getting-gps-location-using-core-location-in-ios-8-vs-ios-7/)
