# 第二章 RV32I 基本整型指令集
本章描述 RV32I 基本整型指令集。内容大多也适用于 RV64I。

> 在设计上，RV32I 足以作为编译器的目标指令集，并支持现代操作系统环境。同时，我们在设计时尽可能降低最小实现方案的硬件要求。RV32I 包含 47 条独特的指令，不过，一个具体的实现方案也许会用 1 条系统（SYSTEM）硬件指令代替 8 条 SCALL / SBREAK / RD* 指令，该指令总是引起自陷，这样硬件指令数量就降低到 40 条。RV32I 能够模拟几乎所有的 ISA 扩展（除了 A 扩展，它需要额外的硬件来支持原子性（atomicity））。

- [2.1 程序员可见的基本整型子集模型](programmers-model.md)
- [2.2 基本指令格式](base-instr-formats.md)
- [2.3 立即数编码变体](imm-encoding-vars.md)
- [2.4 整型计算指令](int-comp-instrs.md)
- [2.5 控制转移指令](ctrl-tran-instrs.md)
- [2.6 取数和存数指令](load-store-instrs.md)
