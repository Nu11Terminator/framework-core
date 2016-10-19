---
title: Dates
---

# Dates

Use the *Dates* type to enable proper formatting of date strings per the selected locale conventions.

The *Dates* type depends on the implementation of jQuery Globalize to ensure that the system receives the time and date information and displays it to the user in a format appropriate for the location and language.


## Prototype methods

**parse**  
Use this method to parse a formatted, locale-specific date or time string.

**format**  
Use this method to create a formatted, locale-specific date or time string for the supplied object.


## Methods

**parse**  
Use this method to parse a formatted, locale-specific date or time string.

**format**  
Use this method to create a formatted, locale-specific date or time string for the supplied object.


## Example 1

```javascript
var Dates = Core.Dates;
```

## Example 2

```javascript
var deDates = new Core.Dates('de');
```
