## 1.几种卷积

### 1.1 深度可分离卷积

> 由depthwise convolution 和 pointwise convolution组成；
>
> 考虑场景为二维卷积，输入张量形状为$W\times H\times C$，普通卷积核大小为$D1\times D2\times C$，共有N个卷积核，卷积后的结果形状为$W\times H\times N$；

* depthwise convolution：与通常的卷积操作差异很大，硬要类比来说，该卷积有$C$个卷积核，每个卷积核的通道数为1，仅对原张量的某一层进行卷积操作，不存在层间的求和；操作后形状仍为$W\times H\times C$；
* pointwise convolution：完全等同于$1\times 1$卷积；卷积核大小为$1\times 1 \times C$，有N个卷积核；

### 1.2  分组卷积

>这篇文章对于分组卷积讲的很好：https://blog.csdn.net/dujuancao11/article/details/116425390；

### 1.3 channel-wise卷积

> 这篇文章对于channel-wise卷积讲的很好：https://zhuanlan.zhihu.com/p/426653247；

* depth-wise separable channel-wise convolution：
  * 不能根据一般的分组channel-wise卷积类推，这里的channel-wise卷积核只有一个，大小为$1\times 1\times d_c$，步长为1；
  * 在“通道”这一维度引入卷积，和W，H可以看作构成三位卷积；