---
title: "Backend"
date: 2022-07-28T23:21:07+08:00
draft: true
---

最近听podcast讲到，经验是解决问题的shortcuts，但有意思的点是从零经验的角度如何将问题定位。不抽象的谈，就比如说最近做的事情，首先是从第三方API拿数据来分析，再根据本有的service里的参数来判断做相应的操作。主干问题是细节类的，比如对语法和ut不熟悉。这部分花了3天就写好了，ut的关键是mock每个if else条件下的合适的参数，得以走通测试。接第三方API，刚开始没有考量过，思路是按照已有的格式写好API接口，并且学了PAW的使用，知道JSON返回的格式有两种(", :)。然后写了5，6句格式转换，提交完protype后成就感爆满。

如何调用一个API？首先看文档，header和response返回类型都是string。

如果刚开始按照正确的方式来写API，并且以此为这个story的切入点，就容易很多。

在不测试的情况下，瞎写一通，学到了JSON的不同格式，但也是走了不少弯路。当然也可能是对相关的知识了解太少。

在做0了解的事情前，一定要找到问题的**新的不确定的核心**开始，然后再了解这个**测试**的方法。

还反映出1个问题，对相关工具不熟悉，比如**docker和数据库, Git**，可能半小时掌握到的知识需要花费很多不必要的时间死磕。

还是得有耐心，冷静。