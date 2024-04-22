---
date: 2018-12-12 13:24:49
layout: post
title: MobileNet模型
subtitle: 目标分类
description: 
image: https://res.cloudinary.com/dm7h7e8xj/image/upload/v1559824021/theme12_e0vxlr.jpg
optimized_image: https://res.cloudinary.com/dm7h7e8xj/image/upload/c_scale,w_380/v1559824021/theme12_e0vxlr.jpg
subtitle: Lorem ipsum dolor sit amet, consectetur adipisicing elit.
category: 'blog'
tags:
  - CNN
  - 目标分类
author: mranderson
---

## MobileNet模型
MobileNet是一系列用于计算机视觉任务的深度卷积神经网络模型，支持ONNX格式表示，它的设计目标是在保持高准确性的同时减小模型的大小和计算复杂度，以便在移动设备和嵌入式系统上高效运行。MobileNet模型系列由Google团队于2017年首次提出，之后不断进行改进和扩展。以下是MobileNet模型的简介以及一个示意图来说明其工作原理：
模型结构：
MobileNet的主要特点是采用了深度可分离卷积（Depthwise Separable Convolution）结构，这种结构在保持模型性能的同时，大幅减小了模型的参数数量和计算量。MobileNet的基本结构如下：
深度可分离卷积（Depthwise Separable Convolution）： MobileNet将标准卷积操作分为两步。首先是深度卷积，也称为逐通道卷积，它对每个输入通道进行单独的卷积操作。然后是逐点卷积（Pointwise Convolution），它使用1x1卷积核来组合不同通道的特征。这种结构大幅减小了计算成本和参数数量。
卷积块（Convolution Block）： MobileNet通常由多个深度可分离卷积层组成的卷积块构成，每个卷积块后跟一个非线性激活函数（如ReLU）。
全局平均池化（Global Average Pooling）： 在模型的最后一层，特征图通过全局平均池化操作降维为一个向量。
全连接层（Fully Connected Layer）： 向量通过一个或多个全连接层，最终用于图像分类或其他任务。
