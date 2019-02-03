MPL:Multi-Layer Perceptron--多层感知机
=====
>A multilayer perceptron (MLP) is a class of **feedforward artificial neural network**. An MLP consists of, at least, three layers of nodes: an input layer, a hidden layer and an output layer. Except for the input nodes, each node is a neuron that uses a nonlinear activation function. MLP utilizes a supervised learning technique called backpropagation for training.Its multiple layers and non-linear activation distinguish MLP from a linear perceptron. It can distinguish data that is not linearly separable.

>多层感知器是一种前向结构的**人工神经网络**，映射一组输入向量到一组输出向量。MPL可以被看做是一个有向图，由多个节点组成，每一层都全连接到下一层。除了输入节点，每个节点都是一个带有非线性激活函数的神经元（或称处理单元）。一种被称为反向传播算法的监督学习方法常被用来训练MPL。MPL是感知机的推广，克服了感知机感知器不能对线性不可分数据进行识别的弱点。
>>感知器（Perceptron），是一种最简单形式的前馈神经网络，是一种**二元线性分类器**。常用的感知机学习算法有：感知机学习、最小二乘法和梯度下降法。为了模拟神经细胞行为，与之对应的感知基础概念是：权量（突触）,偏置（阈值）以及激活函数（细胞体）。在人工神经网络中，感知机也被指为单层的人工神经网络，以区别于较复杂的多层感知机。走位一种线性分类器，感知机可以说是最简单的前向人工神经网络形式。尽管结构简单，感知机能够学习并且解决相当复杂的问题。感知机主要的被指却显示他不能处理线性不可分问题。
>>>https://en.wikipedia.org/wiki/Perceptron 

>>**线性可分与线性不可分**,模式识别中的概念，简单的说如果用一个线性函数可以将两类样本完全分开，就称作这些样本是'线性可分的'。

>>**超平面**，超平面是n维欧式空间中余维等于一的线性子空间，也就是必须是(n-1)维度。这是平面中的直线、空间的平面之推广(n>3才被成为"超"平面），是纯粹的数学概念，不是现实的物理概念。因为是子空间，所以超平面一定经过原点。

>>反向传播算法（Backpropagation --BP）,(也可以指蒙特卡洛树中向上传播的搜索树的方式)，是“误差反向传播”的简称，是一种与最优化方法（如梯度下降法）结合使用的，用来训练人工神经网络的常见方法，该方法对网络中所有的权重计算损失函数的梯度。这个梯度会返回给最优化方法，用来更新权值以最小化损失函数。反向传播要求对每个输入值想得到的已知输出，来计算损失函数梯度。一次，它通常被认为是一种监督式学习方法，虽然他也在一些无监督网络（如自动编码器）中。它是多层前馈网络的Delta规则的推广，可以用链式法则对每层迭代计算梯度。反向传播要求人工神经单元的激励函数可微。
>>>````
>>>初始化网络权值（通常是小的随机值）
>>>  do
>>>     forEach 训练样本 ex
>>>        prediction = neural-net-output(network, ex)  // 正向传递
>>>        actual = teacher-output(ex)
>>>        计算输出单元的误差 (prediction - actual)
>>>        计算 $\Delta w_{h}$ 对于所有隐藏层到输出层的权值  // 反向传递
>>>        计算 $\Delta w_{i}$ 对于所有输入层到隐藏层的权值  // 继续反向传递
>>>        更新网络权值 // 输入层不会被误差估计改变
>>>  until 所有样本正确分类或满足其他停止标准
>>>  return 该网络
>>>````



[^_^]:#("超平面")
[^_^]:#("注释")
<div align="center">
<img src="./resource/MPL-1.png" width="300" height="150" />
</div>



( x^2)$