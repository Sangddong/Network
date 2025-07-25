# MQTT BASIC
### 0. MQTT?
#### (1) What is MQTT
- **Message Queuing Telemetry Transport**
- A messaging protocol based on the **publish-subscribe pattern**
- Lightweight and battery-efficient → widely used in **IoT services**

#### (2) What is Telemetry
- A highly automated communication method<br>
- that measures, collects from remote or inaccessible locations<br>
- and transmits data to a receiving device for the monitoring, display or recording of events<br>

### 1. PUBLISH-SUBSCRIBE Transport
<img width="738" height="413" alt="image" src="https://github.com/user-attachments/assets/b12f2c5f-9f9e-41f3-91d4-b5d2aa615556" /><br>
#### (1) Broker
##### 1) What is Broker?
- A central manager that handles and delivers messages between publishers and subscribers
- A backend system that adjusts between several clients
##### 2) Role of Broker
- Receives and filters messages
- Identifies clients that subscribe each messages
- Send Messages, transmits messages to other system for additional analyze
- Grants authority to clients and certificates
#### (2) Client
##### 1) What is Client?
- MQTT Client : Any device that communicates over a network using the MQTT protocol
- Includes everything from servers to microcontrollers that run MQTT libraries
##### 2) Client types
- Publisher
  - A client that sends messages(=payload) related to specific topics
  - Publishes data to the MQTT broker
- Subscriber
  - A client that receives messages from the broker
  - Subscribes to topics and receives messages when they are published
  - Uses a method similar to polling, where it checks for updates periodically
> *Polling<br>
> A technique where the client repeatedly checks the broker for new data at regular intervals
