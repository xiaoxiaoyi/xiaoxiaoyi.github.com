---
layout: post
title: "ls why no color?"
date: 2013-02-23 18:53
comments: true
categories: 
---

####LS无配色
{% img center /images/ls_nocolor.png %}
####网上解决方法
{% codeblock %}
添加alias ls='ls --color'到.bashrc
{% endcodeblock %}
####结果
{% img center /images/ls_nocolor.png %}
####原因
<center>
my bash use longin shells for rvm use but bashrc for non-login shells
</center>
{% img center /images/bashrc_scope.png %}
####MY解决方法I
{% codeblock %}
添加alias ls='ls --color'到.bash_profile
{% endcodeblock %}
####MY解决方法II
{% codeblock %}
添加
if [ -f ~/.bash_aliases ]; then
    . ~/.bash_aliases
fi
到.bash_profile
{% endcodeblock %}
{% codeblock %}
vim ~/.bash_profile
添加alias ls='ls --color'到.bash_profile
:wq
{% endcodeblock %}
####效果
{% img center /images/bash_result.png %}

