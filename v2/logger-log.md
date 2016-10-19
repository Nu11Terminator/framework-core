---
title: Logger - log
---

# log
Use the *log* method to set the message text for a component (module, service, or view) activity, to specify the severity level of a message, and to optionally assign a category to a log message.
 

## Syntax
`log(message [,severity] [,category])`


## Parameters

**message**  
The message is the text associated with the component activity that the system captures for the log file. You define the message associated with activities in the component.

**severity**  
The severity level you assign to a message dictates what type of information the system captures and displays in a log file. If you do not set the severity parameter for a message, the default level is Info (2).

**category**  
The category you assign to a message provides additional information about a component activity that can be used during troubleshooting. If you do not set the category parameter for a message, the default setting is General.


## Return value
None


## Errors thrown
None


## Logging severity levels

You can assign one of five logging severity levels to a message associated with a Perceptive Client Framework component. The logging level selected by the user determines what messages the user sees in a log. When users select a log level, the system captures all messages at that level and above in the log file. For example, if you assign a severity level of Info (2) to a message, but the system logging level is set to Warning (3), that message is not included in the log file.

Severity value	| Severity setting  | User log level	| Description 
----------------|-------------------|-------------------|-------------
1	            | Verbose	        | All messages	    | Use this level to log detailed user action information.
2	            | Info	            | N/A	            | Use this level to log high-level user action information.
3	            | Warning	        | Warning and Errors| Use this level for minimal logging. This is the default logging level.
4	            | Error	            | Errors only	    | Use this level if core functionality within the web or mobile client is not available.
5	            | Critical	        | N/A	            | Use this level if the web or mobile client is not available.

To maintain optimum system performance and reduce the size of the log file, we recommended setting minimum logging levels unless you are debugging an issue.

## Logging categories

You can optionally assign a category to a message associated with a  component. The two logging categories are General and Performance.

**General**  
Use the General category to indicate the log entry describes the basic functionality of the application.

**Performance**  
Use the Performance category to indicate the log entry describes a performance based metric, such as the time it takes to complete a server call.

## Example

```javascript
define(['logger'], function(Logger) {
    Logger.log('Server call took 5 seconds.', Logger.INFO, Logger.PERFORMANCE);
});
```
