---
title: hexo增加emoji引发的md渲染器的修改
tags:
- hexo
- emoji
categories:
- 技术
updated: 2021-01-29 14:00
---

最开始是想要引入`emoji`，在网上搜到用`hexo-renderer-markdown-it`的方法，确实好使，然后后来又在其他地方看到了其他的渲染器，貌似比`hexo-renderer-markdown-it`更好，所以更新了这篇文章

<h1 id="install">hexo-renderer-markdown-it的使用</h1>

<h2 id="install">安装</h2>

删除原有的`markdown`渲染引擎：`npm un hexo-renderer-marked --save`
安装新的支持`emoji`的引擎： `npm i hexo-renderer-markdown-it markdown-it-emoji --save	`

<h2 id="config">配置</h2>

`Hexo`站点配置文件`_config.yml`中，增加`markdown`相关配置：

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

<h1 id="install">@upupming/hexo-renderer-markdown-it-plus的使用</h1>

各个渲染器，在这篇文章有讲：https://blog.csdn.net/qq_36667170/article/details/105846999

对比起来，目前看起来最好的应该是这个渲染器`@upupming/hexo-renderer-markdown-it-plus`

<h2 id="install">安装</h2>

1. 删除其他的`markdown`渲染引擎
2. 如果之前有安装`markdown-it-emoji`也可以删除，因为`@upupming/hexo-renderer-markdown-it-plus`默认是支持`emoji`的
3. 安装`@upupming/hexo-renderer-markdown-it-plus`： `npm i @upupming/hexo-renderer-markdown-it-plus --save `

<h2 id="config">配置</h2>

`Hexo`站点配置文件`_config.yml`中，修改`markdown`相关配置为：

```
markdown_it_plus:
  render:
    html: true            
    xhtmlOut: false
    breaks: true
    linkify: true
    typographer: true
    quotes: '“”‘’'
  plugins:
  anchors:  
    level: 2
    collisionSuffix: 'v'
    permalink: true
    permalinkClass: header-anchor
    permalinkSide: 'left'
    permalinkSymbol: ¶
```

就可以了