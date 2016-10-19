---
title: PlatformDetector - device
---

# device

Use the *device* method to query for an indicator of the web enabled device that is running the application.

## Syntax
`device()`

## Return value

The return value is a string that describes a device category, according to the web client’s user string. The system compares the user agent string against a set of configurable values in the `platform.json` file. An example of a general device category is iPhone.