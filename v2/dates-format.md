---
title: Dates - format
---

# format

Use this method to create a formatted, locale-specific date or time string for the supplied object. For detailed information about using the *format* method, refer to the JavaScript jQuery Globalize documentation.


## Syntax

`format(date, format)`


## Parameters

**date**  
An instance of a JavaScript Date type.

**format**  
A string or object containing date or time pattern information.

A string for this parameter can only contain raw encoding for a date. See *Skeleton* below.
An object accepts one of the following types of information.

* Skeleton  
`{ skeleton: "GyMMMd" }`
* Date  
`{ date: "full" }`
* Time  
`{ time: "long" }`
* Datetime  
`{ datetime: "short" }`
* Raw pattern  
`{ pattern: "dd/mm" }`  
This is a user defined date or time format string.


## Return value
A string representation of a formatted, locale-specific date or time.


## Errors thrown
None


## Example 1

```javascript
Core.Dates.format( new Date( 2010, 10, 30, 17, 55 ), { datetime: "short" } );
// when app locale is en: "11/30/10, 5:55 PM" 
```

## Example 2

```javascript
var enDates = new Core.Dates('en');
enDates.format( new Date( 2010, 10, 30, 17, 55 ), { datetime: "short" } );
// "11/30/10, 5:55 PM" 
```

## Example 3

```javascript
var deDates = new Core.Dates('de');
deDates.format( new Date( 2010, 10, 30, 17, 55 ), { datetime: "short" } );
// "01.11.10 17:55" 
```

## Notes

Date patterns vary by locale. The three examples below illustrate the variation in presentation of a short datetime format, given

```javascript
Core.Dates.format ( new Date( 2010, 10, 1, 17, 55 ), { datetime: "short" } );
```

* en: "11/1/10, 5:55 PM"
* de: "01.11.10 17:55"
* es: "1/1/10, 17:55"
