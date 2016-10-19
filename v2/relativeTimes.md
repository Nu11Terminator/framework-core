---
title: RelativeTimes
---

# RelativeTimes
Use the *RelativeTimes* type to enable the proper formatting of strings containing relative times for the selected locale conventions.

The *RelativeTimes* type depends on the implementation of jQuery Globalize to ensure that relative times information is received by the system and displayed to the user in a format appropriate for the location and language.


## Prototype Methods

**format**  
Use this method to create a formatted, locale-specific string composed of relative times for the supplied object.


## Methods

**format**  
Use this method to create a formatted, locale-specific string composed of relative times for the supplied object.


## Example 1

```javascript
var RelativeTimes = Core.RelativeTimes;
```

## Example 2

```javascript
var deRelativeTimes = new Core.RelativeTimes('de');
```
