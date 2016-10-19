---
title: Session - end (method)
---

# end

Use the *end* method to disconnect from any active connections and place the session in an inactive state

## Syntax
`end()`

## Example

```` js
var session = Core.session;
session.on('begin', function() {
    var user = session.getUsername();
    console.log('The session is active');
});
````
