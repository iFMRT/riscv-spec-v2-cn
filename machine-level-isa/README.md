# 第三章 Machine-Level ISA

这章描述在 machine-mode (M-mode) 中可用的 machine-level，这是在 RISC-V 系统中最高的特权模式。M-mode 是 RISC-V 硬件实现必须得有的特权模式。M-mode 用于低级访问硬件平台，是通电重置后第一个进入的模式。M-mode 也被用于实现那些直接在硬件上难于实现或是代价高昂的特性。RISC-V machine-level ISA 包括一个通用的核，可由其他被支持的特权级别和其他硬件实现的细节进行拓展。

- [3.1 Machine-Level CSRs](machine-level-csrs.md)
- [3.2 Machine-Mode Privileged Instructions](machine-mode-privileged-instrs.md)
- [3.3 Physical Memory Attributes](physical-memory-attributes.md)
- [3.4 Physical Memory Access Control](physical-memory-access-control.md)
- [3.5 Mbare addressing environment](mbare-addressing-environment.md)
- [3.6 Base-and-Bound environments](base-and-bound-environments.md)
