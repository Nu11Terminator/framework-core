---
title: Collection - url
---

# url

Use the *url* property to set the location of the resource on the server.

The value of the *url* property can be a string or a function that returns the value of the location. Models within a collection use the collection’s *url* as the url root if no *urlRoot* property has been defined on the model.


## Example

A model not in the collection, the URL result will be: `/document/5`.

```javascript
id: 5
urlRoot: '/document'
```


A model not in a collection with `urlRoot` undefined, an error is thrown.

```javascript
id: 5
urlRoot: undefined
```

A model in a collection where the collection’s url is `/page`, the URL result will be: `/document/5`.

```javascript
id: 5
urlRoot: '/document'
```


A model in a collection with url `/page`, `urlRoot` undefined, the URL result will be `/page/5`.

```javascript
id: 5
urlRoot: undefined  
```
