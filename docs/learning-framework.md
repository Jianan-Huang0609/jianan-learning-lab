# 学习框架与路线 · Jianan（草案 2026-11-11）

目标：把 web coding、软件架构、AI agent、DeFi、Snowflake 这几块能力学起来，
用在企业方向上（RA 流程 AI 化、企业数据处理、Agent 落地），同时每学一块就产出一块内容
（白板视频 / 工具 / 笔记），学习即输出。

现状估计（按我已知的背景写的，错的地方请她纠正）：
- 会 Python（PubMed 抓取+翻译+AI 初筛，几百篇文献从几周压到几天）；做过 PO（CER 报告生成、PTR 对比、文献综述/一致性核查工具）；写过 HTML 页面（Hamilton 教学页、学习路径可视化）；AI 方面有 PLAN.md（从 Chatbox 到 Agentic RAG）和 Harness 三部曲讲稿。
- 没系统做过：完整 web 应用、软件架构设计、Snowflake、DeFi。

学习方式（通用规则）：
- 每条路线分 3 级，每级一个可交付物；学完一级就输出一级（视频 / 工具 / 笔记），不攒到最后。
- 每周固定 2 次学习块（每次 60–90 分钟），一次输入、一次输出；Jimmy 每两天在飞书学习空间里提醒进度。
- 材料优先用她已有的：自己的仓库、Harness 逐字稿、飞书 wiki；外部材料只做补充。

---

## Track 1 · Web Coding（网页开发）

目标：能独立做一个完整的小 web 应用（比如把学习空间、SpeakSpark 做成能用的产品页）。

- 现状：会写静态 HTML 页面（Hamilton 教学页、learning-lab、AI-Self-Starter index.html），JS 接触过但不系统。
- L1 网页基础：HTML 语义化 + CSS 布局（Flex/Grid）+ 响应式。输出：把学习空间做成一个静态网页版。
- L2 JavaScript / TypeScript：DOM、事件、fetch、模块化；再学 TypeScript 类型。输出：给 Hamilton 教学页加交互（逐句跟读、词语高亮切换）。
- L3 React + 部署：组件、状态、路由；用 Next.js 或 Vite 起项目，部署到 Vercel / GitHub Pages。输出：SpeakSpark 口语陪练最小可用版（上传音频 → 显示文本 → 对照练习）。
- 材料：MDN、React 官方文档、Next.js 官方教程；她自己的 hamilton-notebook、AI-Self-Starter。

## Track 2 · 软件架构（Software Architecture）

目标：能给一个真实系统画架构、写决策记录（ADR），不再只是“搭起来能跑”。

- 现状：ai-agent-pm-lab 的 Architect track 只有框架；CER diff / R·Agent 项目有真实需求但没画过正式架构。
- L1 设计基础：设计模式常用 10 个（单例、工厂、观察者、策略、适配器等）、分层、模块化。输出：给 CER 一致性核查工具画一张分层图。
- L2 系统设计：API 设计、数据库选型、缓存、队列、鉴权；单体 vs 微服务怎么选。输出：给 R·Agent 写一份系统设计文档（含一张架构图 + 两条 ADR）。
- L3 Agent 架构：Multi-Agent 编排、Prompt-Level 设计、Workflow Automation、State 与 Verifier。输出：把 Consistency Review Agent（QTN Day 3 项目）画成完整架构图，Router + Planner + Tools + State + Verifier 五件套齐全。
- 材料：ai-agent-pm-lab `02-architect/`、Martin Fowler 的架构文章、自己的 CER / R·Agent 代码。

## Track 3 · AI Agent（智能体）

目标：从“知道概念”到“亲手做一个能跑的 agent”，并且能讲给别人听。

