---
title: Session - before:end
---

# before:end

Use the *before:end* event when you need a session to conduct cleanup activities before the system completes the log out process. The system can implement asynchronous operations during the *before:end* event.

To perform an asynchronous operation during the *before:end* event, notify the framework that the operation is being made using the *waitFor* method so the log out process is paused momentarily. When the operation is complete, notify the framework to allow the log out process to resume. If you are performing multiple asynchronous operations, call the *complete* method once after the last operation is complete.

## Parameters

**event**  
This object has a method, *waitFor*, to signal that an asynchronous operation needs to complete before the session ends, and the *complete* method to signal that the operation has ended.

**waitFor**  
Use the *waitFor* method on the event object to notify the system that an asynchronous operation is being made. The *waitFor* method returns a token that is passed as an argument to the *complete* method after the module finishes the process.

**complete**  
This method is executed on the object passed with the *before:end* event.

The application is not responsive when waiting for asynchronous operations to complete. For a positive user experience, do not perform long running operations in the *before:end* event. If an operation takes longer than 5 seconds, the framework times out and continues the log out process, even if there are pending calls. A string identifying any event that did not complete before log out is saved in the log.

The session may not always be valid at the time of this event. If code requires a valid session, check that the session is valid before performing any operations that require the session.

## Example

```javascript
Core.session.on('before:end', function(e) {
    if(this.hasPendingChanges()) {
        var operationToken = e.waitFor('integration server cleanup');

        runCleanup({
            complete: function() {
                e.complete(operationToken);
            }
        });
    }
});
```
