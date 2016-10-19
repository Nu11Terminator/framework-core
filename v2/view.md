---
title: View
---

# View
Use the View base type to create interactive user interface components.


## Prototype properties

**$element**  
The *$element* is created by the framework. Set the content of the *$element* to define the content of the view.

**className**  
Set this property to define the initial CSS type name for the *View*’s DOM element.

**tagName**  
Set this property to specify a *View*’s DOM element type.

**domEvents**  
Set this property to attach event handlers to the DOM elements contained within a *View*.


## Prototype methods

**initialize**  
When there is a defined initialization method, the system calls the method after constructing the object.

**remove**  
Use this method to clear a *View* from the DOM tree and stop listening for events.

**render**  
You must provide the *render* method for the framework. Use this method to update the *$element* property with new HTML.

**setElement**  
Use this method to designate a DOM element as a view’s user interface container.

## Methods

**extend**  
Use this method to create a sub-type of *View*.

## Example
The following code block illustrates the use of the *View* type.

buttonView.js

```javascript
define(['framework-core'], function(Core) {
    return Core.View.extend({
        tagName: 'span', 
        className: 'buttonViewClass',
         
        initialize: function(options) {
            this.buttonText = options.buttonText;
        },
 
        domEvents: {
            'click #myButton': 'onMyButtonClick'
        },
         
        onMyButtonClick: function() {
            alert("This button’s text is " + this.buttonText);
        },
         
        render: function() {
            // NOTE: This would be a good place to use a rendering template framework such as Handlebarsjs
            $button = $('<button>').attr('id', 'myButton').text(this.buttonText);
            this.$element.html($button);
            return this;
        }
    });
});
```

Sample usage

```javascript
define(['./buttonView'], function(ButtonView) {
    var buttonView = new ButtonView({ buttonText: 'sample button' });
    $target.html(buttonView.render().$element);
});
```

Resulting HTML

```html
<span class="buttonViewClass">
    <button id="myButton">Sample Button</button>
</span>
```

