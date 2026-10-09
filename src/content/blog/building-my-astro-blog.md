---
title: '我的 Astro 博客搭建记录'
description: '从本地开发到 GitHub Pages，记录个人博客的创建与自动部署过程。'
pubDate: '2026-10-07'
heroImage: '../../assets/jun-blog-cover.png'
tags: 
  - Astro
  - TypeScript
  - GitHub Pages
---

这是我个人技术博客的第一篇文章，记录目前已经完成的搭建过程。

## 为什么选择 Astro

这个博客以技术文章为主，因此我选择 Astro，通过静态生成输出页面。

后续如果文章需要交互演示，可以使用 MDX 嵌入组件，并根据需要加载客户端脚本。

## 当前技术栈

- Astro：页面与静态站点构建
- TypeScript：开发时类型检查
- Markdown / MDX：文章创作
- Content Collections + Zod：文章元数据校验
- GitHub Actions：自动构建与部署
- GitHub Pages：静态网站托管

## 本地开发

启动开发服务器：

```bash
pnpm dev
```

构建并预览生产版本：

```bash
pnpm build
pnpm preview
```

开发服务器用于即时查看修改，生产预览用于检查构建后的实际效果。

## 自动发布

我的博客仓库使用 main 分支。

提交并推送修改后，GitHub Actions 会自动安装依赖、构建网站，并部署到 GitHub Pages。

整个流程是：

```text
修改内容 → Git 提交 → 推送 main → 自动构建 → 自动发布
```

## 接下来的计划

- 完善博客的视觉设计和阅读体验
- 添加暗黑模式和全文搜索
- 使用 MDX 编写交互式技术演示
- 加入类型检查与关键流程验证
