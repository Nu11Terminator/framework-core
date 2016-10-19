---
title: Currencies
---

# Currencies
Use the *Currencies* type to enable the proper formatting of strings containing currencies for the selected locale conventions.

The *Currencies* type depends on the implementation of jQuery Globalize to ensure that the system receives the currency information and displays it to the user in a format appropriate for the location and language.


## Prototype Methods

**format**  
Use this method to create a formatted, locale-specific string composed of currencies for the supplied object.


## Methods

**format**  
Use this method to create a formatted, locale-specific string composed of currencies for the supplied object.


## Example 1

```javascript
var Currencies = Core.Currencies;
```

## Example 2

```javascript
var deCurrencies = new Core.Currencies('de');
```
