---
title: Events - trigger
---

# trigger

Use the *trigger* method to invoke all registered callbacks of an event.


## Syntax

`trigger(eventName [, ...args])`

## Parameters

**eventName**  
The name of the event the system publishes.

**args**  
A series of arguments that are received in order by each event subscription’s provided callback.


## Return value
None


## Errors thrown
None


## Example

The following code example illustrates how to trigger a callback with a single argument.

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