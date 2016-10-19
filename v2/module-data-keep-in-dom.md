---
title: Module - data-keep-in-dom
---

# data-keep-in-dom

The framework removes the container element of any module that is not currently displayed from the DOM by default. The container element is inserted back into the DOM when a module becomes active again.

## IFrames

The default behavior of removing container elements that are not in use from the DOM can cause problems for modules that contain IFrames. As the frame reloads, contents and data held within the frame are lost.

To prevent the framework from detaching a module’s DOM element from the page while the module is inactive, set the *data-keep-in-dom* attribute on the module’s element or any of the element’s children, such as an IFrame. The *data-keep-in-dom* causes the module’s element to be hidden instead.

This *data-keep-in-dom* attribute should only be used when necessary, as leaving your module’s element in the DOM tree can degrade performance.

## Example

```html
<div>
  <div id="containerElement" data-keep-in-dom>
    <iframe src="http://example.com"></iframe>
  </div>
</div>
```
