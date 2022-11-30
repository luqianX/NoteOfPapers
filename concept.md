## 1.几种卷积

### 1.1 深度可分离卷积

> 由depthwise convolution 和 pointwise convolution组成；
>
> 考虑场景为二维卷积，输入张量形状为$C\times W\times H$，普通卷积核大小为$D1\times D2\times H$，共有N个卷积核，卷积后的结果形状为$C\times W\times N$；

* depthwise convolution：与通常的卷积操作差异很大，硬要类比来说，该卷积有$C$个卷积核，每个卷积核的通道数为1，仅对原张量的某一层进行卷积操作，不存在层间的求和；
* pointwise convolution：完全等同于$1\times 1$卷积；卷积核大小为$1\times 1 \times H$，有N个卷积核；