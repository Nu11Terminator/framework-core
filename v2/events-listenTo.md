---
title: Events - listenTo
---

# listenTo

Use the *listenTo* method to register a callback on a different object that the system invokes after an event occurs.

The advantage of using *listenTo* rather than *on* is that callbacks registered by *listenTo* can be removed exclusively by using the *stopListening* method.


## Syntax

`listenTo(object, eventName, callback)`

## Parameters

**object**  
The object that raises events.

**eventName**  
A string that identifies the name of the event to which the callback is registered.

**callback**  
A function the system invokes when an event triggers. The *trigger* method provides the arguments passed to this callback.


## Return value
None


## Errors thrown
None


## Example

The following code example illustrates how to attach a callback to a different object.

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

    // Attach Events functionality to this object
    Core.Events.enableFor (this);

    this.listenTo(temperature, 'degreesChanged', function(degrees) {
        alert('The temperature is now ' + degrees + ' degrees.');
    });

    //Update and display the new temperature
    temperature.update(65);

    // Remove callbacks that have been added by this object from the system.This does not remove callbacks that may have been added by other objects.
    this.stopListening();
}); 
```