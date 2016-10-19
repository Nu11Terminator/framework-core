---
title: Module
---

# Module
To enable the framework to load a module, the module must be exported from the package. The exported name of a module is used in the modules list in *config.json*.


## Prototype properties

**$element**  
Set this property to define the HTML content that displays in the application window.

**icon**  
Use this property to provide an icon for the module on the home screen.

**mobileModuleActions**  
Set this property to provide additional shell context menu functionality when the application runs on a mobile device.

**offlineCompatible**  
Set this property to enable a module when the application is in offline mode.

**path**  
Set this property to define the initial URL path the framework loads when a user selects a module icon.

**routes**  
Set this property to map URL patterns to a method.

**title**  
Use this property to provide a title for the module on the home screen.


## Prototype methods

**initialize**  
When there is a defined initialization method, the system calls the method after the module is loaded.

**updateIcon**  
Use this method to update the icon based on the current icon properties. You must call this method after the icon is set or when there are changes to the icon properties.


## Methods

**extend**  
Use this method to create a sub-class of Module.


## Events 

**activated**  
Use this when you need to know when your module is the active module.

**deactivated**  
Use this event when you need to know when your module is no longer the active module.

## Other
**data-keep-in-dom**  
To prevent the framework from detaching a module’s DOM element from the page while the module is inactive, set the *data-keep-in-dom* attribute on the module’s element or any of the element’s children.
