---
title: Strings - translate
---

# translate
Use this method to retrieve a translated version of a string resource that is identified by a resource key.
 

## Syntax
`translate (key [,data])`


## Parameters

**key**  
The translation item path.

**data**  
The data passed to the *format* function.


## Return value
The transformed string


## Errors thrown
None


## Example

```javascript
var str = Core.Strings.translate('shell.mainView.missingResource');
// str = "The requested resource was not found."
 
var str2 = Core.Strings.translate('shell.mainView.moduleNotOfflineCompatible', {name: 'module4'});
// translate uses the key 'shell.mainView.moduleNotOfflineCompatible' to grab the string "The module '{name}' is not available in offline mode" and subsequently calls through to format with the supplied data.
// str2 = "The module 'module4' is not available in offline mode"
```
