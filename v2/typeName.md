---
title: TypeName
---

# TypeName
Provide a short description here. The short description should explain the functionality this type enables within the system. For Example - "Use the **OfflineConnection** type to indicate that the current user is not accessing a system connected to a server."


## Prototype properties

**propertyName**  
Prototype properties exist on instances of the object (returned from the `new` keyword) and not the object itself.

**propertyName**  
Provide a description and additional information if necessary.


## Properties

**propertyName**  
Properties can be accessed directly on the object and do not require instances returned from the `new` keyword.

**propertyName**  
Provide a description and additional information if necessary. For Example - "Set this property to define the type of model the collection contains."


## Prototype methods

**methodName**  
Prototype methods exist on instances of the object (returned from the `new` keyword) and not the object itself.

**methodName**  
Provide a description and additional information if necessary. For Example - Use this method to register a callback that the system invokes after an event occurs.


## Methods

**methodName**  
Methods can be accessed directly on the object and do not require instances returned from the `new` keyword.

**methodName**  
Provide a description and additional information if necessary. For Example - Use this method to register a callback that the system invokes after an event occurs.
 

## Events 
*(note that events are not always applicable to the type being documented)*

**eventName**  
Provide a description and additional information if necessary. For Example - "This event is triggered when an item is added to the collection."

**eventName**  
Provide a description and additional information if necessary. For Example - "This event is triggered when a bound property on a view item is set to a different value. The name of the property that changed can be accessed from `e.property`."


## Objects or Notes
(note that objects and notes are not always applicable to the type being documented)


## Example

```javascript
var options = {
    views: views,
    results: annotationResults,
    templates: annotationTemplates,
    imageInformation: imageInfo,
    getTransform: getTransform,
    newAnnotationExtendedOptions: function() {
        return {docID: this.documentId, pageID: this.pageId}
    }.bind(this),
    externalDisplay: false,
};
```

