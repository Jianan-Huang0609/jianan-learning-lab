# PLAN.md — 从 Chatbox 到 Agentic RAG

## 基本信息
- 课件ID: agentic-rag-chatbox
- 学段: 成人/在职
- 学科: AI Engineering / Product Architecture
- 课型: new-concept + architecture walkthrough
- 主题: NotebookLM-like QA 系统的 Chatbox、Intent、RAG、Agent Design、工具调用与可解释输出

## 问题锚点
一个看起来简单的 Chatbox，后端到底如何判断用户意图、检索文档、调用工具、组织证据、生成可信答案，并把“思考过程”展示给用户？

## ABT 叙事
- And: 用户希望像 NotebookLM 一样，直接对文档提问并得到清晰答案。
- But: 如果只是把问题和文档片段丢给 LLM，容易出现检索不准、引用无效、答案粗糙、思考过程不可审计。
- Therefore: 需要把 Chatbox 设计成 Agentic RAG 入口：Intent Router → Retriever → Tools → Evidence Package → Answer Planner → Claim Verifier → Reasoning Summary UI。

## 核心知识点
1. Chatbox 不是输入框，而是任务调度入口
2. Intent Recognition：definition / process_operation / evidence_lookup / comparison / summary / table_lookup
3. RAG 不是向量数据库，而是证据供应链
4. 当前项目状态：文件型 canonical store + runtime chunk + lexical hybrid retrieval
5. Agentic Design：Router + Planner + Tools + State + Verifier
6. Tool Calling：后端函数调用与日志追踪
7. Reasoning Summary：展示可解释执行轨迹，不暴露 raw CoT
8. 升级路线：Direct Source Read、Eval、Persistent Index、Vector、Answer Planner、Claim Verifier

## 页面结构
1. 封面：从 Chatbox 到 Agentic RAG
2. Chatbox 背后发生了什么
3. Intent Recognition
4. RAG 五层结构
5. 当前项目真实链路
6. Agentic Design
7. 工具调用
8. 思考链路展示
9. Workshop 练习
10. 项目升级路线图

## 交付物
- `index.html`：GitHub Pages 可直接打开的单页课件
- `PLAN.md`：教学设计说明

## 自学验收标准
学习者完成本课后，应能独立输出：
1. Chatbox 后端总链路图
2. Intent Route 表
3. Tool Calling 计划
4. Evidence Package 数据结构
5. Answer Planner 答案骨架
6. Reasoning Summary 展示方案
7. 当前项目升级路线图

## 课堂产出任务
用问题“R2 阶段 PO 应该做什么？”完成一次端到端设计：
- route = process_operation
- 检索 Procedure / Scope / Deliverables / R2 相关章节
- 回读 citation 前后文
- 构建 evidence package
- 按角色、阶段、动作、交付物组织答案
- 用 claim verifier 检查每个事实句是否有引用支持


## Tool 分类说明
本课中的 Tool 不是只指 RAG 检索工具，而是 Agentic QA 后端可调用能力：
1. Retrieval tools：section search、fulltext、vector search、table lookup
2. Context tools：direct source context reader、citation context reader
3. Evidence tools：evidence package builder、citation validator
4. Planning tools：answer planner、answer slot filler
5. Verification tools：claim verifier、groundedness checker
6. UI/trace tools：reasoning summary renderer、reference renderer
