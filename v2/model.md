---
title: Model
---

# Model
Use the *Model* type to get a resource from a REST server. This type can contain the following methods and properties.


## Prototype properties

**attributes**  
Set this property to retrieve a hash that contains the model’s state.

**id**  
Set this property to define the id of the model.

**url**  
Set this property to define the location of the resource.

**urlRoot**  
Set this property to define the base location for the resource the model identifies.


## Prototype methods

**destroy**  
Use this method to delete the model from the server using the HTTP method DELETE.

**fetch**  
Use this method to force the model to make a request for data.

**get**  
Use this method to get the current value of a property from the model.

**initialize**  
When there is a defined initialization method, the system calls the method after constructing the object.

**save**  
Use this method to save the model to the server.

**set**  
Use this method to set a property on the model.

**sync**  
Use this method to override the default handling of server communication.

## Methods

**extend**  
Use this method to create a sub-type of *Model*.


## Events 

**sync**  

**change**  

**change:memberName**  


## Example
In the sample model below, the user sends a user ID in the request URL and the server responds with the user’s name and address.

userInfoModel.js

```javascript
define(['framework-core'], function(Core) {
    return Core.Model.extend({
        initialize: function() {
            // optionally set the user ID to some default value
            this.set('id', 123456);
        },
        url: function() {
            return '/RESTfulService/getUserInfo?id=' + this.get(id);
        }
    });
});
```

You may wish to perform special actions before you send the request to the server. For example, you can pass the user ID as a header instead of attaching it to the URL. To do so, you must provide your own implementation of *fetch*. If you do not want to also implement the code necessary to perform the request to the server, make calling fetch the last step on the base Model.

userInfoModel.js

```javascript
define(['framework-core'], function(Core) {
    return Core.Model.extend({
        url: '/RESTfulService/getUserInfo',
        fetch: function(options) {
            options = options || {}; // define options if not provided
            var userId = this.get('id');
            options.beforeSend = function(xhr) {
                xhr.setRequestHeader('id', userId);
            };
            // call fetch on base Model to perform actual server call
            Core.Model.prototype.fetch.call(this, options);
        }
    });
});
```

The user ID is sent as a header to the server. In a real-world application, you may have many models and each one may require the user ID to be sent in the header. In this case, you can build a base model that includes this functionality. Then, all of your other models can extend upon the base model and automatically take advantage of it without having to rewrite a new model each time.

myBase.js

```javascript
define(['framework-core'], function(Core) {
    return Core.Model.extend({
        fetch: function(options) {
            options = options || {}; // define options if not provided
            var userId = this.get('id');
            options.beforeSend = function(xhr) {
                xhr.setRequestHeader('id', userId);
            };
            // call fetch on base Model to perform actual server call
            Core.Model.prototype.fetch.call(this, options);
        }
    });
});
```
