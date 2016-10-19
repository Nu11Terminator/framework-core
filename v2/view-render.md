---
title: View - render
---

# render
Use the *render* method to update the *$element* property with new HTML.

Override the default implementation of *render* to update the *$element* property with new HTML in accordance with the View template. 


## Syntax
`render()`


## Return value
None


## Errors thrown
None


## Example

```javascript
View.extend({
    render: function(){
        this.$element.html($('<h1>').text(this.title));
    }
});
```

