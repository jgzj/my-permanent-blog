---
title: '如何部署这个博客'
date: 2026-03-15T11:00:00+08:00
draft: false
tags: ['教程', '部署', '博客']
author: '博主'
---

## 博客部署指南

### 前提条件

- GitHub 账户
- Cloudflare 账户

### 部署步骤

#### 1. Fork 或克隆仓库

```bash
git clone https://github.com/your-username/my-permanent-blog.git
cd my-permanent-blog
```

#### 2. 配置 Cloudflare Pages

1. 登录 Cloudflare 控制台
2. 进入 Pages → 创建项目
3. 连接 GitHub 仓库
4. 设置构建配置：
   - 构建命令：`hugo --minify`
   - 输出目录：`public`

#### 3. 配置环境变量

在 Cloudflare Pages 设置中添加：
- `HUGO_VERSION` = `0.120.0`

#### 4. 发布

点击部署，等待完成即可！

### 更新文章

方式一：通过管理后台
- 访问 `https://your-blog.pages.dev/admin/`
- 使用 GitHub 登录
- 可视化编辑文章

方式二：直接推送代码
```bash
git add content/posts/new-post.md
git commit -m "添加新文章"
git push
```
