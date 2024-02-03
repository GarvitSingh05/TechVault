# Caching
## Concepts

1. **Locality of Reference Principle:**
    
    - Recently requested data is likely to be requested again.
    - Caching takes advantage of this principle.

2. **Cache Characteristics:**
    
    - Exist at all levels in architecture.
    - Often found at the level nearest to the front end.
    - Acts as short-term memory with limited space.
    - Typically faster than the original data source.

3. **Caching Components:**
    
    - Precalculating results.
    - Pregenerating expensive indexes.
    - Storing copies of frequently accessed data in a faster backend.

## Caches in Different Layers

### 2.1 Client-side

- **Use Case:** Accelerate retrieval of web content.
- **Tech:** HTTP Cache Headers, Browsers.
- **Solutions:** Browser-specific implementations.

### 2.2 DNS

- **Use Case:** Domain to IP Resolution.
- **Tech:** DNS Servers.
- **Solutions:** Amazon Route 53.

### 2.3 Web Server

- **Use Case:** Accelerate retrieval of web content, manage web sessions.
- **Tech:** HTTP Cache Headers, CDNs, Reverse Proxies, Web Accelerators, Key/Value Stores.
- **Solutions:** Amazon CloudFront, ElastiCache for Redis, ElastiCache for Memcached.

### 2.4 Application

- **Use Case:** Accelerate application performance and data access.
- **Tech:** Key/Value data stores, Local caches.
- **Solutions:** Redis, Memcached.
- **Challenges:** Addressed with Global Caches and Distributed Caches.

### 2.5 Database

- **Use Case:** Reduce latency in database query requests.
- **Tech:** Database buffers, Key/Value data stores.
- **Solutions:** Default database caching, optimized configurations, Redis, Memcached.

### 2.6 CDN

- **Use Case:** Serve static media, provide geographic distribution.
- **Solutions:** Amazon CloudFront, Akamai.
- **Alternative:** Building a system without a CDN.

### 2.7 Other Cache

- **Examples:** CPU Cache, GPU Cache, Disk Cache.
- Various types managed by hardware or software.

## Cache Invalidation

- Essential when data is modified in the database to prevent inconsistent behavior.
- Three caching systems: Write-through cache, Write-around cache, Write-back cache.

### Write-through cache

- Pro: Fast retrieval, complete data consistency.
- Con: Higher latency for write operations.

### Write-around cache

- Pro: Reduced write latency.
- Con: Increased cache misses, higher read latency.

### Write-back cache

- Pro: Quick write latency, high write throughput.
- Con: Risk of data loss if the caching layer fails.

## Cache Eviction Policies

- Common eviction policies:
    - FIFO, LIFO, LRU, MRU, LFU, RR.

## Other

### 5.1 Global Caches

- All nodes use the same cache space.
- Effective but can be overwhelmed as the number of clients and requests increase.

### 5.2 Distributed Caches

- Cache divided using consistent hashing.
- Pros: Scalability by adding more nodes.
- Cons: Missing nodes may lead to cache loss.

### 5.3 Design a Cache System

- Considerations for handling 1M QPS.
- Data structures: Map and LinkedList.
- Implementation using the master-slave technique.