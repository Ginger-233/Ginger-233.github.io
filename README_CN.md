# 个人网站使用指南 (User Guide)

本指南针对 [Ginger-233.github.io] 项目，帮助你维护和个性化你的个人主页。
该模版基于 **AcademicPages**，并已根据你的简历进行了定制。

---

## 目录
1. [项目结构](#1-项目结构)
2. [如何修改个人信息 (侧边栏)](#2-如何修改个人信息-侧边栏)
3. [如何管理学术项目/论文](#3-如何管理学术项目论文)
4. [如何修改页面内容 (About/CV)](#4-如何修改页面内容-aboutcv)
5. [如何调整顶部导航栏](#5-如何调整顶部导航栏)
6. [本地运行与发布](#6-本地运行与发布)

---

## 1. 项目结构

核心文件和文件夹如下：

- **`_config.yml`**: 网站的**全局配置文件**。控制网站标题、侧边栏个人信息、社交链接等。
- **`_pages/`**: 存放主要页面（如 `about.md` (首页), `cv.md` (简历) 等）。
- **`_publications/`**: 存放具体的项目或论文页面。每篇文章一个 Markdown 文件。
- **`_data/navigation.yml`**: 顶部导航栏的配置。
- **`images/`**: 存放图片（如头像 `profile.png`）。

---

## 2. 如何修改个人信息 (侧边栏)

打开根目录下的 **`_config.yml`** 文件，找到 `author:` 部分。

```yaml
author:
  avatar           : "profile.png"  # 头像文件名，请将你的照片放入 images/ 文件夹并重命名为 profile.png
  name             : "Ran Zhenning" # 你的名字
  bio              : "..."          # 侧边栏简介
  location         : "Shanghai"     # 地点
  email            : "..."          # 邮箱
  
  # 社交链接 (Social media)
  github           : "Ginger-233"
  googlescholar    : "" # 如果有谷歌学术主页，填入 URL
```

> **注意**: 如果你不填某一项（留空），该图标就不会显示。

### 更改头像
1. 将你的照片（例如 `my_photo.jpg`）放入 `images/` 文件夹。
2. 修改 `_config.yml` 中的 `avatar: "my_photo.jpg"`。

---

## 3. 如何管理学术项目/论文

目前你的"Publications"页面已更名为"Research Projects"，专门展示你的科研项目。

所有的项目文件都在 **`_publications/`** 文件夹中。

### 添加新项目
1. 在 `_publications/` 下新建一个文件，文件名建议格式：`YYYY-MM-DD-project-name.md`。
2. 复制以下**标准模版**：

```yaml
---
title: "项目标题 (e.g., Bi-value Chores under EFX)"
collection: publications
permalink: /publication/2025-10-01-project-name  # 唯一的链接地址
excerpt: '这里写简短的项目摘要，会显示在列表页。<br/><img src="/images/project-image.png">' # 支持 HTML 图片
date: 2025-10-01
venue: 'Project / Conference Name' # 发表的会议或 "Under Review" / "Course Project"
---

## Project Description

这里可以使用 **Markdown** 编写详细的项目介绍。

- **Topic**: Fair Division
- **My Role**: Lead Researcher
- **Contribution**: ...

```

### 如果发表了论文
如果以后发表了论文，可以将 `venue` 改为会议名称，并添加：
```yaml
paperurl: 'http://link-to-paper.pdf'
citation: 'Your Name, et al. (2025). Title. Conference.'
```

---

## 4. 如何修改页面内容 (About/CV)

### 修改首页 (About Me)
编辑 **`_pages/about.md`**。
这是一个标准的 Markdown 文件。你可以自由修改其中的自我介绍、教育背景等。

### 修改简历页 (CV)
编辑 **`_pages/cv.md`**。
目前已根据你的简历填入了 Education, Projects, Skills。
如果你有新的经历，直接按照现有的格式添加即可。

> **提示**: CV页面的底部会自动列出 `_publications` 里的所有项目，无需手动添加项目列表。

---

## 5. 如何调整顶部导航栏

编辑 **`_data/navigation.yml`**。

```yaml
main:
  - title: "Projects"       # 显示的文字
    url: /publications/     # 跳转的链接

  # 如果想隐藏某个菜单，可以在前面加 # 注释掉
  # - title: "Talks"
  #   url: /talks/
```

---

## 6. 本地运行与发布

### 环境配置
你需要安装 Ruby 和 Bundler。
由于你的电脑可能会遇到 Ruby 版本问题，建议使用以下命令尝试安装依赖：

```bash
# 如果你需要本地预览
bundle install
```

### 启动本地服务
```bash
bundle exec jekyll serve
```
成功后，访问 `http://localhost:4000` 预览。

### 发布到 GitHub
只需要将修改后的文件推送到 GitHub 仓库即可。
GitHub Pages 会自动构建并更新网站（通常需要 1-3 分钟）。

```bash
git add .
git commit -m "Update website content"
git push
```

---

如有其他问题，可以参考 `README.md` 中的官方文档链接。
