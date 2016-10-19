---
title: Location - navigate
---

# navigate
Use the *navigate* method to update the browser’s current URL in response to a state change in the active module.

## Syntax
`navigate(fragment [,options])`

## Parameters

** fragment **  
A string that represents the fragment portion of the URL the system is navigating to. The fragment refers to any information following the hash symbol (#) in the URL address.

** options **  
An object that can contain any or all of the following properties.

- **trigger**  
  A boolean value that determines whether or not any matching routes for the new URL are triggered. The default value is false.
    
- **replace**  
  A boolean value that determines whether or not the system creates an entry in the browser’s history. When set to true, the system updates the URL without creating an entry in the browser’s history. The default value is false.


## Return value
None


## Errors thrown
None


## Example
The following code example illustrates how to use the *navigate* method to update the fragment portion of a URL, while also triggering any matching routes.

```javascript
function selectItem(itemID){
    if (!itemId) return;

    //(Code to render the item goes here.)
    Core.Location.navigate('items/' + itemId);
}
```
