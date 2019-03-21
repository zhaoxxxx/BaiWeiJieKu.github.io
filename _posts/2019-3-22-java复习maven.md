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

## 目前技术

![](https://img-blog.csdnimg.cn/201903211703237.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2OTI1NTM2,size_16,color_FFFFFF,t_70)

## 为啥使用

![](https://img-blog.csdnimg.cn/20190321170351181.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2OTI1NTM2,size_16,color_FFFFFF,t_70)

## maven简介

![](https://img-blog.csdnimg.cn/20190321170414573.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2OTI1NTM2,size_16,color_FFFFFF,t_70)

![](https://img-blog.csdnimg.cn/20190321170434215.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2OTI1NTM2,size_16,color_FFFFFF,t_70)

![](https://img-blog.csdnimg.cn/20190321170448473.png)

![](https://img-blog.csdnimg.cn/20190321170504157.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2OTI1NTM2,size_16,color_FFFFFF,t_70)

![](https://img-blog.csdnimg.cn/2019032117051615.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2OTI1NTM2,size_16,color_FFFFFF,t_70)

## 安装

![](https://img-blog.csdnimg.cn/20190321170539262.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2OTI1NTM2,size_16,color_FFFFFF,t_70)

![](https://img-blog.csdnimg.cn/20190321170553653.png)

## 核心概念

![](https://img-blog.csdnimg.cn/20190321170609964.png)

## 简单工程

![](https://img-blog.csdnimg.cn/20190321170623154.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2OTI1NTM2,size_16,color_FFFFFF,t_70)

## 常用命令

![](https://img-blog.csdnimg.cn/2019032117071454.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2OTI1NTM2,size_16,color_FFFFFF,t_70)

## 联网下载

![](https://img-blog.csdnimg.cn/20190321170740905.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2OTI1NTM2,size_16,color_FFFFFF,t_70)

## POM

![](https://img-blog.csdnimg.cn/20190321170800576.png)

## 坐标

![](https://img-blog.csdnimg.cn/20190321170813618.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2OTI1NTM2,size_16,color_FFFFFF,t_70)

## 仓库

![](https://img-blog.csdnimg.cn/20190321170827823.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2OTI1NTM2,size_16,color_FFFFFF,t_70)

## 初步依赖

![](https://img-blog.csdnimg.cn/2019032117084374.png)

![](https://img-blog.csdnimg.cn/20190321170858401.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2OTI1NTM2,size_16,color_FFFFFF,t_70)

![](https://img-blog.csdnimg.cn/20190321170916314.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2OTI1NTM2,size_16,color_FFFFFF,t_70)

## 生命周期

![](https://img-blog.csdnimg.cn/20190321170930769.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2OTI1NTM2,size_16,color_FFFFFF,t_70)

![](https://img-blog.csdnimg.cn/20190321170948240.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2OTI1NTM2,size_16,color_FFFFFF,t_70)



## eclipse

![](https://img-blog.csdnimg.cn/20190321171013294.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2OTI1NTM2,size_16,color_FFFFFF,t_70)

## 高级依赖

![](https://img-blog.csdnimg.cn/2019032117103914.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2OTI1NTM2,size_16,color_FFFFFF,t_70)

![](https://img-blog.csdnimg.cn/20190321171055151.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2OTI1NTM2,size_16,color_FFFFFF,t_70)

![](https://img-blog.csdnimg.cn/20190321171109169.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2OTI1NTM2,size_16,color_FFFFFF,t_70)

![](https://img-blog.csdnimg.cn/20190321171120393.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2OTI1NTM2,size_16,color_FFFFFF,t_70)

![](https://img-blog.csdnimg.cn/20190321171135746.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2OTI1NTM2,size_16,color_FFFFFF,t_70)

## 继承

![](https://img-blog.csdnimg.cn/20190321171403868.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2OTI1NTM2,size_16,color_FFFFFF,t_70)

![](https://img-blog.csdnimg.cn/20190321171226769.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2OTI1NTM2,size_16,color_FFFFFF,t_70)

![](https://img-blog.csdnimg.cn/20190321171242873.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2OTI1NTM2,size_16,color_FFFFFF,t_70)



## 聚合

![](https://img-blog.csdnimg.cn/20190321171253986.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2OTI1NTM2,size_16,color_FFFFFF,t_70)





