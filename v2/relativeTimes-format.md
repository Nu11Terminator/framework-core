---
title: RelativeTimes - format
---

# format
Use this method to create a formatted, locale-specific string containing relative times for the supplied object. For detailed information about using the *format* method, refer to the JavaScript jQuery Globalize documentation.
 

## Syntax
`format(value, unit)`


## Parameters

**value**  
The delta from the current time.

**unit**  
A string with the desired date/time unit.


## Return value
A formatted relative time string.


## Errors thrown
None


## Example 1

```javascript
Core.RelativeTimes.format(1, "day");
// "tomorrow" for en-US app locale
// "morgen" for de-DE app locale
```

## Example 2

```javascript
var enRelativeTimes = new Core.RelativeTimes('en');
enRelativeTimes.format(-1, "month");
// "last month"
```

## Example 3

```javascript
var deRelativeTimes = new RelativeTimes('de');
deRelativeTimes.format(-1, "month");
// "letzten Monat"
```
