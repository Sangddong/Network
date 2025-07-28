
## DIFFERENCE BETWEEN HTTP AND MQTT
### 0. Similarities
#### (0) Network Protocol
- Both MQTT and HTTP are network protocol that transmit data through the internet
#### (1) Application Layer
- Both protocole **operate at the Application level of the OSI 7-Layer model**
#### (2) TCP/IP
- Both protocols run over TCP/IP, which **ensures reliable data trasnmission**
#### (3) Request&Response Structure
- HTTP : follows a Client <-> Server request-response model
- MQTT : uses Publish/Subscribe model, where communication is broker-mediated
#### (4) TLS/SSL
- Both protocols **support encrypted communication** through TLS/SSL
#### (5) Payload
- Both protocols **can send transmit payload** data such as JSON, strings, or binary

### 1. Differences
#### (1) Connection
- MQTT : Persistent Connection
  - maintains long-lived session
- HTTP : Stateless
  - each request is independent and does not retain connection state
#### (2) Message Size
- MQTT : small and lightweight
- HTTP : larger than MQTT
  -  includes complex and verbose headers
#### (3) Quality of Service
- MQTT : allows selection of Quality and Service level (QoS 0, 1, 2)
- HTTP : no QoS mechanism, relies solely on the reliability of TCP/IP
#### (4) Real Time
- MQTT : high
  - supports fast transmission with low bandwidth
- HTTP : low
  - each requests requires a handshake and full HTTP overhead
#### (5) Power Efficiency
- MQTT : good
  - Optimized for IoT with limited power
- HTTP : poor
  - frequent of connection/dsiconnection iscreases power consumption
#### (6) Role of Server
- MQTT : a broker mediates communication between clients
- HTTP : the server responds directly to client request

|feature|MQTT|HTTP|
|-|-|-|
|Connection|Persistent Connection|Stateless|
|Message Size|Small and lightweight|Larer than MQTT|
|Quality of Service|Qos 0, 1, 2|No QoS support|
|Real Time|High|Low|
|Power Efficiency|Good|Poor|
|Role of Server|Broker mediates communication|Server responds directly|
