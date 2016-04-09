# 第二章 控制和状态寄存器 (CSRs)

RISC-V ISA 里所有的特权指令都用 **SYSTEM** 主操作码（major opcode）来编码。主要分为两类：对控制和状态寄存器（CSRs）进行读-修改-写的指令和其他的特权指令。在这一章里，描述了访问 CSRs 的指令，这在所有特权级别都是通用的。后面的章节描述了每个特权级别对应 CSRs 的作用，和其他通常跟特点特权级别相关的特权指令。值得注意的是，尽管 CSRs 和指令对应于一个特权级别，但在更高的特权级别可被访问。

- [2.1  访问 CSRs 的指令]( instr-to-access-csrs.md)
- [2.2 Machine-Mode Privileged Instructions](machine-mode-privileged-instrs.md)
- [2.3 Physical Memory Attributes](physical-memory-attributes.md)
- [2.4 Physical Memory Access Control](physical-memory-access-control.md)
- [2.5 Mbare addressing environment](mbare-addressing-environment.md)
- [2.6 Base-and-Bound environments](base-and-bound-environments.md)