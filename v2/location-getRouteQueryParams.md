---
title: Location - getRouteQueryParams
---

# getRouteQueryParams
Use the *getRouteQueryParams* method to retrieve the query parameters for the route from the current location.
 

## Syntax
`getRouteQueryParams([url])`


## Parameters

**url**  
The URL containing the query parameters that are parsed. If the URL is not provided, the value from `window.location` is used instead. If the URL is not a valid web URL, the behavior of this method is undefined.


## Return value
An object containing all query parameters in the route. Query parameters before the hash symbol are ignored.


## Errors thrown
None


## Example

```javascript
/* 
   Assume the current value of window.location is
   http://example.com/#module?option1=abc&option2=def
*/

// Returns {option1: "abc", option2: "def"}
Location.getRouteQueryParams();

// Returns Object {b: "123", c: "abc", d: null}
Location.getRouteQueryParams("http://example.com/?a=1&b=2#module?b=123&c=abc&d")
```
