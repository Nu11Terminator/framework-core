---
title: Session - isActive
---

# isActive

Use the *isActive* method to determine whether a session is in an active state.

## Syntax
`isActive()`

## Return value

The return value is `true` when a session is active, and `false` when a session is not active.

## Example

```` js
define(['framework-core'], function(Core) {
    var active = Core.session.isActive();
    console.log('The session is ' + (active? '': 'not') + ' active');
}); 
````