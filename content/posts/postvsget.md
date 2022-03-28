---
title: "Post VS Get"
date: 2022-03-28T11:59:17+08:00
draft: false
showToc: true
TocOpen: false
hidemeta: false
comments: true
author: "sober"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
tags:
- network
categories:
- cs
---
# defination

HTTP request

![jZicPi_JxMCi3](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/jZicPi_JxMCi3.png)

# 区别

## get 
1. 参数在url(长度有限)
    
    >1. 'GET' is limited to 2048 characters

2. require data from server

## POST

1. 参数在body

2. 安全性更好

3. update data to webserver

![iJls55_ubLrBj](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/iJls55_ubLrBj.jpg)

![GkhfU0_s1LQvI](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/GkhfU0_s1LQvI.jpg)

# 总结

在面试中很常见的问题，网文写的都不太全。

so和ytb上的解释，区别是：1. 长度和参数位置不同。2. 安全性。不安全的内容用post。

理解区别最好的方式是举例子。

# REF

[when-do-you-use-post-and-when-do-you-use-get](https://stackoverflow.com/questions/46585/when-do-you-use-post-and-when-do-you-use-get)

[What is the difference between POST and GET? [duplicate]](https://stackoverflow.com/questions/3477333/what-is-the-difference-between-post-and-get)