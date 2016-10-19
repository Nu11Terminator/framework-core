---
title: Model - sync
---

# sync
The Model calls the *sync* method every time the system attempts to communicate with a server.

Use the *sync* method if you need to modify the default request (such as adding request headers) or if you need to access the response (such as reading response headers). 

You can override the *sync* method in a base type so that derived models will all use the base implementation (unless the derived type defines its own *sync* override).


## Syntax
`sync(method, model, options)`


## Parameters

**method**  
A string that defines what operation the model is requesting. Possible values are `create`, read, `update`, or `delete`.

**model**  
The model to be saved or read.

**options**  
The options parameter is an object that can contain any or all of the following properties.

- **success**  
    `function(model, response, options)`  
    A callback function that is called if the request succeeds.

- **error**  
    `function(model, response, options, error)`  
    A callback function that is called if the request fails.

Consumers of the model can provide additional properties to the *options* parameter. The *sync* method should provide those values to the jQuery settings object when making the ajax call.


## Return value
You should return a jqXHR or xhr from the *sync* method.
