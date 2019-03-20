---
layout: post
title: "java复习maven"
categories: maven
tags: maven
author: 百味皆苦
music-id: 2602106546
---

* content
{:toc}
## 介绍

- Maven 是专门用于构建和管理Java相关项目的工具。
- Maven是意第绪语，依地语（犹太人使用的国际语），表示专家的意思
- 使用Maven管理的Java 项目都有着相同的项目结构
  1. 有一个pom.xml 用于维护当前项目都用了哪些jar包
  2. 所有的java代码都放在 src/main/java 下面
  3. 所有的测试代码都放在src/test/java 下面
- maven风格的项目，首先把所有的jar包都放在"仓库“ 里，然后哪个项目需要用到这个jar包，只需要给出jar包的名称和版本号就行了。 这样jar包就实现了共享

## 尚硅谷笔记

<img src=“https://img-blog.csdnimg.cn/20190320133043457.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2OTI1NTM2,size_16,color_FFFFFF,t_70” style=“width:1366px height:12138px” />

