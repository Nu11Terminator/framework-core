---
title: Events - enableFor
---

# enableFor

Use the *enableFor* method to add events communication functionality to an object.


## Syntax

`enableFor(target)`


## Parameters

**target**  
The object that receives the *Events* communication functionality.


## Return value
None


## Errors thrown
None


## Example

The following code example illustrates how to attach events communication functionality to an object.

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

    //Attach Events functionality to temperature object
    Core.Events.enableFor(temperature);
    temperature.on('degreesChanged', function(degrees) {
        alert('The temperature is now ' + degrees + ' degrees.');
    });

    // Update the temperature, which will display the new temperature
    temperature.update(65);
});
```