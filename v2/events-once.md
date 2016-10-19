---
title: Events - once
---

# once

Use the *once* method to register a callback that the system invokes after an event occurs.

The *once* method allows the same functionality as the *on* method, except that once the callback is invoked, it is immediately removed from the system.


## Syntax

`once(eventName, callback)`

## Parameters

**eventName**  
A string that identifies the name of the event to which the callback is registered.

**callback**  
A function the system invokes when an event triggers. The arguments passed to this callback are defined and provided by the *trigger* method. When the callback is invoked, the system immediately removes it.


## Return value
None


## Errors thrown
None


## Example

The following code example illustrates how to attach a callback to an event that is fired only once.

```javascript
define (['framework-core'], function(Core) {
    var temperature = {
        degrees: 80,
        update: function(degrees) {
            this.degrees = degrees;

            // Fire callbacks attached to the degreesChanged event
            this.trigger('degreesChanged', degrees);
        }
    };

    // Attach Events functionality to the temperature object
    Core.Events.enableFor (temperature);

    temperature.once ('degreesChanged', function (degrees){
        alert ('The temperature is now ' + degrees + ' degrees.');
    });

    //Update the temperature, which will display the new temperature
    temperature.update(65);

    //Updates the temperature. The temperature is updated, but is not displayed because the callback has already been removed from the system.
    temperature.update(40);
}); 
```