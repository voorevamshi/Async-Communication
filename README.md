# Summary: Modern Async Communication Patterns (2026)

Asynchronous communication allows systems to exchange data without waiting for an immediate response, significantly improving scalability and resilience.

---

### 1. Point-to-Point (Message Queuing)
* **Model:** One producer sends a message to a queue; **exactly one** consumer processes it.
* **Best For:** Background tasks (e.g., image resizing, email delivery).
* **Market Leaders:** Amazon SQS, RabbitMQ, Azure Queues.

### 2. Publish-Subscribe (Pub/Sub)
* **Model:** One producer publishes to a "Topic"; **multiple** subscribers receive a copy.
* **Best For:** Real-time notifications and broadcasting state changes across microservices.
* **Market Leaders:** Google Cloud Pub/Sub, Amazon SNS, Redis Pub/Sub.

### 3. Event Streaming (Distributed Log)
* **Model:** Messages are stored in a continuous, immutable log. Consumers can "replay" data.
* **Best For:** Real-time analytics, audit logs, and high-throughput data pipelines.
* **Market Leaders:** Apache Kafka (v4.x KRaft), Redpanda, Amazon Kinesis.

### 4. Webhooks (HTTP Push)
* **Model:** A server "pushes" data to a predefined URL when an event occurs.
* **Best For:** Third-party integrations (e.g., Stripe payments, GitHub commits).
* **Market Leaders:** Stripe, Twilio, Zapier.

### 5. Change Data Capture (CDC)
* **Model:** Automatically captures row-level changes (Insert/Update/Delete) from a database.
* **Best For:** Keeping search indexes (Elasticsearch) or caches (Redis) in sync with a DB.
* **Market Leaders:** Debezium, AWS DMS.

---

## 📊 Quick Comparison

| Pattern | Logic | Reliability | Replayable? |
| :--- | :--- | :--- | :--- |
| **Queuing** | 1-to-1 | High (ACK based) | ❌ No |
| **Pub/Sub** | 1-to-Many | Moderate | ❌ No |
| **Streaming** | 1-to-Many | Very High | ✅ Yes |
| **Webhooks** | Push-based | Dependent on App | ❌ No |
| **CDC** | DB-to-Event | High | ✅ Yes |

---
*Generated for 2026 Architectural Standards.*
