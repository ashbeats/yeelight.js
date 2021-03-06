# Device

Represents a Yeelight device

## constructor

Constructor

**Parameters**

-   `payload` **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** 

## sendCommand

Send command to device

**Parameters**

-   `command` **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** 

Returns **[Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)&lt;>** 

## powerOn

Power on/off the device

**Parameters**

-   `power` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** 
-   `effect` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** 
-   `duration` **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** 

Returns **[Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)&lt;>** 

## createDeviceFromMessage

Create a Device instance from a raw message

**Parameters**

-   `msg` **[Buffer](https://nodejs.org/api/buffer.html)** 

Returns **[Device](#device)** 

# Discover

**Extends EventEmitter**

Discover Yeelight devices on demand

## constructor

Constructor

## discover

Start discovery of Yeelight Devices. It will send a multicast message
and wait for response. Emits `message` event on response.

Returns **Any** 

## stop

Stop discovery

# Logger

Logger class

## constructor

Constructor

**Parameters**

-   `options` **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** 

## info

Log an info message

**Parameters**

-   `msg` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** 

Returns **Any** 

# Store

# MemoryStore

**Extends Store**

Memory store for Yeelight devices

## constructor

Constructor

## add

Add a Device to the store

**Parameters**

-   `device` **[Device](#device)** 

Returns **Any** 

## getById

Get Device by Id

**Parameters**

-   `id` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** 

Returns **([Device](#device) | Any)** 

## removeById

Remove Device from the store

**Parameters**

-   `id` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** 

Returns **Any** 

## get

Get all devices

Returns **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[Device](#device)>** 

# Watch

**Extends EventEmitter**

Class for watching for advertisments packets from
Yeelight devices.

## constructor

Constructor

## watch

Start listening for advertisments packets from Yeelight
devices. Emits `message` event on response.

Returns **Any** 

## stop

Stop watching

# Yeelight

**Extends EventEmitter**

Device manager for your Yeelight devices

## constructor

Constructor

**Parameters**

-   `options` **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** 

## discover

Start the discovery of connected Yeelight devices. Return
devices found after `discoveryTimeout`.

**Parameters**

-   `discoveryTimeout` **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** 

Returns **[Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)&lt;[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[Device](#device)>>** 

## watch

Start watching for advertisment packets of Yeelight devices.
Emits devices on `device` event.

Returns **Any** 

## stop

Stop watching

Returns **Any** 
