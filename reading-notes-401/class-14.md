# Notes - Day 14

1. What’s the difference between a FIFO and a standard queue? Standard queues provide at-least-once delivery, which means that each message is delivered at least once. FIFO queues provide exactly-once processing, which means that each message is delivered once and remains available until a consumer processes it and deletes it. <a href = "https://aws.amazon.com/sqs/faqs/#:~:text=Standard%20queues%20provide%20at%2Dleast,processes%20it%20and%20deletes%20it.">"Source"</a>

2. How can the server be assured a message was properly received? Through the request, response and use of checksums on the packets.

3. What classic design pattern is best represented by event driven programming? The observer pattern is a software design pattern in which an object, named the subject, maintains a list of its dependents, called observers, and notifies them automatically of any state changes, usually by calling one of their methods. It is mainly used for implementing distributed event handling systems, in "event driven" software. <a href = "https://en.wikipedia.org/wiki/Observer_pattern">"Source"</a>

4. How do you test an event driven system? Logging with timestamps and log aggregation; Distributed tracing to gather metrics about transactions that involve multiple events and messages; Integration testing still needs to be done, as does performance and deployment testing. <a href = "https://blog.gurock.com/event-driven-application-architectures/">"Source"</a>

5. Document the following Vocabulary Terms:

- *FIFO Queue:* A FIFO queue is a queue that operates on a first-in, first-out (FIFO) principle. <a href = "https://queue-it.com/queue-first-in-first-out/">"Source"</a>
- *Pub/Sub:* Publisher/Subscriber, a form of asynchronous service-to-service communication used in serverless and microservices architectures.  <a href = "https://aws.amazon.com/pub-sub-messaging/">"Source"</a>

---
**<a href = "https://github.com/scottie-l/reading-notes/tree/main/reading-notes-401">Back</a>**

---
