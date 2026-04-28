---
title: 布局与排版技巧
description: 居中、并排、折叠块、分隔线、响应式，让 README 排版专业又好看。
tags: [布局, 排版, HTML, Markdown, README]
date: 2026-04-29
---

# 布局与排版技巧

> 内容再好，堆成一坨也没人看。排版是 README 的骨架。

## 一、居中对齐

### 1.1 整体居中

用 `<div align="center">` 包裹整个区域：

```markdown
<div align="center">

# 🚀 项目名称

**一句话描述**

[![Version](https://img.shields.io/badge/version-v1.0.0-blue)](releases)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)

</div>
```

### 1.2 单行居中

```markdown
<p align="center">这行文字居中显示</p>
```

### 1.3 图片居中

```markdown
<p align="center">
  <img src="图片URL" width="400">
</p>
```

## 二、图片并排

### 2.1 两列并排（各占 50%）

```markdown
<div>
  <img src="图1URL" width="49%">
  <img src="图2URL" width="49%">
</div>
```

### 2.2 三列并排

```markdown
<div>
  <img src="图1URL" width="32%">
  <img src="图2URL" width="32%">
  <img src="图3URL" width="32%">
</div>
```

### 2.3 用 HTML 表格（更精确控制）

```markdown
<table>
  <tr>
    <td><img src="图1URL" width="100%"></td>
    <td><img src="图2URL" width="100%"></td>
  </tr>
</table>
```

### 2.4 带标题的图片网格

```markdown
<table>
  <tr>
    <td align="center"><img src="图1URL" width="300"><br>功能一</td>
    <td align="center"><img src="图2URL" width="300"><br>功能二</td>
    <td align="center"><img src="图3URL" width="300"><br>功能三</td>
  </tr>
</table>
```

## 三、折叠块

### 3.1 基础折叠

```markdown
<details>
<summary>点击展开详情</summary>

这里是折叠的内容...

可以是任何 Markdown：文字、代码、表格、图片。

</details>
```

### 3.2 默认展开

```markdown
<details open>
<summary>默认展开的内容</summary>

内容...

</details>
```

### 3.3 嵌套折叠

```markdown
<details>
<summary>外层折叠</summary>

<details>
<summary>内层折叠</summary>

嵌套内容...

</details>

</details>
```

### 3.4 实用场景

```markdown
<details>
<summary>📖 完整命令列表（点击展开）</summary>

| 命令 | 说明 |
|------|------|
| `cmd1` | 说明一 |
| `cmd2` | 说明二 |

</details>
```

## 四、分隔线

### 4.1 标准分隔线

```markdown
---
```

### 4.2 装饰性分隔线

```markdown
<!-- 波浪形分隔线 -->
<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=100&section=footer">

<!-- 纯色分隔线 -->
<img width="100%" src="https://capsule-render.vercel.app?type=rect&color=0:FF6B6B,100:4ECDC4&height=20&section=footer">
```

### 4.3 带文字的分隔线

```markdown
<div align="center">

---

**⭐ 如果觉得有用，请给个 Star！⭐**

---

</div>
```

## 五、响应式设计

### 5.1 移动端友好的图片

```markdown
<img src="图片URL" width="100%" alt="描述">
```

设置 `width="100%"` 让图片自适应屏幕宽度。

### 5.2 响应式表格

表格在移动端容易溢出。解决方案：

```markdown
<details>
<summary>📊 完整配置表（点击展开）</summary>

| 配置项 | 值 | 说明 |
|--------|-----|------|
| ... | ... | ... |

</details>
```

用折叠块包裹大表格，移动端不会溢出。

## 六、Emoji 使用

### 6.1 标题 Emoji

每个章节标题加一个 Emoji，增加辨识度：

```markdown
## ✨ 功能特性
## 🚀 快速开始
## 📁 项目结构
## 📖 文档
## 📄 License
```

### 6.2 常用标题 Emoji

