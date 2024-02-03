# DNS (Domain Name System) Overview

**Definition:** The Domain Name System (DNS) serves as the Internet's phonebook, translating human-readable domain names into computer-friendly IP addresses. This translation is crucial for web browsers to load internet resources.

## How DNS Works

DNS resolution involves converting a hostname  into a corresponding IP address. This process consists of multiple steps, each handled by different DNS servers:

1. **DNS Recursor:**
    
    - Acts as a librarian, receiving queries from client machines.
    - Responsible for making additional requests to satisfy the client's DNS query.

2. **Root Nameserver:**
    
    - The first step in translating human-readable host names.
    - Functions as an index, pointing to different racks of books (more specific locations).

3. **TLD Nameserver:**
    
    - Represents a specific rack of books in a library.
    - Hosts the last portion of a hostname (e.g., ".com" in example.com).

4. **Authoritative Nameserver:**
    
    - Resides at the end of the nameserver query, holding and providing DNS resource records.
    - Acts as a dictionary, translating specific names into their corresponding IP addresses.

## Authoritative DNS Server vs Recursive DNS Resolver

- **Recursive DNS Resolver:**
    
    - Initiates and tracks down DNS records for a client's request.
    - Responsible for making multiple requests until reaching the authoritative DNS nameserver.
    - Caching helps optimize queries and reduces the need for additional requests.

- **Authoritative DNS Server:**
    
    - Holds and is responsible for DNS resource records.
    - The final source of truth for certain DNS records.
    - Responds to queries directly without relying on other sources.

## Steps in a DNS Lookup

1. User types 'example.com' into a browser.
2. DNS resolver receives the query.
3. Resolver queries the root nameserver.
4. Root server points to the TLD nameserver ('.com').
5. TLD server provides the IP address of the domain's nameserver (example.com).
6. Recursive resolver queries the domain's nameserver.
7. IP address for example.com is returned to the resolver.
8. Resolver responds to the browser with the requested IP address.
9. Browser makes an HTTP request to the IP address.
10. Server at the IP returns the webpage to the browser.

## DNS Resolver and Types of DNS Queries

- **DNS Resolver:**
    
    - Initiates DNS queries and processes responses.
    - Key in both recursive and iterative queries.

- **Types of DNS Queries:**
    
    1. **Recursive Query:**
        - Requires a DNS server to respond with the requested resource record or an error message.
    2. **Iterative Query:**
        - Allows a DNS server to return the best answer it can, potentially with a referral to another authoritative DNS server.
    3. **Non-Recursive Query:**
        - Occurs when a DNS resolver queries a DNS server for a record it has access to, either because it's authoritative or cached.

## DNS Caching

**Caching Locations:**

- **Browser DNS Caching:**
    - Modern browsers cache DNS records to improve performance.
- **Operating System Level DNS Caching:**
    - Stub resolver or DNS client within the operating system caches DNS records.
    - Acts as the second local stop before a DNS query leaves the machine.

**DNS Cache Process:**

- Caching helps store data closer to the requesting client, improving load times and reducing bandwidth/CPU consumption.
- Data is cached for a set duration determined by Time-To-Live (TTL).

This comprehensive understanding of DNS, from the resolution process to caching mechanisms, is essential for efficient and reliable internet communication.