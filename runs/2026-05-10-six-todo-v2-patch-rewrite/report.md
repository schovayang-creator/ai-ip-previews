# 运行报告 - 六个 Todo V2 补丁目标回写

## 任务信息 / Task Metadata

- 任务 ID: 2026-05-10-six-todo-v2-patch-rewrite
- 模式: office
- 最终状态: finished
- 分数: 96/100
- 结束时间: 2026-05-10
- 报告路径: `plans/run-reports/2026-05-10-six-todo-v2-patch-rewrite-report.md`
- 页面模板: `templates/run-report-page-template.html`

## 目标 / Objective

纠正此前只给 6 个旧 todo 加 `/goal` 前置规范、但没有根据已有产出和用户原始需求改写任务本体的问题。现在已直接修改原本 6 个 md 文件，把它们从“旧任务”升级为“V2 补丁任务”，旧正文只作为背景参考。

## 交付物 / Deliverables

- 6 个原 `plans/todo/2026-05-09-codex-*.md` 文件均已新增 `当前执行目标：V2 补丁任务（以本段为准）`。
- 每个任务都要求先读已有产出和原始需求，再做二次补丁，不是原样重跑。
- A 任务升级为项目索引/记忆系统 V2：补 AGENTS 路由、decision log、quickstart、用户偏好和旧任务回写教训。
- B 任务升级为国内外趋势引擎 V2：补 YouTube / X / GitHub 高信号源、视觉证据切片、国内外热点、钩子模板。
- C 任务升级为 XHS 系统 V2：补真实 pilot、10-30 条高信号笔记采样、引流/带货/服务路径、样例。
- D 任务升级为工具评估 V2：补真实试用等级、沙箱运行、原始评分 + 适配评分、候选工具安全元数据评估。
- E 任务升级为商业 PRD V2：补可直接试卖的 offer、小红书获客路径、试卖素材、单元经济和阶段顺序。
- F 任务升级为报告系统 V2：补任务文件自包含、默认发布、finished 审查、HTML/索引验收。

## 修改文件 / Files Changed

- `plans/todo/2026-05-09-codex-a-project-index-memory.md`
- `plans/todo/2026-05-09-codex-b-trend-engine.md`
- `plans/todo/2026-05-09-codex-c-xhs-system.md`
- `plans/todo/2026-05-09-codex-d-skill-tool-eval.md`
- `plans/todo/2026-05-09-codex-e-business-prd.md`
- `plans/todo/2026-05-09-codex-f-run-report-publisher.md`

## 新建文件 / Files Created

- `plans/run-reports/2026-05-10-six-todo-v2-patch-rewrite-report.md`

## 验证 / Validation

执行了内容校验脚本，确认 6 个任务文件都包含对应 V2 补丁关键词：

- A：`当前执行目标：V2 补丁任务`、`docs/decision-log.md`、`旧任务必须回写`、`默认发布 HTML 报告页`。
- B：`国内外热点`、`YouTube`、`X/Twitter`、`GitHub`、`视觉证据`。
- C：`小红书`、`真实 pilot`、`10-30 条高信号笔记`、`引流/带货/服务`。
- D：`真实试用等级`、`L0 文档审查`、`L2 沙箱运行`、`二次适配评分`。
- E：`可以拿去卖`、`小红书获客`、`试卖素材清单`、`单元经济`。
- F：`任务文件不自包含`、`默认不发布`、`finished 过宽`、`任务完成审查清单`。

校验结果：`all 6 todo files contain v2 patch requirements`。

## 发布链接 / Publish Links

- 本地报告页面：`publish/ai-ip-previews/runs/2026-05-10-six-todo-v2-patch-rewrite/index.html`
- 本地报告索引：`publish/ai-ip-previews/runs/index.html`
- 预期远程链接：`https://schovayang-creator.github.io/ai-ip-previews/runs/2026-05-10-six-todo-v2-patch-rewrite/`

## 跳过项 / Skipped Items

- 没有新建 6 个额外 todo 文件；按用户要求，直接改在原本 6 个 md 文件里。
- 没有执行 6 个 V2 任务本身；本次只负责把任务提示词改对，让后续 6 个 Codex 按新目标运行。
- 没有 push GitHub；本次只生成本地发布目录。

## 风险 / Risks

- 6 个 V2 任务真正执行后仍需要各自更新运行报告和 HTML 页面。
- 旧正文仍保留在文件后半部分，可能有旧 wording；但文件已明确“当前执行目标 V2 以本段为准”。
- 如果后续 Codex 忽略本段，说明它没有按任务文件顺序读取，需要在最终报告中判为不达标。

## 下一步 / Next Actions

用户可以直接复制以下 6 行分别开 Codex：

```text
/goal /Users/yang/Desktop/AI-IP-Studio/plans/todo/2026-05-09-codex-a-project-index-memory.md
/goal /Users/yang/Desktop/AI-IP-Studio/plans/todo/2026-05-09-codex-b-trend-engine.md
/goal /Users/yang/Desktop/AI-IP-Studio/plans/todo/2026-05-09-codex-c-xhs-system.md
/goal /Users/yang/Desktop/AI-IP-Studio/plans/todo/2026-05-09-codex-d-skill-tool-eval.md
/goal /Users/yang/Desktop/AI-IP-Studio/plans/todo/2026-05-09-codex-e-business-prd.md
/goal /Users/yang/Desktop/AI-IP-Studio/plans/todo/2026-05-09-codex-f-run-report-publisher.md
```

## 自评 / Self-Review

- 分数: 96/100
- 达标原因：这次终于把 V2 补丁目标写进了原本 6 个 md 文件，而不是只改模板或新增说明。
- 扣分原因：尚未实际执行 6 个 V2 任务；这一步应该由 6 个并行 Codex 完成。

## 完成说明 / Completion Note

本次修复的是任务提示词层。6 个旧 todo 现在已经不是原样旧任务，而是“读取已有产出 + 对照原始需求 + 做 V2 补丁 + 默认发布报告”的新任务。用户可以继续按习惯只发送 `/goal + 文件路径`。
