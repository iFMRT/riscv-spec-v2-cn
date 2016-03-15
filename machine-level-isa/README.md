# 第三章 Machine-Level ISA

这章描述在 machine-mode (M-mode) 中可用的 machine-level，这是在 RISC-V 系统中最高的特权模式。M-mode 是 RISC-V 硬件实现必须得有的特权模式。M-mode 用于低级访问硬件平台，是通电重置后第一个进入的模式。M-mode 也被用于实现那些直接在硬件上难于实现或是代价高昂的特性。RISC-V machine-level ISA 包括一个通用的核，可由其他被支持的特权级别和其他硬件实现的细节进行拓展。

- [3.1 Machine-Level CSRs](machine-level-csrs.md)
- [2.2 基本指令格式](base-instr-formats.md)
- [2.3 立即数编码变体](imm-encoding-vars.md)
- [2.4 整型计算指令](int-comp-instrs.md)
- [2.5 Control Transfer Instructions](ctrl-tran-instrs.md)
- [2.6 Load and Store Instructions](load-store-instrs.md)
