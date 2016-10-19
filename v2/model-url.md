---
title: Model - url
---

# url
Use the *url* property to override the default logic that generates the location of the resource on the server.

The value of the *url* property can be a string or a function that returns the location.

The default implementation of the *url* method uses the *urlRoot* property on the model to generate a url in the form of `urlRoot/id`. If *urlRoot* is not defined and the model is part of a collection, the default url method will use the collection’s *url* as the root instead of the *urlRoot* property.

## Example

```javascript
Core.Model.extend({
    url: function(){ return '/document/' + this.customId(); },
    //other properties
});
```
