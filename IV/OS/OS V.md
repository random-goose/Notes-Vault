# Disk Management

#### Formatting
A magnetic is a blank slate, it is just a platter of magnetic recording material. Before a disk can store data, it must be divided into sectors that the disk controller can read and write. This process is called low level formatting for each sector. The data structure for a sector consists of a header, a data area, and a trailer. The header and trailer contain info used by the disk controller, such as sector number and an Error Correction Code (ECC)
When the controller writes a sector of data during an IOP, the ECC is updated with a value calculated from all the bytes in the same data, when the sector is read, the ECC is recalculated and compared to the stored value, if the numbers are different this indicates a data integrity error. The ECC contains enough info, if only a few bits are corrupted, it can help identify which bits are corrupted. The disk controller performs this ECC correction at every IOP.
Before it can be used to hold files, the OS needs to record its own data structures onto the disk. It does it in 2 steps, first is to partition the disk into groups of cylinders, treating each partition like a separate disk. The second step is called logical formatting, it stores the initial file system data structures onto the disk, which include the maps of free and allocated memory.

#### Boot Block
- A boot block is a reversed section of a secondary storage device that contains the necessary items to start the OS
- It initializes the system by loading the OS Kernel into memory during the boot process
- It is located at the start of the storage device
- It includes the master boot record, GUID partition table which contains the bootloader and the partition table
- It is essential for the startup of any computer system and if the boot block is corrupted, the system might fail to boot

#### Bad Blocks
- They are sections of a storage device that are damaged and cannot reliably store data
- OS and device controllers use methods like surface scans to detect bad blocks
- Bad blocks are usually marked as unusable to prevent data from being written to them
- Can lead to a loss of data or corruption if now properly managed
- Modern file systems and device controllers include ECC and bad block management to mitigate these issues

#### Sector Mapping
- Sector mapping refers to the method by which the OS translated logical block addresses (LBA) to the physical sectors of a storage device
- Logical block addressing abstracts the physical layout of the storage, allowing the OS to manage data without worrying about the physical sector locations
- The mapping table or algorithm used by the storage controller or file system translated LBA to actual physical sectors

#### Swap Space Management
- SS is a reserved area on a storage used to extend the system's primary memory
- it provides additional virtual memory by swapping out inactive memory pages from RAM to disk, allowing more applications to run simultaneously.
- There is a dedicated SS on the disk
- It is slower than RAM, so excessive swapping might hinder performance
- Modern OS's use algorithms to efficiently use swap space


# Disk Structure

- Platter
- Spinlde
- Track
- Sector
- Cylinder
- RW Head
- Arm Assembly

# Disk Scheduling

- FCFS - you know how it is
- SSTF - Shortest Seek Time First
- SCAN - Middle - Extreme left - Extreme Right
- C-SCAN - CIrcular - Middle - Extreme left (teleport to) Extreme right - Middle