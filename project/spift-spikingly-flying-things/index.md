---
layout: project
title: SPIFT(SPIkingly Flying Things)
image: images/dataset_image/spift.png
tags:
  - optical flow
  - simulate
  - dataset
collaborators: 
collaborator_icons: []
---

用途：主要用作训练集，包含随机生成的高速运动场景。  
场景类别：100类，每类包含500帧脉冲流。  
光流标签：稠密光流场（每像素包含水平与垂直位移）。每隔10帧(Δt=10)和20帧(Δt=20)生成光流，共50,000帧标签。  
数据格式：脉冲流为二进制矩阵(H×W×N)，光流标签为二维运动矢量场(H×W×2)。  
附加数据：部分场景提供重建灰度图，用于可视化验证。  
### 可支持的任务：
- 光流估计：利用脉冲流直接训练端到端模型(如 SCFlow)。
- 运动去模糊：通过 FAW(Flow-guided Adaptive Window) 验证运动模糊的抑制效果。
- 跨模态分析：研究脉冲流与重建图像/事件流的关联。

数据集链接：待更新
{% include figure.html image="/images/dataset_image/spift_result_1.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/spift_result_2.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/spift_result_3.gif" caption="随机抽取示例如上（每隔10帧生成光流）" width="100%" %}