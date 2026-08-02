---
name: Imagic
description: 基于 Flutter 的 Windows 桌面图片查看器，走 Material Design 3 视觉，全套组件自绘、没有 UI 组件库。
tags: [flutter, dart, windows]
repo: https://github.com/QiuQianZzz/imagic
date: 2026-05-20
featured: false
---

一个 Windows 桌面图片查看器，用 Flutter 写的，UI 全用 MD3 风格的原生组件自己拼，没引入组件库。

## 主要功能

- 支持 JPEG / PNG / GIF / WebP / BMP / TGA / SVG 等常见格式
- PNG 直接走引擎 C++ 解码，其余格式丢到 Isolate 里解码重编码成 PNG，避免切图卡 UI
- 滚轮缩放以光标为中心，200ms easeOutCubic 个缓动，平移直接透传
- 一套种子色生成完整 ColorScheme，系统 / 浅色 / 深色 + 12 套预设色和自定义色相
- 10 个可自定义快捷键（打开关闭、适应窗口、放大缩小、上下张、全屏…），支持组合键和冲突检测
- 自绘标题栏，可选 Windows / macOS 风格窗口控件
- 拖文件进来就打开，能自动加载同目录的相邻图片
- 启动时查 GitHub Releases，带 SHA-256 校验和自动下载安装更新

## 构建

```bash
flutter run -d windows
```

发布走 GitHub Actions，推 `v` 开头的 tag 会自动产出 EXE、MSIX 和绿色版 zip 并建 Release。