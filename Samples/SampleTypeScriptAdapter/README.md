# Sample adapter for the Device Bridge
This sample adapter written in TypeScript forwards D2C messages to an Event Hub.
The code uses a client automatically generated by autorest using the Device Bridge swagger.
Failures are logged in the same Log Analytics workspace used by the Bridge core module.

> NOTE: this code should only be used as a sample reference for how to build adapters for the Device
Bridge. It should not be used in a production setting without proper testing and error handling.

## APIs

### Subscribe
 ```
 POST /subscribe/{deviceId}
 ```
 Creates a C2D message subscription for a device and forwards all C2D messages to an EventHub.


### Unsubscribe
 ```  
 POST /unsubscribe/{deviceId}
 ```

Deletes the C2D message subscription for a device and stops publishing events.
