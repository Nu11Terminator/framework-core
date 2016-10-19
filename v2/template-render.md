---
title: Template - render
---

# render
Use the *render* method to generate a string from the template.
 

## Syntax
`render([data])`


## Parameters

**data**  
The object used to bind the variables in the template.

## Return value
An HTML string


## Errors thrown
None


## Example

```javascript
define(['template!../content/documentTemplate.html'], function(DocumentTemplate) {
    DocumentTemplate.render({ 
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

