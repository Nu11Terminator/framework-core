---
title: View - domEvents
---

# domEvents
Use the *domEvents* property to attach event handlers to the View’s DOM (Document Object Model) *$element*, or any element contained within.

*domEvents* may attach multiple event handlers and can be attached to elements belonging to *$element*, not just *$element* itself.

The information required for each event includes:

- event name
- selector to the event source
- name of the method on the object to call, when the event is triggered.


## Example

```javascript
Core.View.extend({
    domEvents: {
        'click #myButton': 'buttonClicked',
        'dblclick #myImage': 'imageDbClicked',
        'focus .inputBox': 'inputBoxFocused'
    }
});
```
