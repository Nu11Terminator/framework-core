---
title: Module - routes
---

# routes
Use this hash to map a URL pattern to a method that the system calls when the system invokes a URL.

When the browser invokes a URL, the framework finds the matching route and calls the given callback function for that route. Routes can contain parameters that the framework extracts and passes to the given callback function. The framework uses the relative paths for each route as a key and the corresponding callback for each route as a value. You can specify each callback as an inline function or the name of a function defined on the module.

The route `document/:id` matches both `/document/321YWCE_0000G3PHB00000B` and `/document/321YWCG_0000KWVMP000001`. The framework extracts the document ID from the URL and passes it to the callback function.

Setting a value for the routes member of a module causes the system to register the described routes immediately after module initialization.

## Example

```javascript
Module.extend({
    routes: {
        'document': 'onOpenDocumentModule'
        'document/:documentId/page/:pageId': 'onOpenDocumentPage',
        'document/:view/': function(view) { /* You can use an inline function like this */ }
    },
    onOpenDocumentModule: function() { /*do something*/ },
    onOpenDocumentPage: function(documentId, pageId) { /*do something*/ }
});
```
