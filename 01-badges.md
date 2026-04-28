---
title: Badges 徽章完全指南
description: 用 shields.io 打造项目门口的电子门牌，静态徽章、动态徽章、样式选择一文搞定。
tags: [shields.io, badges, 徽章, README]
date: 2026-04-29
---

# Badges 徽章完全指南

> 徽章就是 README 顶部那些小标签——版本号、License、Star 数、构建状态。
> 它们会自动更新，就像你家门口挂了个电子屏。

## 一、什么是 Badges？

打开任何一个正经 GitHub 项目，第一眼看到的通常是这些：

```text
[v1.1.0] [MIT License] [⭐ 42 Stars] [🍴 12 Forks] [Build Passing]
```

这些小标签叫 **Badges**（徽章），由 [shields.io](https://shields.io) 生成。
它们是**动态图片**——仓库数据变了，徽章内容跟着变。

## 二、静态徽章（手动指定内容）

### 2.1 基本语法

```markdown
![描述](https://img.shields.io/badge/标签-内容-颜色)
```

### 2.2 常用静态徽章

```markdown
![Version](https://img.shields.io/badge/version-v1.1.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Python](https://img.shields.io/badge/python-3.10+-yellow)
![Platform](https://img.shields.io/badge/platform-Linux%20|%20macOS-lightgrey)
![Made%20with-Love-red)
![Status](https://img.shields.io/badge/status-active-brightgreen)
```

### 2.3 颜色速查

| 颜色 | 适用场景 |
|------|----------|
| `brightgreen` | 成功、活跃、通过 |
| `green` | 正常、稳定 |
| `yellowgreen` | 测试中 |
| `yellow` | 警告、实验性 |
| `orange` | 有问题 |
| `red` | 错误、停止 |
| `blue` | 信息、版本 |
| `lightgrey` | 中性、平台 |
| `ff69b4` | 粉色（自定义 HEX） |

### 2.4 带链接的徽章

给徽章加个点击跳转：

```markdown
[![Version](https://img.shields.io/badge/version-v1.1.0-blue)](https://github.com/user/repo/releases)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)
```

点击徽章就能跳转到 releases 页面或 LICENSE 文件。

## 三、动态徽章（自动读取仓库数据）

### 3.1 基本语法

```markdown
![描述](https://img.shields.io/github/类型/用户名/仓库名)
```

### 3.2 常用动态徽章

```markdown
<!-- Stars -->
![Stars](https://img.shields.io/github/stars/user/repo?style=social)

<!-- Forks -->
![Forks](https://img.shields.io/github/forks/user/repo?style=social)

<!-- Issues -->
![Issues](https://img.shields.io/github/issues/user/repo)

<!-- Pull Requests -->
![PRs](https://img.shields.io/github/issues-pr/user/repo)

<!-- License -->
![License](https://img.shields.io/github/license/user/repo)

<!-- Last Commit -->
![Last Commit](https://img.shields.io/github/last-commit/user/repo)

<!-- Repo Size -->
![Repo Size](https://img.shields.io/github/repo-size/user/repo)

<!-- Contributors -->
![Contributors](https://img.shields.io/github/contributors/user/repo)

<!-- Watchers -->
![Watchers](https://img.shields.io/github/watchers/user/repo?style=social)

<!-- Release Version -->
![Release](https://img.shields.io/github/v/release/user/repo)

<!-- Tag Version -->
![Tag](https://img.shields.io/github/v/tag/user/repo)
```

### 3.3 自定义参数

```markdown
<!-- 指定分支 -->
![Stars](https://img.shields.io/github/stars/user/repo?style=social&branch=main)

<!-- 显示标签 -->
![Stars](https://img.shields.io/github/stars/user/repo?style=social&label=Star)

<!-- 包含 logo -->
![Build](https://img.shields.io/github/actions/workflow/status/user/repo/ci.yml?logo=github)
```

## 四、样式选择

### 4.1 五种样式对比

| 样式 | 参数 | 适合场景 |
|------|------|----------|
| 扁平 | `?style=flat` | 项目 README（默认） |
| 方角扁平 | `?style=flat-square` | 项目 README（干净） |
| 塑料 | `?style=plastic` | 复古风格 |
| 大号圆角 | `?style=for-the-badge` | 个人主页（张扬） |
| 社交 | `?style=social` | Stars / Forks 专用 |

### 4.2 样式示例

```markdown
<!-- 扁平（默认） -->
![flat](https://img.shields.io/badge/style-flat-blue?style=flat)

<!-- 方角扁平 -->
![flat-square](https://img.shields.io/badge/style-flat--square-blue?style=flat-square)

<!-- 大号圆角 -->
![for-the-badge](https://img.shields.io/badge/style-for--the--badge-blue?style=for-the-badge)

<!-- 社交风格（仅 Stars/Forks/Watchers） -->
![social](https://img.shields.io/github/stars/user/repo?style=social)
```

## 五、组合模板

### 5.1 项目 README 标准组合

```markdown
[![Version](https://img.shields.io/badge/version-v1.1.0-blue?style=flat-square)](releases)
[![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/user/repo?style=social)](https://github.com/user/repo/stargazers)
[![Forks](https://img.shields.io/github/forks/user/repo?style=social)](https://github.com/user/repo/network/members)
[![Issues](https://img.shields.io/github/issues/user/repo)](https://github.com/user/repo/issues)
```

### 5.2 个人主页张扬组合

```markdown
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
```

### 5.3 技术栈带版本

```markdown
![Python](https://img.shields.io/badge/python-3.10+-blue?style=flat-square&logo=python&logoColor=white)
![Node.js](https://img.shields.io/badge/node.js-18+-green?style=flat-square&logo=node.js&logoColor=white)
![Docker](https://img.shields.io/badge/docker-24+-blue?style=flat-square&logo=docker&logoColor=white)
```

## 六、OpenClaw 一键生成

在 OpenClaw 中，你不需要手写这些链接。直接说：

```json
"给 README 加上版本、License、Stars 徽章"
```

OpenClaw 会自动：
1. 读取 `config.json` 中的版本号
2. 检测 LICENSE 文件类型
3. 获取仓库的用户名和仓库名
4. 生成对应的 shields.io 链接
5. 写入 README.md
6. 提交并推送

## 七、常见问题

| 问题 | 原因 | 解决 |
|------|------|------|
| 徽章显示 404 | 仓库名 / 用户名拼错 | 检查 URL 中的路径 |
| 徽章不更新 | 浏览器缓存 | 强制刷新（Ctrl+F5） |
| 动态徽章数据不准 | shields.io 缓存 | 等几分钟自动刷新 |
| 中文乱码 | URL 编码问题 | 用英文或 `%E4%B8%AD%E6%96%87` 编码 |
| 社交样式无效 | 只支持 Stars/Forks/Watchers | 其他类型用 flat |
