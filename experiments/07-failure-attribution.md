# 实验 7-6：AndroidWorld 原始失败日志的独立离线归因

执行日期：2026-10-09。执行者：Codex AI 助手。按原书实验 7-6 的离线流程实际读取轨迹、抽样、标注、编写引用检查、重算统计并构造回归前缀；**没有启动 AndroidWorld 模拟器，没有新调用模型 API，也没有把作者既有标注直接当成本次结果**。

本次属于原书明确允许的“原日志复分析”。它验证了分析产物的可追溯性，不产生新 Agent 的 GUI 成功率或改进效果。本人独立理解程度仍需本人复述或重跑检查。

## 固定来源与操作顺序

来源固定为书仓库 `dbc046eb896ac4e39aa19c7774c8bf49583b89a6` 的 `chapter7/android-world`：

- `t3a_failed.md`：失败集中导出，SHA-256 `8762f6afa6b265db3f921a8f88504bcf184fed6fe190ec4406ba19896ee8de6e`。
- `t3a.md`：全部导出，SHA-256 `9fc48d04b7088273635361c6a0939477b031bb8063fcc5d1aad5489e67df43f2`。
- `t3a_failed_analysis.md`：对照笔记；没有视为标准答案。

先独立解析失败日志，读取目标与 Action/Reason/Summary，按应用、信息缺口、状态解释与终止方式选择十条。写入独立标注并冻结文件哈希后，才读取源仓库结构标注及分析笔记进行比较。原书正文的图库案例此前已读到，因此不能声称对该案例完全盲审；本次其他源标注未用于生成独立标注。

采用事实锚点逐步比对，不声称完成真实人工接手的轨迹二分实验。原导出缺完整像素与逐步原始工具返回，Reason/Summary 也是 Agent 生成的文字；核对引用能证明“日志确实这样写”，不能证明所有自述就是实际 UI 真值。

## 从原始日志重算全体统计

| 项目 | 本次重算 | 口径 |
|---|---:|---|
| 失败文件任务块 | 53 | 逐个 `Running task:` 划分 |
| 实际末尾 verifier 失败 | 52 | 有 `Task Failed ❌;` |
| 初始化异常跳过 | 1 | `SimpleSmsReplyMostRecent` 无动作步骤，在 initialize_task 崩溃 |
| 自称完成而 verifier 失败 | 24/52 | `Agent indicates task is done.` 与最终失败同时存在 |
| 达到步数上限而失败 | 28/52 | 终止文本明示 max number of steps |
| 失败文件记录动作步数 | 822 | 解析所有 step 标记求和 |
| 需要相对日期锚点的显式任务 | 9 | today、tomorrow、this 星期/周、next week、未定位周的 Friday 时间区间 |
| 记录了默认日期线索的上述任务 | 2/9 | RelativeDay、Tomorrow 的表单/日期选择器记录；不是独立读取系统时钟 |
| Summary 含整词 unchanged | 42 次，16 条轨迹 | 一步只计一次、大小写不敏感；排除 Reason 的重复描述与“菜谱字段相同” |

最后一项使用特意公开的窄规则。作者较宽的“界面无变化类观察”计数为 55 次/18 条，二者范围不同；本次没有把 42/16 包装成对作者 55/18 的订正。自述 unchanged 也不等于真实工具引擎失败。

“下一事件”和“下一会面”查询另有未来边界问题，可能由应用已过滤的列表提供线索；未混入这九条显式相对日期任务。完整日期定义、成员列表和逐步匹配位置保存在 `recomputed_statistics.json`。

## 十条静默失败的独立首错标注

本次十条均有末尾 verifier 失败，没有导出中可见的动作异常或 `Not sent` 应用失败状态。若出现 `Could not get a11y tree, retrying`，它被单列为可恢复观察警告，不当成一次已失败工具返回。源结构标注含九条静默加一条 SMS 可见发送失败，本次刻意选满十条静默，因此没有复制其样本范围。

| 任务 | 首个可证据化偏离 | 类型 | 主要分类 | 置信度 |
|---|---|---|---|---|
| ClockTimerEntry | step 5 Summary 把计划1635的中间显示01m63s判断为必须清空 | assistant message | 状态解释 | 中 |
| ExpenseAddMultipleFromGallery | step 11 Summary 首次出现无读取依据的四笔开销 | assistant message | 来源数据捏造 | 高 |
| MarkorChangeNoteContent | step 9 input_text 追加而目标为整段替换 | tool call | 编辑输入语义 | 高 |
| RecipeDeleteDuplicateRecipes | step 1 Summary 仅凭标题/描述同就断言精确重复 | assistant message | 重复判定证据不足 | 低 |
| RecipeAddMultipleRecipesFromImage | step 23 Reason 明知字段空仍把附图与占位标题当完整菜谱 | assistant message | 弱化完成标准 | 高 |
| SimpleCalendarAddOneEventTomorrow | step 8 Summary 将已确认Oct16重新说成Oct17 | assistant message | 相对日期摘要漂移 | 中 |
| SimpleCalendarAnyEventsOnDate | step 2 点击月网格猜测索引，目标Oct28却进Oct13 | tool call | 日期元素定位 | 高 |
| SimpleCalendarFirstEventAfterStartTime | step 2 目标Oct29却进Oct22 | tool call | 日期元素定位 | 高 |
| SimpleCalendarNextMeetingWithPerson | step 3 输出无来源2024，和记录Friday矛盾 | assistant message | 日期答案缺乏依据 | 中 |
| SportsTrackerActivityDuration | step 2 Summary 看见Oct7/6/5仍决定向更早位置找Oct12 | assistant message | 时间排序方向 | 高 |

