---
title: "Process VS Thread"
date: 2022-03-28T15:03:28+08:00
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
- os
categories:
- cs
---

# Defination

![d8GDV0_QdTFcA](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/d8GDV0_QdTFcA.png)

program有很多process，pcb是个虚拟的process容器，process可以creat child process。

process有很多thread，三个状态，running，ready，block。
## Process
> An executing instance of a program is called a process.

1. Seprate Process Control Block, Stack and Address Space.
   1. process之间很难相互影响

2. many process to one program

3. disappear after reboot

4. ps, multiprocess system can excute processes parallelly

## Thread
> A thread is a subset of the process.

1. share **Data, Code, Heap**, no stack

2. many threads to one process share the **same address space**

# 区别

![Tnq49Z_pv2knM](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/Tnq49Z_pv2knM.jpg)

![TA9qeZ_ZO5iaY](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/TA9qeZ_ZO5iaY.jpg)

# 总结

process是独立互不影响的的，thread间是共享的code,data,files。

面试考的就是这点吧。


# REF

- [what-is-the-difference-between-a-process-and-a-thread](https://stackoverflow.com/questions/200469/what-is-the-difference-between-a-process-and-a-thread/200473#200473)
