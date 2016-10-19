---
title: Events - off
---

# off

Use the *off* method to remove a callback that the system invokes after an event occurs.


## Syntax

`off([eventName] [, callback])`


## Parameters

**eventName**  
A string that identifies the name of the event to be removed. If no event name is provided, callbacks for all events are removed.

**callback**  
A callback function to be removed from the given event. If no callback is provided, all callbacks for the given event are removed.


## Return value
None


## Errors thrown
None


## Example

The following code example illustrates how to remove callbacks from an event.

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

    //Turn off the event notifications
    temperature.off('degreesChanged');

    //Update the temperature again. The new temperature will NOT be displayed
    temperature.update(40);
}); 
```