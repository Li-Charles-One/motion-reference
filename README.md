# 动画参考 (Motion Reference)

精选 AI / Remotion 动效模板库、分镜配方卡与视频制片工作流参考合集（代码化「AE 模板」参考仓）。

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

## 收录目录

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
- **协议**：Apache-2.0（注意音效与 Remotion 框架遵循各自许可）
- **按需挂载为 Skill**：`npx skills add Vincentwei1021/video-shotcraft` 或将本目录软链至 `~/.config/opencode/skills/video-shotcraft`

### 2. [`video-talkcraft/`](https://github.com/Vincentwei1021/video-talkcraft) — 口播解说视频动效模板库

`video-shotcraft` 同作者出品的口播解说视频姊妹篇：输入口播文稿 + 配音音频，本机对齐字级时间戳，自动编排 SHOTBOOK 分镜并渲染声画锁定的解说成片（知识科普、产品评测、深度解读）。

- **上游仓库**：[Vincentwei1021/video-talkcraft](https://github.com/Vincentwei1021/video-talkcraft)
- **在线动效画廊（预览选片）**：<https://vincentwei1021.github.io/video-talkcraft/>
- **核心资产**：
  - **108+ 张口播动效配方卡**：动态字卡、数据对比镜头、证据巡游、G5 线稿示意图、六式运动承接转场、视频容器边框八式
  - 自包含即拷即用源码：`video-talkcraft/template/cards/`、`template/components/`（花字/砸字/荧光笔/数字滚动）
  - **字级配音同步与预剪**：`scripts/timestamps_cpu.py`、`scripts/voice_trim.py`
  - **多轨工作台与单片段透明导出**：支持在时间轨右键单独导出 ProRes 4444 / WebM VP9 带透明通道叠加素材
- **协议**：PolyForm Noncommercial 1.0.0（个人、学习、研究免费；将该工具本身用于商业用途需联系原作者授权）
- **按需挂载为 Skill**：`npx skills add Vincentwei1021/video-talkcraft` 或将本目录软链至 `~/.config/opencode/skills/video-talkcraft`

---

## 目录一览

```text
motion-reference/
├── README.md
├── video-shotcraft/    submodule  Vincentwei1021/video-shotcraft  (150 个产品宣传片镜头模板)
└── video-talkcraft/    submodule  Vincentwei1021/video-talkcraft  (108+ 个口播解说动效模板)
```
