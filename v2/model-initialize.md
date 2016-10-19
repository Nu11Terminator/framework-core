---
title: Model - initialize
---

# initialize
You can define an *initialize* method, and the system will call it after the object is created.

## Syntax
`initialize([attributes])`


## Parameters

**attributes**  
The data attributes represented by the model. This object will be available via `model.attributes`.

## Example

```javascript
var CustomModel = Core.Model.extend({
    url: '/custom/model',
    initialize: function() {
        alert(this.attributes);
    }
});
var attributes = { creationTime: new Date() };
var myCustomModel = new CustomModel(attributes);
```

