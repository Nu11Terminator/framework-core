---
title: Model - set
---

# set
Use the *set* method to define or change an attribute on the model.

Model attributes are stored internally in the model, rather than as properties directly on the model itself. For example, to set the value of a name property on a sample document model, call `document.set({name: "value"})`. To access the property directly (as in templating for example), use the *attributes* property.
 
When an attribute changes the state of the model, a change event is triggered unless {silent: true} is passed as an option.

## Syntax
`set(changes [,options])`  

`set(propertyName, value [,options])`


## Parameters

**changes**  
An object containing keys and values that represents the Model's attributes to set.

**propertyName**  
The name of the property on the Model's attributes to set.

**value**  
The value of the property on the Model's attributes to set.

**options**  
The options parameter is an object that can contain any or all of the following properties.

- **unset**  
  This option instructs the Model to delete the value.
- **silent**  
  This option instructs the Model to not trigger the *change* event.


## Return value
The instance of the Model.


## Errors thrown
None
