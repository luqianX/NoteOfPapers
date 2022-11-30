# 用于DeepFake视频检测的动态不一致性学习

* 

## 0.摘要

## 1.简介

* 随着基于深度学习的方法，特别是生成模型的快速发展，各种DeepFake技术（Koujan等人2020；Nirkin、Keller和Hassner 2019）已被提出。由于这些技术可以合成越来越逼真的DeepFake，而这些DeepFakes很难被人类识别，因此滥用它们很容易在全球引发严重的社会问题或政治威胁。因此，开发有效的人脸伪造检测方法具有重要意义。
* 许多研究人员最近开发了基于视频的方法来捕捉深度伪造视频帧间的不一致性，作为DeepFake检测的辨别线索。
  * 早期的方法将此任务视为一般的时间建模问题，并应用LSTM（Sohrawardi等人2019）和3DCNN（Zi等人2020）等经典方法来解决此问题。然而，它们不是专门为DeepFake检测而设计的，因此性能较差，更不用说计算成本高了。
  * 最近的一些工作开始研究DeepFake视频中定位伪造痕迹的不一致性，例如S-MIL（Li et al 2020a）和STIL（Gu et al 2021），并显示出良好的结果。最先进的STIL观察到，真实视频中相邻帧之间的运动比假视频更平滑。他们将这一线索称为不一致性的一种形式，并利用相邻帧之间的时间差异对其进行建模。然而，他们对每个视频应用稀疏采样策略，采样帧的间隔可能太大，无法捕获由细微运动导致的这种不一致性。
* Intra-SIM和Inter-SIM都作为即插即用模块，可以集成到现成的2D-CNN网络中。

## 3.方法

> **段内模块**捕获细粒度的短期运动信息（capture fine-grained short-term motion information）

### 3.1 段内模块Intra-Snippet Inconsistency Module

<img src=".\appendix\002.png" alt="image-20221129231513295" style="zoom: 67%;" />

* 原论文的**Intra-SIM** 框架如上图所示；
* ChannelNet论文地址：**[https://arxiv.org/abs/1809.01330](https://links.jianshu.com/go?to=https%3A%2F%2Farxiv.org%2Fabs%2F1809.01330)**；
* <font color='red'>？这个注意力机制是怎么个原理，还有最后的深度可分离卷积怎么实现的</font>

### 3.2 段间模块Inter-Snippet Interaction Module

* <font color='red'>？核心问题还是在于他的注意力机制是怎么一回事，不能直接用自注意力实现吗</font>

