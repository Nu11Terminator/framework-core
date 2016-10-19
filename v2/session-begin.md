---
title: Session - begin
---

# begin

This event occurs when a session becomes active.

## Example

```` js
var session = Core.session;
session.on('begin', function() {
    var user = session.getUsername();
    console.log('The session is active');
});
````
