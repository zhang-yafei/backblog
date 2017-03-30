---
title: 搭架hexo Blog
date: 2016-09-21 19:26:17
tags: 开发手册
categorys: 开发手册
---
# 搭建hexo Blog

---
>作者：张亚飞

>日期：2016年9月21日

---
##前言
很早以前看过阮一峰写的使用Jekyll和markdown的方式搭建的blog，当时也写了一个页面。每一个页面都是一个独立的主体。如果数量多的话，管理起来很麻烦。

用一个比喻来形容的话，就像一个菜篮子，所有的东西都向里面扔。总体感觉太零碎。于是就放在那边，没有继续写。

##准备工作
需要安装[git](https://git-scm.com/download)和[node.js](https://nodejs.org/en/)，这两个是必须要安装的。还需要注册github，注册的用户名比较特别注意。[参考](http://www.jianshu.com/p/701b1095da11)

##开始搭建Blog
注册完以后，repositories新建玩以后就按照这个流程[HEXO搭建博客](http://baixin.io/2015/08/HEXO%E6%90%AD%E5%BB%BA%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A2/).

不过到hexo deploy这一步时，deploy这一段需要注意一下。：后面一个空格，属性前2个空格，属性值后1个空格

如果原来repositories里面有文件，就是上传失败。需要先拉下来，再上传。
也可以直接把仓库删除以后再新建。

删除方法如下，在github里面选setting，然后拖到最下面。可以看到
![图片](https://zhang-yafei.github.io/images/handbook/github_dele.png)

##增加评论功能
看到这里，你的博客应该已经可以正常访问了。不过，总是觉得缺点什么。没有评论功能的博客，不就和写日记一样了。于是，我就开始琢磨增加评论功能。我看到了评论功能有2种方式[多说](http://duoshuo.com/)和disqus。这里我用的是多说。

1. 注册多说账号，有很多第三方登陆方式。选一种就好了
![注册](https://zhang-yafei.github.io/images/handbook/duoshuo_zhuce_type.png)

2. 在基本信息里面填好自己的github网站后，在设置->基本设置里面只用设置多说的个人**二级域名**和**名称**就好了
![注册](https://zhang-yafei.github.io/images/handbook/duoshuo_page.png)

2. 在themes/主题/_config.yml文件里面加上  
`#多说的评论插件 `  
`duoshuo_shortname: 你的二级域名 `
这里注意：后面需要一个空格，如图所示：
![注册](https://zhang-yafei.github.io/images/handbook/duoshuo_add.png)

##附录常用命令

* hexo generate #生成静态页面至public目录  
* hexo clean #将生成的public，souce里面的文件清空
* hexo deploy #将.deploy目录部署到GitHub
* hexo new "postName" #新建文章
* hexo new page "pageName" #新建页面
* hexo server #开启预览访问端口（默认端口4000，'ctrl + c'关闭server）
* hexo help  # 查看帮助
* hexo version  #查看Hexo的版本