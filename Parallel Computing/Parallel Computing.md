### Parallel Computing Notes 🔥
#### By Garvit Singh, IT Undergraduate

###### **What is Parallel Computing?**
1. Parallel Systems refer to tightly coupled systems. 
2. The term 'Parallel Computing' refers to a model where the computation is divided among several processors sharing the same memory. 
3. The architecture of a parallel computing system is characterised by homogeneity of components, each processor is of the same type and posseses the same capabilities. 
4. The shared memory has a single address space, which is accessible to all the processors. 
5. Parallel programs are then broken down into several units of executions that can be allocated to different processors, and can communicate with each other through the shared memory. 

<div style="page-break-after: always;"></div>

###### **What is Parallel Processing?**
- Processing of multiple tasks simultaneously on multiple processors is called parallel processing.
- The parallel program consists of multiple active processes(tasks) simultaneously solving a given problem.
- A given task is divided into mutiple subtasks using divide-and-conquer technique, and each one of them is processed on different CPUs.
- Programming on multi-processor system using divide-and-conquer technique is called parallel programming.
- Parallel processing provides a cost-effective solution by increasing the number of CPUs in a computer and by adding an efficient communication system between them.
- The workload can now be shared between different processors. This results in higher computing power and performance than a single processor system.

<div style="page-break-after: always;"></div>

###### **Hardware Architectures for Parallel Processing**
The core elements of parallel processing are CPUs. Based on a number of instruction and data streams that can be processed simultaneously, computing systems are classified into four categories:
- Single Instruction Single Data (SISD)
- Single Instruction Multiple Data (SIMD)
- Multiple Instruction Single Data (MISD)
- Multiple Instruction Multiple Data (MIMD)

1. **Single Instruction Single Data (SISD)**
	- A SISD Computing system is a uniprocessor machine capable of executing a single instruction, which operates on a single data stream.
	- In SISD, machine instructions are processed sequentially, and hence computers adopting this model are popularly called sequential computers.
	- All the instructions and data to be processed have to be stored in the primary memory.

2. **Single Instruction Multiple Data (SIMD)**
	- A SIMD computing system is a multiprocessor machine capable of executing the same instruction on all CPUs, but operating of different data streams.
	- Machines based on SIMD model are well suited for scientific computing since they involve lots of vector and matrix operations.

3. **Multiple Instruction Single Data (MISD)**
	- A MISD computing system is a multiprocessor machine capable of executing different instructions on different processors, but all of them operate on the same data set.
	- Machine built using MISD model are not useful for most applications, they lack practical application.

4. **Multiple Instruction Multiple Data (MIMD)**
	- A MIMD computing system is a multiprocessor machine capable of executing multiple instructions on multiple data sets.
	- Each processor in MIMD has separate instructions and data streams, and hence machine built using this model are well suited for all kinds of applications.
	- Processors in MIMD work asynchronously.
	- MIMD machine are classified into the following
		1. **Shared Memory MIMD Machine**
			- All processors are connected to a single global memory and they all have access to it. 
			- Systems based on this model are also called tightly-coupled multiprocessor systems. 
			- The communication between processors takes place through the shared memory.
			- Easier to program but less tolerant to failures and hard to extend.
		
		2. **Distributed Memory MIMD Machine**
			- All processors have a local memory
			- Also called loosely coupled multiprocessor systems
			- Communication between processors takes place through the interconnection network. The network can be configured to tree, mesh, cube etc.
			- Each processor operates asynchronously.
			- More tolerant to failures and easier to extend.
			- Distributed MIMD architectures are better than Shared Memory MIMD in every way.

<div style="page-break-after: always;"></div>

###### **Approaches To Parallel Programming**
1. **Data Parallelism**
- Divide & conquer technique is used to split data into multiple sets and each data set is processed by different processors using the same instruction.

2. **Process Parallelism**
- A given operation has multiple distinct activities, which can be processed on multiple processors.

3. **Farmer & Worker Model**
- A job distribution approach is used.
- One processor is configured as the master and all others are designated as the slaves.
- The master processor assigns jobs to the slave processors, and they inform the master processor upon completion. Master collects the results.

<div style="page-break-after: always;"></div>


Thanks For Reading! 💙

<img src="https://i.imgur.com/rOlCWgG.jpg" alt="GS" width="300"/>

######    By GARVIT SINGH
Information Technology