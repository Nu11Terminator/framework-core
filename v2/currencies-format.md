---
title: Currencies - format
---

# format
Use this method to create a formatted, locale-specific string containing the currency value for the supplied object. For detailed information about using the *format* method, refer to the JavaScript jQuery Globalize documentation.
 

## Syntax
`format(value, unit)`


## Parameters

**value**  
The value to be formatted.

**currency**  
A string with the desired locale.


## Return value
A formatted currency string.


## Errors thrown
None


## Example 1

```javascript
Core.Currencies.format( 3.14, 'USD' );
// "$3.14" for en-US app locale
// "3,14 $" for de-DE app locale
```

## Example 2

```javascript
var enCurrencies = new Core.Currencies('en');
enCurrencies.format( 3.14, 'USD' );
// "$3.14"
```

## Example 3

```javascript
var deCurrencies = new Currencies('de');
deCurrencies.format( 3.14, 'USD' );
// "3,14 $"
```
