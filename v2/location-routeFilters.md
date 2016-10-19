---
title: Location - routeFilters
---

# routeFilters
Use the routeFilters collection to modify the default handling of routes. See the [Route Filters](routeFilters.html) topic for details.

## Example

```javascript
function myFilter(next, routeArguments) { /*do stuff here*/ next(routeArguments); }

Core.Location.routeFilters.add(myFilter);
Core.Location.routeFilters.remove(myFilter);
```
