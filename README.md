# 📝Tutorial & Exercise📝

**Student Details :**

|  `Attribute`  | `Information`              |
|---------------|----------------------------|
| Name          | Ardhika Satria Narendra    |
| Student ID    | 2206821866                 |
| Class         | Advanced Programming KKI   |

---
<details>
<summary>Module 08: Software Architectures</summary>

## Questions and Answers

### -> Reflection 

#### a. How many data your publlsher program will send to the message broker in one run?
The publisher program will send five events to the message broker in one run, as indicated by five separate calls to publish_event with different user data in the code snippet provided.

#### The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?
This URL is used for both the publisher and subscriber to connect to the same RabbitMQ server running on the local machine. It ensures that both the publisher and subscriber are interacting with the same message queue, allowing the subscriber to receive and process messages sent by the publisher.

#### Running RabbitMQ as message broker
![alt text](image.png)

#### Sending and processing event
![alt text](image-1.png)

![alt text](image-2.png)

I successfully set up an event-driven architecture with Rust, where my publisher dispatched events seamlessly to a subscriber via RabbitMQ. The clean RabbitMQ dashboard indicated an efficient process with no message queue backlog.

#### Monitoring chart based on publisher 

![alt text](image-3.png)

After running the publisher program multiple times, the RabbitMQ management interface displayed spikes in the 'Message rates' graph, specifically under the 'Publish' metric. These spikes correlate with the execution instances of the publisher, indicating that messages are being sent to the queue. Each peak represents a batch of messages published, which the subscriber consumes. This real-time feedback from RabbitMQ's dashboard is valuable as it visually confirms the publisher’s activity and the subsequent handling of messages by the subscriber, ensuring the system's responsiveness and reliability. This is the explaination about the direct relationship between running the publisher and the message rate changes.

---

</details>
