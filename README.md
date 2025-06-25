# CIFAR-10 卷积神经网络分类实验

本项目基于卷积神经网络（CNN）实现了对 CIFAR-10 图像数据集的分类任务，包含模型训练、测试、权重保存与结果可视化等完整流程，适合深度学习初学者和相关课程实验参考。

## 目录结构

```
test/
├── CIFAR10_CNN_weights.h5   # 训练好的CNN模型权重文件
└── test.py                  # 主程序：模型定义、训练、测试与权重保存
```

## 环境依赖

- Python 3.7+
- tensorflow
- matplotlib
- numpy

建议使用虚拟环境进行依赖管理：

```bash
pip install tensorflow matplotlib numpy
```

## 文件说明

- `test.py`  
  主程序文件，包含以下主要功能：
  - 加载 CIFAR-10 数据集
  - 数据预处理与归一化
  - 定义卷积神经网络结构
  - 模型训练与测试，准确率输出
  - 保存训练好的模型权重为 `CIFAR10_CNN_weights.h5`
  - 训练过程与结果的可视化（损失与准确率曲线、预测样例展示）

- `CIFAR10_CNN_weights.h5`  
  已训练好的模型权重文件，可直接用于模型加载与推理，无需重复训练。

## 快速开始

1. 安装依赖（见上文）。
2. 运行主程序：

   ```bash
   python test/test.py
   ```

   程序将自动训练模型并保存权重到 `CIFAR10_CNN_weights.h5`，如已存在权重文件可直接加载进行测试和可视化。

## 结果展示

- 训练与验证集的损失、准确率曲线将自动绘制。
- 随机选取10张测试图片，展示其真实标签与模型预测结果。
- 训练和测试过程中的时间点会在终端输出。

## 参考

- [TensorFlow 官方文档](https://www.tensorflow.org/)
- [CIFAR-10 数据集介绍](https://www.cs.toronto.edu/~kriz/cifar.html)
