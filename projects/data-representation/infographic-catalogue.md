# Infographic 候选目录

> **工作估算：约 19 张，最终数量未定。** 下方原有 13 项是宽泛候选主题，不等于逐张制作清单。按当前建议的粒度，宽泛主题会在不同机制或例子处拆分；后续再根据图面阅读尺寸、信息密度和 worked example 的可读性合并或调整。

## 建议的逐张工作目录（约 19 张）

这份目录用于帮助判断整套内容的规模。每张围绕一个主要学习问题和一条解释主线；编号是工作顺序，不是考试章节或已锁定的发布数量。

| # | 模块 | 单张图要解释的内容 |
|---:|---|---|
| 1 | Bits, Bytes & Magnitudes | 一个 bit 有两种状态；bit 数如何决定 pattern 数；直接建立 `1 byte = 8 bits`、`2^8 = 256 patterns`。 |
| 2 | Bits, Bytes & Magnitudes | byte 以上的容量单位，以及十进制与二进制前缀各自表示的数量。 |
| 3 | Representing Numbers | 同一个 denary 整数如何写成 binary 与 hexadecimal；binary 位值和 hexadecimal 四位分组如何连接。 |
| 4 | Representing Numbers | 如何用 powers of 2 将 binary 转为 denary，以及用连续除以 2 和倒序余数将 denary 转为 binary。 |
| 5 | Representing Numbers | unsigned 与 signed 整数怎样解释固定宽度的位模式，以及各自的数值范围。 |
| 6 | Representing Numbers | 二进制整数加减如何进行，以及固定宽度下 overflow 怎样出现。 |
| 7 | Representing Numbers | BCD 如何逐个十进制数位编码，以及它与普通 binary 整数的区别。 |
| 8 | Representing Numbers | logical、arithmetic 与 cyclic shifts 如何移动位，并处理移出或补入的位。 |
| 9 | Representing Numbers | bitwise logic 与 masks 如何检查、保留或改变指定位置的位。 |
| 10 | Representing Numbers | floating-point 的字段如何表示数值，以及位宽对范围和精度的影响。 |
| 11 | Representing Text | 字符如何映射到字符代码并保存为位模式；用 ASCII 与 Unicode 建立范围与编码的概念。 |
| 12 | Representing Images | bitmap 如何用像素网格、resolution 与 colour depth 描述图像。 |
| 13 | Representing Images | vector 图形如何用对象、属性与绘制顺序描述图像。 |
| 14 | Representing Sound | 连续波形如何经过时间采样和振幅量化成为数字声音。 |
| 15 | Storage & Compression | bitmap 图像的像素参数如何估算未压缩数据量。 |
| 16 | Storage & Compression | 声音的 sample rate、sample resolution、声道与时长如何估算未压缩数据量。 |
| 17 | Storage & Compression | RLE 如何利用连续重复的数据形成可逆的压缩表示。 |
| 18 | Storage & Compression | Huffman 如何利用符号出现频率构造不同长度的可逆编码。 |
| 19 | Storage & Compression | 有损压缩如何移除部分信息，以及体积和可感知质量如何取舍。 |

**粒度校准：** 若压缩到约 12–14 张，会合并更多不同机制；若拆到每种编码或表示各自独立，可能超过 20 张。当前按约 19 张作为中间粒度，先逐张制作和检查，再依据真实版面决定是否合并或拆分。图面只呈现知识、解释、术语和必要例子，不放 syllabus 标签或覆盖率信息。

## 决定合并或拆分的标准

- 一项作品有一个学习者能用一句话表达的问题和一个清楚的核心结论。
- 主机制、概念关系或因果过程能够在图面上看懂。
- 至少一个 worked example 能在目标阅读尺寸下展示输入、关键中间状态、结果和单位。
- 需要区分的概念与适用边界有足够空间，不靠缩小文字来塞进内容。
- 两个主题只有在共享一个自然的问题和机制时才合并；若机制、先备知识或例子相差太大，就考虑拆开。

**当前内容策划记录：** 第一项宽泛候选拆为两个学习问题：bit 数怎样形成更多 pattern；容量 prefixes 怎样表示十进制与二进制数量级。第一份 brief 处理前者；工作目录第 2 项已完成内容 brief、visual brief、成图和发布文案。此工作目录仍可在逐张制作中调整。

目录里的例子均为**例子种子**。它们用于安排内容方向，不等于经过完整来源核查的正式例子。正式 brief 仍需核实输入、每一步、结果、单位，以及教学简化或实现条件。

## 候选内容

### 1. 位与容量

