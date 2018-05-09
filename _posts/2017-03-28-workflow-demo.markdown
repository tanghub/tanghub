---
layout:     post
title:      "IOS Workflow 初探"
subtitle:   "IOS Workflow Demo"
date:       2017-03-28
author:     "Tang"
header-img: ""
header-mask: 0.3
catalog:    true
tags: life
    
---


Workflow 在被[Apple Inc.](http://www.apple.com/)收购之后开始了免费之路，一下子火了起来，国人对免费向来比较崇尚，身边的人用的人也越来越多...

那么Workflow究竟是什么，能给我们那么大吸引呢?个人感觉他的能力主要体现在简单、高效。将需要N步完成的事情（操作）串联成一步，大大提高了效率，随着他的更新似乎也出现了类似编程的扩展性，可玩性非常高。

我们先来一个生活中的场景做演示。作为一个生活在杭州的人，生活已经离不开蚂蚁的支付宝，不带钱的生活已经再普通不过了。那么支付宝的最常用场景是要么你扫别人码支付，要么别人扫你码支付。通常的做法是：找到支付宝->打开支付宝->点击扫一扫，或者付款。对一个装了很多应用的人来说去找这个动作是很费时的（当然你或许会放在常用位置），通过workflow可以见到两步，选择支付-选择扫码还是支付，OK结束（看着没减少啥步骤，但试想如果将微信支付加进去这个就省时了）。

下面是一个通过workflow制作的AliPay，您可以清楚的看到执行过程，非常简单。
![w1](/img/workflow/workflow-pay1.PNG)![w1](/img/workflow/workflow-pay2.PNG)

其中涉及支付的url schema 如下：
* 扫码支付 `alipayqr://platformapi/startapp?saId=10000007`
* 支付码 `alipayqr://platformapi/startapp?saId=20000056`

大致交互流程为，选择一种支付方式直接打开对应的支付宝界面，最终效果参考如下：
![w3](/img/workflow/workflow-pay3.PNG)

workflow的使用操作简单，大家可自行创建分享，可玩性很高。个人理解是workflow通过action的输入(input)输出(result)来做串联，同时提供一些增强的功能，比如IF，SELECT 等，对一些具有一定编程能力的人来说用起来很暂。