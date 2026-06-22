# 06 · 卷积神经网络

## SIFT 算法

尺度不变特征变换（Scale-Invariant Feature Transform）：传统计算机视觉中的关键点检测与特征描述算法。

---

## 卷积操作参数

| 参数 | 含义 |
|------|------|
| Depth（深度） | 卷积核数量（输出通道数） |
| Stride（步长） | 卷积核滑动步长 |
| Padding（填充） | 边缘补零 |
| Bias（偏置） | 每个输出通道的偏置项 |

---

## 经典架构

| 网络 | 核心创新 |
|------|----------|
| **VGG** | 使用小卷积核（3×3）堆叠增加深度 |
| **GoogleNet** | Inception 模块：多尺度并行卷积 |
| **ResNet** | 残差连接（Skip Connection），解决深层退化 |

> 层数越深，训练效果越好（在 ResNet 出现后方可实现真正的深层训练）。

---

## 归一化方法

| 方法 | 归一化维度 |
|------|-----------|
| Batch Norm | 对 batch 维度归一化 |
| Layer Norm | 对 feature 维度归一化（Transformer 常用） |
