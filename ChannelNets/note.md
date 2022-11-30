# ChannelNets: Compact and Effificient Convolutional Neural Networks via Channel-Wise Convolutions

## 0.摘要

* 卷积神经网络（CNN）已显示出解决各种人工智能任务的强大能力。然而，不断增加的模型大小在资源有限的应用中使用它们时带来了挑战。

* ChannelNets使用三种channel-wise卷积实例：group channel-wise卷积， depth-wise separable channel-wise卷积，和卷积分类层。 

* ChannelNets在参数数量和计算成本方面实现了显著降低，而不损失准确性。值得注意的是，我们的工作是首次尝试压缩完全连接的分类层，这通常占紧凑型神经网络总参数的25%。

  

## 1.简介

## 2.背景和动机

## 3.Channel-Wise Convolutions和ChannelNets

> 在这项工作中，我们在第3.1节中提出了channel-wise convolution，基于此我们构建了**ChannelNets**。在第3.2节中，我们应用group channel-wise convolutions来解决分组引起的信息不一致问题。然后，我们在第3.3节中推广了我们的方法，这导致了深层中深度方向可分离卷积的直接替换。通过对广义方法的分析，我们提出了一个卷积分类层来代替第3.4节中的完全连接输出层，这进一步减少了参数和计算量。最后，第3.5节介绍了**ChannelNets**的体系结构。

### 3.1 Channel-Wise Convolutions

### 3.2 Group Channel-Wise Convolutions

### 3.3 Depth-Wise Separable Channel-Wise Convolutions

* 1×1组卷积简单地缩放深度卷积中的卷积核。由于每一层中的批归一化[8]已经涉及缩放项，因此1×1组卷积变得多余，可以删除。
* 