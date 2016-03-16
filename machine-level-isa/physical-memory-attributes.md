### 3.3 Physical Memory Attributes

访问系统物理存储器是由 machine-mode 作为中介来处理。因为物理存储器空间的布局是高度独立于系统的，这节描述指定每个物理地址范围属性的方法，而不是指定一个给定硬件平台的细节。

物理存储器映射到一个完整的系统，包括各种存储器区域和各种存储器映射的控制寄存器。一些存储器区域可能不存在，一些可能只读，一些可能不支持子字（subword）或者甚者字块（subblock）的访问，一些可能不支持原子操作，还有一些可能不支持 cache 一致性。类似地，存储器映射的控制寄存器所支持的访问宽度，是否读写带来副作用这些的差别也很大。

尽管很多系统在虚拟存储器页表（virtual memory page table）指定这样的属性，但这会把平台特定的信息插入到虚拟层，除非每个页表的每个平台物理存储器区域入口项里的属性被正确地初始化，否则会导致系统错误。除此之外，可用的页表大小可能不会针对物理存储器空间里指定的属性进行优化。

对于 RISC-V，我们把机器物理存储器属性的规范分成单独的定制硬件结构。很多情况下，在系统设计时就已经知道每个物理地址区域的属性，可被硬连线到系统的每个 RISC-V处理器的存储器数据通路上。Alternatively, machine-level control registers can be provided to specifythese attributes at a granularity appropriate to each region on the platform (for example, if an on-chip SRAM can be flexibly divided between cacheable and uncacheable uses). These attributes will be applied to any access to the physical memory region, including accesses that have undergone virtual to physical memory translation.

To aid in system debugging, we strongly recommend that RISC-V processors trap illegal physical memory accesses precisely at the core, instead of reporting them as imprecise machine check errors from the memory subsystem.
