---
title: "Git多用户"
date: 2022-02-22T14:26:09+08:00
draft: False
showToc: true
TocOpen: false
hidemeta: false
comments: true
author: "sober"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: false
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
tags:
- git
categories:
- tool
cover:
    image: "<image path/url>" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
---
## 需求
1. git用户和repo分离
2. 多ssh key登陆

## Q1
``` 
git config --local user.name "xxx"
git config --local user.email "xxx"
   ```
   修改当前项目下的git用户<br />
   前提是添加多用户ssh key到～/.ssh/config
## Q2
### 1. 生成key
 ```
 ssh-keygen -t rsa -C "user2@email.com"
  ```
名字加后缀，不要覆盖之前的key

### 2. 添加key到ssh agent中
 ```
 ssh-agent bash
 ssh-add ~/.ssh/keyname
  ```
### 3. 修改ssh的config
``` 
Host github-user2
HostName github.com
User git
   ``` 
Host 名称随意
当添加remote repo时，Host 替换：
 ```
 git remote add origin git@github-user2:repoUrl
  ```
而不是
 ```
 git remote add origin git@github.com:repoUrl
 ```
- git clone 如是

## 总结
这样就可以愉快的使用多账号提交代码了！
