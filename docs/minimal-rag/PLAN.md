# PLAN.md — 最小RAG流程

## 基本信息
- 课件ID: minimal-rag
- Node ID: ext-a1b2c3d1
- 学段: 成人/在职
- 学科: 信息技术
- 课型: new-concept

## 问题锚点
没有RAG的LLM为什么会胡说八道？怎么让AI基于真实文档回答？

## 教学骨架
### ABT叙事
- And: LLM训练时学到了大量世界知识
- But: 训练数据有截止日期，不含私有文档，容易产生幻觉
- Therefore: RAG在推理时检索外部文档，让LLM有据可依

### 核心知识点
1. 文档加载与分块（TextLoader, RecursiveCharacterTextSplitter）
2. 文本嵌入（OpenAIEmbeddings, text-embedding-3-small）
3. 向量存储与检索（ChromaDB, 相似度搜索）
4. 提示构建与生成（retrieval chain, RAG prompt template）
5. 端到端流程：加载→分块→嵌入→存储→检索→生成

### 互动设计
- Canvas绘制RAG管线流程图（悬停查看每步详情）
- 代码编辑器片段（可复制运行的Python代码）
- 检索结果对比展示

## 页面结构（15页）
0. 封面
1. 问题锚点
2. 学习目标
3. 前测
4. LLM幻觉问题
5. RAG五步管线
6. 管线可视化（Canvas互动）
7. 动手写代码（代码编辑器）
8. 检索质量对比
9. 完整RAG Chain实现（习题讲解）
10. 概念测试
11. 后测
12. 小结
13. 知识图谱
14. AI学伴

## 资源清单
- Hero: assets/minimal-rag-hero.svg (4.9KB)
- TTS: tts/s01.mp3, tts/s02.mp3, tts/s03.mp3
- Canvas: rag-pipeline-canvas
