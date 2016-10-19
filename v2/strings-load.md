---
title: Strings - load
---

# load
Use this method to load string resources.
 

## Syntax
`load (data)`


## Parameters

**data**  
The data passed to load. The first level of keys must be locales. For example:

```javascript
    {
      en: {
        hello: "Hello"
      },
      pt: {
        hello: "Olá"
      }
    }
```


## Return value
A *Translations* object


## Errors thrown
None


## Example 1

```javascript
var Translations = Core.Strings.load({en: {hello: 'hello'}, de: {hello: 'hallo'}}); 
var hello = Translations.get('hello'); 
// hello = "hello" for en app locale
// hello = "hallo" for de app locale
```
