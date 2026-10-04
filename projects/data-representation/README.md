# Data Representation

## 产品说明

这是一套以知识和解释为核心的计算机科学学习内容，帮助学习者理解计算机怎样用 bits 表示不同信息、执行数值运算、存储数据，并通过压缩改变容量与质量之间的取舍。

主要读者是 IGCSE 与 AS/A Level Computer Science 学生，以及讲授这些概念的教师。学习者预计理解十进制位值和整数四则运算；课程从 bit 与 binary 的基本含义开始，不假设编程、电子学或数字音频背景。内部策划文档使用中文，面向学习者的图文默认使用英语。

## 学习路径

| 模块 | 学习者要回答的问题 | 核心知识 | 与路径的连接 |
|---|---|---|---|
| Bits, Bytes & Magnitudes | 信息如何用有限的二进制状态表示，容量怎样衡量？ | bit、nibble、byte、数量级、容量单位、binary 与 decimal prefixes | 建立后续各类数据共同使用的底层与容量尺度。 |
| Representing Numbers | 一组 bits 如何表示不同数值并支持运算？ | binary、denary、hexadecimal、进制转换、有符号整数、BCD、整数运算、bit manipulation、floating point | 展示固定宽度和解释规则如何影响数值范围、精度与操作。 |
| Representing Text | 字符怎样映射为代码并存成 bits？ | character set、character code、ASCII、extended ASCII、Unicode | 把位模式的解释扩展到字符和符号。 |
| Representing Images | 计算机如何描述像素图和图形对象？ | bitmap、pixel、header、resolution、colour depth、vector object、property、drawing list | 为图像质量和文件大小的关系准备概念。 |
| Representing Sound | 连续声音怎样转成离散数据？ | analogue/digital、sampling、sample rate、sample resolution、accuracy | 为声音数据量估算和压缩建立表示模型。 |
| Storage & Compression | 不同表示占多少空间，压缩又改变了什么？ | 图像与声音大小估算、存储与传输、有损与无损压缩、RLE、Huffman | 汇总前面各类数据，比较容量、质量和信息可恢复性的取舍。 |

课程开篇可用同一位模式贯穿数字与文本：`01000001` 按 unsigned binary 解释为 `65`，按 ASCII 解释为 `A`。它是帮助建立主线的教学装置，可以放进第一项内容，不预设为独立作品。

## 编辑原则

- 内容顺序按概念依赖和学习者理解过程组织。内部完整性审查只按概念家族进行，不逐条映射考试目标，也不逐年比较 syllabus。
- 任何一项正式内容都要解释一个清晰的问题，并包含可追踪的 worked example；目录中的例子只是待深化的种子。
- 正式 brief 需区分事实、推导、教学简化和实现差异，并让重要技术断言可追溯到来源。
- 图上不出现 syllabus 名称或代码、考试年份、章节号、等级徽标或覆盖率标记。术语、公式和例子可按理解需要出现。
- 教材只作为教学方法的研究线索；重新组织概念并用 Visual CS 的视觉语言表达，不复刻教材页面或插画。
- 最终作品数量尚未确定；当前建议以约 19 张作为逐张规划的工作估算。目录中的 13 项是宽泛候选主题，已在工作目录里按不同学习问题拆分，之后仍可根据 worked example 的可读性、内容密度和阅读尺寸决定合并或拆分。

## 内容包

- [内部概念覆盖检查](coverage-matrix.md)：概念家族、模块归属、知识连接和待审查点。
- [Infographic 候选目录](infographic-catalogue.md)：学习问题、解释主线、例子种子和边界；不固定作品数量。
- [教材参考记录](textbook-reference-notes.md)：区分已从文字确认的描述和仍待原始材料核对的线索。
- [Content brief 模板](../../docs/CONTENT_BRIEF_TEMPLATE.md)：后续逐项研究和撰写内容时使用。
- [建议的逐张工作目录](infographic-catalogue.md#建议的逐张工作目录约-19-张)：当前约 19 张的内容粒度估算，最终数量仍开放。

## 逐项内容规划

- [Bits and Bytes — How Many Patterns Can Eight Bits Hold?](bits-and-bytes/content-brief.md)：第一项内容 brief 已复核；对应的 [visual brief](bits-and-bytes/visual-brief.md) 和[图像初稿](bits-and-bytes/eight-bits-256-patterns-infographic.png)已建立。
- [Data Size Prefixes — kB vs KiB, MB vs MiB](byte-prefixes/content-brief.md)：第二项内容 brief 和 visual brief 已复核；[成图](byte-prefixes/data-size-prefixes-kb-kib-mb-mib-infographic.png)、[发布文案](byte-prefixes/publishing-copy.md)和[最终图像复核](byte-prefixes/review-notes.md)已完成。
- [173 in Denary, Binary & Hex](number-bases/content-brief.md)：第三项内容 brief、visual brief、成图、[英文发布文案](number-bases/publishing-copy.md)和[最终图像复核](number-bases/review-notes.md)已完成。
- [Binary ↔ Denary: How to Convert](binary-conversion/content-brief.md)：单独讲 binary 与 denary 双向转换的操作方法；[visual brief](binary-conversion/visual-brief.md)、[可编辑 SVG](binary-conversion/binary-denary-conversion-infographic.svg)、[最终图像](binary-conversion/binary-denary-conversion-infographic.png)、[英文发布文案](binary-conversion/publishing-copy.md)和[最终图像复核](binary-conversion/review-notes.md)均已完成。
- [Pinterest 与网站发布文案](bits-and-bytes/publishing-copy.md)：第一张图的英文标题、说明、tags 和网站替代文本。
- 第一项宽泛候选已细分为两个学习问题：先解释 bit 数与 pattern 数的关系，再解释容量 prefixes；该内容路径仍可调整，也不预设最终作品数量。

## 制作阶段

首项内容 brief 已复核，约 19 张的工作目录和第一份 visual brief 已建立，后续逐项撰写并复核内容和视觉 brief，再制作、校对图像；工作方式遵循仓库的[内容准备指南](../../docs/CONTENT_GUIDE.md)、[解释指南](../../docs/EXPLANATION_GUIDE.md)、[信息图制作指南](../../docs/INFOGRAPHIC_GUIDE.md)和[端到端流程](../../docs/WORKFLOW.md)。

获批的总体设计见[Data Representation 内容产品设计](../../docs/superpowers/specs/2026-10-04-data-representation-design.md)。
