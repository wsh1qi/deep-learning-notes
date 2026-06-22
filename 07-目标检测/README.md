# 07 · 目标检测

## 评价指标

### IoU（交并比）

$$\text{IoU} = \frac{\text{交集面积}}{\text{并集面积}}$$

### PR 曲线 & AP & mAP

- **PR 曲线**：Precision-Recall 曲线
- **AP**：Average Precision（单类别）
- **mAP**：Mean Average Precision（多类别平均）

---

## R-CNN 系列

| 方法 | 流程 | 瓶颈 |
|------|------|------|
| **R-CNN** | 取若干候选区域 → 逐区域 CNN 特征提取 → 分类 + 边界框回归 | 每个区域独立过 CNN，极慢 |
| **Fast R-CNN** | 先对整张图做卷积 → 再取候选区域 → ROI Pooling | 候选区域选择仍耗时 |
| **Faster R-CNN** | 引入 RPN（区域提议网络），将候选区域选择放到 GPU | 极大提高效率 |

### 位置精修：边界框回归

四个修正量：$dx, dy, dw, dh$

### 后处理：非极大值抑制（NMS）

将和置信度最高框重叠度过高的框删除。

---

## SSD（Single Shot Detector）

多尺度融合特征：
- 高分辨率特征图 → 检测小物体
- 低分辨率特征图 → 检测大物体

实现精确检测。

---

## DERT

CNN + Transformer 架构，端到端目标检测。
