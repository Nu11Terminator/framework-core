---
title: Events - on
---

# on

Use the *on* method to register a callback that the system invokes after an event occurs.


## Syntax

`on(eventName, callback)`


## Parameters

**eventName**  
A string that identifies the name of the event to which the callback will be registered.

**callback**  
A function that the system invokes when an event is triggered. The arguments passed to this callback are defined and provided by the *trigger* method.


## Return value
None


## Errors thrown
None


## Example

The following code example illustrates how to add callbacks to an event.

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

    temperature.on ('degreesChanged', function (degrees){
        alert ('The temperature is now ' + degrees + ' degrees.');
    });

    //Update the temperature, which will display the new temperature
    temperature.update(65);
}); 
```