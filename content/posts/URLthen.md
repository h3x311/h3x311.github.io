---
title: "URL then what happened?"
date: 2022-03-29T11:10:49+08:00
draft: false
showToc: true
TocOpen: true
hidemeta: false
comments: true
author: "sober"
disableHLJS: false 
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

# Make a Http Request --> use curl

client 向 server 发送request
![jM5805_qmnT7j](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/jM5805_qmnT7j.jpg)
request head
![6OPwju_BdK5cG](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/6OPwju_BdK5cG.png)
first line of request, Http1.1 --> All plain text
![8mgmRo_UjJ3dv](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/8mgmRo_UjJ3dv.png)

# Why Http good?

![iGmdbq_pCT1mh](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/iGmdbq_pCT1mh.png)

1. client - server model

2. plain text

3. add headers value key for more extend

4. stateless for independent
![l6TBND_2wAS3W](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/l6TBND_2wAS3W.jpg)

5. 可靠reliability



# status code

![BdW7Vt_zZRbS5](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/BdW7Vt_zZRbS5.png)

206 - range of requests succeed

## rediect_3

![VeStqd_C5yWgQ](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/VeStqd_C5yWgQ.png)

## client_4

![e2Mjtt_Jxewsb](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/e2Mjtt_Jxewsb.jpg)

I would never request.404

## server_5

![GDkx2z_UApWiN](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/GDkx2z_UApWiN.png)

You can request again.500

# headers

![NE12Qn_TpMQLX](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/NE12Qn_TpMQLX.jpg)


![aryLcg_WYOCgK](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/aryLcg_WYOCgK.jpg)

![X6AnZx_SNetUp](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/X6AnZx_SNetUp.jpg)

# 总结

![dXPep2_vFum6E](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/dXPep2_vFum6E.png)

![KCqDBh_h28tB5](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/KCqDBh_h28tB5.png)

![7FscJJ_G15Q7J](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/7FscJJ_G15Q7J.png)