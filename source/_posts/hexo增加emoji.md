---
title: hexo增加emoji
tags:
- hexo
- emoji
categories:
- 技术
---

<h1 id="install">安装</h1>

删除原有的`markdown`渲染引擎：`npm un hexo-renderer-marked --save`
安装新的支持`emoji`的引擎： `npm i hexo-renderer-markdown-it markdown-it-emoji --save	`

<h1 id="config">配置</h1>

Hexo 站点配置文件`_config.yml`中，增加`markdown`相关配置：

```
markdown:
  render:
    html: true
    xhtmlOut: false
    breaks: true
    linkify: true
    typographer: true
    quotes: '“”‘’'
  plugins:
    - markdown-it-footnote
    - markdown-it-sup
    - markdown-it-sub
    - markdown-it-abbr
    - markdown-it-emoji
  anchors:
    level: 2
    collisionSuffix: 'v'
    permalink: true
    permalinkClass: header-anchor
    permalinkSymbol: ¶
```

就可以使用`emoji`了，感谢这位博主 银河小徐 的文章~ 

原文链接是：https://hasaik.com/posts/9b280ea3.html

文章中还有`emoji`编码合集，特别方便~

