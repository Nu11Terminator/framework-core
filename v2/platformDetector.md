---
title: PlatformDetector
---

# PlatformDetector

Use the *PlatformDetector* type to query environment descriptors that provide information about the web client running the application.

The system determines client information by analyzing the user agent string sent by the web client with each request. The system compares the user agent string against a set of configurable values in the *platform.json* file. The *platform.json* file is located in the root folder of the application.

## Prototype Methods

**type**  
Returns the general category of the client that is running. Example: `'tablet'`

**device**  
Returns a specific indicator of the web enabled device that is running the application. Example: `'iPad'`

## Example

platforms.json

```json
{
    "tablet": [
        { "name": "iPad", "regex": "ipad" },
        { 
            "name": "androidTablet", 
            "regex": "(?=.*android)(?!.*mobile).*|xoom|i800|gt-p1000|sgh-t849|shw-m180s|kindle" 
        },
    ],
    "phone": [
        { "name": "iPhone", "regex": "iphone" },
        { "name": "androidPhone", "regex": "android.*mobile" },
    ]
}
```

Example usage.js

```javascript
define(['framework-core'], function(Core) {
    var platform = new Core.PlatformDetector();
    console.log('The detected platform is: ' + platform.type());
    console.log('The detected device is: ' + platform.device());
});

// When the above code is executed on an iPhone, the expected output is:
// The detected platform is: phone
// The detected device is: iPhone
```
