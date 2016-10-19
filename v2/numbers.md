---
title: Numbers
---

# Numbers
Use the *Numbers* type to enable the proper formatting of strings containing numerals for the selected locale conventions.

The *Numbers* type depends on the implementation of jQuery Globalize to ensure that numerical information is received by the system and displayed to the user in a format appropriate for the location and language.


## Prototype methods

**format**  
Use this method to create a formatted, locale-specific string composed of numerals for the supplied object.

**parse**  
Use this method to parse a string representing a number that is formatted based upon the current locale information.


## Methods

**format**  
Use this method to create a formatted, locale-specific string composed of numerals for the supplied object.

**parse**  
Use this method to parse a string representing a number that is formatted based upon the current locale information.


## Example 1

```javascript
var Numbers = Core.Numbers;
```

## Example 2

```javascript
var deNumbers = new Core.Numbers('de');
```
