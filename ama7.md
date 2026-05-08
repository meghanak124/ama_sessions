# AMA session 7

## 1. Which type of DB is faster?

It depends on the use case: - **In-memory databases (Redis)** → Fastest
(microseconds) - **NoSQL (MongoDB)** → Faster for flexible, large-scale
reads/writes - **Relational DB (MySQL, PostgreSQL)** → Slower than NoSQL
but strong consistency

------------------------------------------------------------------------

## 2. Which protocol does RabbitMQ follow?

RabbitMQ mainly uses: - **AMQP (Advanced Message Queuing Protocol)**
RabbitMQ uses AMQP as its primary messaging protocol, which runs on top of TCP for network communication.

------------------------------------------------------------------------

## 3. Why is RabbitMQ called smarter than Kafka?

RabbitMQ is called "smarter" because: 
- Complex routing (exchange types: direct, topic, fanout) 
- Message prioritization 
- Acknowledgements & retries built-in 
- Flexible delivery rules

Kafka is simpler but: 
- High throughput 
- Distributed log system 
- Better for big data streaming

RabbitMQ = Smart routing 
- Kafka = High performance

------------------------------------------------------------------------

## 4. What is Docker Hub?

Docker Hub is: - A cloud-based repository for Docker images - Used to
store, share, and pull container images
Example: - You push your app image → Others can pull and run it

------------------------------------------------------------------------

## 5. What is a broker in Kafka?

A **Kafka broker** is: - A server that stores and manages messages -
Handles producers (who send data) and consumers (who read data)

Kafka cluster = Multiple brokers working together

------------------------------------------------------------------------

## 6. Difference between Form and ModelForm (Django)

### Form:
-   Manually define fields
-   Not linked to database

### ModelForm:
-   Automatically created from models
-   Directly connected to database

- Form = Manual 
- ModelForm = Auto + DB connected

------------------------------------------------------------------------

## 7. How to structure a prompt?

Good prompt structure: 
1. Role → "You are a backend expert" 
2. Task → "Explain Kafka" 
3. Context → "For beginners" 
4. Format → "Give bullet points"
Example: "You are a backend engineer. Explain Kafka for beginners with examples in bullet points."

------------------------------------------------------------------------

## 8. What is a message queue?

A message queue is: 
- A system that allows communication between services asynchronously

Flow: Producer → Queue → Consumer
Benefits: - Decoupling - Scalability - Reliability
Examples: - RabbitMQ - Kafka - AWS SQS


