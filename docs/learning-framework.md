# 学习框架与路线 · Jianan（草案 2026-11-11）

目标：把 web coding、软件架构、AI agent、Vibe Coding、Snowflake 这几块能力学起来，
用在企业方向上（RA 流程 AI 化、企业数据处理、Agent 落地），同时每学一块就产出一块内容
（白板视频 / 工具 / 笔记），学习即输出。

现状估计（按我已知的背景写的，错的地方请她纠正）：
- 会 Python（PubMed 抓取+翻译+AI 初筛，几百篇文献从几周压到几天）；做过 PO（CER 报告生成、PTR 对比、文献综述/一致性核查工具）；写过 HTML 页面（Hamilton 教学页、学习路径可视化）；AI 方面有 PLAN.md（从 Chatbox 到 Agentic RAG）和 Harness 三部曲讲稿。
- Vibe Coding：已经形成不少正确直觉（2026-07-15 面试四问归档），但还没固化成一套企业可识别、可验证、可展示的工程方法；方法 Gap 和认证证据 Gap 最大。
- Snowflake：公司已经在用，但她还没开始用——先搞清公司内部怎么用。
- 没系统做过：完整 web 应用、软件架构设计。

飞书学习空间在 Jianan Brain（学习知识中枢）里，不是单拎出来的新空间：每条线都连着她原来已有的内容（学习路径整合、个人目标与学习规划、AI Agent 学习资源地图、AI学习笔记、Vibe Coding 面试四问等），每条线的页面里都有“学习笔记”区——学完把总结写在里面，不只是打勾的清单。

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

## Track 4 · Vibe Coding（用 AI 写代码）

目标：把 Vibe Coding 固化成一套企业可识别、可验证、可展示的工程方法——不只是“会用 AI 写代码”。

- 现状（2026-07-15 面试四问归档）：她不是“不会 Vibe Coding”，而是已经形成不少正确直觉，但还没固化成方法。理论 Gap 中等；方法 Gap 较高（文件职责、Source of Truth、状态流转、需求到测试的追踪关系没完全定义）；实践 Gap 不均衡（企业后端联调、权限、安全、设计系统、CI/CD、可观测和回滚的闭环证据偏弱）；认证证据 Gap 最高（需要真实项目里的文档、PR、测试报告、CI 结果和运行截图组成证据包）。表达方式要从“我有这些文件”改成“我遇到这个问题，做了这个判断，用这些文件控制实施，最后通过这些测试和结果证明它有效。”
- 文件规范（六个文件的职责边界）：`PRD.md`（为什么做、为谁做、解决什么问题、成功指标）；`spec.md`（系统必须表现成什么样、边界和验收条件）；`plan.md`（如何实现、分几个 phase、依赖和风险）；`tasks.md`（谁在什么时候完成哪个可验收任务）；`progress.md`（当前在哪、阻塞、下一步）；`CHANGELOG.md`（各版本对用户可见的新增、修改和修复）。
- L1 文件规范：把一个小项目按六个文件拆清楚，建立“需求 → 任务 → 代码变更 → 测试”的追踪关系。输出：一套六文件模板 + 一个小项目的完整证据包。
- L2 工程闭环：企业后端联调、权限、安全、设计系统、CI/CD、可观测、回滚。输出：一个带 CI + 测试报告 + 运行截图的项目。
- L3 方法沉淀：把做法写成可复用的方法（skill / 模板），能讲给别人听。输出：一篇方法笔记 + 一期白板视频（Vibe Coding 主题）。
- 材料：飞书《AI 产品经理 Vibe Coding 面试四问》、学习路径整合 Track A（已经在用 Claude Code / OpenClaw / 各 coding agent 做实际工作）。

## Track 5 · Snowflake 数据处理

目标：用上公司已经在用的 Snowflake，能处理真实数据（先从她自己的文献/注册数据入手，再接企业场景）。

- 现状：公司已经在用 Snowflake，但她还没开始用。先搞清公司内部怎么用，再学。
- L0 企业内切入点：找到公司里 Snowflake 的现有用法（谁在用、用在哪个项目、数据从哪来、权限怎么开）。输出：一页“公司 Snowflake 现状”笔记。
- L1 是什么：Snowflake 是云数据仓库，存算分离、按用量计费；和 Excel / 本地数据库的区别。输出：一页自己的解释笔记（“Snowflake 一句话”+ 一张对比表）。
- L2 会用：SQL 基础（SELECT / JOIN / GROUP BY / 窗口函数）、建库建表、加载数据（COPY / Snowpipe）。输出：把一批 PubMed 文献数据导进 Snowflake，跑通 5 个查询。
- L3 处理数据：ETL/ELT、数据建模（星型模型）、DBT、做看板。输出：一个“文献初筛数据看板”（比如按年份/期刊/主题统计），能讲清楚数据从哪来、怎么洗、怎么用。
- 材料：Snowflake 官方免费试用账号 + 官方文档、DBT 官方教程；她自己的 PubMed 数据；公司内部现有 Snowflake 项目文档 / 同事（L0 时找）。
- 企业连接：中期目标是 CER / 文献 / 注册文档的数据流跑进 Snowflake，变成可复用的数据资产。

## 企业方向（总目标）

这五条线最终汇到一处：RA 流程 AI 化 + 企业数据 + Agent 落地。
- 短期锚点：Consistency Review Agent（QTN Day 3 项目）——Track 2 的 L3 和 Track 3 的 L2/L3 都指向它。
- 中期锚点：把 CER / 文献 / 注册文档的数据流跑进 Snowflake（Track 5 的 L3），变成可复用的数据资产。
- 长期锚点：Web Coding（Track 1 的 L3）+ 软件架构（Track 2）做出能给团队用的小产品（SpeakSpark 或 RA 助手）。SpeakSpark 目前变现和推进完全搁置；她觉得可以和音乐剧相关技巧/内容结合（包括小人动画），再决定要不要推——是否推一个 application 仍在讨论，见 2026-11-11 的讨论。

## 进度追踪（飞书学习空间里同步，Jianan Brain）

- 每条 track 一个 session：目标 / 当前级别 / 本周任务 / 待做清单 / 完成打勾；每条线的页面里还有“学习笔记”区，学完把总结写在里面（学了什么、怎么理解、哪里卡住、下一步），不只是打勾。
- 顶部一块空白 idea 板：任何想法随时扔进去，Jimmy 每两天分拣（待看 / 进行中 / 已用 / 放弃）。
- 提醒：Jimmy 每两天检查一次进度，没动静就提醒她；每周对照一次“学了什么、产出了什么”。
- 已有内容都连进框架了：学习路径整合、个人目标与学习规划、AI Agent 学习资源地图（进度总入口）、AI学习笔记、Vibe Coding 面试四问、Building Effective Agents 解读等，见飞书学习空间 hub 的“已有内容”一节。
