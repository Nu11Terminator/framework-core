---
title: Route Filters - Filter Function
---

# Filter Function
Use a filter function to modify the default handling of routes. A filter function receives route fragment and instructs the framework to perform the next routing action.

## Syntax
`function(next, routeFragment)`


## Parameters

**next**  
Use the **next** function to execute the route. If multiple route filters have been added, the **next** function may call the next filter
in the collection. The route callback will be executed when the final route filter has called **next**.  

Syntax: `next(routeFragment)`

**routeFragment**  
An string representing the fragment for the route. Each filter is responsible for calling the **next** function with the intended route 
fragment. The filter may choose to change the fragment passed to the **next** filter. 

## Return value
None

## Note
> The framework may execute the added route filters in any order, and the order may vary each time a route is executed.


## Example

```javascript
function logRoute(next, fragment) {
    if(window.isDocumentDebugMode) {
        console.log('Executing a route fragment:');
        console.log(fragment);
    }
    next(fragment);
}
```

