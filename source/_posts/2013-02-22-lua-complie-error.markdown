---
layout: post
title: "lua complie error"
date: 2013-02-22 23:32
comments: true
categories: 
---



####编译错误提示
{% img center /images/lua_complie_error.png %}
####解决方法
/usr/bin/ld: cannot find -lncurses 
{% codeblock %}
1.如果没有那就是缺少库文件
$ sudo apt-cache search ncurses-
有这样一个结果：
libncurses5-dev - developer's libraries and docs for ncurses
安装libncurses

sudo apt-get install libncurses5-dev
 2.如果有这个文件，那么就不缺少库，只是文件类型的问题
查看此库应该不是以so结尾的，输入下面的代码，创建连接即可

sudo ln -rf  libncurses(*****)  libncurses.so
{% endcodeblock %}
####测试
{% img center /images/hellowrold_lua.png %}
####测试结果
{% img center /images/hellowrold_lua_result.png %}


####意外收获

打开图片命令
{% codeblock %}
eog XXX.png
{% endcodeblock %}

屏幕截图
{% codeblock %}
抓取桌面：scrot desktop.png
抓取窗口：scrot -bs window.png
抓取区域：scrot -s rectangle.png
延时抓取：scrot -cd 10 menu.png
操作抓图：scrot action.png -e ‘mv $f ~/images/’
{% endcodeblock %}



