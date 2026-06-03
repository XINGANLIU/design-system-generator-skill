<div align="center">

# 🎨 设计系统生成器

**一个颜色输入 → 完整设计系统输出**

一个 AI Agent Skill，从一个品牌色自动生成完整的、可投产的设计系统。
支持 **Antigravity** · **Claude Code** · **Cursor** · **Codex** · **Trae** 等所有主流 AI 编码助手。

[![License: Apache 2.0](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
[![Agent Skills](https://img.shields.io/badge/Agent%20Skills-Open%20Standard-8b5cf6)](https://agentskills.io)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

[English](README.md) · [中文](README_CN.md)

</div>

---

## ✨ 功能特色

| 特性 | 说明 |
|------|------|
| 🎯 **一色生成** | 只需提供一个 hex 颜色 — 所有其他内容自动推导 |
| 🌈 **OKLCH 色彩系统** | 感知均匀的调色板，10 级色阶 + 语义色 |
| 📐 **W3C 标准** | 输出遵循 W3C Design Tokens 规范（`$value`/`$type` 格式） |
| 🌗 **明暗双主题** | 通过 `light-dark()` + `[data-theme]` 自动支持亮/暗主题 |
| 🧩 **11 个组件** | 按钮、卡片、输入框、徽章、提示、头像、骨架屏、提示框、模态框、导航栏、分割线 |
| ♿ **WCAG 2.2 AA** | 所有颜色组合通过无障碍对比度验证 |
| 🖥️ **实时预览** | 自包含 HTML 预览页，可视化整个设计系统 |
| 🔌 **多平台适配** | 适配 Antigravity、Claude Code、Cursor、Codex、Trae 等 |
| 0️⃣ **零依赖** | 纯 CSS 自定义属性 — 无需预处理器或框架 |

---

## 🚀 快速上手

### 1. 安装

**Antigravity / Gemini CLI：**

```bash
git clone https://github.com/XINGANLIU/design-system-generator-skill.git
cp -r design-system-generator-skill ~/.gemini/config/plugins/design-system-generator
```

**Claude Code：**

```bash
git clone https://github.com/XINGANLIU/design-system-generator-skill.git .design-system-generator
# 然后使用 /design-system 命令
```

**Cursor：**

```bash
# 克隆到项目根目录，.cursorrules 会自动被检测
git clone https://github.com/XINGANLIU/design-system-generator-skill.git .
```

**Codex / 其他 Agent：**

```bash
git clone https://github.com/XINGANLIU/design-system-generator-skill.git
# 引用 AGENTS.md 或 skills/design-system-generator/SKILL.md
```

### 2. 使用

告诉你的 AI 助手：

```
帮我用 #6366f1 作为主色生成一个设计系统
```

或者更详细：

```
创建一个以珊瑚色 (#f97316) 为主色的设计系统，使用 Outfit 字体，胶囊形按钮
```

### 3. 获取结果

Agent 会在你的项目中生成这些文件：

```
design-system/
├── tokens.json       # W3C Design Tokens（机器可读）
├── tokens.css        # CSS 自定义属性（在项目中导入这个！）
├── components.css    # 即用的组件样式
└── preview.html      # 在浏览器中打开预览
```

### 4. 在项目中使用

```html
<head>
  <link rel="stylesheet" href="design-system/tokens.css">
  <link rel="stylesheet" href="design-system/components.css">
</head>
<body>
  <button class="btn btn--primary">开始使用</button>
</body>
```

---

## 🏗️ 工作原理

Skill 采用结构化的 5 阶段工作流：

| 阶段 | 内容 |
|------|------|
| **1. 品牌输入** | 收集品牌色、字体、圆角风格、密度偏好 |
| **2. 调色板生成** | 基于 OKLCH 算法生成：主色（10 级）、中性色（10 级）、语义色（4 色 × 5 变体） |
| **3. Token 架构** | 输出 W3C Design Tokens JSON + CSS 自定义属性 + 明暗主题语义映射 |
| **4. 组件样式** | 生成 11 个组件，含变体、状态、动画、无障碍支持 |
| **5. 预览交付** | 创建可视化预览 HTML 页面，带主题切换 |

---

## 🔌 多平台兼容

| Agent | 适配文件 | 工作方式 |
|-------|---------|---------|
| **Antigravity** | `plugin.json` + `skills/` | 原生插件 — 自动检测 |
| **Claude Code** | `.claude/commands/design-system.md` | 使用 `/design-system` 命令 |
| **Cursor** | `.cursorrules` | 自动加载为项目规则 |
| **Codex** | `AGENTS.md` | 自动加载为 Agent 指令 |
| **Trae** | `.trae/rules/design-system.md` | 自动加载为项目规则 |
| **其他** | `skills/.../SKILL.md` | 直接引用 SKILL.md |

---

## 🤝 贡献

欢迎贡献！你可以：

- 🎨 添加新的组件模式
- 🌍 添加新的示例主题
- 🔧 改进 OKLCH 调色算法
- 📝 完善文档和翻译
- 🐛 报告问题或提出建议

---

## 📄 许可

[Apache 2.0](LICENSE) — 作者 [XINGANLIU](https://github.com/XINGANLIU)

---

<div align="center">

**一个颜色输入 → 完整设计系统输出** 🎨

如果这个 Skill 对你有帮助，请在 GitHub 上给个 ⭐！

</div>
