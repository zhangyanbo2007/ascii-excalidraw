# ascii-excalidraw

> Convert ASCII art diagrams to hand-drawn Excalidraw JSON files
>
> 将 ASCII 字符画转换为手绘风格 Excalidraw JSON 文件

---

## Overview / 概述

A Claude Code skill that parses ASCII diagrams and converts them into beautiful, hand-drawn style Excalidraw files. It analyzes structure first, then generates JSON module-by-module for accuracy.

一个 Claude Code 技能，解析 ASCII 图并转换为精美的手绘风格 Excalidraw 文件。先分析结构，再逐模块生成 JSON 确保准确性。

---

## Quick Start / 快速开始

### In Claude Code

```
/ascii-excalidraw
```

Then paste your ASCII diagram. The skill will:
1. Analyze the structure (boxes, arrows, containers, layers)
2. Assign semantic colors based on keywords
3. Generate Excalidraw JSON module by module
4. Output a `.excalidraw` file for excalidraw.com

在 Claude Code 中输入 `/ascii-excalidraw`，然后粘贴 ASCII 图。技能会自动分析结构、分配颜色、逐模块生成 JSON，输出 `.excalidraw` 文件。

---

## Examples / 示例

### Example 1: Architecture Diagram / 系统架构图

**Input:**
```
┌────────────┐      ┌──────────────┐      ┌──────────┐
│   Web App  │─────▶│  API Server  │─────▶│ Database │
────────────┘      └──────┬───────┘      └──────────
                           │
                     ┌─────▼─────┐
                     │   Cache   │
                     └───────────┘
```

**Output:** Color-coded boxes with arrow connections in hand-drawn style.

See `examples/01-architecture.excalidraw` for the generated file.

### Example 2: PPO Training Loop / PPO 训练循环

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

**Output:** Flow diagram with color-coded phases and feedback loop arrows.

See `examples/02-ppo-loop.excalidraw` for the generated file.

---

## Color Palette / 颜色方案

| Component | Fill | Stroke |
|---|---|---|
| Frontend / 前端 | `#a5d8ff` | `#1971c2` |
| Backend / 后端 | `#d0bfff` | `#7048e8` |
| Database / 数据库 | `#b2f2bb` | `#2f9e44` |
| External / 外部 | `#ffc9c9` | `#e03131` |
| Queue / 队列 | `#fff3bf` | `#f08c00` |
| AI/ML | `#eebefa` | `#9c36b5` |
| Auth / 认证 | `#c3fae8` | `#087f5b` |
| Monitor / 监控 | `#fcc2d7` | `#e64980` |

---

## Features / 功能特性

- **Structure-first analysis** — Parses boxes, arrows, containers before generating JSON
- **Module-by-module generation** — Each component generated separately for accuracy
- **Semantic color assignment** — Auto-colors by keyword (web→blue, db→green, etc.)
- **Hand-drawn sketch style** — Excalifont, hachure fills, variable roughness
- **Layout planning** — Text width estimation and proportion checking before generation
- **Bilingual documentation** — README in English and Chinese

---

## File Structure / 文件结构

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

## License / 许可

MIT
