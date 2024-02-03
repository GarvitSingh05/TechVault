# Distributed Consensus: An Overview

In a distributed system, where multiple interconnected nodes collaborate through message passing, achieving agreement on a common value is crucial for coordination among processes. This phenomenon is known as **Distributed Consensus**.

## Why Consensus is Required?

In distributed systems, when multiple nodes are involved in large computations, they need to agree on common values to stay updated about the entire system's state. Consensus is essential in scenarios where nodes must coordinate and share information.

## Achieving Consensus in Distributed Systems

Consider a distributed system with n connected nodes. One node initiates the process by proposing a value v to all other nodes, asking if they agree. Two scenarios can unfold:

1. **All nodes agree on value v:** In this case, all nodes can proceed with their tasks using v as the agreed-upon value.
    
2. **Some nodes disagree:** If a node suggests a different value w, achieving consensus becomes challenging.
    

For consensus to be successful, three fundamental conditions must be satisfied:

- **Agreement:** All non-faulty nodes should agree on the same value.
- **Validity:** The decided-upon value must be suggested by a non-faulty node, and all other non-faulty nodes must adopt that value.
- **Termination:** Every non-faulty node should eventually agree on some value.

_Note: A non-faulty node is one that is not crashed, attacked, or malfunctioning._

## Challenges in Distributed Consensus

Distributed systems face two main types of failures:

1. **Crash Failure:** Nodes become unresponsive due to hardware, software, or network faults.
    
2. **Byzantine Failure:** Nodes behave abnormally, forwarding different messages to different peers, often due to internal or external attacks.
    

Consensus algorithms that can handle Byzantine failures can address any consensus problem in a distributed system.

## Consensus Algorithms

### 1. Voting-based Consensus Algorithms

One prominent example is **Practical Byzantine Fault Tolerance (pBFT)**. It operates on the principle that if more than two-thirds of all nodes are honest, consensus can be reached. pBFT divides the distributed system into three phases (pre-prepare, prepare, commit) and uses a primary (leader) and secondary (backup) node structure. The algorithm ensures that a consensus is achieved using the majority rule.

### 2. Other Notable Algorithms

- **HotStuff**
- **Paxos**
- **Raft**

### 3. Proof-based Consensus Algorithms

As networks expanded with blockchain and distributed ledgers, proof-based consensus gained prominence. Participants need to provide sufficient proof to contribute to decision-making. Examples include:

- **Proof of Work (PoW)**
- **Proof of Stake (PoS)**

## Application of Distributed Consensus

Consensus algorithms find applications in various real-world scenarios, including:

- **Blockchain and Cryptocurrencies**
- **Google Page-Rank**
- **Load Balancing**

Understanding and implementing distributed consensus is crucial for the stability and reliability of distributed systems.