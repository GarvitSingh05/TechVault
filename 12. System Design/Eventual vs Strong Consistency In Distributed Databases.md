# Eventual vs Strong Consistency in Distributed Databases

## Introduction and Real-Life Analogy

To comprehend the concepts of eventual and strong consistency in distributed databases, let's draw an analogy from real life. Imagine maintaining "Tech Notes" on a laptop, backed up on an external hard disk and synchronized with Dropbox to mitigate the risk of data loss.

In this scenario, the laptop serves as the primary source for reading and writing (Master), while the external hard disk and Dropbox act as replicas (Slave) ensuring redundancy for reliability.

## Case 1: Eventual Consistency

- **Definition:**
    
    - Eventual consistency allows multiple replicas of a database to become consistent over time. The term "consistency" implies that a read request for a data entity made to any node of the database should return the same data.

- **Implementation:**
    
    - When a write request occurs in one replica, databases devise a strategy to propagate this update to other replicas eventually.
    - The time taken for nodes to achieve consistency may or may not be predefined.

- **Implications:**
    
    - Reading from a replica that is not yet updated may return stale data.
    - Offers low latency with the risk of providing outdated information.

- **Analogy:**
    
    - External hard disk retains stale data for 15 days, providing quick access (low latency) with the understanding that it will be updated in the next fortnight.

## Case 2: Strong Consistency

- **Definition:**
    
    - Strong consistency ensures that data is promptly passed to all replicas as soon as a write request is made to one of the replicas.

- **Implementation:**
    
    - All replicas are updated simultaneously with new data, causing delays in responding to subsequent read/write requests as they prioritize consistency.

- **Implications:**
    
    - Provides up-to-date data but introduces high latency due to synchronization delays.

- **Analogy:**
    
    - Veronica requests the latest Tech Notes, and although she receives up-to-date information, there is a delay as all replicas are busy ensuring consistency.

## Conclusion

- **Eventual Consistency:**
    
    - Offers low latency but may respond to read requests with stale data.

- **Strong Consistency:**
    
    - Provides up-to-date data but at the cost of high latency.

Understanding the trade-offs between eventual and strong consistency is crucial in designing distributed databases based on specific requirements and performance considerations.