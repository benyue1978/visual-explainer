# Data Representation 内容产品设计

**状态：** 设计方向已确认；内容包框架已建立，候选作品数量仍未确定

**产品方向：** 知识与解释优先；考纲仅用于内部范围审查

**视觉状态：** 尚未开始制作第一张图

## 1. 产品目标

把 Data Representation 建成一套连贯的计算机科学学习内容。学习者先理解 bits 如何表示信息，再看数字、文字、图像和声音各自如何编码，最后比较文件大小、存储与压缩之间的关系。

这套内容应当让学习者能够：

- 解释同一组 bits 如何依照不同规则表示不同类型的信息。
- 描述常见数值、文字、图像与声音表示的基本机制。
- 跟随具体数值完成一次编码、计算或大小估算。
- 分清容易混淆的概念，例如数值表示与字符编码、图像分辨率与色深、声音采样率与采样精度，以及有损与无损压缩。
- 理解不同表示与压缩方式带来的容量、精度、质量和可恢复性取舍。

### 目标学习者与先备知识

主要读者是学习 Cambridge IGCSE 与 AS/A Level Computer Science 的学生，也包括需要讲授这些概念的教师。图面默认使用英语术语与文案；本设计稿和内部 brief 使用中文。

学习者预计理解十进制位值与整数四则运算。课程从 bit 和 binary 的基本含义开始讲，不假设学生具备电子学、编程或数字音频背景；必要概念会在第一次使用时解释。

## 2. 产品原则

### 2.1 以概念组织内容

六个模块构成一条学习路径。模块边界由学生要理解的概念与认知负荷决定，不由考试章节决定。相关概念可以跨模块连接；例如图像和声音的表示会在文件大小与压缩模块中重新汇合。

### 2.2 用考纲做内部范围检查

设计阶段会参考 Cambridge IGCSE Computer Science 0478 与 AS & A Level Computer Science 9618 的数据表示内容，检查概念是否有明显遗漏。检查以概念家族为单位，不把每条考试目标逐项对应到某一张图，也不让考纲决定内容顺序。

内部 coverage matrix 用于记录：

- 概念家族及其核心知识点；
- 它所在的内容模块；
- 需要进一步解释或验证的部分；
- 与其他模块之间的连接。

资格代码、考试年份、章节编号和覆盖状态仅用于编辑阶段的内部审查，不能进入学习者可见的图面。正式事实仍要以来源支持；来源版本作为参考资料元数据保存，不作为课程结构。

### 2.3 以具体例子支撑解释

每一项 infographic 内容都要包含至少一个完整、可追踪的 worked example。正式 brief 必须给出准确输入、关键中间状态、最终结果和单位处理，并核实每一步。目录里的例子种子用于比较内容方向，不能代替正式 worked example。例子服务于概念解释，避免仅用术语、公式或装饰性图形填充页面。适合时，可在相邻内容间复用一个例子，帮助学习者看见概念之间的关系。

### 2.4 图面不出现考试标签

不在图上放置 syllabus 名称或编号、考试年份、IG／AS／A2 徽标、章节号或覆盖率标记。内容难度通过解释本身自然展开。需要延伸时，可用不依附考试分类的编辑性提示，例如“继续想一想”或“更深一层”。

### 2.5 参考教材的教学方法，重做自己的表达

教材用于研究教学方法，例如比较、放大、状态追踪、波形采样与 worked example。保留有效的解释机制，使用 Visual CS 已有的品牌视觉系统重新组织内容；不复刻教材插画、页面构图或专有视觉资产。

## 3. 概念路径

产品由一个总问题串联：**计算机怎样把不同信息变成 bits，又怎样解释、计算、存储和压缩这些 bits？**

开篇先用一组相同的 bits 建立全课程主线：`01000001` 在 unsigned binary 下表示 `65`，在 ASCII 字符编码下表示 `A`。重点是位模式本身不标注含义；它的解释取决于使用的表示规则。后续数字和文本模块再次调用这组例子，形成前后连接。这是一个开篇教学装置，可以并入第一项内容，不额外规定一张独立海报。

