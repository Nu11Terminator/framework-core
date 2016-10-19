---
title: Translations - get
---

# get
Use this method to retrieve a translated version of a string resource that is identified by a resource key.
 

## Syntax
`get (key [,data])`


## Parameters

**key**  
The translation item path.

**data**  
The data passed to the *format* function.


## Return value
The transformed string. Will be undefined, if string match cannot be found.


## Errors thrown
None


## Example 1

```javascript
var Translations = Core.Strings.load({en: {hello: 'hello'}, de: {hello: 'hallo'}}); 
var hello = Translations.get('hello'); 
// hello = "hello" for en app locale
// hello = "hallo" for de app locale
```
 
## Example 2

```javascript
var Translations = Core.Strings.load({en: {hello: 'hello'}, de: {hello: 'hallo'}}); 
var deTranslations = new Translations('de'); 
var deHello = deTranslations.get('hello'); 
// deHello = "hallo" 
```
