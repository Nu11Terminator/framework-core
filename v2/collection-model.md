---
title: Collection - model
---

# model

Set the *model* property to define the type of model the collection contains.

When the *model* property is defined, you can pass raw attributes objects (and arrays) to the *add* method, and the attributes will be converted into a model of the proper type. 


## Example

```javascript
define(['framework-core', './drawerModel'], function(Core, DrawerModel) {
    return Core.Collection.extend({
        url: '/drawer',
        model: DrawerModel
    });
});
```
