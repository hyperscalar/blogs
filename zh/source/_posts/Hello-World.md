---
title: 你好，世界
date: 2018-03-20
categories:
- 杂项
tags:
- 测试
mathjax: true
---

这是我的个人博客。

主要分享对于技术学习和思考，但不局限于此。

坚持原创，不定时更新。

<!-- more -->

## 代码

```java
// Java
class HelloWorld {

    public static void main() {
        System.out.println("Hello World!");
    }
}
```

```c
// C
#include "stdio.h"

int main() {
    printf("Hello World!\n");
    return 0;
}
```

## 公式

$$
E = mc^2
$$

## 图表

```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```

## 图片

{% asset_img San-Francisco.png San Francisco %}

## 笔记

{% note default %} Hello World! {% endnote %}

{% note primary %} Hello World! {% endnote %}

{% note success %} Hello World! {% endnote %}

{% note info %} Hello World! {% endnote %}

{% note warning %} Hello World! {% endnote %}

{% note danger %} Hello World! {% endnote %}
