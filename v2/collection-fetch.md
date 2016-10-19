---
title: Collection - fetch
---

# fetch

Use the *fetch* method to have the collection make a request to retrieve data.

The *fetch* method makes a request to the location returned by the *url* method.


## Syntax

`fetch(options)`


## Parameters

**options**  
The options parameter is an object that can contain any or all of the following properties.

- **success**  
`function(collection, response, options)`  
A callback function that is called if the request succeeds.  
- **error**  
`function(collection, response, options, error)`  
A callback function that is called if the request fails.  


## Return value
None


## Errors thrown
The *error* parameter is required. If you do not provide an error callback, the call to fetch will throw an error.  The *error* parameter to the error callback contains a message property with a generic, localized message for the given HTTP error. This message is appropriate to display to a user when a more specific error message is not available.


## Example

```javascript
var invoiceCollection = new InvoiceCollection();

invoiceCollection.fetch({
    success: function(collection, response, options) {
        collection.each(function(invoice){
        //Do something
        });
    },
    error: function(collection, response, options, error) {
        //Handle error
    }
}); 
```

## Notes
You can provide additional properties to the options object. The framework then provides those values to the jQuery *settings* object when making the ajax call.
