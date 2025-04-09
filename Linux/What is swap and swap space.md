Subject: [[Linux]] #linux 

Links:
- [SwapFaq](https://help.ubuntu.com/community/SwapFaq)
- [Swap - ArchDoc](https://wiki.archlinux.org/title/Swap)

#### What is?
Virtual Memory = Physical Memory (RAM) + Swap Space

Linux divides its physical RAM into chunks of memory called pages

Swap space is the area on a hard disk

Swap holds memory pages temporarily inactive

Swap space is used when physical memory needs space for active processes and the available amount is not sufficient, then the operating system sends the inactive memory pages to the **swap space**, freeing up that physical memory for other uses.

Swap:
	access time is slower (depend on the hardware)
	is not a replacement for the physical memory
	can be a dedicated swap partition (recomended)
	can be a swap file
	or both (partition and file)

Linux kernel has a Out Of Memory killer mechanism that will automatically attempt to free up memory by killing processes. So, if the amount of physical memory is less than the amount of memory required, you should use Swap 
#### Usage
Significant number of memory pages used by large programs during it startup may only be used for initialization and then never used again. The system can use swap space to free the memory or use as disk cache.

Hibernation feature writes out the content of RAM to the swap partition. (needs swap partition as big as RAM size).

**Unforeseeable Circumstances** can and will happen, so swap is used to give you an extra delay to finish what you working on or to discover what is happening.

The Linux kernel moves reserved RAM used by programs that are not being really used into swap, so it can be used as cached memory.

To optimize swap performance, the swap space can be used on different physical drives. This will reduce or eliminate the competition for the resource

#### How much swap do I need?
Recommended (highly) - swap space should be equal to the amount of RAM
	Maximum - twice the amount of RAM
	If you need more swap space than double of your RAM size, you should get more RAM

#### Some notes
Swap is associated with a swap partition, but can be increased using a swap file or increasing the size of the swap (if your disk has free space)

Swappiness parameter controls the tendency of the kernel to move processes out of physical memory and onto the swap disk. 
	Slower response times if processes are too aggressively moved out of memory
		Swappiness - can have a value between 0 <-> 100 (or 200)
		Swappiness near 0 - kernel avoid swapping processes out of physical memory, until necessary
		Swappiness near 100 - kernel move processes to swap cache
		Ubuntu default - swappiness=60
		A value of swappiness=10 is recommended (for Desktops, not servers)

