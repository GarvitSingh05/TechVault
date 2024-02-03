# Fault Tolerance: Building Resilient Systems

**Definition:** Fault tolerance refers to a system's capability to handle errors and outages without losing functionality. It is essential for maintaining continuous operation, especially in critical applications.

## Comparative Fault Tolerance

Consider a scenario with two applications - one connected to a single database instance (Application 1) and the other to two instances, including a standby replica (Application 2). In this example, Application 2 is more fault-tolerant. If its primary database fails, it seamlessly switches to the standby replica, ensuring uninterrupted operation.

## Approaches to Achieve Fault Tolerance

1. **Multiple Hardware Systems:**
    
    - Utilizing different physical servers for critical components.
    - Effective against hardware failures or power outages.

2. **Multiple Software Instances:**
    
    - Implementing containerization platforms like Kubernetes for running multiple software instances.
    - Allows routing traffic to functional instances in case of errors.

3. **Backup Power Sources:**
    
    - Using generators to safeguard against power outages.
    - Commonly employed in on-premises systems.

## Fault Tolerance vs. High Availability

**High Availability:** Refers to total uptime, and while closely related, it's distinct from fault tolerance. Achieving high availability often involves building fault-tolerant systems but isn't solely reliant on fault tolerance. Regular system maintenance can impact high availability.

## Fault Tolerance Goals

Building fault-tolerant systems is complex and may incur higher costs. Determining the level of fault tolerance required is crucial. Survival goals can range from surviving node failures to entire cloud provider outages.

## Normal Functioning vs. Graceful Degradation

- **Normal Functioning:**
    
    - Aiming for the application to remain online and fully functional despite failures.
    - Offers an optimal user experience but tends to be more expensive.

- **Graceful Degradation:**
    
    - Allowing outages to impact functionality without completely knocking the application offline.
    - Acceptable for less essential systems, considering economic factors.

## Setting Survival Goals

Determining how much downtime and what types of failures an application can survive. Common goals include surviving node, availability zone, region, or even cloud provider failures.

## The Cost of Fault Tolerance

- **Direct Costs:**
    
    - Additional expenses associated with fault-tolerant architectures.
    - Balanced against the costs of potential outages.

- **Indirect Costs:**
    
    - Downtime costs in dollars, reputation damage, engineering hours, and team morale.
    - Weighing the costs of achieving fault tolerance against the impact of outages.

## Fault-Tolerant Architecture Examples

### Achieving Fault Tolerance in the Application Layer

- **Multi-Region Architecture:**
    - Utilizing Kubernetes with microservices distributed across regions.
    - Horizontal scaling of microservices for flexibility and fault tolerance.

### Achieving Fault Tolerance in the Persistence Layer (Database)

- **CockroachDB:**
    - Distributed SQL database providing fault tolerance and strong consistency.
    - Treated as a single-instance Postgres database by the application.

Building resilient systems involves balancing the complexity and costs associated with achieving fault tolerance against the potential impact of system outages. It requires careful consideration of survival goals and a strategic choice of technologies and architectures.