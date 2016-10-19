---
title: Module - path
---

# path
Use the *path* property to define the initial URL path that the framework loads when a user selects a module icon. The path can only contain lowercase letters.

When a user selects a module icon, the framework loads the relative URL. The system prepends the *path* to all defined routes.

## Examples

When you define the *path* as `documents` and the user clicks the module icon, the system directs the user to the URL `http://domain/#documents`.

When you define the path as `documents` and the route as `/view/:id`, the full route is `http://domain/#documents/view/:id`.

