---
title: Collection
---

# Collection

Use the *Collection* type to get a set of resources from the REST server.


## Prototype properties

**model**  
Set this property to define the type of model the collection contains.

**url**  
Set this property to define the location of the resource.

**length**  
Use this property to get the number of models contained within the collection.

**models**  
The framework sets this property to expose the resource models returned by the server.


## Prototype methods

**add**  
Use this method to add a new model to the collection.

**get**  
Use this method to get a model from the collection.

**fetch**  
Use this method to force the collection to make a request for data.

**sync**  
Use this method to override the default handling of server communication.

**remove**  
Use this method to remove one or more models from the collection.

**each**  
Use this method to provide a callback function to iterate over each model in the collection.

**initialize**  
When there is a defined initialization method, the system calls the method after constructing the object.


## Methods

**extend**  
Use this method to create a sub-type of the *Collection* type.


## Example

DocumentCollection.js

```javascript
define(['framework-core', './documentModel'], function(Core, DocumentModel) {
    return Core.Collection.extend({
        url: '/documents',
        model: DocumentModel
    });
});
```

DocumentModel.js

```javascript
define(['framework-core'], function(Core) {
    return Core.Model.extend({
        url: '/documents',
    });
});
```

Usage.js

```javascript
define(['./documentCollection', './documentModel'], function (DocumentCollection, DocumentModel) {
    var documents = new DocumentCollection();
    documents.fetch({
        success: function () {
            alert('Successfully retrieved documents.');

            //Now, add a new Document to the collection (it won't be saved to the server unless we sync the data)
            var document = new DocumentModel({
                id: '12345678',
                name: 'Test Document',
                description: 'Test Description',
            });

            // Note that add will accept a single model or an array of models
            documents.add(document);
            var document2 = documents.get('12345678');
            alert(document2.get('description')); //Alerts: Test Description
            documents.each(function (doc) {
                alert(doc.get('description'));
            });
        },

        error: function () {
            alert('An error occurred while retrieving documents.');
        }
    });
});
```