- 现状：PLAN.md 8 个知识点在纸上；Harness 三部曲讲稿在手；没亲手跑通过完整闭环。
- L1 五个概念（Harness）：上下文窗口 → 记忆 Skills/Rules → RAG → 工具调用 → Plan Mode → 自主循环。材料就是崔博文三部曲逐字稿。输出：五期白板视频（每期一个概念）+ 每期一篇图文板书笔记。
- L2 亲手做：按 PLAN.md 的链路做一个最小 agent——Intent Router → Retriever → Tools → Evidence Package → Answer Planner → Claim Verifier → Reasoning Summary UI。输出：一个能跑的 Chatbox + 7 项验收交付物（链路图、Intent Route 表、Tool Calling 计划、Evidence Package 结构、Answer Planner 骨架、Reasoning Summary 方案、升级路线图）。
- L3 评测与部署：Eval（准确率、幻觉率）、日志追踪、部署到自己的小服务。输出：一份 eval 报告 + 一个可演示的 agent 链接。
- 材料：`jianan-learning-lab/docs/agentic-rag-chatbox/PLAN.md`、Harness 逐字稿、`minimal-rag/`、`embedding-models/`。

## Track 4 · DeFi 框架（⚠️ 待确认方向）

- 现状：不知道她说的 DeFi 具体指什么。以下按“去中心化金融”写的，如果意思不对请她纠正（也可能是她想学的别的框架名）。
- 如果是去中心化金融：
  - L1 区块链基础：钱包、交易、Gas、智能合约是什么。输出：一篇自己的解释笔记（白板视频可做一期）。
  - L2 DeFi 协议：AMM（Uniswap）、借贷（Aave）、质押、稳定币。输出：一张 DeFi 全景图（自己画的板书）。
  - L3 风险与合规：智能合约风险、监管视角（结合她的 RA 背景：合规思维是优势）。输出：一篇“DeFi 合规视角”笔记。
- 如果不是这个意思：把这条 track 换成她说的那个框架，路线重写。

## Track 5 · Snowflake 数据处理

目标：知道 Snowflake 是什么、会用、能处理真实数据（先从她自己的文献/注册数据入手）。

- 现状：没用过（按她问的“这个咋用？是啥？怎么处理的数据？”判断为零基础）。
- L1 是什么：Snowflake 是云数据仓库，存算分离、按用量计费；和 Excel / 本地数据库的区别。输出：一页自己的解释笔记（“Snowflake 一句话”+ 一张对比表）。
- L2 会用：SQL 基础（SELECT / JOIN / GROUP BY / 窗口函数）、建库建表、加载数据（COPY / Snowpipe）。输出：把一批 PubMed 文献数据导进 Snowflake，跑通 5 个查询。
- L3 处理数据：ETL/ELT、数据建模（星型模型）、DBT、做看板。输出：一个“文献初筛数据看板”（比如按年份/期刊/主题统计），能讲清楚数据从哪来、怎么洗、怎么用。
- 材料：Snowflake 官方免费试用账号 + 官方文档、DBT 官方教程；她自己的 PubMed 数据。
- 企业连接：Siemens Healthineers 内部数据方向——先把个人小项目跑通，再看企业场景怎么接（需她补充公司内部情况）。

## 企业方向（总目标）

这五条线最终汇到一处：RA 流程 AI 化 + 企业数据 + Agent 落地。
- 短期锚点：Consistency Review Agent（QTN Day 3 项目）——Track 2 的 L3 和 Track 3 的 L2/L3 都指向它。
- 中期锚点：把 CER / 文献 / 注册文档的数据流跑进 Snowflake（Track 5 的 L3），变成可复用的数据资产。
- 长期锚点：Web Coding（Track 1 的 L3）+ 软件架构（Track 2）做出能给团队用的小产品（SpeakSpark 或 RA 助手）。

## 进度追踪（飞书学习空间里同步）

- 每条 track 一个 session：目标 / 当前级别 / 本周任务 / 待做清单 / 完成打勾。
- 顶部一块空白 idea 板：任何想法随时扔进去，Jimmy 每两天分拣（待看 / 进行中 / 已用 / 放弃）。
- 提醒：Jimmy 每两天检查一次进度，没动静就提醒她；每周对照一次“学了什么、产出了什么”。
