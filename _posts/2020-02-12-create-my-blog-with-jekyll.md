---
layout: post
title:  "Jekyll 搭建静态博客"
date:   2020-02-12 
categories: jekyll
tags: Ruby RubyGems Jekyll
---

* content
{:toc}

搭建自己的博客！





## 搭建过程(Windows)

主要环节有：安装Ruby，安装RubyGems，安装jekyll，安装代码高亮插件，安装node.js

### 安装Ruby

ruby官网下载安装：[https://www.ruby-lang.org/en/downloads/](https://www.ruby-lang.org/en/downloads/)

安装时默认配置环境变量；安装时自动安装msys2,速度慢,但是得等,要不后面装Jekyll时麻烦。

```
	ruby -v 
	ruby 2.7.0p0 (2019-12-25 revision 647ee6f091) [x64-mingw32]
```


### 安装RubyGems

官网下载 [http://rubygems.org/pages/download](http://rubygems.org/pages/download) zip包   

cd到RubyGems目录   

执行安装 
```
	ruby setup.rb
```  


### 用RubyGems安装Jekyll

执行下面的语句安装   

```
	gem install jekyll
```

异常
```
nvalid gem: package is corrupt, exception while verifying: undefined method`path2class' for #<Psych::ClassLoader:0x0000010c9d0be0> (NoMethodEr
```
解决[Stackover](https://stackoverflow.com/questions/20850737/install-rails-error-invalid-gem-package-is-corrupt):
```
Stephens-MacBook-Pro-2:~ Steve$ mv .rvm old.rvm

找到那个文件，重新命名，继续重新安装JEKYLL，会自动下载。
```

至此jekyll就已经安装完毕了，后续就是个性化的自己设定了。



### 创建博客

在E盘新建一个工作区jekyllWorkspace

cd到jekyllWorkspace   

执行jekyll new name创建新的工作区   
```
E:\>  md jekyllworkspace
E:\>  cd jekyllworkspace
E:\jekyllworkspace  jekyll new Family
E:\jekyllworkspace cd  Family
E:\jekyllworkspace\Family  jekyll  serve --watch

```

浏览器打开：http://127.0.0.1:4000/



## Ref 
[1] [徐代龙的技术专栏](https://643435675.github.io/2015/02/15/create-my-blog-with-jekyll/) 

[2][Github搭建个人博客](https://blog.csdn.net/xudailong_blog/article/details/78762262)

[3] [Jekyll](http://jekyllrb.com/)
