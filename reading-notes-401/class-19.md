# Notes - Day 19

1. Describe the similarities between AWS API Gateway + Lambda functions and an ExpressJS Server?

- AWS Api Gateway works with a few clicks you can create an API that acts as a “front door” for applications to access data, business logic, or functionality from your back-end services, or any Web application. Amazon API Gateway handles all the tasks involved in accepting and processing up to hundreds of thousands of concurrent API calls, including traffic management, authorization and access control, monitoring, and API version management.  <a href = "https://www.express-gateway.io/eg-vs-amazon-aws-api-gateway/">"Source"</a>
- Express.js is a Node.js web application server framework, that allows you to spin up robust APIs and web servers, designed for building single-page, multi-page, and hybrid web applications. It is the de facto standard server framework for node. ExpressJS Server works with using middleware. <a href = "https://stackoverflow.com/questions/12616153/what-is-express-js">"Source"</a>

2. List the AWS Database offerings and talk about the pros and cons of each?

- Amazon Aurora, RDS, Redshift are relational: Traditional applications, enterprise resource planning, customer relationship management ecommerce.
- Amazon DynamoDB uses key-value: High-traffic web applications, ecommerce systems, gaming applications.
- Amazon ElastiCache, MemoryDB for Redis use in-memory: Caching, session management, gaming leaderboards, geospatial applications.
- Amazon DocumentDB for Dcoument: Content management, catalogs, user profiles.
- Amazon Keyspaces for wide Column: High-scale industrial apps for equipment maintenance, fleet management, and route optimization.
- Amazon Neptune with graph: Fraud detection, social networking, recommendation engine.
- Amazon Timestream time series: Internet of Things (IoT) applications, DevOps, industrial telemetry.
- Amazon LedgerDB for ledger: Systems of record, supply chain, registrations, banking transactions. <a href = "https://aws.amazon.com/products/databases/?nc=sn&loc=0">"Source"</a>

3. What’s the difference between a FIFO and a standard queue? Standard queues provide at-least-once delivery, which means that each message is delivered at least once. FIFO queues provide exactly-once processing, which means that each message is delivered once and remains available until a consumer processes it and deletes it. Duplicates are not introduced into the queue. <a href = "https://aws.amazon.com/sqs/faqs/#:~:text=Standard%20queues%20provide%20at%2Dleast,processes%20it%20and%20deletes%20it.">"Source"</a>

4. How can the server be assured a message was properly received? The packets are numbered and given a checksum value. The packets are asembled in order by number and the checksums are compared against an expected checksum. If any packet is missing or data is not complete or mutatated, the packet numbers and checksums won't match. The server can then send a request for the missing data.

5. Document the following Vocabulary Terms:

- *Serverless API:* Serverless is a cloud computing execution model where the cloud provider dynamically manages the allocation and provisioning of servers. A serverless application runs in stateless compute containers that are event-triggered, ephemeral, and fully managed by the cloud provider. <a href = "https://hackernoon.com/what-is-serverless-architecture-what-are-its-pros-and-cons-cc4b804022e9">"Source"</a>
- *Triggers:* The trigger() method triggers the specified event and the default behavior of an event for the selected elements. <a href = "https://www.w3schools.com/jquery/event_trigger.asp#:~:text=Definition%20and%20Usage,default%20behavior%20of%20the%20event.">"Source"</a>
- *Dynamo vs Mongo:*
    - Mongo: MongoDB is platform-agnostic and configured with the database to run virtually anywhere from a local machine, container, or on-premise deployment to any cloud provider. It requires users to manage all the infrastructure and configurations. MongoDB is a schema-free database.
    - Dynamo: DynamoDB is limited to AWS and can only configure and use DynamoDB through AWS. It's a fully managed database. DynamoDB is a schema-less database but with no ability to enforce schemas.
 <a href = "https://www.bmc.com/blogs/mongodb-vs-dynamodb/">"Source"</a>
- *Dynamoose vs Mongoose:* Dynamoose is a modeling tool for Amazon's DynamoDB. Mongoose provides a straight-forward, schema-based solution to modeling your application data and includes built-in type casting, validation, query building, business logic hooks and more, out of the box. Mongoose is an open source tool with 19K GitHub stars and 2.63K GitHub forks. Amazon DynamoDB and Mongoose are primarily classified as "NoSQL Database as a Service" and "Object Document Mapper (ODM)" tools respectively. <a href = "https://stackshare.io/stackups/amazon-dynamodb-vs-mongoose">"Source"</a>

---
**<a href = "https://github.com/scottie-l/reading-notes/tree/main/reading-notes-401">Back</a>**