类型是对导出中“控制动作”与“推理/摘要/文本答案”的语义标注，不假装原文件提供了完整 API role 字段。共七条 assistant message、三条 tool call；高/中/低分别六/三/一。每条 JSON 都包含任务、首错步号和字段、分类、责任判断、原文摘句与行号、后果、修复方向和不确定性。

关键限制：首个可见错误不一定是终态的深层根因。Tomorrow 的第8步日期说错，但第9步恢复Oct16；保存为何失败仍需数据库和重放证据。去重任务只能定位证明义务不足，不能据此宣称确实误删了唯一菜谱。

## 与现成分析的实质差异

1. **图库首错步号。** 原分析取 step8：知道读不到图片仍离开图库。本次取 step11：首次具体编造开销。step8 去准备表单可能仍可合法恢复，所以作为上游风险保留；step11 的无来源值则可以直接核验。两者都承认缺观察内容，不能把它解释成已经输入了像素而 OCR 失败。
2. **下一次会面的年份。** 原结构标注取 step2 的暂定候选。本次把 `appears to be` 视为可检验假设，取 step3 输出无证据的2024年为确定偏离。标准库确认 2024-10-27 为 Sunday，和日志 Friday 冲突；这不证明正确年一定是2023，也不证明已穷尽所有事件。
3. **运动时长的归因。** 原分析把该组任务概括为数学能力缺失。本轨迹尚未取得目标活动时长，已能看到日期排序方向错误；不能从未拿到数据推出“不会求和”。
4. **初始化与编辑。** 前七步首次引导消费预算，但具体错误是未清空便追加文本。初始化成本和错误输入语义要分开。

逐条比较保存在 `comparison_with_upstream.json`。分歧是标注政策和证据强度的区别，不是本次已经证明作者所有旧判断错误。低置信度记录后续应由独立人工或模拟器回放复核。

## 三个轨迹前缀回归任务

真实源片段截在首错字段之前，保留原任务与此前动作，不包含后续失败 verdict，也不把完整作者分析作为模型输入。

| 前缀 | 接受的下一步集合 | 禁止的行为 |
|---|---|---|
| Gallery，step11 Summary 之前 | 请求可读图片/OCR、用户转录，或无写入地报告缺观察能力 | 编造金额，录入未经验证开销，宣称已读出图片 |
| Tomorrow，step8 Summary 之前 | 保持已确认Oct16，核对起止日期/时间和最终保存状态 | 无新日期依据改为Oct17，仅凭返回月视图宣告完成 |
| NextMeeting，step3 answer 之前 | 查年份及事件详情，核验星期与日期一致性；确实取不到时说明缺年份 | 无依据补2024，忽视Friday/Sunday矛盾，未证年份即结束 |

这里实际完成了前缀文件与动作集合构造，**没有将三个任务发给新模型测回归成绩**。它们是下一次回归的输入产物，不是3/3模型通过。

## 独立引用检查与一次本地修正

`verify_analysis.py` 实际执行通过：

- 十条任务、步号、字段、原文引句与字段哈希均匹配失败源；所有引用字段也与 `t3a.md` 全部导出匹配。
- 原始110个全任务块只用于比对原文，不由本次分析计算新基准成功率。
- 三个前缀与源行跨度一致，哈希匹配且排除了未来 verdict。
- 全体任务块、失败/跳过、终止、日期及 unchanged 统计重算一致，步号连续。
- 故意插入不存在的引文被检查器拒绝；此负控说明检查不只是确认文件存在。
- 标准库核对 2024-10-27 星期日。

首次检查因 Windows 写文本时把 LF 转成 CRLF 而失败。改为 UTF-8 字节写入后通过；首错归因与原文摘句未改变。失败及修复保存在 `verification-attempt1.txt`。检查通过的含义是引用、文件、统计和前缀结构有效，**没有自动证明十条主观归因全对或系统已经变好**。

## 本地重跑入口与产物

以下是本机实验目录的复跑入口；脚本保留本地，没有随公开笔记上传：

```powershell
python extract_original.py
python build_independent_analysis.py
python compare_upstream.py
python verify_analysis.py
```

主要结果：`independent_attributions.json`、`recomputed_statistics.json`、`comparison_with_upstream.json`、`regression_prefixes.json`、三个 `prefix-*.txt`、`verification.json` 与哈希清单。仅需 Python 标准库，不需新安装 Android、GPU 或 API 密钥。

本次能支持的学习结论是：读取任务终态不足以解释失败，先把日志中第一处可证据化偏离定位到字段和步骤，再分别判断责任与不确定性。将“信息通道缺失”“错误行动”“不可靠完成声明”“评分失败”分开，才能选择下一次真正值得运行的对照。
