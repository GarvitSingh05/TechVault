# CAP Theorem for Databases: Consistency, Availability & Partition Tolerance

## Introduction

The CAP Theorem, originating from theoretical computer science, asserts that in the face of network failures in a distributed database, one can ensure either consistency or availability, but not both simultaneously. It involves three key components:

1. **Consistency:**
    
    - All reads provide the most recent write or an error.

2. **Availability:**
    
    - All reads contain data, but it might not be the most recent.

3. **Partition Tolerance:**
    
    - The system continues to operate despite network failures (e.g., dropped partitions, slow or unavailable connections between nodes).

## Tradeoff in Network Failures

In normal operations, a distributed database offers all three components. However, during a network failure, a tradeoff must be made between consistency and availability. Partition tolerance is considered a necessity, given the inherent nature of distributed data stores.

### Decision During Network Failure

- **High Consistency:**
    
    - Guarantees the most up-to-date information.
    - Comes at the cost of lower availability.

- **High Availability:**
    
    - Prioritizes providing available services.
    - Comes at the cost of lower consistency.

## User Queries: Consistent or Available?

The choice between consistency and availability is evident during user queries to a database. The value returned depends on the decision made:

- **High Availability:**
    
    - Responds to the user with the current value on the server.
    - No guarantee that the value is the most recent, risking delayed writes in transit.

- **High Consistency:**
    
    - Waits for the new write or returns an error to the query.
    - Sacrifices availability to ensure the returned data is consistent.

## Choosing System Needs

The choice between consistency and availability is often considered in the context of system requirements. While the CAP theorem suggests a strict tradeoff, professionals emphasize the importance of considering the specific application's needs.

**Eric Brewer**, the initial proposer of the CAP theorem, suggests maximizing combinations of consistency and availability based on the application's requirements and incorporating plans for operation during and after a partition.

## Database Types: SQL vs NoSQL

The choice between consistency and availability is reflected in the selection of database types, such as SQL and NoSQL. NoSQL databases, known for ease of use, scalability, and resilience, can be categorized based on their support for high availability or high consistency.

### Examples of NoSQL Databases:

- Cloud Firestore
- Firebase Real-time DB
- MongoDB
- MarkLogic
- Couchbase
- CloudDB
- Amazon DynamoDB

## Consistency in Databases

Consistent databases are suitable when the accuracy of the returned information is crucial. Examples include financial data, where users expect precise and up-to-date account information.

### Examples of Consistent Databases:

- Bank account balances
- Text messages

**Database Options for Consistency:**

- MongoDB
- Redis
- HBase

## Availability in Databases

Availability-focused databases are preferred when the continuous service is prioritized over having the most accurate information. E-commerce businesses often prioritize availability to enable 24/7 shopping.

**Database Options for Availability:**

- Cassandra
- DynamoDB
- Cosmos DB

Some databases, like Cosmos and Cassandra, allow users to adjust settings to prioritize either consistency or availability based on their preferences.

In summary, the CAP theorem introduces a fundamental tradeoff in distributed databases, emphasizing the need to balance consistency and availability based on the specific requirements of the application. The choice is influenced by factors such as system needs, database types, and the nature of the data being handled.