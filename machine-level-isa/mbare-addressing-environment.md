## 3.5 Mbare addressing environment

Mbare 环境在重置时被选中或是在写入`mstatus`寄存器的 `VM` 字段时进入。

在 Mbare 环境中，所有虚拟地址转换到物理地址没有变化，超出的高位会被截断。上一节描述的物理存储器属性和访问控制可被用作限制访问。
