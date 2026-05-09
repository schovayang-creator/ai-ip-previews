# 运行报告 - V2 任务防旧报告误判硬锁

## 任务信息 / Task Metadata

- 任务 ID: 2026-05-10-v2-hard-lock-against-old-report-complete
- 模式: office
- 最终状态: finished
- 分数: 97/100
- 结束时间: 2026-05-10
- 报告路径: `plans/run-reports/2026-05-10-v2-hard-lock-against-old-report-complete-report.md`
- 页面模板: `templates/run-report-page-template.html`

## 目标 / Objective

修复另一个 Codex 继续把旧任务报告、自评 94/100、旧交付物存在当成当前 V2 任务完成证据的问题。现在 6 个 todo 文件都写入了更硬的防误判规则：旧报告和旧 HTML 只能作为输入，不能作为 V2 完成依据。

## 交付物 / Deliverables

- 6 个 `plans/todo/2026-05-09-codex-*.md` 均已写入 `V2 防误判硬规则（必须遵守）`。
- 每个任务都明确禁止：只复核旧产物后宣布 `complete` / `finished`。
- 每个任务都明确禁止：把旧报告的分数、状态、checklist 当成当前 V2 完成证据。
- 每个任务都明确禁止：把旧 HTML 页面当成当前 V2 发布结果。
- 每个任务都要求生成新的 `*-v2-report.md` 和新的 `runs/*-v2/index.html`。
- 每个任务都要求至少有一个 V2 目标相关的实质文件改动；否则只能进 `review`，不能 finished。
- 每个任务都要求最终回复必须包含新的 V2 报告路径和新的 V2 HTML 路径，否则视为未完成。

## 修改文件 / Files Changed

- `plans/todo/2026-05-09-codex-a-project-index-memory.md`
- `plans/todo/2026-05-09-codex-b-trend-engine.md`
- `plans/todo/2026-05-09-codex-c-xhs-system.md`
- `plans/todo/2026-05-09-codex-d-skill-tool-eval.md`
- `plans/todo/2026-05-09-codex-e-business-prd.md`
- `plans/todo/2026-05-09-codex-f-run-report-publisher.md`

## 新建文件 / Files Created

- `plans/run-reports/2026-05-10-v2-hard-lock-against-old-report-complete-report.md`

## 验证 / Validation

已用 `rg` 验证 6 个文件均包含：

- `V2 防误判硬规则（必须遵守）`
- `禁止只复核旧产物后宣布 complete / finished`
- `禁止把旧报告 ... 当成本次 V2 的完成证据`
- `禁止把旧 HTML 页面 ... 当成本次 V2 发布结果`
- 新的 V2 Markdown 运行报告路径
- 新的 V2 HTML 报告页路径
- `至少一个与 V2 补丁目标直接相关的实质文件改动`
- `最终回复必须包含新的 V2 报告路径和新的 V2 HTML 路径`

## 发布链接 / Publish Links

- 本地报告页面：`publish/ai-ip-previews/runs/2026-05-10-v2-hard-lock-against-old-report-complete/index.html`
- 本地报告索引：`publish/ai-ip-previews/runs/index.html`
- 预期远程链接：`https://schovayang-creator.github.io/ai-ip-previews/runs/2026-05-10-v2-hard-lock-against-old-report-complete/`

## 风险 / Risks

- 如果某个 Codex 不读任务文件前半部分，仍可能误判；但现在任务文件已经把禁止项放在旧正文前面，合理执行时不应再误判。
- 旧正文仍保留为历史参考，不能覆盖 V2 防误判硬规则。

## 下一步 / Next Actions

重新启动 6 个 `/goal` 时，如果它回复“旧产物已完成”，可直接判定它没有遵守任务文件；正确完成必须产生 `*-v2-report.md` 和 `*-v2/index.html`。

## 自评 / Self-Review

- 分数: 97/100
- 达标原因：这次将“旧报告不能作为完成证据”写成了明确禁止项，并给每个任务指定了新的 V2 report / HTML 路径。
- 扣分原因：尚未实际执行 6 个 V2 任务本身。

## 完成说明 / Completion Note

当前 6 个 todo 文件已经具备硬锁：不能再用旧 94/100 报告或旧 HTML 页面宣布 V2 complete；必须做新补丁、新报告、新 HTML。
