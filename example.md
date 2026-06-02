---
unit_code: "10359"
student_id: "2023210000"
security: ""
classification: "TP391"
degree_category: "学历硕士"
title_zh: "基于深度学习的图像分类方法研究"
title_en: "Research on Image Classification Methods Based on Deep Learning"
author: "张三"
author_en: "Zhang San"
advisor_name: "李四"
advisor_title: "教授"
major: "计算机科学与技术"
research_direction: "人工智能与模式识别"
complete_time: "2026年6月"
complete_month_en: "June"
complete_year_en: "2026"

defense_committee:
  chair: "专家工作单位，职称，姓名"
  members:
    - "专家工作单位，职称，姓名"
    - "专家工作单位，职称，姓名"
    - "专家工作单位，职称，姓名"
  advisor: "合肥工业大学，教授，李四"

graduation_destination:
  work_unit: ""
  telephone: ""
  email: ""
  address: ""
  postcode: ""

acknowledgments: |
  本论文是在导师李四教授的悉心指导下完成的。李老师严谨的治学态度、渊博的学识和对科研工作的热忱使我受益良多，在此表示衷心感谢。

  感谢课题组同学在实验设计、数据分析和论文撰写过程中给予的帮助。

  作者：张三
  2026年6月2日

abstract_zh: |
  随着人工智能技术的快速发展，深度学习在图像分类领域取得了显著成果。本文针对传统图像分类方法准确率不高、泛化能力不足的问题，提出一种基于改进卷积神经网络的图像分类方法。

  本文首先对现有图像分类方法进行系统综述，然后在经典残差网络结构中引入注意力机制，设计新的特征增强模块。实验结果表明，所提方法在多个公开数据集上取得了较好的分类性能。
keywords_zh: [深度学习, 图像分类, 卷积神经网络, 注意力机制, 迁移学习]

abstract_en: |
  With the rapid development of artificial intelligence, deep learning has achieved remarkable progress in image classification. This dissertation proposes an improved convolutional neural network method to address the limitations of traditional image classification approaches.

  Existing methods are reviewed first, and then an attention mechanism is introduced into a residual network to construct a feature enhancement module. Experimental results show that the proposed method achieves competitive classification performance on public datasets.
keywords_en: [deep learning, image classification, convolutional neural network, attention mechanism, transfer learning]

references:
  - "何凯明，张翔宇，任少卿，等．深度残差学习用于图像识别[J]．IEEE计算机视觉与模式识别会议，2016：770-778．"
  - "Vaswani A., Shazeer N., Parmar N., et al. Attention is all you need[C]. Advances in Neural Information Processing Systems, 2017: 5998-6008."

appendix: |
  附录1 主要符号说明

  CNN：卷积神经网络。

academic_achievements: |
  1）参加的学术交流与科研项目

  （1）面向图像分类的深度学习方法研究，校级研究生创新项目，2025-2026。

  2）发表的学术论文（含专利和软件著作权）

  （1）张三，李四. 基于注意力机制的图像分类方法[J]. 计算机应用研究，2026，43(1)：1-8.
---

# 第一章 绪论

## 1.1 研究背景

图像分类是计算机视觉领域中最基本也是最重要的任务之一。随着互联网和移动设备的普及，图像数据规模持续增长，如何高效准确地对海量图像进行自动分类成为亟待解决的问题。

深度学习技术的出现为图像分类带来了重要变化。自卷积神经网络在大规模图像识别任务中取得突破以来，基于深度学习的图像分类方法已经成为主流研究方向。

## 1.2 国内外研究现状

### 1.2.1 传统图像分类方法

传统图像分类方法主要依赖人工设计的特征提取器。这些方法在特定场景下表现良好，但泛化能力有限，难以适应复杂多变的实际应用环境。

### 1.2.2 基于深度学习的方法

近年来，卷积神经网络在图像分类任务中取得显著进展。网络结构不断深化，特征表达能力持续提升。

# 第二章 相关理论与技术

## 2.1 卷积神经网络基础

卷积神经网络是一类适合处理网格结构数据的深度学习模型，其核心组件包括卷积层、池化层和全连接层。

表2.1 不同方法在示例数据集上的分类准确率
Tab 2.1 Classification accuracy of different methods on the example dataset

| 方法 | 准确率(%) | 参数量(M) |
|---|---:|---:|
| VGG-16 | 93.2 | 138.4 |
| ResNet-50 | 95.1 | 25.6 |
| 本文方法 | 96.5 | 26.8 |

# 第三章 总结与展望

## 3.1 工作总结

本文针对图像分类任务，提出一种基于改进卷积神经网络的分类方法。通过引入注意力机制，有效提升了模型的特征表达能力和分类性能。