- **学习问题：** 从 bit 到 byte 和更大单位，容量如何增长？相似的前缀又有何不同？
- **解释主线：** 由 bit、nibble、byte 逐步连接到较大容量单位；再比较 binary 与 decimal prefixes。
- **例子种子：** `1 KiB = 1,024 bytes`，`1 kB = 1,000 bytes`。
- **边界与易混点：** 区分大小写与前缀体系；单位换算要说明使用哪个目标单位和语境。
- **模块连接：** Bits, Bytes & Magnitudes；为所有文件大小估算准备单位。
- **状态：** 首张图制作中；[bit patterns 内容 brief](bits-and-bytes/content-brief.md) 已复核，[visual brief](bits-and-bytes/visual-brief.md) 与[图像初稿](bits-and-bytes/eight-bits-256-patterns-infographic.png)已建立；容量 prefixes 单独列入工作目录第 2 项。

### 2. 同一个数的多种写法

- **学习问题：** 同一个整数如何用 denary、binary 和 hexadecimal 表示？
- **解释主线：** 展开 place value，再把 binary 的四位一组对应到一位 hexadecimal。
- **例子种子：** `173₁₀ = 10101101₂ = AD₁₆`。
- **边界与易混点：** Hex 是让人更紧凑地读写 binary 的表示法，不是另一种底层数据。
- **模块连接：** Representing Numbers；可连接后续文本编码中的“数值如何被解释”。
- **状态：** 第三项已完成 content brief、visual brief、信息图与英文发布文案；文件位于 `projects/data-representation/number-bases/`。

### 3. Binary 与 denary 互转

- **学习问题：** 给定一个 binary 数或 denary 数，怎样一步步算出另一种表示？
- **解释主线：** Binary → denary：将每一位乘以对应的 2 的幂后相加；denary → binary：连续除以 2，记录余数并自下而上读取。
- **例子种子：** `110101₂ = 53₁₀`；同一数反向计算以检查结果。
- **边界与易混点：** 最右一位对应 `2⁰ = 1`；除法余数要从下往上读。示例按正整数讲解，`0₁₀ = 0₂` 可作为简短边界。
- **模块连接：** Representing Numbers；在 denary/binary/hex 表示关系之后，单独讲双向转换的可复用步骤。
- **状态：** Content brief、visual brief、成图、英文发布文案和最终图像复核均已完成并标记 READY；文件位于 `projects/data-representation/binary-conversion/`。

### 3. 有符号整数与整数运算

- **学习问题：** 固定位宽如何表示正负数、执行运算并限制可表示范围？
- **解释主线：** 对照 unsigned、one’s complement 与 two’s complement，再追踪加法结果和位宽边界。
- **例子种子：** 8-bit `+5 = 00000101`；one’s complement `−5 = 11111010`；two’s complement `−5 = 11111011`。可另用 8-bit unsigned `11111111 + 00000001 = 1 00000000`（存回 8 位为 `00000000`）和 8-bit two’s complement `01111111 + 00000001 = 10000000`（解释为 `−128`）对照不同解释下的 overflow。
- **边界与易混点：** 表示规则与“取反加一”的计算捷径要分开；范围取决于位宽，并区分有符号与无符号 overflow。
- **模块连接：** Representing Numbers；与 bit manipulation 共享位宽和位模式概念。
- **状态：** Candidate。

### 4. BCD

- **学习问题：** BCD 如何编码每个十进制数位，它与普通 binary 整数有何不同？
- **解释主线：** 对照相同十进制数的普通 binary 编码与逐位 BCD 编码。
- **例子种子：** 十进制 `59` 的普通 8-bit binary 为 `00111011`；BCD 为 `0101 1001`。
- **边界与易混点：** BCD 的每一组编码对应一个十进制数位，不是整个整数的纯二进制表示；实际应用应由来源支持。
- **模块连接：** Representing Numbers；可与数字显示或十进制输入联系。
- **状态：** Candidate。

### 5. Bit manipulation

- **学习问题：** 移位、循环移位、逻辑运算和 mask 如何改变或检查一组位？
- **解释主线：** 追踪输入位经过操作后的每个位置，并明确哪些位丢失、保留或补入。
- **例子种子：** 8-bit `00010110` logical left shift 两位得到 `01011000`；再用一个简单 bitwise mask 标出目标位。
- **边界与易混点：** logical、arithmetic、cyclic shifts 的行为不同；一次只比较清楚一种操作，并说明适用位宽。
- **模块连接：** Representing Numbers；复用整数位表示与二进制运算。
- **状态：** Candidate。

### 6. 浮点数

- **学习问题：** mantissa 与 exponent 如何表示实数，有限位数如何限制精度和范围？
- **解释主线：** 展示字段如何组合成数值，并沿编码、还原与舍入过程追踪一个值。
- **例子种子：** 选一个小型教学浮点格式，展示编码、还原及 normalisation。
- **边界与易混点：** 先声明字段宽度、符号和舍入约定；浮点是有限精度近似，不暗示所有实数都能精确表示。
- **模块连接：** Representing Numbers；可与声音、图像中的量化精度作概念联系，但表示机制不同。
- **状态：** Candidate。

