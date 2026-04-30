# ascii-excalidraw

> Convert ASCII art diagrams to hand-drawn Excalidraw JSON files.

<details>
<summary>🇨🇳 中文说明</summary>

> 将 ASCII 字符画转换为手绘风格 Excalidraw JSON 文件。

</details>

---

## Overview

A Claude Code skill that parses ASCII diagrams and converts them into beautiful, hand-drawn style Excalidraw files. It analyzes structure first, then generates JSON module-by-module for accuracy.

<details>
<summary>🇨 概述</summary>

一个 Claude Code 技能，解析 ASCII 图并转换为精美的手绘风格 Excalidraw 文件。先分析结构，再逐模块生成 JSON 确保准确性。

</details>

---

## Quick Start

In Claude Code, trigger the skill:

```
/ascii-excalidraw
```

Then paste your ASCII diagram. The skill will:

1. Analyze the structure (boxes, arrows, containers, layers)
2. Assign semantic colors based on keywords
3. Generate Excalidraw JSON module by module
4. Output a `.excalidraw` file for [excalidraw.com](https://excalidraw.com)

<details>
<summary>🇨🇳 快速开始</summary>

在 Claude Code 中触发技能：

```
/ascii-excalidraw
```

然后粘贴 ASCII 图。技能会自动：

1. 分析结构（方框、箭头、容器、层级）
2. 根据关键词分配语义颜色
3. 逐模块生成 Excalidraw JSON
4. 输出可在 [excalidraw.com](https://excalidraw.com) 打开的 `.excalidraw` 文件

</details>

---

## Examples

### Example 1: System Architecture

**Input:**

```
┌────────────┐      ┌──────────────┐      ┌──────────┐
│   Web App  │─────▶│  API Server  │─────▶│ Database │
────────────┘      └─────────────┘      ──────────
                           │
                     ┌─────▼─────┐
                     │   Cache   │
                     └───────────┘
```

**Output:** Color-coded boxes (blue/violet/green/yellow) with arrow connections in hand-drawn style. See `examples/01-architecture.excalidraw`.

<details>
<summary>🇨🇳 示例一：系统架构图</summary>

**输出：** 按组件类型着色的方框（蓝/紫/绿/黄）和箭头连接，手绘风格。详见 `examples/01-architecture.excalidraw`。

</details>

---

### Example 2: PPO Training Loop

**Input:**

```
────────────┐    ┌────────────┐    ┌────────────┐
│  Collect   │───▶│  Compute   │───▶│   Update   │
│  Traject.  │    │ Advantage  │    │  Policy    │
└────────────┘    ────────────┘    └─────┬──────┘
         ▲                                │
         │         ┌────────────         │
         ─────────│  Evaluate  │◀────────
                   │  & Check   │
                   └────────────┘
```

**Output:** Flow diagram with color-coded phases and feedback loop arrows. See `examples/02-ppo-loop.excalidraw`.

<details>
<summary>🇨🇳 示例二：PPO 训练循环</summary>

**输出：** 带颜色区分的阶段和反馈循环箭头的流程图。详见 `examples/02-ppo-loop.excalidraw`。

</details>

---

## Color Palette

| Component | Fill | Stroke |
|---|---|---|
| Frontend | `#a5d8ff` | `#1971c2` |
| Backend | `#d0bfff` | `#7048e8` |
| Database | `#b2f2bb` | `#2f9e44` |
| External | `#ffc9c9` | `#e03131` |
| Queue | `#fff3bf` | `#f08c00` |
| AI/ML | `#eebefa` | `#9c36b5` |
| Auth | `#c3fae8` | `#087f5b` |
| Monitor | `#fcc2d7` | `#e64980` |

<details>
<summary>🇨🇳 颜色方案</summary>

| 组件 | 填充色 | 描边色 |
|---|---|---|
| 前端 | `#a5d8ff` | `#1971c2` |
| 后端 | `#d0bfff` | `#7048e8` |
| 数据库 | `#b2f2bb` | `#2f9e44` |
| 外部服务 | `#ffc9c9` | `#e03131` |
| 消息队列 | `#fff3bf` | `#f08c00` |
| AI/ML | `#eebefa` | `#9c36b5` |
| 认证 | `#c3fae8` | `#087f5b` |
| 监控 | `#fcc2d7` | `#e64980` |

</details>

---

## Features

- **Structure-first analysis** — Parses boxes, arrows, containers before generating JSON
- **Module-by-module generation** — Each component generated separately for accuracy
- **Semantic color assignment** — Auto-colors by keyword (web→blue, db→green, etc.)
- **Hand-drawn sketch style** — Excalifont, hachure fills, variable roughness
- **Layout planning** — Text width estimation and proportion checking before generation

<details>
<summary>🇨🇳 功能特性</summary>

- **结构优先分析** — 在生成 JSON 前解析方框、箭头、容器
- **逐模块生成** — 分别生成每个组件，避免出错
- **语义颜色分配** — 根据关键词自动着色（web→蓝，db→绿等）
- **手绘草图风格** — Excalifont 字体、hachure 填充、可变粗糙度
- **布局规划** — 生成前估算文字宽度和比例检查

</details>

---

## File Structure

```
├── SKILL.md                     # Skill definition
├── README.md                    # This file (bilingual)
├── examples/
│   ├── 01-architecture.ascii    # Example: system architecture
│   ├── 01-architecture.excalidraw
│   ├── 02-ppo-loop.ascii        # Example: PPO training loop
│   └── 02-ppo-loop.excalidraw
└── scripts/
    └── merge_modules.py         # Module assembly helper
```

---

## Links

- [ClawHub](https://clawhub.ai) — Install with `clawhub install publish-ascii-excalidraw`
- [Hermes PR](https://github.com/NousResearch/hermes-agent/pull/17720)
- [anthropics/skills PR](https://github.com/anthropics/skills/pull/1068)

---

## License

MIT
