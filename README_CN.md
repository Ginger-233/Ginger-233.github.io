# 个人网站使用指南

这份指南将帮助你维护和更新你的个人主页。

## 1. 快速开始 (本地运行)

如果你想在本地预览网站更改，请确保安装了 Ruby 和 Jekyll。

```bash
bundle install
bundle exec jekyll serve
```

访问 `http://localhost:4000` 即可预览。

## 2. 如何修改基本信息

所有网站的全局配置都在 `_config.yml` 文件中。
你可以修改：
- **title** / **name**: 你的名字
- **description**: 网站描述
- **author**: 侧边栏的个人信息 (Email, 地点, 学校等)
- **social**: 社交媒体链接 (Github, Google Scholar 等)

## 3. 如何添加项目/发表论文

所有的项目或论文都存放在 `_publications` 文件夹下的 `.md` 文件中。

### 添加新项目
1. 在 `_publications` 文件夹中创建一个新文件，命名格式建议为 `YYYY-MM-DD-project-name.md`。
2. 复制以下模板内容并修改：

```yaml
---
title: "项目名称"
collection: publications
permalink: /publication/2025-10-01-project-name
excerpt: '项目简短描述，会显示在列表页。'
date: 2025-10-01
venue: '发表会议/期刊 或 项目类型'
paperurl: '论文链接 (可选)'
citation: '引用格式 (可选)'
---
这里可以使用 Markdown 格式撰写项目的详细介绍。
**Topic**: ...
**Contribution**: ...
```

## 4. 如何修改页面内容

- **关于我 (About)**: 修改 `_pages/about.md`。
- **简历 (CV)**: 修改 `_pages/cv.md`。

## 5. 常见问题

- **修改后没变化？** 尝试重启 `jekyll serve`。
- **中文乱码？** 确保文件以 UTF-8 编码保存。

更多详细文档可参考原模板 [AcademicPages Docs](https://academicpages.github.io/markdown/)。
