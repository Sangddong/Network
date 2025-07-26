# HOW MQTT WORKS
### 1. Structure of Message
- Topic
- Payload
- QoS
- Retain flag
- Message ID
#### (1) TOPIC
- A keyword used by the broker to **filter messages** for client
- Topics are organized in a **hierarchical structure** similar to folders or directories, using `/` as a seperator
- Example) Broker can organize topics of smart home like :<br>
  - `home/first_floor/living_room/light`<br>
  - `home/first_floor/kitchen/temperature`<br>
  - `home/second_floor/room/temperature`<br>
  - `home/second_floor/bathroom/light`<br>
#### (2) Payload
- A actual data to be sent
- JSON / Binary / string format ...
#### (3) Qos
- Quality of Service
- Defines the level of transmission guarantee
  
| Level | Description | Characteristics |
| - | - | - |
| QoS 0 | At most once | Fast, possible message loss |
| QoS 1 | At least once | Reliable, but possible duplicates |
| QoS 2 | Exactly once | Safest, no duplication, slowest |

#### (4) Retain flag
- Indicates wether message should be kept by the broker
- Retain = true
  -> The broker stores the last retained message per topic
  -> The retained message is immediately sent to new subscribers
- Commonly used to **maintain the latest state** of a device or sensor
#### (5) Message ID
- Used for message tracking in Qos 1, Qos 2 levels
### 2. Transmission of Message
- MQTT uses a **Message Bus System**
<img width="912" height="603" alt="image" src="https://github.com/user-attachments/assets/0c7119e2-5012-48c6-b634-267285333869" /><br>
> 1. The broker creates Message Bus
> 2. The broker puts messages onto the bus
> 3. Clients subscribed to specific topics read messages from the bus
(1) Message Flow in MQTT
> 1. The publisher sends a message to broker
> 2. The broker checks which clients are subscribed to the corresponding topic
> 3. The broker delivers the message to each subscriber according their Qos level
