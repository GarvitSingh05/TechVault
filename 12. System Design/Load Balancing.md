# Load Balancing

## Definition

Load balancing is a crucial method for distributing network traffic evenly across a pool of resources supporting an application. Acting as an invisible facilitator, a load balancer ensures that multiple resource servers are utilized equally, optimizing application performance.

## Benefits of Load Balancing

Load balancing offers several advantages, enhancing an application's:

- **Availability:** Reduces downtime by automatically redirecting traffic during server failures or maintenance.
- **Scalability:** Intelligently distributes network traffic, preventing bottlenecks and enabling seamless scaling.
- **Security:** Adds an extra layer of security, mitigating DDoS attacks and monitoring traffic for malicious content.
- **Performance:** Improves response time, reduces network latency, and ensures reliability of computing resources.

## Load Balancing Algorithms

Load balancing algorithms guide load balancers in selecting the best server for client requests. These algorithms fall into two categories:

### Static Load Balancing

1. **Round-robin Method:** Distributes traffic in a circular sequence to different servers.
2. **Weighted Round-robin Method:** Assigns weights to servers based on priority or capacity.
3. **IP Hash Method:** Uses mathematical computation on client IP addresses to map them to individual servers.

### Dynamic Load Balancing

1. **Least Connection Method:** Directs traffic to servers with the fewest active connections.
2. **Weighted Least Connection Method:** Considers server capacities and assigns weights accordingly.
3. **Least Response Time Method:** Considers server response time and active connections for optimal server selection.
4. **Resource-based Method:** Analyzes server resource usage to distribute traffic efficiently.

## Load Balancing Process

In a typical setup, user requests to an application running on multiple servers (server farm) first go to the load balancer. The load balancer then routes each request to a suitable server in the server farm, ensuring even distribution of workload.

## Types of Load Balancing

Load balancing can be categorized based on the characteristics checked in client requests:

- **Application Load Balancing:** Considers request content (e.g., HTTP headers) for optimal traffic redirection.
- **Network Load Balancing:** Examines IP addresses and network information to optimize traffic distribution.
- **Global Server Load Balancing:** Manages application load across geographically distributed servers.
- **DNS Load Balancing:** Configures domain routing to balance network traffic across distributed resources.

## Types of Load Balancing Technology

Load balancers come in two types:

- **Hardware Load Balancers:** Physical appliances securely process and redirect large volumes of traffic to multiple servers.
- **Software Load Balancers:** Applications that perform load balancing functions, offering flexibility and compatibility with modern cloud environments.

### Comparison:

- **Hardware Load Balancers:** Require initial investment, configuration, and maintenance; may underutilize capacity during peak times.
- **Software Load Balancers:** More flexible, scalable, and cost-effective, suitable for modern cloud environments.

## AWS Elastic Load Balancing (ELB)

**Elastic Load Balancing (ELB)** is a fully managed service by AWS that automatically distributes incoming application traffic to multiple targets across AWS and on-premises resources. ELB offers four types of software load balancers:

- **Application Load Balancer (ALB):** Routes HTTP-based traffic.
- **Network Load Balancer (NLB):** Balances TCP and UDP-based requests.
- **Gateway Load Balancer:** Routes traffic to third-party virtual appliances.
- **Classic Load Balancer:** Routes traffic to applications in the Amazon EC2-Classic network.

### Use Cases:

- **Terminix:** Utilizes Gateway Load Balancer for handling increased throughput.
- **Second Spectrum:** Reduces hosting costs by 90% using AWS Load Balancer Controller.
- **Code.org:** Efficiently manages a 400% spike in traffic with Application Load Balancer.

In conclusion, load balancing is a critical component for optimizing application performance, enhancing availability, scalability, security, and overall user experience. AWS ELB provides a comprehensive solution to efficiently manage and distribute traffic in diverse application environments.