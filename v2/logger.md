---
title: Logger
---

# Logger
Use the *Logger* type to record messages to the application log.


## Methods

**log**  
Use this method to add a message to the application log and optionally specify the severity level and category of the message.


## Example

Use *Logger* by directly referencing `logger` as the dependency name. The example below illustrates how to get an instance of Logger.

```javascript
define(['logger'], function(Logger){
    Logger.log('Server call took 5 seconds.', Logger.INFO, Logger.PERFORMANCE);
});
```

