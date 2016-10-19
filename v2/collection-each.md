---
title: Collection - each
---

# each

Use the *each* method to iterate over all models in the collection.


## Syntax

`each(callback)`


## Parameters

**callback**  
A function invoked for each model in a collection. The callback is provided with the model as a parameter.


## Return value
None


## Errors thrown
None


## Example

```javascript
var invoiceCollection = new InvoiceCollection();
invoiceCollection.fetch();
invoiceCollection.each(function(invoice){
    // Do something
});
```