| 模块 | 学习问题 | 核心概念 | 与后续内容的连接 |
|---|---|---|---|
| 1. Bits, Bytes & Magnitudes | 信息如何用有限的二进制状态表示，容量又如何衡量？ | bit、nibble、byte、二进制数量级、容量单位、binary 与 decimal prefixes | 为所有后续数据类型建立共同底层与容量尺度 |
| 2. Representing Numbers | 一组 bits 如何表示不同数值，又如何进行运算？ | binary、denary、hexadecimal、转换、Hex 的用途、有符号整数、one’s/two’s complement、BCD、算术、overflow、bit manipulation、floating point | 展示相同数据宽度如何对应不同数值范围、精度与操作 |
| 3. Representing Text | 字符如何转换为数值和二进制？ | character set、character code、ASCII、extended ASCII、Unicode | 连接符号、数值和具体二进制编码 |
| 4. Representing Images | 计算机如何描述像素图和图形对象？ | bitmap、pixel、file header、image/screen resolution、colour depth、vector object、property、drawing list | 为图片质量与文件大小计算准备概念 |
| 5. Representing Sound | 连续声音如何成为离散数据？ | analogue/digital、sampling、sample rate、sample resolution、accuracy | 为声音文件大小与压缩建立模型 |
| 6. Storage & Compression | 不同数据表示占多少空间，压缩改变了什么？ | 图像与声音大小估算、存储与传输需求、有损与无损压缩、RLE 与 Huffman 等编码方法 | 汇总前五个模块，呈现体积、质量与信息保留的取舍 |

## 4. 内部概念覆盖检查

这张表检查内容完整性，不是公开的考试逐条对照表。它允许一个概念由多项内容共同解释，也允许一项内容连接多个概念。

| 概念家族 | 需要检查的知识范围 | 主要模块 | 审查重点 |
|---|---|---|---|
| 数字底层与容量 | bit/nibble/byte、二进制数量级、容量单位、二进制与十进制前缀 | Bits, Bytes & Magnitudes | 单位换算方向、符号大小写、1024 与 1000 的语境 |
| 整数与数值表示 | binary/denary/hexadecimal、进制转换、Hex 的用途、有符号数、one’s/two’s complement、BCD | Representing Numbers | 分清位模式、解释规则与数值；BCD 与普通二进制的差异 |
| 数值运算与 bit 操作 | 加减法、overflow、logical/arithmetic/cyclic shifts、bitwise operations、masking | Representing Numbers | 位宽、丢失或补入的位，以及移位与算术结果的关系 |
| 实数表示 | mantissa、exponent、normalisation、精度、范围、rounding、overflow/underflow | Representing Numbers | 明确浮点是有限精度近似，示例每一步一致 |
| 文本编码 | character set、字符代码、ASCII、extended ASCII、Unicode 及其字符范围差异 | Representing Text | 编码映射不是字符本身；比较字符范围与编码容量，不要求背诵不必要的字符码 |
| 图像表示 | bitmap、header、像素、resolution、screen resolution、colour depth、vector drawing objects/properties/list | Representing Images | 清楚区分像素网格和绘图对象；解释质量、缩放与容量 |
| 声音表示 | analogue/digital、sampling、sample rate、sample resolution，以及采样参数对准确度与文件大小的影响 | Representing Sound | 横向时间采样与纵向振幅精度分别解释，再连接到准确度和数据量 |
| 文件大小与压缩 | 图片/声音大小估算、有损/无损、RLE、Huffman 与媒体适用性 | Storage & Compression | 将大小计算、无损编码和有损取舍分开解释；涵盖文本、bitmap、vector 与 sound 的相关压缩方式；区分编码思路与建树操作 |

矩阵中的检查结果只供内容团队审阅。若来源要求出现新的概念，优先判断它属于哪一个知识家族、会改变哪个学习目标，以及是否需要拆出新的学习内容；不为填满一张 syllabus 表而自动增加图。

## 5. Infographic Catalogue 草案

