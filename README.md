# AI Agent 学习笔记

从概念到实践：用 DeepSeek Harness 学习上下文、工具、反馈循环与结果验证。

整理日期：2026-09-16。学习材料：[《AI Agent 入门》第一章](https://github.com/bojieli/ai-agent-book/blob/main/book/chapter1.md)。本仓库是个人学习总结，不是原书转载，也不是框架官方文档。

## 阅读顺序

1. [核心概念与工程理解](01-concepts.md)
2. [实验 1-1：上下文消融](02-context-ablation.md)
3. [实验 1-3：研究任务功能复现](03-research-workflow.md)
4. [十道思考题与学习心得](04-reflections.md)

## 我最重要的收获

- 模型说要执行，不代表工具真的执行。
- 工具执行成功，不代表模型看到了有效结果。
- 运行正常结束，不代表任务已经完成。
- 历史是否有用，取决于其中是否包含当前仍需要的信息。
- 验证既要检查答案，也要检查评分程序本身。

## 笔记的证据与范围

实验使用 DeepSeek Harness `0.1.5-rc.2`。本文依据本地实验报告、结果记录和学习过程整理；本次整理读取了已有报告和离线验证输出，没有重新发起模型实验。

上下文实验 A/B/C/E 各运行一次，D 未测试。研究实验验证了 Harness 组织工具的功能流程，没有验证提供商托管的完整研究循环。实验结果不能作为通用模型排行榜或统计结论。

本仓库发布 Markdown 笔记，不附原始会话、凭据、机器路径或整套实验源码。因此它是学习记录，不是独立可运行的复现实验包。文中实验文件名用于说明本地证据类型，不代表这些文件已经上传。

## 参考资料

- [学习原文：AI Agent 入门](https://github.com/bojieli/ai-agent-book/blob/main/book/chapter1.md)
- [DeepSeek Harness 源码](https://github.com/deepseek-ai/deepseek-harness)
- [本次使用的版本](https://github.com/deepseek-ai/deepseek-harness/releases/tag/dsh-v0.1.5-rc.2)

笔记由本人学习过程与实验记录整理，AI 辅助撰写。概念解释属于个人理解，模型与接口能力以实际使用版本为准。
