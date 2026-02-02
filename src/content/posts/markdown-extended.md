---
title: Markdown 扩展特性
published: 2024-05-01
updated: 2024-11-29
description: '阅读更多关于 Mizuki 中 Markdown 特性的信息'
image: ''
tags: [演示, 示例, Markdown, mizuki]
category: '示例'
draft: false 
---

## GitHub 仓库卡片
你可以添加链接到 GitHub 仓库的动态卡片。在页面加载时，仓库信息会从 GitHub API 获取。

::github{repo="matsuzaka-yuki/Mizuki"}

使用代码 `::github{repo="matsuzaka-yuki/Mizuki"}` 创建 GitHub 仓库卡片。

```markdown
::github{repo="matsuzaka-yuki/Mizuki"}
```

## 提示框 (Admonitions)

支持以下类型的提示框：`note` (备注)、`tip` (提示)、`important` (重要)、`warning` (警告)、`caution` (小心)

:::note
突出显示用户即使在浏览时也应考虑的信息。
:::

:::tip
帮助用户更成功的可选信息。
:::

:::important
用户成功所需的关键信息。
:::

:::warning
由于潜在风险，需要用户立即注意的关键内容。
:::

:::caution
操作可能产生的负面后果。
:::

### 基本语法

```markdown
:::note
突出显示用户即使在浏览时也应考虑的信息。
:::

:::tip
帮助用户更成功的可选信息。
:::
```

### 自定义标题

提示框的标题可以自定义。

:::note[我的自定义标题]
这是一个带有自定义标题的备注。
:::

```markdown
:::note[我的自定义标题]
这是一个带有自定义标题的备注。
:::
```

### GitHub 语法

> [!TIP]
> 也支持 [GitHub 语法](https://github.com/orgs/community/discussions/16925)。

```
> [!NOTE]
> 也支持 GitHub 语法。

> [!TIP]
> 也支持 GitHub 语法。
```

### 剧透 (Spoiler)

你可以在文本中添加剧透内容。剧透文本也支持 **Markdown** 语法。

内容 :spoiler[被隐藏了 **哎呀**]！

```markdown
内容 :spoiler[被隐藏了 **哎呀**]！
```
