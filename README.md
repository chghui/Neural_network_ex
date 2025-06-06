# 🧠 Neural Network - Classification of Handwritten Digits (ex3)

## 📘 项目简介

本项目基于吴恩达《机器学习》课程中的 Exercise 3，使用\*\*前馈神经网络（Feedforward Neural Network）\*\*对手写数字进行分类。数据来源于经典的 MNIST 类似数据集，共有5000张20×20像素的灰度图像。

该 Notebook **无需训练模型**，直接加载已经训练好的神经网络参数（Theta1 和 Theta2），并通过前向传播算法进行预测。



## 📚 内容结构

Notebook 包含以下主要部分：

1. **数据可视化**：

   * 随机展示部分手写数字样本，帮助理解输入数据的结构。
2. **神经网络前向传播实现**：

   * 实现 `predict()` 函数，使用训练好的模型进行多分类预测。
3. **模型评估**：

   * 计算模型在训练集上的准确率，并逐个预测部分样本展示预测效果。
4. **神经网络原理介绍（结合PPT使用）**：

   * 与讲解PPT联动，理解输入层、隐藏层、输出层的矩阵运算流程。
   * 理解激活函数（sigmoid）和 softmax 在输出中的作用。



## 🧠 神经网络结构说明

* **输入层**：400个神经元（对应20×20像素）
* **隐藏层**：25个神经元，使用 sigmoid 激活函数
* **输出层**：10个神经元，代表10个数字类（1到10，其中“0”被表示为“10”）

前向传播计算过程：

```python
z2 = X.dot(Theta1.T)
a2 = sigmoid(z2)
a2 = np.insert(a2, 0, 1, axis=1)  # 添加偏置项
z3 = a2.dot(Theta2.T)
a3 = sigmoid(z3)
```



## ▶️ 如何运行

1. 环境要求：

   * Python 3.x
   * NumPy, Matplotlib, Scipy
   * Jupyter Notebook

2. 运行步骤：

   * 启动 Jupyter Notebook
   * 打开 `ex3-neural network.ipynb`
   * 按顺序运行所有代码单元，即可完成预测与可视化分析。



## 📊 结果示例

* **预测准确率**：约为 **98%**



## 🔗 扩展资料与参考链接

* 吴恩达课程官网：[https://www.coursera.org/learn/machine-learning](https://www.coursera.org/learn/machine-learning)
