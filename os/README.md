#### 1.Linux有哪些内存模型？
答：内存模型描述的是对物理内存的管理方法，主要分为三种：flat memory，discontiguous memory和sparse memory。
- flat是平坦内存模型，物理地址空间连续时，使用数组索引物理地址，缺点是有内存空洞
- discontiguous是空洞内存模型，物理地址是分散的，使用map索引物理地址，缺点是开销大
- sparse是稀疏内存模型，解决空洞内存模型的弊端提出，map索引的不是单个物理地址，而是整个section
