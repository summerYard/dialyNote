---
title: hexo图片路径问题
tags:
- hexo
- hexo图片
categories:
- 技术
updated: 2021-01-29 10:16
---

文章名称是中文时，`md`文件引入图片后，路径经常不对导致图片出不来，网上搜了之后基本都是安装`hexo-asset-image`，但是用了之后并没有起作用，最后发现了`hexo-image-link`这个插件，终于解决了……

这个插件使用非常简单：

1. 安装：`npm install hexo-image-link --save`
2. 修改`hexo`的配置文件`_config.yml`中的`post_asset_folder`为`true`
3. md文件中的图片路径用这个格式： <code>\!\[图片说明]\(文件名/图片名)</code>

就可以了~