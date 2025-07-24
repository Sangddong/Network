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
- MQTT Client : Every device that communicates through network by using MQTT
- Every device from server to micro controller that executes MQTT libraries can be client
##### 2) Client types
- Publisher
  - Which **sends** messages
  - Sends messages(=payload) about specific topics to 
- Subscriber
  - Which **receives** messages
  - Checks topics at broker by using polling method
  - Polling : A way to check periodically
