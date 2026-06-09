# PLAN.md — 嵌入模型原理

## 基本信息
- 课件ID: embedding-models
- Node ID: ext-d4e5f6g2
- 学段: 成人/在职
- 学科: 信息技术
- 课型: new-concept

## 问题锚点
计算机怎么理解"猫"和"狗"这两个词的意思相近？

## 教学骨架
### ABT叙事
- And: 我们知道计算机只能处理数字
- But: 最简单的One-Hot编码无法表达语义相似性
- Therefore: 稠密嵌入向量将语义映射到高维空间，余弦相似度量化语义距离

### 核心知识点
1. One-Hot → 稠密向量：词嵌入的演进
2. 余弦相似度：数学定义与直观理解
3. 主流嵌入模型对比（text-embedding-3, bge, jina）
4. PCA/t-SNE降维可视化
5. 嵌入在RAG/搜索/分类中的应用

### 互动设计
- 向量相似度计算器（输入两个词，计算余弦相似度）
- 语义空间Canvas可视化
- t-SNE聚类Canvas示意
- 模型对比表

## 页面结构（15页）
0. 封面
1. 问题锚点
2. 学习目标
3. 前测
4. One-Hot到稠密向量
5. 余弦相似度详解
6. 相似度计算器（Canvas互动）
7. 主流模型对比（含表格）
8. 降维可视化（Canvas互动）
9. 嵌入实战应用（习题讲解）
10. 概念测试
11. 后测
12. 小结
13. 知识图谱
14. AI学伴

## 资源清单
- Hero: assets/embedding-models-hero.svg (4.9KB)
- TTS: tts/s01.mp3, tts/s02.mp3, tts/s03.mp3
- Canvas: semantic-space-canvas, tsne-viz-canvas
