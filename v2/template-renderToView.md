---
title: Template - renderToView
---

# renderToView
Use the *renderToView* method to define the root element in a template, rather than having the *View* generate the root element for you.

The view’s *$element* defines the containing root element of a view. The *View* generates the *$element*. If the template also contains a root element, the result may contain unnecessary elements. Use the template's *renderToView* method, instead of *render*, to define the root element in the template, when you do not want the *View* to generate it for you. Using *renderToView* causes the view's *className* and *tagName*  properties to be ignored.

If the root element of the template contains an *id* attribute, the system ignores the *View*’s *id* property. Otherwise, the *id* attribute on the rendered HTML is set to the view’s *id* property value.


## Syntax
`renderToView(viewInstance [,data])`


## Parameters

**viewInstance**  
The instance of a *View* in which the rendered template’s content is assigned to the *$element* property.

**data**  
The object used to bind the variables in the template.


## Return value
None


## Errors thrown
None

## Example

```javascript
define(['template!../content/documentTemplate.html', './documentView'], function(DocumentTemplate, DocumentView) {
    var view = new DocumentView();
    DocumentTemplate.renderToView(documentView, { 
        name: 'Invoice 1234',
        price: 12997.99,
        country: 'USA',
        properties: [
            { name: 'Supplier Provided', value: true },
            { name: 'Priority', value: 99 },
            { name: 'Load', value: null }
        ]
    });
});
```


