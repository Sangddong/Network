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
기본적으로 네트워크를 통해 MQTT를 사용하여 통신하는 모든 디바이스를 MQTT 클라이언트 디바이스라고 할 수 있습니다.
- MQTT Client : Every device that communicates through network by using MQTT
- Every device from server to micro controller that executes MQTT libraries can be client
- Publisher : Which **Sends** messages
- Subscriber : Which **receives** messages
