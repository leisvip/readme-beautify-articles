---
title: 统计卡片全攻略
description: GitHub 统计卡、Top 语言、连续贡献、成就奖杯，让你的 README 会说话。
tags: [GitHub, 统计, stats, streak, trophy]
date: 2026-04-29
---

# 统计卡片全攻略

> 一张卡片胜过千言万语。让数据替你说话。

## 一、GitHub Readme Stats — 你的成绩单

### 1.1 这是什么？

一张自动生成的卡片，展示你的 GitHub 数据：
总提交数、总 Star、总 Fork、总 PR、总 Issue、贡献仓库数。

**免费，无需注册，任何人可用。**

### 1.2 基础用法

```markdown
![Stats](https://github-readme-stats.vercel.app/api?username=你的用户名&show_icons=true&theme=radical)
```

### 1.3 常用参数

| 参数 | 说明 | 示例 |
|------|------|------|
| `username` | GitHub 用户名 | `username=leisvip` |
| `show_icons` | 显示图标 | `show_icons=true` |
| `theme` | 主题颜色 | `theme=radical` |
| `hide_border` | 隐藏边框 | `hide_border=true` |
| `include_all_commits` | 包含所有提交 | `include_all_commits=true` |
| `count_private` | 包含私有仓库 | `count_private=true` |
| `hide` | 隐藏指定字段 | `hide=stars,commits,prs` |
| `show` | 只显示指定字段 | `show=reviews,issues` |
| `card_width` | 卡片宽度 | `card_width=400` |

### 1.4 可选主题

```markdown
<!-- 赛博朋克 -->
![Stats](https://github-readme-stats.vercel.app/api?username=user&theme=radical)

<!-- 东京夜 -->
![Stats](https://github-readme-stats.vercel.app/api?username=user&theme=tokyonight)

<!-- 吸血鬼 -->
![Stats](https://github-readme-stats.vercel.app/api?username=user&theme=dracula)

<!-- 北欧冷淡 -->
![Stats](https://github-readme-stats.vercel.app/api?username=user&theme=nord)

<!-- 复古暖色 -->
![Stats](https://github-readme-stats.vercel.app/api?username=user&theme=gruvbox)

<!-- 暗黑 -->
![Stats](https://github-readme-stats.vercel.app/api?username=user&theme=dark)

<!-- Vue 风格 -->
![Stats](https://github-readme-stats.vercel.app/api?username=user&theme=vue)
```

### 1.5 隐藏和显示字段

```markdown
<!-- 隐藏特定字段 -->
![Stats](https://github-readme-stats.vercel.app/api?username=user&hide=stars,commits,prs,issues)

<!-- 只显示特定字段 -->
![Stats](https://github-readme-stats.vercel.app/api?username=user&show=reviews,discussions_started,discussions_answered)
```

## 二、Top Languages — 你会什么？

### 2.1 基础用法

```markdown
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=你的用户名&layout=compact)
```

### 2.2 四种布局

```markdown
<!-- 紧凑布局（默认） -->
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=user&layout=compact)

<!-- 甜甜圈图 -->
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=user&layout=donut)

<!-- 纵向甜甜圈 -->
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=user&layout=donut-vertical)

<!-- 饼图 -->
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=user&layout=pie)
```

### 2.3 高级参数

```markdown
<!-- 排除指定仓库 -->
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=user&exclude_repo=repo1,repo2)

<!-- 隐藏指定语言 -->
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=user&hide=html,css)

<!-- 显示更多语言（默认 5 个） -->
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=user&langs_count=8)

<!-- 隐藏进度条 -->
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=user&hide_progress=true)
```

## 三、Streak Stats — 连续贡献天数

### 3.1 这是什么？

显示你连续多少天都在提交代码。火焰图标 + 天数，激励自己别断更。

### 3.2 基础用法

```markdown
![Streak](https://github-readme-streak-stats.vercel.app/?user=你的用户名&theme=radical)
```

