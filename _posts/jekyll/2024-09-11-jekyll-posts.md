---
layout: post
title: "Jekyll Posts"
date: 2024-09-11 11:07:39 +0800
categories: jekyll
tags: [jekyll, tutorials]
---

`_posts`文件夹是博客文章所在的位置，使用markdown编写。

## 创建帖子

将帖子创建在`_posts`文件夹下，也可以放在该文件夹的子目录中，格式如下：

```plaintext
YEAR-MONTH-DAY-title.MARKUP
```



其中`YEAR`是四位数字， `MONTH`和`DAY`都是两位数字， `MARKUP`是表示文件中使用的格式的文件扩展名。例如，以下是有效的帖子文件名示例：

```plaintext
2011-12-31-new-years-eve-is-awesome.md
2012-09-12-how-to-write-a-blog.md
```

## 帖子内容

### 编写`front matter`

每个帖子需要在开头定义 Front Matter，使用 --- 符号包裹的 YAML 格式配置。以下是一个 Front Matter 示例：

```yaml
---
layout: post
title: "My First Post"
date: 2024-09-11 10:30:00 +0800
categories: [tech, jekyll, tutorials]
tags: [markdown, github-pages]
author: Your Name
published: true
---
```

| 变量           | 类型                                                         | 描述                                                         |
| -------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **layout**     | 字符串                                                       | 指定 Jekyll 用于渲染页面或文章的布局文件。布局文件通常位于 _layouts 文件夹中，文件格式通常为 .html。布局文件定义了页面的框架，比如头部、脚部、导航栏等，而文章或页面的内容会被插入到这个框架中。 |
| **title**      | 字符串                                                       | 页面或文章的标题，会显示在页面的 <title> 标签或页面内容中。  |
| **data**       | 日期时间字符串`YYYY-MM-DD HH:MM:SS +/-TTTT`，小时、分钟、秒和时区偏移量是可选的 | 文章或页面的发布日期。Jekyll 会根据这个日期为文章排序，默认从文件名中提取日期，如果 Front Matter 中没有定义。 |
| **permalink**  | 字符串                                                       | 自定义文章或页面的 URL（永久链接）。如果需要处理的博客文章 URL 不是站点范围的样式（默认`/year/month/day/title.html` ），那么可以设置此变量，它将用作最终 URL。 |
| **categories** | 字符串或字符串数组                                           | 为文章指定一个或多个分类。指定为[YAML 列表](https://en.wikipedia.org/wiki/YAML#Basic_components)或空格分隔的字符串。 |
| **tags**       | 字符串或字符串数组                                           | 为文章指定一个或多个标签，用于内容组织和过滤。与类别一样，标签可以指定为[YAML 列表](https://en.wikipedia.org/wiki/YAML#Basic_components)或空格分隔的字符串。 |
| **author**     | 字符串                                                       | 定义文章的作者名，可以在页面中显示或用于分类。               |
| **published**  | 布尔值                                                       | 是否发布文章。设置为 false 则不会在生成站点时包括此页面。    |

### 编写内容

使用 Markdown 编写内容。

## 本地预览文章

在发布之前，你可以在本地预览文章。首先，确保 Jekyll 已经安装好，然后运行以下命令：

```bash
bundle exec jekyll serve --port 4001
```

## 将网站部署到服务器或平台



