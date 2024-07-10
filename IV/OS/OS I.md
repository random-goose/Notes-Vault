## What the fuck is a kilometer
An operating system is a low level system software that handles the software and hardware resources of the computer. It acts like an interface between the software and the hardware resources by taking the responsibility for managing and controlling all the activities and sharing of computer resources. It performs low level operations such as processor management, memory management, disk management, task scheduling etc.

## Functions of Operating System
- **Resource Management**: The OS manages and allocates memory, CPU time, and other hardware resources among the various programs and processes running on the computer
- **Process Management**: The operating system is responsible for stopping, and managing processes and programs. It also controls the scheduling of processes and allocates resources to them
- **Memory Management**: The OS manages the computer's primary memory and provides mechanisms to optimize memory usage.
- **Job Accounting:** It keeps track of time and resources used by various processes
- **File Management:** The OS provides the user with a file management system that is used for creating, deleting, moving and manipulation of files.
- **Device Management:** The OS manages I/O Operations between different peripheral devices such as keyboards, mice, printers, displays etc.
- **Networking:** The OS allows the computer to use networking hardware to connect to the internet
- **UI:** The OS provides the user with a user friendly interface to interact with the computer
- **System Calls:** The OS provides applications running on it to interact with the hardware by means of a system calls API

## Types of OS:
Batch Processing OS: 
	Earlier days of OS's, where all the processes that needed to be executed were lined up and processed using punch cards.
Multiprogramming OS:
	Allowed for multiple programs to run simultaneously, with a list of programs waiting in main memory and one being executed at a time: Active, Ready, and Waiting.
	Jobs are scheduled to maximize resource utilization and improved performance
	Introduced in IBM's OS/360
Time Sharing OS:
	Allowed multiple users to concurrently use a single processor by scheduling not only the tasks of each user but between the individual users of the system
	Each user gets their own time slice. quantum of processing
	Implemented in UNIX where multiple users can access the system resources via the terminal
Networking OS:
	Allows the computer to connect to other computers via the internet and facilitates communication, and share resources over the network
	implements protocols such as TCP/IP, UDP to establish connections over the web
	extends the resource allocation capabilities to include network resources.
Real Time OS:
	Designed to process data and provide responses within a set strict time limit and is used for sensitive applications such as in the healthcare industry or in industrial applications
	Three types of RTOS are Hard, Firm, and Soft RTOS, in order of strictness.
Multiprocessing OS:
	Allows for the use of multiple processors (or multicore CPUs) by a single system
		Symmetric:
			Gives equal load to all the processors present
		Asymmetric:
			Makes the different processors perform different tasks

## Process Management
Process management is an essential component of an OS that enables the execution of numerous applications at once, enhancing the resource utilization and system responsiveness. It involves identifying the steps involved in completing a task, accessing the resource req for each step, and executing the task.
New -> Ready -> Running -> Waiting ... Terminated
![[Pasted image 20240705125611.png]]

| PCB             | Critical Data structure containing info about process necessary for process management |
| --------------- | -------------------------------------------------------------------------------------- |
| Prog State      | current state of program - ready / wait / active                                       |
| Prog Counter    | address of instruction to execute                                                      |
| CPU Registers   | stack pointers                                                                         |
| CPU Sch Info    | scheduling queue and pointers                                                          |
| Mem Mgmt Info   | page tables, segmentation tables                                                       |
| Accounting Info | amount of cpu time                                                                     |
| I/O ops info    | list of i/o devices allocated to the process                                           |
## Threads
A process is divided into a number of lightweight tasks which can be easily executed, these tasks are called threads. The thread has a program counter which keeps track of which instruction to execute next, registers which hold its current working variables and stack which is the execution history

### Thread States:
1. Born State: thread is just created
2. Ready State: thread is waiting for CPU
3. running: system assigns the processor to the thread
4. sleep: thread becomes ready after the designated sleep time expires
5. dead: thread is finished executing 

### Multi-threading
a process is divided into a number of smaller tasks called threads, when multiple threads are executed simultaneously, its called multithreading.
In a program, if multithreaded, even if some portion of it is blocked, the whole program is not blocked as the other threads can continue being executed. It yields performance benefits only if multiple CPUs are present.
- Kernels are multithreaded
### Types of Threads
| User Level                                       | Kernel Level                                          |
| ------------------------------------------------ | ----------------------------------------------------- |
| managed by user level library                    | managed by os - system calls                          |
| creating and executing is fast                   | creating executing is slower                          |
| context switching is faster                      | context switching is slower                           |
| is a thread is blocked, whole process is blocked | if kernel thread is blocked, it doesn't effect others |
### Multithreading Models
Many-To-One - n user threads to one kernel thread - at a time only one thread can access the thread
One-To-One - no parallelism - each user thread is mapped to one kernel thread
Many-To-Many - 

### Hyper Threading - Simultaneously Multithreading
allows the physical cores of the processor to become multiple logical processors for performance - typically one physical core acts like two logical processors. It allows two streams to be executed in parallel, akin to having two separate processors all together. 