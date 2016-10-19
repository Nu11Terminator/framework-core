---
title: Collection - remove
---

# remove

Use the *remove* method to remove one or more models from a collection.

The *remove* method by default triggers a *remove* event. To suppress this event, pass ```{ silent: true }``` as the options parameter. The index of the model removed is available to listeners through ```options.index```.


## Syntax

`remove(models [, options])`


## Parameters

**models**  
The models parameter may be a single model, or an array of models.

**options**  
- **silent**  
When set to `true` the framework will not trigger the *remove* event.


## Return value
None


## Errors thrown
None


## Example

```javascript
collection.remove([model1, model2, model3]);
```
