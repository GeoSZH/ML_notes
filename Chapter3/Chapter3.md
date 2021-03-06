## Chapter3 
### 线性模型
线性模型形式简单、易于建模，但却蕴涵着机器学习中一些重要的基本思想.许多功能更为强大的非线性模型(nonlinear model)可在线性模型的基础上通过引入层级结构或高维映射而得.此外，由于ω直观表达了各属性在预测中的重要性，因此线性模型有很好的可解释性(comprehensibility) .例如若在西瓜问题中学得"f<sub>好瓜</sub>(x)=0.2* x<sub>色泽</sub>+0.5* x<sub>根蒂</sub>+0.3* x<sub>敲声</sub>+1" ，则意味着可通过综合考虑色泽、根蒂和敲声来判断瓜好不好，其中根蒂最要紧，而敲声比色泽更重要。

#### 一元线性回归
在一元线性回归的部分，最重要的就是我们把X，Y，W等都看作是向量，然后通过求loss function，不管是通过最小二乘法还是最大似然估计都可以得出最终的表达式，因为这次打卡剩余时间较紧，这里不以公式来展示两个推导过程而是贴出两个视频链接，分别是吃瓜教程https://www.bilibili.com/video/BV1Mh411e7VU?p=2 和白板推导https://www.bilibili.com/video/BV1aE411o7qd?p=9 ，两个都讲的比较清楚。

然而在实际的应用中仍然有需要注意的地方：

![image](https://user-images.githubusercontent.com/88269254/169829547-6d11f26f-be01-4f7d-959f-534a9e7f0f8d.png)

最后，在西瓜书的配套视频中，睿哥最后讲了我们应该注意的机器学习三要素：
- **模型**：根据具体问题，确定假设空间
- **策略**：根据评价标准，确定选取最优模型的策略（通常会产出一个“损失函数”）
- **算法**：求解损失函数，确定最优模型

#### 对数线性回归
![image](https://user-images.githubusercontent.com/88269254/169829768-c0ee3530-3343-4b2b-8c5d-913d3135ffd0.png)

#### 对数几率回归（LR）
对数几率回归就是逻辑回归，虽然逻辑回归名字里有回归，但是其实它是一个分类算法。这里视频中讲的很详细，以前我也跟另一条视频推导过逻辑回归，最大似然估计最后得出的式子其实是**负的cross entropy**。这里贴出当时的视频链接，因为中间没有对信息论的介绍，所以短一点，这个视频可以与吃瓜教程中的任选一个观看即可。https://www.bilibili.com/video/BV1aE411o7qd?p=17

这里也可以总结出三要素：

- **模型**：线性模型，输出值的范围为，近似阶跃的单调可微函数
- **策略**：极大似然估计，信息论
- **算法**：梯度下降，牛顿法

#### Fisher判别
线性判别分析LDA 的思想非常朴素: 给定训练样例集D设法将样例投影到一条直线上，使得同类样例的投影点尽可能接近、异类样例的投影点尽可能远离;在对新样进行分类时，将其投影到同样的这条直线上，再根据投影点的位置来确定新样本的类别. 图3.3 给出了一个二维示意图.

![image](https://user-images.githubusercontent.com/88269254/169839099-e8ba5d15-4f3f-4a66-9723-fec58dccdc58.png)

![image](https://user-images.githubusercontent.com/88269254/169839413-e14b07de-edbc-4546-9642-d4a2b3e9c1fd.png)

其实LDA也可以写出三要素，也是显而易见的。这里的证明没有给出详细的过程，后面有时间我手写一遍会重新添加上。再后的两个内容看看就可以，时间不太宽裕，手头还有别的事，后面有机会可能会补。