以下是内容候选，不是固定的海报数量。每项先确定学习问题与解释机制，再根据内容密度决定合并或拆分。表里的 worked example 是例子种子；正式 brief 要补足精确输入、过程、结果和校验。

| 内容项 | 学习问题与解释主线 | Worked example 种子 | 易混点或边界 |
|---|---|---|---|
| 位与容量 | 从 bit 逐步扩展到 byte 与更大容量单位，并比较二进制和十进制前缀 | `1 KiB = 1,024 bytes` 与 `1 kB = 1,000 bytes`；比较一组 GiB/GB 数值 | `KiB` 与 `kB` 的符号、数量级及题目指定的目标单位 |
| 同一个数的多种写法 | 同一整数在 denary、binary、hexadecimal 中如何保持相同数值；Hex 为何更紧凑 | `173₁₀ = 10101101₂ = AD₁₆` | Hex 是 binary 的简洁人类表示，不是另一种计算机底层数据 |
| 有符号整数与整数运算 | 固定宽度如何表示正负数、执行加减并产生 overflow | `+5 = 00000101`；8-bit one's complement `−5 = 11111010`、two's complement `−5 = 11111011`；分别展示 unsigned 与 signed overflow 边界 | 表示规则与“取反加一”算法分别解释；范围以位宽为条件，并区分有符号与无符号 overflow |
| BCD | 每个十进制数位如何各自编码，以及它与普通二进制整数的不同 | `59` 的普通 binary 与 BCD 对照，再联系一种适用的十进制显示场景 | BCD 逐位表示十进制数，不等同于整数的纯二进制；实用场景需有来源依据 |
| Bit manipulation | 移位、循环移位、逻辑运算与 mask 如何改变或检查位 | `00010110` logical left shift 两位得到 `01011000`；再用一个简单 mask 标出目标位 | 逻辑、算术、循环移位行为不同；说明哪些位被丢弃或补入 |
| 浮点数 | mantissa 与 exponent 如何描述实数，位分配如何影响精度与范围 | 一个小型浮点格式的编码、还原与 normalisation | 教学格式需明确；不要暗示有限位数能精确表达所有实数 |
| 文本 | 字符如何经字符集映射到数值，再以二进制保存 | ASCII `'A'` → 十进制代码 `65` → `01000001` | 字符、字符代码、字符集和具体编码的区别；例子明确写出使用的字符集 |
| Bitmap 图像 | 像素网格、resolution 和 colour depth 如何影响画面与数据 | 一个 `2 × 2` 小网格逐像素着色，并计算像素数据量 | image resolution 与 screen resolution 的区别；header 另作标注 |
| Vector 图形 | 绘图对象、属性和绘图列表如何描述图像，何时适合使用 vector | 用圆形、线段及其属性重建简单图形 | vector 与 bitmap 的表示方式和放大结果不同 |
| 声音 | 连续波形如何经采样与量化形成数字数值 | 8 个采样点映射到有限振幅级别 | sample rate 控制时间采样密度；sample resolution 控制振幅级别 |
| 文件大小 | 图片像素/色深与声音采样/时长如何形成估算大小 | `320 × 200 × 8 = 512,000 bits = 64,000 bytes`；`8000 samples/s × 8 bits/sample × 2 s = 128,000 bits = 16,000 bytes` | 区分 bit 与 byte，按题目要求处理单位和精度；说明结果是原始数据量估算，不含未给出的 header 或压缩开销 |
| 无损压缩 | 重复模式和符号频率如何形成较短的编码？ | `AAAAAAAAAABBBCC` → RLE `10A 3B 2C`；频率 A:10、B:3、C:2，可用一个有效 Huffman 编码示例 A:`1`、B:`01`、C:`00`，payload 为 20 bits（不计字典或 header） | 原始信息可以完整还原；RLE 与 Huffman 利用不同的数据规律，实际文件还要考虑保存编码信息的开销 |
| 有损压缩 | 为什么永久移除部分信息，容量下降会怎样影响质量？ | 一组图像或声音压缩前后的细节对照 | 适用于图像、声音或视频等场景；不把 lossy 写成可无损还原 |

