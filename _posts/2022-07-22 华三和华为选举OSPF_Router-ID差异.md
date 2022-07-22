---
title:      「小探讨」华三和华为选举OSPF Router-ID差异
date:        2022-07-22
author:      Zhy
header-style: text
catalog: true 
tags:
    - 网络
    - 华三和华为差异化
---

有关华三和华为 OSPF R-ID选举的小探讨

笔者最近在备战华三考试时看到笔试题有个选项很有趣，叫做‘华三设备OSPF选举router-id的区别’ 本着华为优选最先配置的地址，想当然的选了之后发现是错了，立马就做了个实验复现一下，记录下来也方便以后会看。

配置命令即结果如下

下图所示为华为配置：

![image-20220722112841747](https://s1.ax1x.com/2022/07/22/jO9j3Q.png)



下图所示为华三配置：

![image-20220722112848644](https://s1.ax1x.com/2022/07/22/jOCpBq.png)



结论：

1. 华三是遵循国际标准所规定的优选活跃Loopback接口大的次选活跃物理接口的IP地址。
2. 华为是优选最先配置了接口的IP地址作为Router-ID