---
title: Numbers - format
---

# format
Use this method to create a formatted, locale-specific string containing numerals for the supplied object. For detailed information about using the *format* method, refer to the JavaScript jQuery Globalize documentation.
 

## Syntax
`format(number [,attributes])`


## Parameters

**number**  
The string composed of numerals.

**attributes**  
A JSON object containing any additional format information.

- **style**	 
  A string value defined by the following attributes.
  - decimal(default)
  - percentage
- **minimumIntegerDigits**  
  A non-negative integer that indicates the minimum number of integer digits. The return value is padded with zeros when necessary.
- **minimumFractionDigits**  
  A non-negative integer that indicates the minimum number of fraction digits. The return value is rounded or padded with trailing zeros when necessary.
- **maximumFractionDigits**  
  A non-negative integer that indicates the maximum number of fraction digits. The return value is rounded or padded with trailing zeros when necessary.
- **minimumSignificantDigits**  
  A positive integer that indicates the minimum number of fraction digits shown. When the *minimumSignificantDigits* property is present, the *maximumSignificantDigits* property must also be present.When present, these properties override the minimum and maximum integer and fraction digits. The formatter uses however many integer and fraction digits are required to display the specified number of significant digits.
- **maximumSignificantDigits**  
  A positive integer that indicates the maximum number of fraction digits shown. When the *minimumSignificantDigits* property is present, the *maximumSignificantDigits* property must also be present. When present, these properties override the minimum and maximum integer and fraction digits. The formatter uses however many integer and fraction digits are required to display the specified number of significant digits.
- **round**  
  A string value defined by the following attributes.
  - ceil
  - floor
  - round (default)
  - truncate
- **useGrouping**  
  A Boolean value that indicates whether a grouping separator is used. The default value is true and therefore implements a grouping separator.



## Return value
A formatted number string.


## Errors thrown
None


## Example 1

```javascript
Core.Numbers.format( 3.141592, { maximumFractionDigits: 2 } );
// "3.14" for en-US app locale
// "3,14" for de-DE app locale
```

## Example 2

```javascript
var enNumbers = new Core.Numbers('en');
enNumbers.format( 3.141592, { maximumFractionDigits: 2 } );
// "3.14"
```

## Example 3

```javascript
var deNumbers = new Core.Numbers('de');
deNumbers.format( 3.141592, { maximumFractionDigits: 2 } );
// "3,14" for de-DE app locale
```
