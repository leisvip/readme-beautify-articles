---
title: Star History 趋势图
description: 用 Star History 展示项目成长轨迹，单仓库曲线、多仓库对比、Repobeats 脉搏。
tags: [Star History, 趋势图, GitHub, Repobeats]
date: 2026-04-29
---

# Star History 趋势图

> 项目火不火，一张图说了算。

## 一、什么是 Star History？

Star History 是一张折线图，展示仓库从创建到现在 Star 数的变化趋势。

- 线越陡 → Star 涨得越快 → 项目越火
- 线平了 → 增长放缓
- 线突然翘起来 → 某次推广 / 上了热搜

**图表实时更新**，不需要你手动维护。Star 涨了，图自动变。

## 二、单仓库趋势图

### 2.1 基础用法

```markdown
[![Star History Chart](https://api.star-history.com/svg?repos=用户名/仓库名&type=Timeline)](https://star-history.com/#用户名/仓库名&Timeline)
```

点击图表可以跳转到 star-history.com 查看交互式版本。

### 2.2 完整示例

```markdown
## 📈 Star History

[![Star History Chart](https://api.star-history.com/svg?repos=leisvip/daily-report&type=Timeline)](https://star-history.com/#leisvip/daily-report&Timeline)
```

### 2.3 图表类型

| 类型 | 参数 | 说明 |
|------|------|------|
| 时间线 | `type=Timeline` | 按时间展示 Star 增长（最常用） |
| 日期 | `type=Date` | 按日期展示 |

## 三、多仓库对比

### 3.1 基础用法

多个仓库名用逗号分隔：

```markdown
[![Star History](https://api.star-history.com/svg?repos=user/repo1,user/repo2&type=Timeline)](https://star-history.com/#user/repo1,user/repo2&Timeline)
```

### 3.2 实际场景

```markdown
<!-- 对比自己的两个项目 -->
[![Star History](https://api.star-history.com/svg?repos=leisvip/daily-report,leisvip/another-project&type=Timeline)](https://star-history.com/#leisvip/daily-report,leisvip/another-project&Timeline)

<!-- 对比同类项目 -->
[![Star History](https://api.star-history.com/svg?repos=user/repo,competitor/repo&type=Timeline)](https://star-history.com/#user/repo,competitor/repo&Timeline)
```

## 四、Repobeats — 仓库活动脉搏

### 4.1 这是什么？

一张自动生成的图表，展示仓库的活动指标：
提交频率、PR 数量、Issue 数量、代码变更量。

### 4.2 使用方法

1. 访问 [repobeats.axiom.co](https://repobeats.axiom.co)
2. 输入你的仓库 URL
3. 复制生成的 Markdown 代码
4. 粘贴到 README.md

```markdown
![Repobeats](https://repobeats.axiom.co/api/embed/仓库ID.svg)
```

### 4.3 与 Star History 的区别

| 维度 | Star History | Repobeats |
|------|-------------|-----------|
| 展示内容 | Star 增长曲线 | 提交 / PR / Issue 活动 |
| 更新频率 | 实时 | 每日 |
| 适合场景 | 项目受欢迎程度 | 项目活跃度 |
| 需要配置 | 否 | 需要获取仓库 ID |

## 五、放在 README 的哪个位置？

### 5.1 推荐位置

**项目 README**：放在 License 之前，作为最后一个章节。

```markdown
## 📈 Star History

[![Star History Chart](https://api.star-history.com/svg?repos=user/repo&type=Timeline)](https://star-history.com/#user/repo&Timeline)

## 📄 License

[MIT](LICENSE)
```

### 5.2 居中显示

```markdown
<div align="center">

## 📈 Star History

[![Star History Chart](https://api.star-history.com/svg?repos=user/repo&type=Timeline)](https://star-history.com/#user/repo&Timeline)

</div>
```

## 六、前提条件

| 条件 | 说明 |
|------|------|
| 仓库必须公开 | 私有仓库无法生成图表 |
| 至少 1 个 Star | 0 Star 的仓库图表为空 |
| 仓库存在超过 1 天 | 新仓库数据太少，曲线不明显 |

## 七、OpenClaw 一键生成

在 OpenClaw 中直接说：

```json
"加一个 Star History 趋势图"
```

OpenClaw 会自动：
1. 获取仓库的用户名和仓库名
2. 生成 Star History SVG 链接
3. 嵌入 README.md 底部
4. 提交并推送

多仓库对比：

```json
"对比 repo1 和 repo2 的 Star 趋势"
```

## 八、常见问题

| 问题 | 原因 | 解决 |
|------|------|------|
| 图表为空 | 仓库 0 Star | 先给自己点个 Star |
| 图表不更新 | star-history 缓存 | 等几小时自动刷新 |
| 对比图太挤 | 仓库太多 | 控制在 3 个以内 |
| 图表加载慢 | SVG 太大 | 正常现象，首次加载较慢 |
| 私有仓库不显示 | API 无法访问 | 只支持公开仓库 |
