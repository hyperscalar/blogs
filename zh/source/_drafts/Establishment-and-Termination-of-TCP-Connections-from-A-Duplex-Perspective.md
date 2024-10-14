---
title: 从双工的角度看 TCP 连接的建立与释放
date:
updated:
categories:
- 计算机网络
tags:
- 视角
---

由于 TCP 是一个全双工的协议，因此我们可以从全双工的角度来理解 TCP 连接的建立与释放的过程。

<!-- more -->

## 什么是双工？

首先，何为全双工。全双工是指协议允许数据在两个方向上同时传输。

其次，何为半双工。半双工是指协议允许数据在两个方向上传输，但不能同时进行。

可以看到，无论是全双工还是半双工，都需要支持数据的双向传输，差别在于能不能同时进行，而单工则仅支持数据的单向传输。

## TCP 连接的建立（三次握手）

{% asset_img Establishment-of-TCP-Connections.png TCP 链接的建立过程 %}

而要理解建立 TCP 连接为什么需要三次握手，我们可以从双工的角度来切入；现在试想，要建立一个双工的连接，我们需要确认什么？

其实概括起来一共就 4 点：

1. 我方有发送数据的能力；
1. 对方有发送数据的能力；
1. 我方有接收数据的能力；
1. 对方有接收数据的能力。

现在我们来看三次握手的具体过程：

1. 我方向对方发送一个数据包，并且对方接收到了；

   这个时候对方确认了我方有发送数据的能力；

1. 对方基于收到的数据包中的某些信息，向我方发送一个数据包，并且我方接收到了；

   这个时候我方确认了对方有接收和发送数据的能力；

1. 我方基于收到的数据包，向对方发送一个数据包，并且对方接收到了；

   这个时候对方确认了我方具有接收数据的能力。

至此，建立一个双工连接需要确认的 4 点都已确认完毕，这就是为什么偏偏是三次握手。

## TCP 连接的释放（四次挥手）

{% asset_img Termination-of-TCP-Connections.png TCP 链接的释放过程 %}