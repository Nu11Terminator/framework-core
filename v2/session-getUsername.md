---
title: Session - getUsername
---

# getUsername
Use the *getUsername* method to retrieve the user name of the currently authenticated user.

## Syntax
getUsername()

## Return value
The return value is a string that represents the user name of the currently authenticated user.

## Example
``` js
define(['framework-core'], function(Core) {
    var username = Core.session.getUsername();
    alert(username);
});
```