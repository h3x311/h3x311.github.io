---
title: "Cs61b"
date: 2022-05-14T21:22:33+08:00
draft: false
---

## 1st day

看了篇[用python实现的各种基础数据结构](https://xnth97.github.io/2017/12/19/data-structure-note/)，写的很好，试着以后写笔记有一个goal。而不是copy feelings。

卡在markdown本地图片上传，本地笔记会分享上来的，未来的某一天。

## 1st
1. 变量类型必须有，且不可改变，在运行前verify
	1. ![Qz65SR_4Z5cVh](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/Qz65SR_4Z5cVh.png)
2.  A func is called a method
	1. define func --> public staic
	2. func's parameters and return value must declared type
	3. Only one return val

## 2nd
1. 没有main的method可以在有main的method里被调用
	1. ![3bwDza_fRYy3a](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/3bwDza_fRYy3a.png)
## 3rd list
1. link 两个list
	1. ![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/Pasted%2520image%252020220308163147.png)
	![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/Pasted%2520image%252020220308163156.png)
	![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/Pasted%2520image%252020220308163606.png)
	ptr是指针
## 4th 
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/Pasted%2520image%252020220309233711.png)

<img width="408" alt="image" src="https://user-images.githubusercontent.com/39543393/157618060-233dc6b0-b52a-4108-b080-8ddfa6efb689.png">
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/Pasted%2520image%252020220310170855.png)
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/Pasted%2520image%252020220310172140.png)
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/Pasted%2520image%252020220310172157.png)

# list
1. a = b时，发生了什么？
	1. ![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/Pasted%2520image%252020220323212551.png)
	箭头指在相同的内存空间
### this
>"this" because it is a java keyword and it always refers to the current object.


## Sentinel Nodes
为了减少len为0的代码，加上sentinel node，就不在乎有没有node

## arraycopy

深拷贝，而不是指向同一个地址。所以拷贝之后的行为是独立于copy值的。

## lab3
### add libraries

![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/Pasted%2520image%252020220406215134.png)
### how to build test
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/Pasted%2520image%252020220406221239.png)
-[ juit](https://junit.org/junit4/javadoc/4.12/org/junit/Assert.html)
- debugger --> breakpoint
- print
- refactor 

## proj1a
1. class declare --> <>
2. 在class内定义private class
3.  whats constructor

## 8_Inheritance, Implements
### overloading
1. multiple methods with same name, different parameters
	1. ![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/Pasted%2520image%252020220414123736.png)
	2. ![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/Pasted%2520image%252020220414123932.png)
	保持一致。当一个method内容改变，另一个也要跟着改变。



### Hypernyms, Hyponyms, and Interface Inheritance
1.  create a hypernym
	1. public **interface** List61B<item>
2. add implements to hyponyms
	1. public class AList<item> implements List61B<item>{}
		1. define all attributes and behaviors for list61b interface


### overiding

1. 如果subclass和superclass的method相同。称为 subclass override superclass
> method is overloaded
> subclass overide superclass

add @Override for public method of subclass
> @Override is optional
> why use it? for protecting against typos


### Implementation Inheritance
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/Pasted%2520image%252020220414164752.png)
interface inheritance, 继承signature，no implementation
Java 继承implementation--> use default

1. java is type static, but method dynamic in overriding

#### overload vs overriding
1. 当调用overload时，是调用对应的method。
2. 当调用overriding时，是调用overriding的method。
#### interface vs implementation inherience
1. 'is a', not 'has a'
	1. ![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/Pasted%2520image%252020220414175530.png)
2. ![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/Pasted%2520image%252020220414175641.png)
## disc4
1. super(parameters) --> subclass call superclass's constructor

## Extends, Casting, Higher Order Functions
1. What can be inherienced?
	1. instance
	2. static variables
	3. method
	4. nested classes
	5. NOT constructors
2. If u don't use super(), u'll hava super() with no parameters.
### Encapsulation
1. a modular, like a cell, 不需要知道组成的结构和method的实现，直接调用对应的method就可以。
2. inheritance--> subclass's override method 调用 heritance method, 会引起冲突，破坏了encapsulation
### Type Checking and Casting
1. variable --> 检查左边被赋值的对象是否属于右边赋值的类型。
2. expression --> subclass check the method by superclass, but no other subclasses. Or it will be compiler-type check error.
### Casting
1. use cast to avoid the compiler-type check.
### High Order function
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/Pasted%2520image%252020220415190912.png)
## Subtype Polymorphism vs. HoFs
#### polymorphism
1. provide a single interface to entites of different type
	1. 支持多类型的实体
2. 比较hof 和 subtype polymorphism
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/Pasted%2520image%252020220421153224.png)
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/Pasted%2520image%252020220421221857.png)

Use interface of  type for better code.
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/Pasted%2520image%252020220421225607.png)
### Libraries, Abstract Classes, Packages
#### Abstract Data Types (ADTS)
1. 


![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/Pasted%2520image%252020220425000937.png)

