---
title: TypeWrapper
---

# TypeWrapper
Use the *TypeWrapper* type to publish custom types across package boundaries.

Packages can publish a set of export types intended for consumption by code from other packages. It is recommended that you do not alter the export types unless the consuming code needs access to new or different functionality. A change in functionality can require a package’s version to be updated to reflect additions or removal of exported symbols.

*TypeWrapper* provides a convenience method for generating an outer type around an existing inner type. This allows you to export an outer type as well as an inner type that you can alter as needed, resulting in less frequent changes to the package’s interface.


## Methods

**wrap**  
The *wrap* method receives the type to be wrapped and the list of the inner type members that are proxied to the outer type. If a new member is added to the inner type the new member does not appear on the outer type unless it is named in the call to the wrap function.
