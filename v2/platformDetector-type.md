---
title: PlatformDetector - type
---

# type

Use the *type* method to query for general category information about the client that is currently running.

## Syntax
`type()`

## Return value

The return value is a string that describes the general category of the client that is running, according to the web client’s user agent string. The system compares the user agent string against a set of configurable values in the *platform.json* file. Examples of general client type categories are `phone` and `desktop`.
