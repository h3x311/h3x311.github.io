---
title: "Git_CMD"
date: 2022-09-05T19:31:34+08:00
draft: false
---

记录2类git cmd，1是突发情况，2是可复用的。

# 突发情况

## 回滚

> reset在merge分支时，会失效。
> push代码后，用revert比较好。-n 是舍弃后面SHA的commit内容

### reset

``` git reset --hard <commidId> && git push --force
```

### revert

``` git revert -n <sha>
```
# 复用

``` git commit --amend --no-edit 
```
> 复用上一个commit内容


