---
title: 动态特效与动画
description: 打字动画、头部装饰图、贪吃蛇贡献图，让你的 README 动起来。
tags: [动画, typing SVG, capsule render, snake, README]
date: 2026-04-29
---

# 动态特效与动画

> 静态的 README 千篇一律，会动的 README 万里挑一。

## 一、Typing SVG — 打字动画

### 1.1 这是什么？

README 开头的标题会像终端一样逐字「打」出来，光标还在闪。

```markdown
> 赛博牛马日报_
```

### 1.2 基础用法

```markdown
[![Typing SVG](https://readme-typing-svg.demolab.com/?lines=赛博牛马日报;完成任务自动打卡，说声「日报」就出报告)](https://git.io/typing-svg)
```

### 1.3 常用参数

| 参数 | 说明 | 示例 |
|------|------|------|
| `lines` | 多行文字（用 `;` 分隔） | `lines=第一行;第二行` |
| `size` | 字号 | `size=27` |
| `color` | 文字颜色 | `color=36BCF7` |
| `center` | 居中 | `center=true` |
| `pause` | 每行暂停毫秒 | `pause=1000` |
| `font` | 字体 | `font=JetBrains+Mono` |
| `weight` | 字重 | `weight=700` |
| `width` | 宽度 | `width=435` |
| `height` | 高度 | `height=50` |
| `vCenter` | 垂直居中 | `vCenter=true` |
| `repeat` | 循环播放 | `repeat=true` |

### 1.4 居中大标题

```markdown
<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com/?lines=🚀+赛博牛马日报;完成任务自动打卡;说声「日报」就出报告&center=true&size=30&color=36BCF7)](https://git.io/typing-svg)

</div>
```

### 1.5 常用颜色

| 颜色 | HEX | 风格 |
|------|-----|------|
| 蓝色 | `36BCF7` | 科技感 |
| 绿色 | `37D67A` | 生态 / 成功 |
| 紫色 | `9C27B0` | 神秘感 |
| 橙色 | `FF9800` | 活力 |
| 红色 | `F44336` | 警示 |
| 白色 | `FFFFFF` | 干净 |

## 二、Capsule Render — 头部装饰图

### 2.1 这是什么？

README 顶部或底部的装饰性图片，可以是波浪形、蛇形、矩形等。
通常用作 Header 或 Footer 的视觉分隔。

### 2.2 基础用法

```markdown
<!-- 顶部波浪 -->
![Header](https://capsule-render.vercel.app/api?type=waving&color=gradient&height=300&section=header&text=赛博牛马日报&fontSize=30&fontColor=ffffff)
```

### 2.3 类型选择

| 类型 | 参数 | 效果 |
|------|------|------|
| 波浪 | `type=waving` | 随风飘动的波浪 |
| 蛇形 | `type=snake` | 蛇形曲线 |
| 柔和 | `type=soft` | 柔和渐变 |
| 矩形 | `type=rect` | 简洁矩形 |
| 自动 | `type=auto` | 随机选择 |

### 2.4 颜色方案

```markdown
<!-- 渐变色 -->
![Header](https://capsule-render.vercel.app/api?type=waving&color=gradient&height=300)

<!-- 自定义颜色 -->
![Header](https://capsule-render.vercel.app/api?type=waving&color=0:FF6B6B,100:4ECDC4&height=300)

<!-- 指定颜色 -->
![Header](https://capsule-render.vercel.app/api?type=waving&color=A855F7&height=300)
```

### 2.5 常用场景

```markdown
<!-- 顶部标题区 -->
![Header](https://capsule-render.vercel.app/api?type=waving&color=gradient&height=300&section=header&text=项目名称&fontSize=30&fontColor=ffffff)

<!-- 底部分隔线 -->
![Footer](https://capsule-render.vercel.app/api?type=waving&color=gradient&height=100&section=footer)
```

## 三、Snake Animation — 贪吃蛇贡献图

### 3.1 这是什么？

一个动画，用「贪吃蛇」的方式展示你的 GitHub 贡献图。
蛇走过的地方就是你提交过代码的日期。

### 3.2 使用方法

需要 GitHub Actions 自动生成 SVG，然后在 README 中引用。

**步骤 1：创建 GitHub Actions 工作流**

在仓库中创建 `.github/workflows/snake.yml`：

```yaml
name: Generate Snake
on:
  schedule:
    - cron: "0 */12 * * *"
  workflow_dispatch:
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: Platane/snk@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: dist/github-snake.svg
      - uses: crazy-max/ghaction-github-pages@v3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

**步骤 2：在 README 中引用**

```markdown
![Snake](https://raw.githubusercontent.com/用户名/仓库名/output/github-snake.svg)
```

### 3.3 参数说明

| 参数 | 说明 | 示例 |
|------|------|------|
| `outputs` | 输出格式 | `dist/github-snake.svg` |
| `github_user_name` | 用户名 | `${{ github.repository_owner }}` |

支持输出格式：`.svg`、`.gif`、`.json`

## 四、组合使用

### 4.1 Header + 打字动画

```markdown
<div align="center">

![Header](https://capsule-render.vercel.app/api?type=waving&color=gradient&height=200&section=header)

[![Typing SVG](https://readme-typing-svg.demolab.com/?lines=🚀+项目名称;一句话描述&center=true&size=27)](https://git.io/typing-svg)

</div>
```

### 4.2 完整页面结构

```markdown
<div align="center">

<!-- 头部装饰 -->
![Header](https://capsule-render.vercel.app/api?type=waving&color=gradient&height=200&section=header)

<!-- 打字动画标题 -->
[![Typing SVG](https://readme-typing-svg.demolab.com/?lines=🚀+赛博牛马日报;完成任务自动打卡&center=true&size=27)](https://git.io/typing-svg)

<!-- Badges -->
[![Version](https://img.shields.io/badge/version-v1.1.0-blue)](releases)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)

</div>

---

<!-- 正文内容 -->

## ✨ 功能特性

...

---

<!-- 底部装饰 -->
![Footer](https://capsule-render.vercel.app/api?type=waving&color=gradient&height=100&section=footer)
```

## 五、性能注意事项

| 特效 | 加载时间 | 建议 |
|------|----------|------|
| Typing SVG | 快 | 可以用 |
| Capsule Render | 快 | 可以用 |
| Snake SVG | 中等 | 建议用 SVG 而非 GIF |
| GIF 动画 | 慢 | 控制文件大小 |

**总原则：** README 中的图片总数控制在 10 张以内，避免加载过慢。

## 六、OpenClaw 一键生成

在 OpenClaw 中直接说：

```json
"README 开头加个打字动画，内容是项目名和一句话介绍"
```

```json
"加个波浪形的头部装饰"
```

```json
"加贪吃蛇贡献图"
```

OpenClaw 会自动创建 GitHub Actions 工作流、生成 SVG 链接、写入 README、提交推送。

## 七、常见问题

| 问题 | 原因 | 解决 |
|------|------|------|
| 打字动画不显示 | URL 编码问题 | 用英文或正确编码中文 |
| 波浪图不加载 | 服务暂时不可用 | 等几分钟重试 |
| 贡献图空白 | 没有公开贡献 | 正常，等有提交后自动出现 |
| GIF 太大 | 帧数太多 | 改用 SVG 格式 |
| Actions 未运行 | 未启用 Actions | 在仓库 Settings → Actions 中启用 |
