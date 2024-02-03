# RPC vs. REST: A Comprehensive Comparison

## Introduction

Remote Procedure Call (RPC) and Representational State Transfer (REST) are two distinct architectural styles in API design, serving as communication mechanisms between software components. Both aim to facilitate interactions between distributed applications, but they differ in structure, implementation, and underlying principles.

## Similarities between RPC and REST

1. **Abstraction:**
    
    - Both abstract away the lower-level network communications, allowing developers to focus on functionality rather than technical details.

2. **Communication:**
    
    - Both RPC and REST utilize HTTP as the underlying protocol, with popular message formats being JSON and XML.

3. **Cross-language compatibility:**
    
    - Developers can implement APIs in any programming language, as long as the network communication adheres to the RPC or REST interface standard.

4. **Architecture principles:**
    
    - Both follow architectural principles, although RPC focuses on functions or actions, while REST revolves around resources or objects.

## RPC Principles

1. **Remote Invocation:**
    
    - The client makes a remote function call on the server as if it were a local call.

2. **Passing Parameters:**
    
    - Parameters are sent from the client to the server function, similar to a local function call.

3. **Stubs:**
    
    - Function stubs exist on both the client and server, with the client making the function call and the server invoking the actual function.

## REST Principles

1. **Client-Server:**
    
    - Decouples clients and servers, treating them as independent systems.

2. **Stateless:**
    
    - The server keeps no record of client state between requests, treating each request independently.

3. **Cacheable:**
    
    - Responses may be cached by clients or intermediary systems based on specified cache directives.

4. **Layered System:**
    
    - Intermediaries can exist between the client and server without their knowledge, operating as if directly connected.

5. **Uniform Interface:**
    
    - Clients and servers communicate through a standardized set of instructions and messaging formats, with resources identified by URLs.

## Key Differences: RPC vs. REST

1. **Time of Development:**
    
    - RPC originated in the late 1970s and early 1980s, while REST was coined by Roy Fielding in 2000.

2. **Operational Format:**
    
    - REST has standardized server operations using HTTP methods, while RPC may lack standardized operations.

3. **Data Passing Format:**
    
    - REST allows flexible data passing in various formats, while RPC fixes the data format during implementation.

4. **State:**
    
    - REST is strictly stateless, while RPC can be stateful or stateless based on design.

## When to Use: RPC vs. REST

- **RPC:**
    
    - Used for calling remote functions on a server requiring action results, suitable for complex calculations or triggering remote procedures.
        
    - Examples:
        
        - Capturing a photo with a remote device's camera.
        - Running a machine learning algorithm on the server for fraud detection.
        - Transferring money between accounts in a remote banking system.

- **REST:**
    
    - Used for CRUD operations (Create, Read, Update, Delete) on server data objects, offering a uniform way to expose server data and structures.
        
    - Examples:
        
        - Adding a product to a database.
        - Retrieving playlist contents.
        - Updating a person's address.
        - Deleting a blog post.

## Why REST Replaced RPC

While REST APIs have become the standard, RPC, especially in the form of gRPC, hasn't disappeared. REST is favored for its simplicity, but RPC persists and performs well in specific use cases. Modern RPC implementations like gRPC offer advantages, including streaming client-server communications.

## Summary of Differences: RPC vs. REST

|  | RPC | REST |
| ---- | ---- | ---- |
| **What is it?** | System for remote function calls | A set of rules for structured data exchange |
| **Used for** | Performing actions on a remote server | CRUD operations on remote objects |
| **Best Fit** | Complex calculations or triggering remote processes | Exposing server data uniformly |
| **Statefulness** | Stateless or stateful | Stateless |
| **Data Passing Format** | Consistent structure defined by server | Structure determined independently by server, supporting multiple formats |

This comprehensive comparison outlines the distinctions and similarities between RPC and REST, helping developers make informed decisions based on their application requirements and use cases.