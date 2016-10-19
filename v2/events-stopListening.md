---
title: Events - stopListening
---

# stopListening

Use the *stopListening* method to remove callbacks that have been registered by this object onto a different object using the *listenTo* method.


## Syntax

`stopListening([object] [, eventName] [, callback])`

## Parameters

**object**  
The other object from which to remove callbacks. If no argument is provided, all callbacks registered by this object, on all other objects are removed.

**eventName**  
A string that identifies the name of the event from which one or more callbacks are removed. If no argument is provided, all callbacks which have been registered by this object for this event are removed.

**callback**  
A function that is removed from the system for the given eventName. If no argument is provided, all callbacks which have been registered by this object for the given eventName are removed.


## Return value
None


## Errors thrown
None


## Example

The following code example illustrates how to remove event callbacks that have been registered on a different object.

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
    
    //Update the temperature. The temperature is updated, but is not displayed.
    temperature.update(40); 
}); 
```