### 7. 文本

- **学习问题：** 字符如何映射到代码，再以 binary 保存？
- **解释主线：** 追踪字符、字符集中的数值代码和保存的位模式，随后比较字符范围。
- **例子种子：** 在 ASCII 下，`'A' → 65 → 01000001`。
- **边界与易混点：** 区分字符、字符代码、字符集与具体编码；清楚声明使用 ASCII，不能把所有文本编码都说成同一映射。
- **模块连接：** Representing Text；回访开篇的 `01000001`，对照 unsigned binary 的解释。
- **状态：** Candidate。

### 8. Bitmap 图像

- **学习问题：** 像素网格、resolution 和 colour depth 如何共同描述画面？
- **解释主线：** 由图像放大到像素网格，再显示每个 pixel 的颜色代码和数据量。
- **例子种子：** 一个 `2 × 2` 网格按顺序放入四个 2-bit 颜色代码 `00 01 / 10 11`；原始像素 payload 为 `4 pixels × 2 bits = 8 bits`，不含 header。
- **边界与易混点：** 区分 image resolution 与 screen resolution；说明像素数据和 header 的范围；不要把像素网格说成 vector 对象。
- **模块连接：** Representing Images；为图像文件大小估算提供 pixel 数和 colour depth。
- **状态：** Candidate。

### 9. Vector 图形

- **学习问题：** 绘图对象、对象属性和绘图顺序如何描述一幅图？
- **解释主线：** 用形状对象和属性列表逐步重建一个简单图形，再比较放大时与 bitmap 的差异。
- **例子种子：** 用一个圆和一条线定义简单图标，记录各自的位置、大小或端点、线条属性及绘制顺序。
- **边界与易混点：** Vector 保存绘图对象和属性，不是逐像素网格；清晰缩放不代表任何尺寸或复杂度下都更省空间。
- **模块连接：** Representing Images；与 bitmap 对照，并在存储模块比较两种表示的取舍。
- **状态：** Candidate。

### 10. 声音

- **学习问题：** 连续波形如何经采样和量化成为数字数值？
- **解释主线：** 从 analogue 波形显示时间采样点，再把每个测量值映射到有限振幅级别。
- **例子种子：** 用 8 个采样点展示波形，并把各点映射到有限的振幅级别。
- **边界与易混点：** sample rate 决定时间采样密度；sample resolution 决定可表示的振幅级别；二者分别影响准确度与数据量。
- **模块连接：** Representing Sound；为声音文件大小估算和压缩提供采样模型。
- **状态：** Candidate。

### 11. 文件大小

- **学习问题：** 图片和声音的表示参数如何形成未压缩数据量估算？
- **解释主线：** 将像素数与每像素位数相乘；将每秒采样数、每个采样的位数和时长相乘，再换算 bit 与 byte。
- **例子种子：** 图片：`320 × 200 × 8 = 512,000 bits = 64,000 bytes`。声音：假设单声道，`8,000 samples/s × 8 bits/sample × 2 s = 128,000 bits = 16,000 bytes`。
- **边界与易混点：** 说明这是 raw data 估算；除非输入明确给出，否则不计 header、压缩、声道或其他文件开销；按题目要求处理单位和精度。
- **模块连接：** Storage & Compression；回接图像、声音表示与容量单位。
- **状态：** Candidate。

### 12. 无损压缩

- **学习问题：** 如何利用重复模式或符号频率缩短编码，并完整还原原始信息？
- **解释主线：** 对照 RLE 的重复计数和 Huffman 根据频率分配不同长度编码的方式。
- **例子种子：** `AAAAAAAAAABBBCC` 的 RLE 可写为 `10A 3B 2C`。若频率为 A:10、B:3、C:2，一个有效的 Huffman 编码可用 A:`1`、B:`01`、C:`00`，payload 共 20 bits，不计编码表或 header。
- **边界与易混点：** 原始信息可完整还原；RLE 与 Huffman 利用的数据规律不同；实际文件需考虑保存编码信息的开销。
- **模块连接：** Storage & Compression；复用文本符号或像素模式，并与有损压缩比较。
- **状态：** Candidate。

### 13. 有损压缩

- **学习问题：** 为什么压缩时永久移除部分信息，体积变化如何影响可感知质量？
- **解释主线：** 用压缩前后细节对照呈现被移除的信息、体积与质量之间的取舍。
- **例子种子：** 选一组图像或声音样本，展示压缩前后的数据或可感知细节差异；正式 brief 决定具体材料和比较条件。
- **边界与易混点：** 有损结果不能按原样无损还原；适用情境和被移除细节需按选定格式及样本准确说明。
- **模块连接：** Storage & Compression；与无损压缩并列比较可恢复性和体积取舍。
- **状态：** Candidate。
