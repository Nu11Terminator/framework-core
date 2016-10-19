---
title: Dates - parse
---

# parse

Use the *parse* method to parse a formatted, locale-specific date or time string.


## Syntax

`parse(string [, format])`

## Parameters

**string**  
The formatted, locale-specific date or time string.

**format**  
An array of possible formats used for parsing.

An object accepts one of the following types of information.

* Skeleton  
`{ skeleton:"GyMMMd" }`
* Date  
`{ date: "full" }`
* Time  
`{ time: "long" }`
* Datetime  
`{ datetime: "short" }`
* Raw pattern  
`{ pattern: "dd/mm" }`  
This is a user defined date or time format string.

For detailed information about populating the *format* parameter, refer to the JavaScript jQuery Globalize documentation.


## Return value
An instance of a JavaScript Date type.


## Errors thrown
None


## Example 1

```javascript
Core.Dates.parse( "11/30/10, 5:55 PM", { datetime: "short" } );
// Date( 2010, 10, 30, 17, 55 )
```

## Example 2

```javascript
var enDates = new Core.Dates('en');
enDates.parse( "11/30/10, 5:55 PM", { datetime: "short" } );
// Date( 2010, 10, 30, 17, 55 )
```

## Example 3

```javascript
var deDates = new Core.Dates('de');
deDates.parse( "01.11.10 17:55", { datetime: "short" } );
// Date( 2010, 10, 30, 17, 55 )
```
