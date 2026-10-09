# 全书学习完成表与 109 项实验索引

核对日期：2026-10-09。配套：[共学总章](18-co-learning-summary.md)、[全书目录](README.md)。

## 本次完成的范围

十章 Markdown 学习笔记、独立共学总章和全书索引已整理齐备。这里的阅读完成指材料已整理，个人独立掌握情况尚待自测。历史操作仅依据已有笔记归档，本次没有重跑全部实验或逐项核验原始日志。

原书固定版本为 `dbc046eb896ac4e39aa19c7774c8bf49583b89a6`，正文实验编号逐项提取并检查连续性，章内数量为 4、10、12、5、16、14、14、19、9、6，合计 109。这个数字表示原书学习范围，不能作为个人通过数。

## 十章覆盖表

| 章 | 主题 | 学习材料 | 个人实验范围 |
|---|---|---|---|
| 1 | 入门与闭环 | [概念](01-concepts.md)、[消融](02-context-ablation.md)、[研究](03-research-workflow.md)、[反思](04-reflections.md) | 消融与研究的历史机制改编；原版仍有未执行项 |
| 2 | 上下文工程 | [笔记](05-chapter2-context-engineering.md)、[证据](06-chapter2-experiment-evidence.md)、[Skill](07-chat-writing-skill.md) | 十主题历史操作或改编；原验收缺项保留 |
| 3 | 记忆与知识库 | [笔记](08-chapter3-memory-and-rag.md)、[证据](09-chapter3-experiment-evidence.md) | 十二主题小规模机制改编 |
| 4 | 工具 | [笔记](10-chapter4-tools.md)、[范围](12-chapter45-experiment-evidence.md) | 部分、缩小及本地状态演示 |
| 5 | 代码与运行框架 | [笔记](11-chapter5-code-and-harness.md)、[范围](12-chapter45-experiment-evidence.md) | 部分、缩小及未执行项目 |
| 6 | 交互 | [笔记](13-chapter6-interaction.md) | 阅读与路线；正式实验未执行 |
| 7 | 评估 | [笔记](14-chapter7-evaluation.md) | 阅读与路线；正式实验未执行；新增三项已补索引 |
| 8 | 模型后训练 | [笔记](15-chapter8-post-training.md) | 阅读与路线；无训练/蒸馏实测 |
| 9 | 持续进化 | [笔记](16-chapter9-continuous-evolution.md) | 本次阅读；无自动进化实验验收 |
| 10 | 多 Agent 协作 | [笔记](17-chapter10-multi-agent.md) | 本次阅读；整理分工不计入原书对照 |

## 状态怎样解释

- **历史机制改编/缩小对照**：已有实际操作记录，规模、模型、环境或目标有差异，具体失败见证据笔记。
- **部分/状态演示/功能产物**：只验证若干组件或功能，未覆盖原书端到端验收。
- **未执行**：没有相应正式运行记录；阅读、安装、编写草稿和普通浏览器发布不计作通过。
- **完整原验收**：需要逐项满足原任务及验收条件。本清单未据现有材料给任何项目补授此标签。

工具可用、HTTP 正常、任务结束、离线流程检查通过和业务答案正确分别记录。更新读书范围不会倒改历史成绩。

## 全部实验主题与个人操作边界

下面的主题名称用于定位原文，不表示已运行源码。每章的原文链接指向同一个固定版本；项目依赖与执行状态应另外核对原书该章 README 和验收记录。

### 第 1 章 · 4 项

