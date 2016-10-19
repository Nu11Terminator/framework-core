---
title: Session
---

# Session

The *Session* type contains the following methods.

Access the active *Session* instance using the *App* object. The *Session* object tracks the state of connections; active or inactive. A session becomes active when a user authenticates against a configured *connection*.

## Methods

**getUsername**  
Use this method to get the user name of the currently authenticated user.

**isActive**  
Use this method to indicate whether the session is active.

**end**  
Use this method to disconnect from any active connections and place the session in an inactive state.

## Events

**before:end**  
This event occurs before a session ends.

**begin**  
This event occurs when a session becomes active.

**end**  
This event occurs when a session becomes inactive.

## Example

The following code sample illustrates the use of the *Session* type.

```javascript
define(['framework-core'], function(Core) {
    function SessionStatusIndicator() {
        var session = Core.session;

        // Check the initial state of the session
        if (session.isActive()) {
            console.log('The session is active');
            console.log('The authenticated user is "' + session.getUsername() + '"');
        }

        session.on('begin', function() {
            var user = session.getUsername();
            console.log('The session is active');
        });

        session.on('end', function() {
            console.log('The session is inactive');
        });
    }

    return SessionStatusIndicator;
});
```
