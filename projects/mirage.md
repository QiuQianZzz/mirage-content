---
name: Mirage
description: 这个网站本身。基于 Flutter 与 Material Design 3 的静态个人站，内容用 Markdown 管理。
tags: [flutter, dart, web]
repo: https://github.com/QiuQianZzz/mirage
date: 2026-01-01
featured: true
---

做这个站的思路很直接：想要一个自己说了算、能持续更新的地盘，同时页面看着舒服。

## 做得比较顺心的地方

- **深浅主题切换**：切换时从点击处向外扩散一圈，旧画面被"推开"，比瞬间换色多一点手感。
- **动态背景**：一层淡淡的网格 + 跟着鼠标走的光晕，纯装饰，不挡内容。
- **内容全走 Markdown**：文章、项目、技能都是 `.md` 文件，配上 YAML 头写标题日期标签。想改什么直接改文件，跟着 Git 走。
- **内容用子模块管理**：内容单独放一个 git 仓库挂进来，想换平台带目录走就行。

## 技术栈

- Flutter（Web）
- go_router 路由
- flutter_markdown 渲染正文

站内那篇《这个站是怎么搭起来的》写得更细，包括踩的坑。