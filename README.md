# 动画参考 (Motion Reference)

精选 AI / Remotion 动效模板库、分镜配方卡、UI 组件与视频制片工作流参考合集（代码化「AE 模板」与动效技法参考仓）。

通过 `git submodule` 收录上游仓库，便于本地查阅镜头源码（`.tsx`）、分镜拆解文档与工作台实现，也可按需软链给 Claude Code / Codex / OpenCode 作为 Skill 使用。

> Remotion 官方底层开发规范与 Studio 交互技能见 [NIUBI-skills-collection](https://github.com/Li-Charles-One/NIUBI-skills-collection) 中的 `skills/remotion-skills`。

## 克隆与更新

首次克隆（含子模块）：

```bash
git clone --recurse-submodules https://github.com/Li-Charles-One/motion-reference.git
```

已克隆但子模块为空：

```bash
git submodule update --init --recursive
```

拉取上游最新模板与镜头：

```bash
git submodule update --remote --merge
```

---

## 一、全流程成片与分镜配方库（Vincentwei1021 三部曲）

### 1. [`video-shotcraft/`](https://github.com/Vincentwei1021/video-shotcraft) — 产品宣传片分镜与动效模板库

把真实网页/产品界面截图与文案，用 Remotion 代码逐帧渲染成大厂级产品发布宣传片（复刻 Figma、Notion、Raycast、Slack、Perplexity、ClickUp 等官方宣传片镜头语言）。

- **上游仓库**：[Vincentwei1021/video-shotcraft](https://github.com/Vincentwei1021/video-shotcraft)
- **在线镜头画廊（预览选片）**：<https://vincentwei1021.github.io/video-shotcraft/>
- **核心资产**：
  - **124 张分镜配方卡 / 150 个预设镜头**（10 大类：开场遮罩、2.5D 网页运镜/爆炸图、转场、大字排版、UI 入场、交互波纹、数据突变、聚光灯强调、节奏闪切、片尾收束）
  - 配方文档：`video-shotcraft/references/shots/<category>/<card>.md`
  - Remotion 源码：`video-shotcraft/demos/<category>/<card>/`
  - **Motion Workbench**：浏览器内类剪映多轨编辑器
  - **JianYing Export**：一键导出 Mac 剪映专业版可编辑草稿（独立分镜轨、原生字幕轨、BGM/SFX 音轨）

### 2. [`video-talkcraft/`](https://github.com/Vincentwei1021/video-talkcraft) — 口播解说视频动效模板库

输入口播文稿 + 配音音频，本机对齐字级时间戳，自动编排 SHOTBOOK 分镜并渲染声画锁定的解说成片（知识科普、产品评测、深度解读）。

- **上游仓库**：[Vincentwei1021/video-talkcraft](https://github.com/Vincentwei1021/video-talkcraft)
- **在线动效画廊（预览选片）**：<https://vincentwei1021.github.io/video-talkcraft/>
- **核心资产**：
  - **108+ 张口播动效配方卡**：动态字卡、数据对比镜头、证据巡游、G5 线稿示意图、六式运动承接转场、视频容器边框八式
  - 自包含即拷即用源码：`video-talkcraft/template/cards/`、`template/components/`（花字/砸字/荧光笔/数字滚动）
  - **多轨工作台与单片段透明导出**：支持在时间轨右键单独导出 ProRes 4444 / WebM VP9 带透明通道叠加素材

### 3. [`anything2explainer/`](https://github.com/Vincentwei1021/anything2explainer) — 黑底科技科普与原理图解动画

输入任意主题或技术概念，自动用 Remotion 绘制暗黑画布（Black-canvas）信息图、结构流向图、原理拆解动画，配齐 TTS 语音、字幕与底部章节进度条（中英双语支持）。

- **上游仓库**：[Vincentwei1021/anything2explainer](https://github.com/Vincentwei1021/anything2explainer)
- **适用场景**：硬件/家电/算法原理拆解、黑底科技感流程图与数据科普短片

---

## 二、即拷即用的 Remotion 组件库（`shadcn/ui` 风格）

### 4. [`remocn/`](https://github.com/Remocn/remocn) — Remotion 生产级动画组件与场景库

Remotion 界的 `shadcn/ui`，提供可调节、可直接复制到工程里的生产级文字入场、转场过渡、动态背景与预设场景组件。

- **上游仓库**：[Remocn/remocn](https://github.com/Remocn/remocn)

### 5. [`snapcn/`](https://github.com/shadcn-labs/snapcn) — 产品演示专用 Remotion 组件注册表

面向产品与数码演示视频的 Remotion 组件集合：文字揭示（Text Reveal）、设备样机外框（手机/桌面窗口套壳）、终端命令行动画、Logo 定版出场与完整演示场景。

- **上游仓库**：[shadcn-labs/snapcn](https://github.com/shadcn-labs/snapcn)

---

## 三、动效技法字典与全能制片知识库

### 6. [`motion-skills/`](https://github.com/iart-ai/motion-skills) — 50 个细分领域动效技能包

由 iart.ai 开源的 14 个技能包（共 50 个子 Skill），覆盖动态字体排版（Kinetic Typography）、数据可视化（Data-viz）、科普解说、竖屏短视频（TikTok/Reels）、WebGL 3D 视觉与 Manim 数学物理动画。

- **上游仓库**：[iart-ai/motion-skills](https://github.com/iart-ai/motion-skills)

### 7. [`awesome-ai-motion/`](https://github.com/gongnyang/awesome-ai-motion) — 637 种动效技法图鉴

面向 AI Agent 的动效实战图鉴：归纳了 637 种动效技法、128 个参考预览短片与 11 套完整场景配方（无限画布平移、多层深度视差、3D 卡片翻转堆叠、形态匹配剪辑、数据故事等）。

- **上游仓库**：[gongnyang/awesome-ai-motion](https://github.com/gongnyang/awesome-ai-motion)

### 8. [`OpenMontage/`](https://github.com/calesthio/OpenMontage) — 全链路开源 Agent 视频制片系统

包含 12 条视频制作流水线、100+ 工具脚本与 700+ 个制片知识/技能文件，覆盖从分镜策划、运镜语法、动态图形到后期合成的全流程参考。

- **上游仓库**：[calesthio/OpenMontage](https://github.com/calesthio/OpenMontage)

---

## 目录一览

```text
motion-reference/
├── README.md
├── video-shotcraft/      submodule  Vincentwei1021/video-shotcraft    (150 个产品宣传片镜头模板)
├── video-talkcraft/      submodule  Vincentwei1021/video-talkcraft    (108+ 个口播解说动效模板)
├── anything2explainer/   submodule  Vincentwei1021/anything2explainer (黑底科技科普与原理图解动画)
├── remocn/               submodule  Remocn/remocn                     (shadcn 风格 Remotion 组件库)
├── snapcn/               submodule  shadcn-labs/snapcn                (产品/样机/文字揭示组件库)
├── motion-skills/        submodule  iart-ai/motion-skills             (50 个动效/数据可视化/WebGL/Manim 技能)
├── awesome-ai-motion/    submodule  gongnyang/awesome-ai-motion       (637 种动效技法与参数图鉴)
└── OpenMontage/          submodule  calesthio/OpenMontage             (12 条管线 + 700+ 制片知识库)
```
