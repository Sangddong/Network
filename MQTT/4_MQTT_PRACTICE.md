# MQTT PRACTICE
### 0. Install MQTT Library
#### (1) Install the MQTT Library
<a href="https://www.npmjs.com/package/mqtt">npm mqtt</a>
``` terminal
npm install mqtt --save
```
#### (2) Import the MQTT module at the top of your script
``` javascript
const mqtt = require('mqtt');
```

### 1. Methods
#### (1) `connect()`
``` javascript
const url = `${protocol}://${host}:${port}`;
const client = mqtt.connect(url, options);
```
- Url Composition

|composition|description|example|
|-|-|-|
|Protocol|Connection type|`mqtt://`, `mqtts://`, `ws://`, `wss://`|
|Host|Broker's address|`broker.hivem.com`, IP address|
|Port|Depends on protocol|`1883`, `8883`, `9001`, `443`|

- Port

|Protocol|Port|description|
|-|-|-|
|MQTT (TCP)|`1883`|basic unencrypted connection|
|MQTT over TLS|`8883`|encrypted secure connection|
|MQTT over WebSocket|`9001`|WebSocket connection|
|MQTT over Secure WebSocket|`443`|TLS + WebSocket (`wss://`)|

- Options: Used to configure client behavior during connection

``` javascript
const options = {
  clientId: 'myClientId',
  userName: 'myUserName',    // when the broker requests authentication
  password: 'myPassword',    // when the broker requests authentication
  clean: true,               // true: new session, false: maintain session
  keepalive: 60,             // Ping transmission cycle
  reconnectPeriod: 1000,     // automatic reconnection interval
  connectTimeOut: 30 * 1000  // connection timeout
};
```
#### (2) `subscribe()`
- The subscribe() method allows the client to listen to a specific topic. 
- Once subscribed, the client will receive all messages published to that topic.