| Emoji | 含义 | 适用场景 |
|-------|------|----------|
| 🚀 | 火箭 | 快速开始、部署 |
| ✨ | 星星 | 功能特性 |
| 📁 | 文件夹 | 项目结构 |
| 📖 | 书 | 文档 |
| 📋 | 剪贴板 | 命令速查 |
| ⚙️ | 齿轮 | 配置 |
| 🔧 | 扳手 | 安装、工具 |
| 📊 | 图表 | 统计数据 |
| 📈 | 上升趋势 | 增长、趋势 |
| 🐛 | 虫子 | Bug、问题 |
| 💡 | 灯泡 | 提示、建议 |
| ⚠️ | 警告 | 注意事项 |
| 📄 | 文档 | License |
| 🎯 | 靶心 | 目标、定位 |
| 🔥 | 火 | 热门、重要 |
| 💬 | 对话气泡 | 讨论、反馈 |
| 🏆 | 奖杯 | 成就、致谢 |

### 6.3 注意事项

- 标题最多 1 个 Emoji，放在开头
- 正文少量点缀，不要堆砌
- 代码块内不要用 Emoji（会影响代码复制）

## 七、表格技巧

### 7.1 对齐方式

```markdown
| 左对齐 | 居中 | 右对齐 |
|:-------|:----:|-------:|
| 内容 | 内容 | 内容 |
```

### 7.2 表格内换行

```markdown
| 功能 | 说明 |
|------|------|
| 功能一 | 这是很长的说明，<br>需要换行 |
```

用 `<br>` 实现表格内换行。

### 7.3 表格内代码

```markdown
| 命令 | 说明 |
|------|------|
| `npm install` | 安装依赖 |
| `npm start` | 启动项目 |
```

## 八、链接技巧

### 8.1 锚点跳转

```markdown
<!-- 目录 -->
[快速开始](#-快速开始)
[功能特性](#-功能特性)

<!-- 章节 -->
## 🚀 快速开始
## ✨ 功能特性
```

注意：中文标题的锚点需要加 `-` 连接，Emoji 用 URL 编码。

### 8.2 外部链接

```markdown
[GitHub](https://github.com)
```

### 8.3 文件链接

```markdown
[查看配置](config.json)
[开发手册](dev-guide/README.md)
```

### 8.4 链接带标题（hover 提示）

```markdown
[GitHub](https://github.com "点击访问 GitHub")
```

## 九、完整布局模板

```markdown
<div align="center">

<!-- 头部装饰 -->
<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=200&section=header">

<!-- 打字动画 -->
[![Typing SVG](https://readme-typing-svg.demolab.com/?lines=🚀+项目名称;一句话描述&center=true&size=27)](https://git.io/typing-svg)

<!-- Badges -->
[![Version](https://img.shields.io/badge/version-v1.0.0-blue?style=flat-square)](releases)
[![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/user/repo?style=social)](https://github.com/user/repo/stargazers)

<!-- 导航 -->
[快速开始](#-快速开始) · [功能](#-功能) · [文档](#-文档)

</div>

---

## ✨ 功能特性

| 特性 | 说明 |
|------|------|
| 🎯 特性一 | 描述 |
| 📊 特性二 | 描述 |

## 🚀 快速开始

\```bash
安装命令
\```

## 📊 统计

<div>
  <img src="统计卡URL" width="49%">
  <img src="语言卡URL" width="49%">
</div>

## 📈 Star History

[![Star History Chart](https://api.star-history.com/svg?repos=user/repo&type=Timeline)](https://star-history.com/#user/repo&Timeline)

## 📄 License

[MIT](LICENSE)

---

<!-- 底部装饰 -->
<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=100&section=footer">
```

## 十、OpenClaw 一键排版

在 OpenClaw 中直接说：

```json
"标题居中，徽章也居中"
```

```json
"统计卡和语言卡并排显示"
```

```json
"把开发手册放到折叠块里"
```

```json
"加个波浪形的分隔线"
```

OpenClaw 会自动生成对应的 HTML / Markdown 代码，写入文件，提交推送。

## 十一、常见问题

| 问题 | 原因 | 解决 |
|------|------|------|
| 居中不生效 | 缺少 `<div align="center">` | 用 HTML 标签包裹 |
| 图片不并排 | 总宽度超过 100% | 调整 `width` 百分比 |
| 折叠块不工作 | `<details>` 标签未闭合 | 检查 `</details>` 是否存在 |
| 分隔线不显示 | 前后没有空行 | 分隔线前后各加一行空行 |
| 表格渲染异常 | 缺少分隔行 | 确保有 `\|---\|---\|` |
| Emoji 不显示 | 平台不支持 | 用 Unicode Emoji |