图册可在内容审核后补充或拆分项目，例如将 storage prefixes 单独成图，或将不同 bit 操作拆开。最终决定依据是每张图是否只有一个清晰学习目标、是否能在目标阅读尺寸下展示必需解释，以及 worked example 是否可读。

## 6. Textbook Reference Notes 记录规范

每个教材参考条目记录：

- 书名、版本、章节、页码和图号；
- 可借鉴的教学手法及其帮助理解的概念；
- Visual CS 将如何重新组织、补充例子和重画关系；
- 需要纠正或标注的简化、术语、边界条件；
- 是否存在第三方资产或许可限制。

目前提供的 `Pasted text.txt` 提及两张教材材料，并明确描述了 binary/decimal prefixes 的对照表。原始截图、教材书目信息和页码并未随该文件提供。文字中还提到 pixel zoom、wave sampling、bit boxes、register、文件大小流程与 RLE 等一般教学设备；这些只作为待核对的设计线索，不作为已确认的截图记录。后续拿到原图和书目信息后再补齐条目；在此之前不编造来源页码或截图细节。

## 7. 视觉与内容 brief 规则

每项正式 brief 必须包含：

1. 一个以学习者问题表达的学习目标。
2. 一句准确的核心结论。
3. 一个主机制或概念关系图。
4. 一段完整 worked example，标出输入、中间步骤和结果。
5. 必须区分的相邻概念、边界条件或常见误解。
6. 与其他模块的知识连接，以及不在本项解释的内容。
7. 事实来源和对来源限制的记录。

视觉继续遵循仓库现有 [Visual CS 品牌指南](../../STYLE.md) 与 [内容指南](../../CONTENT_GUIDE.md)：暖象牙底色、深蓝黑文字与线条、克制的辅助色、清晰的主视觉与阅读路径、适配主题的示意图。不要把每一项都做成相同卡片网格；版式随概念机制变化。

图上不出现考试代码、年份、章节号、考试覆盖徽标或覆盖率。图上可以出现对理解有帮助的英文术语、公式与例子。内部 brief 默认中文撰写；面向 Cambridge 学生的图面文案默认英文，首次制作前可再确认。

## 8. 交付结构与完成标准

正式内容包拟放入 `projects/data-representation/`，包括：

- `README.md`：产品说明、概念路径与文件索引。
- `coverage-matrix.md`：内部概念级完整性检查，不含逐条考试目标映射。
- `infographic-catalogue.md`：学习问题、解释主线、例子和模块连接。
- `textbook-reference-notes.md`：可追溯的教材教学方法观察与改编决定。
- 各项正式内容的独立 brief 与后续资源。

在任何图像制作前，内容产品设计视为可进入下一阶段的条件：

- 六个模块的边界和顺序已审阅；
- 内部概念检查没有未处理的重要空白；
- 每一项图册候选都有学习问题、worked example 和明确边界；
- 术语、计算例子和文件大小公式已逐项核对来源；
- 所有教材参考都区分“已核对来源”与“仅从文字获知”；
- 图面遵守不放 syllabus 标记的原则。

## 9. 来源

- [Cambridge IGCSE Computer Science 0478 syllabus](https://www.cambridgeinternational.org/Images/763431-2029-2031-syllabus.pdf) — 内部检查二进制、数值系统、字符、声音、图像、存储与压缩等内容范围。
- [Cambridge International AS & A Level Computer Science 9618 syllabus](https://www.cambridgeinternational.org/Images/721397-2027-2029-syllabus.pdf) — 内部检查 prefixes、数值表示、字符、multimedia、compression、bit manipulation 与 floating point 等内容范围。
- 本仓库的 [Visual CS 品牌指南](../../STYLE.md)、[内容指南](../../CONTENT_GUIDE.md)、[信息图制作指南](../../INFOGRAPHIC_GUIDE.md) 和 [端到端流程](../../WORKFLOW.md)。