### 3.3 常用参数

| 参数 | 说明 | 示例 |
|------|------|------|
| `user` | 用户名 | `user=leisvip` |
| `theme` | 主题 | `theme=radical` |
| `hide_border` | 隐藏边框 | `hide_border=true` |
| `type` | 显示类型 | `type=png`（默认 svg） |
| `locale` | 语言 | `locale=zh` |

### 3.4 主题

与 Readme Stats 共享主题库：`radical`、`tokyonight`、`dracula`、`nord`、`gruvbox`、`dark` 等。

## 四、Profile Trophy — 成就奖杯

### 4.1 这是什么？

一排小奖杯图标，展示你的 GitHub 成就。Star 达标有奖杯，PR 合并达标有奖杯，Issue 关闭达标也有。

### 4.2 基础用法

```markdown
![Trophy](https://github-profile-trophy.vercel.app/?username=你的用户名&theme=radical&no-frame=true&column=7)
```

### 4.3 常用参数

| 参数 | 说明 | 示例 |
|------|------|------|
| `username` | 用户名 | `username=leisvip` |
| `theme` | 主题 | `theme=radical` |
| `no-frame` | 隐藏边框 | `no-frame=true` |
| `column` | 每行显示数量 | `column=7` |
| `row` | 行数 | `row=2` |
| `margin-w` | 水平间距 | `margin-w=20` |
| `margin-h` | 垂直间距 | `margin-h=20` |

### 4.4 指定奖杯类型

```markdown
<!-- 只显示特定奖杯 -->
![Trophy](https://github-profile-trophy.vercel.app/?username=user&theme=radical&no-frame=true&title=Stars,Followers,Commits,PRs,Issues,Repositories)
```

## 五、Activity Graph — 贡献活动图

### 5.1 这是什么？

一条折线图，展示你过去一年的贡献活动趋势。

### 5.2 基础用法

```markdown
![Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=你的用户名&theme=redical)
```

### 5.3 常用参数

| 参数 | 说明 | 示例 |
|------|------|------|
| `username` | 用户名 | `username=leisvip` |
| `theme` | 主题 | `theme=redical` |
| `hide_border` | 隐藏边框 | `hide_border=true` |
| `area` | 填充区域 | `area=true` |
| `color` | 线条颜色 | `color=58A6FF` |
| `line` | 线条颜色 | `line=58A6FF` |
| `point` | 圆点颜色 | `point=58A6FF` |

## 六、并排显示技巧

### 6.1 统计卡 + 语言卡并排

```markdown
<div>
  <img src="https://github-readme-stats.vercel.app/api?username=user&show_icons=true&theme=radical" width="49%">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=user&layout=compact&theme=radical" width="49%">
</div>
```

### 6.2 三列并排

```markdown
<table>
  <tr>
    <td><img src="统计卡URL" width="100%"></td>
    <td><img src="语言卡URL" width="100%"></td>
    <td><img src="活动图URL" width="100%"></td>
  </tr>
</table>
```

## 七、OpenClaw 一键生成

在 OpenClaw 中，你不需要手写这些 URL。直接说：

```json
"给 README 加上统计卡、语言卡、连续贡献、成就奖杯，用 tokyonight 主题"
```

OpenClaw 会自动：
1. 获取你的 GitHub 用户名
2. 生成所有组件的 URL
3. 用 HTML 表格布局
4. 写入 README.md
5. 提交并推送

## 八、常见问题

| 问题 | 原因 | 解决 |
|------|------|------|
| 卡片显示空白 | 用户名错误 | 检查 `username` 参数 |
| 统计数据不准 | 只统计公开仓库 | 加 `count_private=true` |
| 主题颜色不对 | 缓存问题 | 等几分钟刷新 |
| 语言占比偏差 | 只统计代码文件 | 正常现象 |
| 奖杯不显示 | 用户没有公开仓库 | 至少创建一个公开仓库 |
