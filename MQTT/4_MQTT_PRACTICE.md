# MQTT PRACTICE
### 0. Install MQTT Library
#### (1) Install MQTT
<a href="https://www.npmjs.com/package/mqtt">npm mqtt</a>
``` terminal
npm install mqtt --save
```
#### (2) Import MQTT module at the top of the script
``` javascript
const mqtt = require('mqtt');
```

### 1. Methods
#### (1) `connect`
``` javascript
const url = `${protocol}://${host}:${port}`;
const client = mqtt.connect(url, options);
```
- Composition of Url 
  - Protocol: connection method
  - Host: Broker's address
  - Port: depends on protocol

|composition|description|example|
|-|-|-|
|Protocol|`mqtt://`: TCP<br> `mqtts://`: TLS/SSL,<br> `ws://`: WebSocket,<br> `wss://`: WebSocket with secure|`mqtt://`, `mqtts://`, `ws://`, `wss://`|
|Host|Broker's address|`broker.hivem.com`, IP address|
|Port|`1883`, `8883`, `9001`|Port number|

- Port

|Protocol|Port|description|
|-|-|-|
|MQTT (TCP)|`1883`|basic connection|
|MQTT over TLS|`8883`|connection with secure|
|MQTT over WebSocket|`9001`|WebSocket connection|
|MQTT over Secure WebSocket|`443` or `wss://`|TLS + WebSocket|

- Options: configs Client Id, authentication, keep-alive by option
``` javascript
const options = {
  clientId: 'myClientId',
  userName: 'myUserName',  // when the broker requests authentication
  password: 'myPassword',  // when the broker requests authentication
  clean: true,  // true: new session, false: maintain session
  keepalive: 60,  // Ping transmission cycle
  reconnectPeriod: 1000,  // automatic reconnection interval
  connectTimeOut: 30 * 1000  // connection timeout
};
```
