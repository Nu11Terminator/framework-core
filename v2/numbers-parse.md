---
title: Numbers - parse
---

# parse
Use this method to parse a string representing a number that is formatted based upon the current locale information. For detailed information about using the *parse* method, refer to the JavaScript jQuery Globalize documentation.

The string that is parsed is formatted based upon the current system locale. The value returned is a standard number in standard format without locale-based formatting.
 

## Syntax
`parse(string)`


## Parameters

**string**  
The string representing a number.


## Return value
A number representing the string.


## Errors thrown
If a value is invalid, *NaN* is returned.


## Example 1

In the example below, the current locale is de-DE. The string representing the value of pi that the system parses is "3,14".

```javascript
Core.Numbers.parse("3,14")
// "3.14" for de-DE app locale
```

## Example 2

```javascript
Core.Numbers.parse("12,735.00")
// "12735" for en-US app locale
```

## Example 3

```javascript
Core.Numbers.parse("abcd")
// "NaN"
```

## Example 4

```javascript
var enNumbers = new Core.Numbers('en');
enNumbers.parse("12,735.00")
// "12735"
```

## Example 5

```javascript
var deNumbers = new Core.Numbers('de');
deNumbers.parse("3,14")
// "3.14" for de-DE app locale
```
