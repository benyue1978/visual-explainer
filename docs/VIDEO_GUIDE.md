# 视频制作流程与工具

本指南规定 Visual CS 教学视频从研究到交付的制作流程，并说明每个阶段的产物与常用工具。根据项目需要，可替换单个工具，但要保留相应的内容、预览、对齐、字幕、渲染和质量检查步骤。

视频使用深色画布，并沿用 [Visual CS 品牌风格](STYLE.md) 的字体层级、语义配色、线条和插画语言；信息图使用浅色纸面画布。两种媒介保持同一母品牌识别度。

## 标准流程

```text
Topic
  ↓
Research + Concept Model + Script
(ChatGPT)
  ↓
STE Rewrite
(ChatGPT + ASD-STE100)
  ↓
Generate / Modify Video Source
(Codex)
  ↓
Composition + Scenes + Animation
(Remotion / React / SVG / Three.js / Manim)
  ↓
Preview / Animatic
(Remotion Studio)
  ↓
Narration
(Gemini TTS / ElevenLabs)
  ↓
Alignment
(WhisperX)
  ↓
Captions
(WebVTT / SRT)
  ↓
Compose + Render
(Remotion / FFmpeg)
  ↓
Multimodal QA
(Gemini / ChatGPT Vision)
  ↓
Revise Code
(Codex)
  ↺ 回到预览、旁白或渲染环节重新检查
  ↓
Final MP4
(Remotion / FFmpeg)
```

## 各环节的工作内容

### 1. Topic

明确主题、目标观众、预期时长或发布用途（如已有），以及观众看完后应该理解什么。范围太大时先缩小到一个可以讲清的核心问题。

### 2. Research + Concept Model + Script — ChatGPT

- 整理可靠资料、术语、机制、前置知识和常见误区。
- 画出概念模型：参与对象、状态、关系、输入输出和因果过程。
- 按学习顺序形成脚本，先建立直觉，再逐步引入正式术语和定义。
- 标明需要来源支撑的事实，以及比喻或教学简化的边界。

**产物：** research notes、concept model、初版 narration/script。

### 3. STE Rewrite — ChatGPT + ASD-STE100

把脚本改写为更受控、简洁、可理解的英语表达，检查句子复杂度、术语一致性和代词指代。ASD-STE100 是语言改写的参考标准，不代替技术审校，也不要求所有输出语言都改成英语。

改写后要对照原始概念模型，确认没有丢失条件、因果关系或技术含义。必要时保留术语并先解释，不为追求简单而引入错误。

**产物：** 可供配音和分镜使用的脚本版本，以及待确认术语。

### 4. Generate / Modify Video Source — Codex

Codex 根据脚本、场景说明和已有视觉规范生成或修改可维护的视频源代码。改动应围绕场景和视觉对象组织。先在主题项目内实现；当不同项目确实重复使用同一视觉规律时，再把它提炼成共享组件或包，避免预先搭建尚无实际用途的代码层。

**产物：** 可在 Remotion Studio 中预览的代码和 composition。

### 5. Composition + Scenes + Animation — Remotion / React / SVG / Three.js / Manim

- 用 scenes 划分讲解阶段，用 composition 组织完整视频。
- 使用 React 组合画面；SVG 表达矢量图、箭头、结构和关系。
- Remotion 控制帧、序列、过渡和输出。
- 需要三维或数学可视化时，使用 Three.js 或 Manim 制作专用素材，并确保输出格式和画面风格能接入最终视频流程。
- 通过同一对象在不同 scene 中持续出现，帮助观众追踪状态和因果变化。

**产物：** 可播放的分镜版场景和动画。

### 6. Preview / Animatic — Remotion Studio

先看场景顺序、画面节奏、视觉解释和大致时长。此阶段重点是验证讲解结构与画面是否匹配；发现结构问题时先调整场景和代码，再进入精细配音。

**产物：** animatic / 预览版，以及需调整的场景和时间点。

### 7. Narration — Gemini TTS / ElevenLabs

按通过初审的脚本生成旁白。可使用 Gemini TTS 或 ElevenLabs；检查发音、停顿、节奏、术语读法和情绪是否适合教学，并根据声音质量和控制需求选择工具。

**产物：** 旁白音频与采用的脚本版本。

### 8. Alignment — WhisperX

将最终旁白与词句或时间戳对齐，为字幕和音画同步提供基础。脚本或音频一旦变化，就重新对齐受影响内容。

**产物：** 词级或句级时间戳、需要人工校正的对齐结果。

### 9. Captions — WebVTT / SRT

从已校正的对齐结果生成字幕，检查断句、标点、专有名词和阅读时长。根据发布平台选择 WebVTT 或 SRT；字幕格式和具体平台要求待项目确定。

**产物：** 与旁白版本一致的字幕文件。

### 10. Compose + Render — Remotion / FFmpeg

将场景、动画、旁白和字幕组合并渲染。Remotion 负责可编程的画面和视频 composition；FFmpeg 用于媒体处理、转码或最终封装。

**产物：** 候选成片及可复现的渲染设置。

### 11. Multimodal QA — Gemini / ChatGPT Vision

从成片抽取画面并结合音频或字幕检查：

- 技术内容和因果关系是否正确。
- 旁白、画面和字幕是否同步。
- 图形、文字和对比是否易读。
- 视觉对象身份是否连续，动画是否清楚表达变化。
- 是否有遮挡、裁切、闪烁、意外空白或其他渲染问题。

模型检查用于发现问题，技术准确性和主观可读性仍需人工判断。

**产物：** 带时间点的问题清单和修订建议。

### 12. Revise Code — Codex

根据 QA 问题修改源代码，重新预览相关场景；如果旁白、脚本或时间发生变化，同步重新生成对齐结果和字幕，然后重新渲染和检查。

### 13. Final MP4 — Remotion / FFmpeg

所有画面、旁白、字幕与输出规格确认后，生成最终 MP4。保留对应代码、脚本、音频、字幕和渲染设置，以便之后修订。

## 迭代与交付记录

这不是只能从上到下执行一次的流水线。Animatic 可能暴露脚本问题；旁白可能改变节奏；QA 可能要求重写场景、重配音或重做字幕。任何上游内容改变，都要重新检查依赖它的下游产物。

每个项目保留采用的工具与版本、脚本和音频版本、人工修订、字幕、渲染设置及最终成片。修改上游内容后，重新检查所有受影响的旁白、时间戳、字幕和画面。
