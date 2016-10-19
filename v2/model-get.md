---
title: Model - get
---

# get
Use the *get* method to get the current value of a property from the model.

Model attributes are stored internally in the model, rather than as properties directly on the model itself. For example, to get the value of a name property on a sample document model, call `document.get("name")`. To access the property directly (as in templating for example), use the *attributes* property.
 

## Syntax
`get(propertyName)`


## Parameters

**attributeName**  
The name of the property on the Model's attributes to return.


## Return value
The value of the attribute.


## Errors thrown
None