[固定版本正文](https://github.com/bojieli/ai-agent-book/blob/dbc046eb896ac4e39aa19c7774c8bf49583b89a6/book/chapter1.md)

| 编号 | 原书主题 | 个人操作边界 | 记录入口 |
|---|---|---|---|
| 1-1 | 上下文的关键作用 | 历史机制改编；A/B/C/E 单次，D 未测试 | [笔记](02-context-ablation.md) |
| 1-2 | Kimi K3 原生 Agent 能力 | 未执行原版任务 | 无个人运行记录 |
| 1-3 | GPT-5.6 原生 Deep Research 能力 | 历史研究流程改编；非托管研究复现 | [笔记](03-research-workflow.md) |
| 1-4 | 文生图工作流与原生图像生成的对照 | 未执行原版对照 | 无个人运行记录 |

### 第 2 章 · 10 项

[固定版本正文](https://github.com/bojieli/ai-agent-book/blob/dbc046eb896ac4e39aa19c7774c8bf49583b89a6/book/chapter2.md)

| 编号 | 原书主题 | 个人操作边界 | 记录入口 |
|---|---|---|---|
| 2-1 | 本地 LLM 服务部署与工具调用 | 历史缩小机制改编；完整原验收未完成 | [笔记](06-chapter2-experiment-evidence.md) |
| 2-2 | 注意力机制可视化 | 历史缩小机制改编；完整原验收未完成 | [笔记](06-chapter2-experiment-evidence.md) |
| 2-3 | 常见的错误上下文管理模式 | 历史缩小机制改编；完整原验收未完成 | [笔记](06-chapter2-experiment-evidence.md) |
| 2-4 | 提示工程的消融实验 | 历史缩小机制改编；完整原验收未完成 | [笔记](06-chapter2-experiment-evidence.md) |
| 2-5 | 提示注入攻防实验 | 历史缩小机制改编；完整原验收未完成 | [笔记](06-chapter2-experiment-evidence.md) |
| 2-6 | 使用 Agent Skills 从论文生成演示文稿 | 历史演示文稿功能产物；非完整原验收 | [笔记](06-chapter2-experiment-evidence.md) |
| 2-7 | 从个人范文创建“去 AI 味”写作 Skill | 聊天代拟 Skill 改编；本人原创与人工改稿缺项 | [笔记](06-chapter2-experiment-evidence.md) |
| 2-8 | 通过注意力可视化验证 Agent 状态栏的效果 | 历史缩小机制改编；完整原验收未完成 | [笔记](06-chapter2-experiment-evidence.md) |
| 2-9 | 几种好用的 Agent 状态栏技术 | 历史缩小机制改编；完整原验收未完成 | [笔记](06-chapter2-experiment-evidence.md) |
| 2-10 | 上下文压缩策略对比 | 历史缩小机制改编；完整原验收未完成 | [笔记](06-chapter2-experiment-evidence.md) |

### 第 3 章 · 12 项

[固定版本正文](https://github.com/bojieli/ai-agent-book/blob/dbc046eb896ac4e39aa19c7774c8bf49583b89a6/book/chapter3.md)

| 编号 | 原书主题 | 个人操作边界 | 记录入口 |
|---|---|---|---|
| 3-1 | 用三层次框架评估记忆系统 | 历史缩小机制改编；完整原验收未完成 | [笔记](09-chapter3-experiment-evidence.md) |
| 3-2 | 记忆策略的对比实验研究 | 历史缩小机制改编；完整原验收未完成 | [笔记](09-chapter3-experiment-evidence.md) |
| 3-3 | 基于本地模型的智能日志脱敏 | 历史缩小机制改编；完整原验收未完成 | [笔记](09-chapter3-experiment-evidence.md) |
| 3-4 | 构建向量检索服务：ANN 索引算法的比较研究 | 历史缩小机制改编；完整原验收未完成 | [笔记](09-chapter3-experiment-evidence.md) |
| 3-5 | 探究稀疏检索：从零实现 BM25 搜索引擎 | 历史缩小机制改编；完整原验收未完成 | [笔记](09-chapter3-experiment-evidence.md) |
| 3-6 | 混合检索流水线：结合稀疏、稠密与重排序 | 历史缩小机制改编；完整原验收未完成 | [笔记](09-chapter3-experiment-evidence.md) |
| 3-7 | 结构化索引：RAPTOR 与 GraphRAG 的知识组织哲学 | 历史缩小机制改编；完整原验收未完成 | [笔记](09-chapter3-experiment-evidence.md) |
| 3-8 | 智能体化 RAG 与非智能体化 RAG 的对比研究 | 历史缩小机制改编；完整原验收未完成 | [笔记](09-chapter3-experiment-evidence.md) |
| 3-9 | 利用智能体化 RAG 构建用户记忆 | 历史缩小机制改编；完整原验收未完成 | [笔记](09-chapter3-experiment-evidence.md) |
| 3-10 | 上下文感知检索：解决 RAG 的上下文丢失问题 | 历史缩小机制改编；完整原验收未完成 | [笔记](09-chapter3-experiment-evidence.md) |
| 3-11 | 利用上下文感知检索增强用户记忆 | 历史缩小机制改编；完整原验收未完成 | [笔记](09-chapter3-experiment-evidence.md) |
| 3-12 | 从结构化数据中提取隐性知识：以司法判例分析为例 | 历史缩小机制改编；完整原验收未完成 | [笔记](09-chapter3-experiment-evidence.md) |

### 第 4 章 · 5 项

[固定版本正文](https://github.com/bojieli/ai-agent-book/blob/dbc046eb896ac4e39aa19c7774c8bf49583b89a6/book/chapter4.md)

| 编号 | 原书主题 | 个人操作边界 | 记录入口 |
|---|---|---|---|
| 4-1 | 主动工具发现 | 历史缩小对照 | [笔记](12-chapter45-experiment-evidence.md) |
| 4-2 | 感知工具 MCP 服务器 | 历史部分 MCP 验证 | [笔记](12-chapter45-experiment-evidence.md) |
| 4-3 | 多模态信息提取：三种技术范式的对比分析 | 未执行 | [笔记](12-chapter45-experiment-evidence.md) |
| 4-4 | 执行工具 MCP 服务器 | 历史部分 MCP 验证 | [笔记](12-chapter45-experiment-evidence.md) |
| 4-5 | 协作工具 MCP 服务器 | 历史本地 pending 状态演示 | [笔记](12-chapter45-experiment-evidence.md) |

### 第 5 章 · 16 项

[固定版本正文](https://github.com/bojieli/ai-agent-book/blob/dbc046eb896ac4e39aa19c7774c8bf49583b89a6/book/chapter5.md)

| 编号 | 原书主题 | 个人操作边界 | 记录入口 |
|---|---|---|---|
| 5-1 | 跨厂商的轨迹接管 | 未执行 | [笔记](12-chapter45-experiment-evidence.md) |
| 5-2 | 输出到一半断掉之后的接续 | 历史手工 JSON 前缀对照 | [笔记](12-chapter45-experiment-evidence.md) |
| 5-3 | 使用代码生成工具提升数学解题能力 | 历史六题缩小对照 | [笔记](12-chapter45-experiment-evidence.md) |
| 5-4 | 使用代码生成工具提升逻辑思考能力 | 历史三题缩小对照 | [笔记](12-chapter45-experiment-evidence.md) |
| 5-5 | 小模型通过代码化知识提升执行规则的准确性 | 历史确定性规则演示 | [笔记](12-chapter45-experiment-evidence.md) |
| 5-6 | 基于论文的 PPT 自动生成 | 本章未重跑；未做单/双 Agent 比较 | [笔记](12-chapter45-experiment-evidence.md) |
| 5-7 | 论文讲解视频的自动生成 | 未执行 | [笔记](12-chapter45-experiment-evidence.md) |
| 5-8 | 基于 API 的智能视频剪辑 | 未执行 | [笔记](12-chapter45-experiment-evidence.md) |
| 5-9 | 同一个零件的两种生成路线——代码与生成模型 | 未执行 | [笔记](12-chapter45-experiment-evidence.md) |
| 5-10 | 自适应的日志解析系统 | 历史解析与进程内替换 | [笔记](12-chapter45-experiment-evidence.md) |
| 5-11 | 生产日志的智能诊断系统 | 历史合成日志诊断与修复 | [笔记](12-chapter45-experiment-evidence.md) |
| 5-12 | 动态表单生成的意图澄清系统 | 历史表单缩小实测 | [笔记](12-chapter45-experiment-evidence.md) |
| 5-13 | 自然语言交互的 ERP Agent | 历史 SQLite 改编 | [笔记](12-chapter45-experiment-evidence.md) |
| 5-14 | 对话式界面定制系统 | 未执行 | [笔记](12-chapter45-experiment-evidence.md) |
| 5-15 | 动态生成软件的权限内嵌数据对象 | 历史网关机制演示；非独立隔离 | [笔记](12-chapter45-experiment-evidence.md) |
| 5-16 | 开发一个能创造 Agent 的 Agent | 历史短循环与模拟响应协议测试 | [笔记](12-chapter45-experiment-evidence.md) |

### 第 6 章 · 14 项

[固定版本正文](https://github.com/bojieli/ai-agent-book/blob/dbc046eb896ac4e39aa19c7774c8bf49583b89a6/book/chapter6.md)

| 编号 | 原书主题 | 个人操作边界 | 记录入口 |
|---|---|---|---|
| 6-1 | 事件驱动的邮件处理 Agent | 阅读已整理；正式实验未执行 | [笔记](13-chapter6-interaction.md) |
| 6-2 | 带并行执行和打断能力的异步 Agent | 阅读已整理；正式实验未执行 | [笔记](13-chapter6-interaction.md) |
| 6-3 | 模型原生异步与回合中途引导 | 阅读已整理；正式实验未执行 | [笔记](13-chapter6-interaction.md) |
| 6-4 | 构建传统语音 Agent | 阅读已整理；正式实验未执行 | [笔记](13-chapter6-interaction.md) |
| 6-5 | 使用 Qwen2-Audio 模拟流式语音感知 | 阅读已整理；正式实验未执行 | [笔记](13-chapter6-interaction.md) |
| 6-6 | 本地运行 MiniCPM-o 4.5，对比端到端与自级联 | 阅读已整理；正式实验未执行 | [笔记](13-chapter6-interaction.md) |
| 6-7 | 基于 Fish Audio 的控制标记驱动 TTS | 阅读已整理；正式实验未执行 | [笔记](13-chapter6-interaction.md) |
| 6-8 | 运行 Computer Use（Anthropic 参考路径或开放模型路径） | 阅读已整理；正式实验未执行 | [笔记](13-chapter6-interaction.md) |
| 6-9 | 使用 browser-use 实现自动浏览器操作 | 阅读已整理；正式实验未执行 | [笔记](13-chapter6-interaction.md) |
| 6-10 | 真机遥操作 XLeRobot 整理桌面 | 阅读已整理；正式实验未执行 | [笔记](13-chapter6-interaction.md) |
| 6-11 | 在模拟器中测量同任务的理想控制上限 | 阅读已整理；正式实验未执行 | [笔记](13-chapter6-interaction.md) |
| 6-12 | 使用 Gemini Robotics-ER 1.5 驱动 XLeRobot 自主整理桌面 | 阅读已整理；正式实验未执行 | [笔记](13-chapter6-interaction.md) |
| 6-13 | 在模拟器中比较三种自主整理桌面的闭环 | 阅读已整理；正式实验未执行 | [笔记](13-chapter6-interaction.md) |
| 6-14 | 同一桌面任务的 RGB 跨环境测试 | 阅读已整理；正式实验未执行 | [笔记](13-chapter6-interaction.md) |

### 第 7 章 · 14 项

[固定版本正文](https://github.com/bojieli/ai-agent-book/blob/dbc046eb896ac4e39aa19c7774c8bf49583b89a6/book/chapter7.md)

| 编号 | 原书主题 | 个人操作边界 | 记录入口 |
|---|---|---|---|
| 7-1 | 运行 τ²-bench 并对比 τ-bench 的演进 | 阅读已整理；正式实验未执行 | [笔记](14-chapter7-evaluation.md) |
| 7-2 | 人肉执行基准测试任务 | 阅读已整理；正式实验未执行 | [笔记](14-chapter7-evaluation.md) |
| 7-3 | 构建基于 Rubric 的用户记忆评估系统 | 阅读已整理；正式实验未执行 | [笔记](14-chapter7-evaluation.md) |
| 7-4 | Advanced JSON Cards 与 RAG 的对比评估 | 阅读已整理；正式实验未执行 | [笔记](14-chapter7-evaluation.md) |
| 7-5 | 构建全自动 TTS 质量评估流水线 | 阅读已整理；正式实验未执行 | [笔记](14-chapter7-evaluation.md) |
| 7-6 | 对 AndroidWorld 失败轨迹做失败归因 | 阅读已整理；正式实验未执行 | [笔记](14-chapter7-evaluation.md) |
| 7-7 | 轨迹前缀边界评估：同一上下文的多种表示 | 阅读已整理；正式实验未执行 | [笔记](14-chapter7-evaluation.md) |
| 7-8 | 从配对比较数据构建模型排行榜 | 阅读已整理；正式实验未执行 | [笔记](14-chapter7-evaluation.md) |
| 7-9 | 在固定 Coding Harness 中测量模型的行动阈值 | 阅读已整理；正式实验未执行 | [笔记](14-chapter7-evaluation.md) |
| 7-10 | Agent 任务的端到端成本分析 | 阅读已整理；正式实验未执行 | [笔记](14-chapter7-evaluation.md) |
| 7-11 | 多维度模型性能基准测试 | 阅读已整理；正式实验未执行 | [笔记](14-chapter7-evaluation.md) |
| 7-12 | 用户记忆系统的端到端选型评估 | 阅读已整理；正式实验未执行 | [笔记](14-chapter7-evaluation.md) |
| 7-13 | AndroidWorld 的评估和改进 | 阅读已整理；正式实验未执行 | [笔记](14-chapter7-evaluation.md) |
| 7-14 | 配置 OpenVLA 与 RoboTwin2 的具身智能环境 | 阅读已整理；正式实验未执行 | [笔记](14-chapter7-evaluation.md) |

### 第 8 章 · 19 项

[固定版本正文](https://github.com/bojieli/ai-agent-book/blob/dbc046eb896ac4e39aa19c7774c8bf49583b89a6/book/chapter8.md)

| 编号 | 原书主题 | 个人操作边界 | 记录入口 |
|---|---|---|---|
| 8-1 | Q-learning 在寻宝游戏中的表现 | 阅读已整理；正式实验未执行 | [笔记](15-chapter8-post-training.md) |
| 8-2 | 传统 RL 与 LLM Agent 的对比研究 | 阅读已整理；正式实验未执行 | [笔记](15-chapter8-post-training.md) |
| 8-3 | 从头训练 LLM——算法改进的威力 | 阅读已整理；正式实验未执行 | [笔记](15-chapter8-post-training.md) |
| 8-4 | 自己训练 VLM | 阅读已整理；正式实验未执行 | [笔记](15-chapter8-post-training.md) |
| 8-5 | 继续预训练学习新语言 | 阅读已整理；正式实验未执行 | [笔记](15-chapter8-post-training.md) |
| 8-6 | 语音 SFT——从 “声音复制” 到 “副语言建模” （扩展） | 阅读已整理；正式实验未执行 | [笔记](15-chapter8-post-training.md) |
| 8-7 | 多语言思考——让模型用任意语言思考 （扩展） | 阅读已整理；正式实验未执行 | [笔记](15-chapter8-post-training.md) |
| 8-8 | Prompt 蒸馏——以更小开销复现可用能力 | 阅读已整理；正式实验未执行 | [笔记](15-chapter8-post-training.md) |
| 8-9 | 思维链（Chain of Thought, CoT）蒸馏 | 阅读已整理；正式实验未执行 | [笔记](15-chapter8-post-training.md) |
| 8-10 | AdaptThink——学会 “何时不思考” | 阅读已整理；正式实验未执行 | [笔记](15-chapter8-post-training.md) |
| 8-11 | GeneralPoints——单轮 RL 的 “记忆与泛化” 对照 | 阅读已整理；正式实验未执行 | [笔记](15-chapter8-post-training.md) |
| 8-12 | V-IRL-VL——多轮视觉导航 | 阅读已整理；正式实验未执行 | [笔记](15-chapter8-post-training.md) |
| 8-13 | SimpleVLA-RL——结果奖励下的开放探索 （扩展） | 阅读已整理；正式实验未执行 | [笔记](15-chapter8-post-training.md) |
| 8-14 | ReTool——代码解释器增强数学解题 | 阅读已整理；正式实验未执行 | [笔记](15-chapter8-post-training.md) |
| 8-15 | AWorld-train——在沙盒中学习使用工具 | 阅读已整理；正式实验未执行 | [笔记](15-chapter8-post-training.md) |
| 8-16 | RLVP——奖励结果、惩罚路径 | 阅读已整理；正式实验未执行 | [笔记](15-chapter8-post-training.md) |
| 8-17 | 从“过早结束”问题案例到 DPO 修复 | 阅读已整理；正式实验未执行 | [笔记](15-chapter8-post-training.md) |
| 8-18 | 作用域敏感的中文弯引号 SFT | 阅读已整理；正式实验未执行 | [笔记](15-chapter8-post-training.md) |
| 8-19 | 特殊字符串的精确复制 SFT | 阅读已整理；正式实验未执行 | [笔记](15-chapter8-post-training.md) |

### 第 9 章 · 9 项

[固定版本正文](https://github.com/bojieli/ai-agent-book/blob/dbc046eb896ac4e39aa19c7774c8bf49583b89a6/book/chapter9.md)

| 编号 | 原书主题 | 个人操作边界 | 记录入口 |
|---|---|---|---|
| 9-1 | 为客服 Agent 构建轨迹验证器 | 阅读已整理；正式实验未执行 | [笔记](16-chapter9-continuous-evolution.md) |
| 9-2 | 从 τ²-bench 失败轨迹提炼转接与工具使用规则 | 阅读已整理；正式实验未执行 | [笔记](16-chapter9-continuous-evolution.md) |
| 9-3 | 基于失败轨迹优化航空客服的系统 Prompt | 阅读已整理；正式实验未执行 | [笔记](16-chapter9-continuous-evolution.md) |
| 9-4 | 从用户反馈中进化需求澄清与 Spec 确认 Skill | 阅读已整理；正式实验未执行 | [笔记](16-chapter9-continuous-evolution.md) |
| 9-5 | 从浏览器轨迹生成可验证工作流 | 阅读已整理；正式实验未执行 | [笔记](16-chapter9-continuous-evolution.md) |
| 9-6 | 由失败轨迹触发 Agent 自我修改 | 阅读已整理；正式实验未执行 | [笔记](16-chapter9-continuous-evolution.md) |
| 9-7 | 由用户反馈触发高风险操作确认门禁 | 阅读已整理；正式实验未执行 | [笔记](16-chapter9-continuous-evolution.md) |
| 9-8 | 把这本书交给 Hermes：它能升级自己吗？ | 阅读已整理；正式实验未执行 | [笔记](16-chapter9-continuous-evolution.md) |
| 9-9 | 评估 Agent 是否在持续进化 | 阅读已整理；正式实验未执行 | [笔记](16-chapter9-continuous-evolution.md) |

### 第 10 章 · 6 项

[固定版本正文](https://github.com/bojieli/ai-agent-book/blob/dbc046eb896ac4e39aa19c7774c8bf49583b89a6/book/chapter10.md)

| 编号 | 原书主题 | 个人操作边界 | 记录入口 |
|---|---|---|---|
| 10-1 | 共享上下文中的多角色转换——系统提示词与 Skill 的对比 | 阅读已整理；正式实验未执行 | [笔记](17-chapter10-multi-agent.md) |
| 10-2 | 书籍翻译 Agent | 阅读已整理；正式实验未执行 | [笔记](17-chapter10-multi-agent.md) |
| 10-3 | 自主编排的电话 + 电脑 Agent | 阅读已整理；正式实验未执行 | [笔记](17-chapter10-multi-agent.md) |
| 10-4 | 同时从多个网站搜集信息的 Agent | 阅读已整理；正式实验未执行 | [笔记](17-chapter10-multi-agent.md) |
| 10-5 | 运行斯坦福 AI 小镇 | 阅读已整理；正式实验未执行 | [笔记](17-chapter10-multi-agent.md) |
| 10-6 | 语音狼人杀 Agent 系统 | 阅读已整理；正式实验未执行 | [笔记](17-chapter10-multi-agent.md) |

## 下一步用证据更新这张表

每次补做记录：任务与初始状态、来源版本、模型/提示/工具版本、固定预算、实际执行、独立真值、结果、失败、差异和公开范围。先完成一个可重复的小闭环，再选择语音、训练、外部服务或真机项目。

本清单优先帮助找到缺口，不生成通过率、能力排行榜或结业成绩。完整验收应另存新的运行证据，不覆盖旧记录。
