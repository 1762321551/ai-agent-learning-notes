# AI Agent 学习笔记

从概念到实践：学习上下文、工具、反馈循环与结果验证。

更新日期：2026-10-09。学习材料：[《深入理解 AI Agent》十章目录](https://github.com/bojieli/ai-agent-book/blob/dbc046eb896ac4e39aa19c7774c8bf49583b89a6/README.md)。全书十章的 Markdown 学习材料已补齐；个人独立掌握与正式实验验收仍需实践。本仓库是个人学习总结，AI 辅助整理。

## 先读共学总章

[总章：从“模型会回答”到“系统能交付”](18-co-learning-summary.md)把我们的聊天、库存与研究实验、评分修正和后续路线连成一篇完整总结。

[全书学习完成表与 109 项实验索引](19-course-completion-checklist.md)按当前版本逐项列出主题和个人操作边界。109 是原书范围，不能作为个人通过数。

## 十章导航

| 章 | 主题 | 主笔记 | 实验与补充 |
|---|---|---|---|
| 1 | 入门 | [核心概念](01-concepts.md) | [消融](02-context-ablation.md)、[研究](03-research-workflow.md)、[反思](04-reflections.md) |
| 2 | 上下文工程 | [学习笔记](05-chapter2-context-engineering.md) | [证据](06-chapter2-experiment-evidence.md)、[写作 Skill](07-chat-writing-skill.md) |
| 3 | 记忆与知识库 | [学习笔记](08-chapter3-memory-and-rag.md) | [实验证据](09-chapter3-experiment-evidence.md) |
| 4 | 工具 | [学习笔记](10-chapter4-tools.md) | [实验范围](12-chapter45-experiment-evidence.md) |
| 5 | 代码与运行框架 | [学习笔记](11-chapter5-code-and-harness.md) | [实验范围](12-chapter45-experiment-evidence.md) |
| 6 | 交互 | [学习笔记](13-chapter6-interaction.md) | 阅读与实验路线 |
| 7 | 评估 | [学习笔记](14-chapter7-evaluation.md) | 已补当前 14 项阅读路线 |
| 8 | 模型后训练 | [学习笔记](15-chapter8-post-training.md) | 阅读与训练验收设计 |
| 9 | 持续进化 | [学习笔记](16-chapter9-continuous-evolution.md) | 9 项实验学习与验收路线 |
| 10 | 多 Agent 协作 | [学习笔记](17-chapter10-multi-agent.md) | 6 项实验学习与验收路线 |

## 阅读顺序

1. [核心概念与工程理解](01-concepts.md)
2. [实验 1-1：上下文消融](02-context-ablation.md)
3. [实验 1-3：研究任务功能复现](03-research-workflow.md)
4. [十道思考题与学习心得](04-reflections.md)
5. [第二章：上下文工程实测与反思](05-chapter2-context-engineering.md)
6. [第二章：实验数据与证据边界](06-chapter2-experiment-evidence.md)
7. [实验 2-7：聊天记录驱动的写作 Skill](07-chat-writing-skill.md)
8. [第三章：记忆、知识库与检索](08-chapter3-memory-and-rag.md)
9. [第三章：实验结果与证据边界](09-chapter3-experiment-evidence.md)
10. [第四章：工具发现、协议与执行边界](10-chapter4-tools.md)
11. [第五章：代码能力、运行框架与结果验证](11-chapter5-code-and-harness.md)
12. [第四、五章：实验覆盖与证据边界](12-chapter45-experiment-evidence.md)
13. [第六章：交互、事件与持续变化的环境](13-chapter6-interaction.md)
14. [第七章：评估、失败归因与可重复的改进](14-chapter7-evaluation.md)
15. [第八章：模型后训练](15-chapter8-post-training.md)
16. [第九章：持续进化](16-chapter9-continuous-evolution.md)
17. [第十章：多 Agent 协作](17-chapter10-multi-agent.md)
18. [共学总章](18-co-learning-summary.md)
19. [全书学习完成表与实验索引](19-course-completion-checklist.md)

## 我最重要的收获

- 模型说要执行，不代表工具真的执行。
- 工具执行成功，不代表模型看到了有效结果。
- 运行正常结束，不代表任务已经完成。
- 历史是否有用，取决于其中是否包含当前仍需要的信息。
- 验证既要检查答案，也要检查评分程序本身。

## 笔记的证据与范围

第一章使用 DeepSeek Harness `0.1.5-rc.2`。第一章笔记在 2026-09-16 依据已有报告和离线验证整理，没有在整理时重新发起模型实验。

上下文实验 A/B/C/E 各运行一次，D 未测试。研究实验验证了 Harness 组织工具的功能流程，没有验证提供商托管的完整研究循环。实验结果不能作为通用模型排行榜或统计结论。

第二章在 2026-09-19 实际执行了本地 Qwen3 推理、注意力与 KV 测量，以及独立脚本调用 DeepSeek API 的对照实验；另完成论文制稿与聊天驱动的写作 Skill。十项均有操作记录或改编说明，但不是原书全部基准的严格复现。工具调用成功而计算错误、简单样本没有拉开差距等结果均保留，详情见第二章笔记。

第三章在 2026-09-19 完成覆盖 12 个主题的缩小机制实验：四种记忆格式、本地脱敏、真实向量索引、混合检索、结构表达、迭代检索与上下文前缀等。共 120 次云端请求，并执行本地模型与索引计算。保留脱敏漏检、前缀丢失依赖关系等失败；不是原书全部验收通过，未完整复现 60 个记忆案例、Intel 大型手册和真实司法数据集。

第四、五章在 2026-09-22 完成选定的机制实验：共 47 次真实模型请求，并执行 MCP 标准输入输出通信、生成代码、SQLite 查询、数据网关与浏览器表单验证。保留输出截断、参数约定不匹配和初版评分漏检等问题；逐项列出 21 个原书实验的覆盖情况，其中包含缩小改编及未执行项，不代表全部复现或全部通过。

第六、七章于 2026-09-26 完成阅读笔记，结合已有学习经历解释交互与评估，并整理实验目标和后续路线；本次未执行这两章的实验，不把原书成绩计入个人结果。

第八章于 2026-09-26 完成阅读笔记，整理 Mid-training、SFT、RL、奖励、蒸馏与训练验收；本次没有执行模型训练或本章基准实验。

第九、十章与共学总章于 2026-10-09 完成阅读整理。同步补入第七章当前目录的 7-12～7-14 路线，并按固定版本核对全部 109 个实验编号。本次没有新增正式实验运行，也没有重验全部历史原始日志；整理分工不作为多 Agent 性能对照。

本仓库发布 Markdown 笔记，不附原始会话、凭据、机器路径或整套实验源码。因此它是学习记录，不是独立可运行的复现实验包。文中实验文件名用于说明本地证据类型，不代表这些文件已经上传。

## 参考资料

- [学习原文：AI Agent 入门](https://github.com/bojieli/ai-agent-book/blob/main/book/chapter1.md)
- [DeepSeek Harness 源码](https://github.com/deepseek-ai/deepseek-harness)
- [本次使用的版本](https://github.com/deepseek-ai/deepseek-harness/releases/tag/dsh-v0.1.5-rc.2)

笔记由本人学习过程与实验记录整理，AI 辅助撰写。概念解释属于个人理解，模型与接口能力以实际使用版本为准。
