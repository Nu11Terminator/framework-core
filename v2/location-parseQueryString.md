---
title: Location - parseQueryString
---

# parseQueryString
Use this method to parse a query string into an object containing data from the string.

The *parseQueryString* method is useful for parsing the last argument in a *Module*'s route handler which is always the query string section of the route url.
 

## Syntax
`parseQueryString(queryString)`


## Parameters

**queryString**  
The query string to parse. The string should be in the format of `key1=value&key2=value&option`.

Keys do not require a value. If there is no equal sign, the substring becomes the key and the value is `null`. For example, when *queryString* is `key=value&enabled`, the result is `{key: "value", enabled: null}`.

Any URL fragments that are not part of the query string must be removed or they are included as part of a key. For example, passing `http://example.com?a=b&c=d` will result in an object that looks like the following, which is likely incorrect: `{"http://example.com?a":"b", c:"d"}`.


## Return value
An object containing all query parameters in the string. The keys and values will be URL decoded.


## Errors thrown
None


## Example

```javascript
// Returns Object {key1: "value", key2: "value", option: null}
Core.Location.parseQueryString('key1=value&key2=value&option');

// Returns Object {"has a space": "true", number: "1", boolean: "true"}
Core.Location.parseQueryString("has%20a%20space=true&number=1&boolean=true");
```
