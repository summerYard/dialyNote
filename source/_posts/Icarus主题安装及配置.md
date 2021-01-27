---
title: Icarus主题安装及配置
tags:
- hexo主题
- Icarus
categories:
- 技术
---


# 关于Icarus主题的几个有用的网站及文章

http://blog.cuzz.site/

https://blog.csdn.net/weixin_43980832/article/details/104736491?utm_medium=distribute.pc_relevant.none-task-blog-baidujs_title-6&spm=1001.2101.3001.4242

https://blog.csdn.net/marvine/article/details/89816846

https://blog.zhangruipeng.me/hexo-theme-icarus/uncategorized/icarus%E5%BF%AB%E9%80%9F%E4%B8%8A%E6%89%8B/

https://blog.zhangruipeng.me/hexo-theme-icarus/tags/Icarus%E7%94%A8%E6%88%B7%E6%8C%87%E5%8D%97/

https://blog.zhangruipeng.me/hexo-theme-icarus/Configuration/icarus%E7%94%A8%E6%88%B7%E6%8C%87%E5%8D%97-%E4%B8%BB%E9%A2%98%E9%85%8D%E7%BD%AE/


# 安装后的修改

1. `npm install` 安装主题后，将主题代码从 `node_modules` 目录下拷了出来，放到了`theme/icarus`目录中,并将项目根目录下的`_config.landscape.yml`文件也迁移到了`theme/icarus`目录,并改名为`_config.yml`
2. 这个主题的样式用到了 `node_modules`中的 `bulma-stylus`下的文件,为了修改方便,也拷了出来,放到了`theme/bulma-stylus`目录,并修改了icarus主题代码中的引用路径

弄好之后,配置项修改了一部分,去掉了不想要的,将最新文章以及标签等移到了右边


Welcome to [Hexo](https://hexo.io/)! This is your very first post. Check [documentation](https://hexo.io/docs/) for more info. If you get any problems when using Hexo, you can find the answer in [troubleshooting](https://hexo.io/docs/troubleshooting.html) or you can ask me on [GitHub](https://github.com/hexojs/hexo/issues).