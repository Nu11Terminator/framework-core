---
title: Collection - add
---

# add

Use the *add* method to add a new model to a collection.

By default, the *add* method triggers an *add* event. To suppress an add event, pass ```{ silent: true }``` as the options parameter. The system passes the newly created model as a parameter to event listeners.


## Syntax

`add(models [, options])`


## Parameters

**models**  
This parameter can include a single model or an array of models.

**options**  
Use this parameter to explicitly instruct the framework to trigger or suppress the *add* event.


## Return value
None


## Errors thrown
None


## Example

```javascript
viewCollection.add(new ViewModel({
    id: '301YW1Y_006CY7ZX000013',
    name: 'Sample Document View',
    description: 'Sample Description'
    })); 
});
```