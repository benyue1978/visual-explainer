# 内部概念覆盖检查

> **用途：** 编辑阶段检查知识家族有没有明显遗漏，以及概念之间的连接是否清楚。这不是面向学习者的 syllabus 对照表，也不是逐条考试目标与作品的映射。

矩阵按概念而不是考试结构组织。一个知识家族可以跨越多项内容，一项内容也可以连接多个家族。官方课程文件只用作粗略范围审查，帮助发现可能漏掉的概念；不比较 syllabus 年份或版本，不跟踪考试代码、章节或逐条目标。矩阵结果只供内容团队使用，不能移入学习者可见的图面。

| 概念家族 | 需要解释的知识 | 主要模块 | 与其他模块的连接 | 编辑审查与待核事项 |
|---|---|---|---|---|
| 数字基础与容量 | bit、nibble、byte；二进制数量级；容量单位；binary 与 decimal prefixes。 | Bits, Bytes & Magnitudes | 所有数据类型最终都由位模式表示；容量概念用于图片、声音和压缩比较。 | 核对单位换算方向、符号大小写及 1000/1024 的使用语境；Worked example 要明确目标单位与采用的前缀。 |
| 整数与数值表示 | binary、denary、hexadecimal；进制转换；Hex 的用途；有符号整数；one’s complement、two’s complement；BCD。 | Representing Numbers | 与文本编码共同说明位模式依赖解释规则；与文件大小连接位数和可表示范围。 | 区分位模式、解释规则和数值；说明 BCD 是逐个十进制数位编码；范围例子要写明位宽。 |
| 数值运算与 bit 操作 | 二进制加减法；overflow；logical、arithmetic、cyclic shifts；bitwise operations 与 masking。 | Representing Numbers | 复用整数表示的位宽；与计算机存储位和状态变化相连。 | 清楚标出位宽、进位、丢失或补入的位；区分移位种类与算术解释；Worked example 每步都按同一位宽计算。 |
| 实数表示 | mantissa、exponent、normalisation；精度与范围；rounding；overflow 与 underflow。 | Representing Numbers | 延伸数值表示，之后可与图像、声音中的精度和近似作概念比较。 | 明确浮点数是有限精度表示；教学格式需声明字段宽度、编码约定和舍入规则；编码、还原与结果要一致。 |
| 文本编码 | character set、character code；ASCII、extended ASCII、Unicode；字符范围和编码容量。 | Representing Text | 通过 `01000001` 回接数字模块，展示相同位模式也可代表字符。 | 区分字符、字符代码、字符集与具体编码；字符范围依赖编码，不要求背诵无助于理解的具体字符码。 |
| 图像表示 | bitmap、pixel、header、image resolution、screen resolution、colour depth；vector drawing objects、properties、drawing list。 | Representing Images | 分别连接数字表示、声音的离散表示和存储大小估算。 | 区分像素网格与绘图对象；区分图像分辨率和屏幕分辨率；解释放大、质量与数据量时声明模型范围。 |
| 声音表示 | analogue/digital；sampling；sample rate；sample resolution；采样如何影响准确度与数据量。 | Representing Sound | 为声音文件大小公式与有损压缩提供前置模型。 | 分开解释时间轴上的采样密度和振幅量化级别；例子需说明采样点、量化值和简化假设。 |
| 文件大小与压缩 | 图像和声音大小估算；存储与传输需求；有损/无损压缩；RLE、Huffman 及相关媒体的压缩方式。 | Storage & Compression | 汇合前五个模块中的表示宽度、像素、采样和容量单位。 | 将大小估算、无损编码和有损取舍分开解释；核对 bit/byte、时间和单位；说明是否计入 header、编码表、声道或压缩开销。 |

## 内部范围参考

以下官方文件只用于核对是否有重要知识家族遗漏，不用于定义本课程的模块顺序或图册数量。日常更新不要求按年份维护差异表。

- [IGCSE Computer Science：Data Representation 范围参考](https://www.cambridgeinternational.org/Images/763431-2029-2031-syllabus.pdf)
- [AS & A Level Computer Science：Data Representation 范围参考](https://www.cambridgeinternational.org/Images/721397-2027-2029-syllabus.pdf)

## 审查状态

目前这份矩阵是设计阶段的范围清单，不表示正式内容 brief 已经研究或验证。每个未来 brief 仍需为重要断言提供适当来源或透明推导，并核对完整例子的输入、中间状态、结果和单位。若发现新概念，先判断它属于哪个知识家族、会不会改变学习目标，再决定现有内容是否需要调整；不为了填满一张考试清单而自动新增作品。
