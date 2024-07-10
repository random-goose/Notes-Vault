## I/O
I/O Devices are the devices that are responsible for the input and output ops in the system; there are two types:
- Block
- Character
Block Devices
	Stores information in a block of fixed size and own-address. It is possible to read/write each and every block independently. In a hard disk, it is always possible to seek another cylinder and wait for the required block to rotate under the head, hence, a hard disk is a block accessible device. 
Character Devices
	Accepts / Receives a stream of characters without regarding any block structure, it isn't addressable and cannot perform any seek perform. Printers, Mice, Keyboards, Mice, Network ops are all character ops.

## Device Controllers
They are software modules that can be plugged into an OS to handle a particular device, they take help from device driver to communicate with the devices.
The device controller works like an interface between a device and a device driver. I/O Units like keyboards and mice consist of a mechanical component and an electronic component, where the electronic component houses the controller.
There is always a device controller may be able to handle multiple devices. They are connected to the computers using a plug and socket, where the socket is connected to the device controller.

- Synchronous I/O - CPU waits for I/O ops
- Asynchronous I/O - I/O ops proceed concurrently with CPU execution

![[Pasted image 20240706011705.png]]

### DMA
Slow devices like keyboards will generate an interrupt to the CPU after each byte is transferred. If a fast device like a drive were to generate an interrupt, it will inhibit the performance of the CPU to handle the interrupts. So, a typical computer will use a DMA hardware to reduce the overhead on the CPU.
DMA grants the I/O module authority to read from and write directly to the system memory. The DMA module itself controls the exchange of data between main memory and the I/O device. CPU is only interrupted during the start and end of the operation.
For this, we need a DMAC that manages the data transfers and arbitrates access to the system bus. They are programmed with the source and destination pointers, counters to track the number of transferred bytes, and settings.
![[Pasted image 20240706013259.png]]

1. Device driver is instructed to transfer disk to a buffer address X
2. Device driver then instruct disk controller to transfer data to buffer
3. Disk controller starts DMA transfer
4. Disk controller starts sending bytes to DMAC
5. counter ticks down for every time
6. when counter becomes zero, DMAC interrupts CPU to complete the transfer


# File Management

### File
Computers can store information on various storage media such as magnetic disks, tapes, disks. The physical storage is converted into a logical storage unit by the OS. The unit of logical storage is called a file.

A file is a collection of similar records. A record is a collection of related fields that can be treated as a unit by some application. A field is some basic element of any data. Any individual field contains a single value. A DB is a collection of related data.

#### File Attributes
- Name: Every file is named for the convenience of the user and is referred by its name, it's a string of characters
- Identifier: it is a unique tag of numbers given by the OS and is used to identify the file within the file system
- Type: files are of many types and can be identified by the extension
- Location: is a pointer to the logical address of that file
- Size: the current size of that file in bytes, blocks or words
- Protection: Access control info which determines who can access the file
- Metadata: time, date, creator info etc

#### File Operations
- **Creation:** 
	1. Check if needed space is present on disk
	2. Make an entry for a new file in the directory which includes the name, path etc.
- **Writing:** To write to a file, we have to know the name of the file and the information to be written, then we send a write pointer to the appropriate and write to its place
- **Reading:** To read a file, firstly search the directories and locate the file, then we keep a read pointer to the location of that file and once the read operation is done, it is moved
- **Repositioning:** The directory i indexed and the file is found, and the current file position is given a new value
- **Deleting:** To delete the file, we first locate it and then release the file space and erase the directory entry of that file
- **Truncating:** To truncate a file, we remove the contents of the file, but keep the metadata and attributes


#### File Types
- Executable
- Source Code
- Object
- Batch
- Text
- Word Processor
- Library
- Print or View
- Archive
- Multimedia

#### File Access Methods
- Sequential
- Direct Access
- Indexed

### File Allocation Methods

#### Contiguous
![[Pasted image 20240710152137.png]]
Advantages:
- Simple
- Fast Access
- Low overhead
Problems
- Finding space for file
- external fragmentation
- compaction off-like or on-line

#### Linked List
![[Pasted image 20240710152244.png]]
Advantages
- No external fragmentation
- dynamic file size
- Efficient Space Utilization
Problems
- Only Sequential Access
- locating a block can take many IOps
- Pointer Reliability
- 

#### Indexed
![[Pasted image 20240710152420.png]]
Advantages
- Fast Random Access
- Flexible File Size
- No External Fragmentation
Disadvantages
- Overhead of index table
- complexity
- limited index size

### Free Space Management

#### Bitmap or Bit Vector
It is a series of bits where each bit corresponds to a disk block. It can only have two values 0 or 1, where 1 indicates free space and 0 indicates the presence of a file. 
ex: 00111011010101

#### Linked List
In this approach, the free disk blocks are linked together in the form of a linked list using a pointer. The block of the very first free space is stored on a separate location of disk and is cached in memory.

- Grouping:
	Modify linked list of store addresses of the next n-1 free blocks in the first free block, plus a pointer to the next block that contains free-block-pointers
	An advantage of this approach is that the addresses of a group of free disk blocks can be found easily.
- Counting:
	Because free space is frequently contiguously used and freed with contiguous allocation and deletion, keep the address of the first free block and the count of following free blocks

### Directory Implementation

#### Linear List
In this approach, all the files in a directory are maintained as singly linked list. Each file contains the pointers to the data blocks which are assigned to it and the next file in the directory.

- When a new file is created, then the entire list is checked whether the new file name is matching an existing one, and if it doesn't exist the file can be created either at the start or the end of the list.
- The list needs to be traversed in case of every operation on the files, causing some indecency.

#### Hash Table
To overcome the drawbacks of singly linked list implementation of directories, this is an alternative approach which is hash table.
This approach suggests to use hash table along with linked lists, A key value pair for each file in the directory gets generated and stored in the hash table. This key can be determined by applying the hash on the file name while the key key points ot the ccorrespinding file stored in the directory.
Now searching becomes efficient due tot he fact that now, entire list will not be searched on every operation. Only hash table entries are checked using the key and if an enrty found then the corresponsing file will be fetched using teh value.

