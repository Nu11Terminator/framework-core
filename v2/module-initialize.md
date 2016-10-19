---
title: Module - initialize
---

# initialize
The system calls the *initialize* method after the module is loaded.

The system can trigger the *initialize* method before the user session is established. If any part of the initialization depends on an active user session, it is best to place the initialization code in a connection event.
 

## Syntax
`initialize()`


## Example

```javascript
Module.extend({
    initialize: function() {
        alert("Module has been initialized");
    }
});

```

