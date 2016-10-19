---
title: Events
---

# **Events**

Use the *Events* type to enable communication to any object through loosely coupled events.

Many API objects automatically have this communication functionality, including any created instance of the *Module*, *View*, *Model*, or *Collection* API types.

Use the *enableFor* method to add event functionality to any object. Do not use the *Events* object for cross module communication, instead use the *EventAggregator* type. 


## Prototype methods

**off**  
Use this method to remove a callback that the system invokes after an event occurs.

**on**  
Use this method to register a callback that the system invokes after an event occurs.

**trigger**  
Use this method to invoke all registered callbacks of an event.

**once**  
Use this method to register a callback that the system invokes after an event occurs. Once the callback is invoked, it is immediately unregistered.

**listenTo**  
Use this method to listen for events on a different object. Use *listenTo* method rather than *on* to allow *stopListening* to remove all listeners attached by this object only.

**stopListening**  
Use this method to remove a listener or multiple listeners that have been attached to different objects using *listenTo*.


## Methods

**enableFor**  
Use this method to extend the functionality provided by all other methods within the *Event* class onto an existing object.
