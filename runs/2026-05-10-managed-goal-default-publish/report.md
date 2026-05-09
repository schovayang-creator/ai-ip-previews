# 运行报告 - 托管 Goal 默认发布规则补丁

## 任务信息 / Task Metadata

- 任务 ID: 2026-05-10-managed-goal-default-publish
- 模式: office
- 最终状态: finished
- 分数: 96/100
- 结束时间: 2026-05-10
- 报告路径: `plans/run-reports/2026-05-10-managed-goal-default-publish-report.md`
- 页面模板: `templates/run-report-page-template.html`

## 目标 / Objective

把用户最新要求固化到项目标准里：正常开启 goal 模式通常就是托管任务，所以运行报告页面默认要发布到 GitHub Pages 发布目录；只有任务明确写“不发布”时才允许跳过。

## 交付物 / Deliverables

- 已把 goal/todo 标准链路改成 `publish by default`。
- 已把任务卡模板的 `publish_report_required` 默认值改成 `true`。
- 已把托管工作流的 `publish_report_required` 默认值改成 `true`。
- 已在运行报告发布工作流里写明：托管 `/goal` 默认要求生成可远程查看的完成报告。
- 已保留安全边界：默认生成发布目录和页面，不代表无条件 push；push/远程上线仍按用户授权或发布任务要求执行。

## 修改文件 / Files Changed

- `skills/goal-task-builder.md`
- `workflows/managed-goal-task-v0.md`
- `workflows/run-report-publishing-v0.md`
- `plans/tasks/README.md`
- `plans/tasks/TASK-TEMPLATE.md`
- `templates/task-card-template.md`
- `templates/run-report-template.md`

## 新建文件 / Files Created

- `plans/run-reports/2026-05-10-managed-goal-default-publish-report.md`

## 验证 / Validation

- 使用 `rg` 检查到核心文件均已出现 `publish_report_required: true` 或“默认发布”规则。
- `templates/task-card-template.md` 和 `plans/tasks/TASK-TEMPLATE.md` 已默认写入 `publish_report_required: true`。
- `workflows/run-report-publishing-v0.md` 已明确托管 `/goal` 默认发布运行报告页。
- 本报告已通过 `scripts/publish_run_report.py --check`，并生成本地 HTML 页面。

## 发布链接 / Publish Links

- 本地页面路径：`publish/ai-ip-previews/runs/2026-05-10-managed-goal-default-publish/index.html`
- 本地索引路径：`publish/ai-ip-previews/runs/index.html`
- 预期远程链接：`https://schovayang-creator.github.io/ai-ip-previews/runs/2026-05-10-managed-goal-default-publish/`
- 说明：当前生成的是本地发布目录；是否 push 到 GitHub 由后续发布动作决定。

## 风险 / Risks

- 默认发布会增加每个任务的收尾工作量，但符合托管场景下“用户回来手机能看报告”的要求。
- 如果某些敏感任务不适合发布，任务卡必须明确写“不发布”并说明原因。

## 下一步 / Next Actions

- 后续重写 6 个补丁任务时，默认把 `publish_report_required` 保持为 `true`。
- 每个 Codex 完成任务后，都应生成中文 Markdown 报告、本地 HTML 报告页，并更新 `/runs/` 索引。

## 自评 / Self-Review

- 分数: 96/100
- 达标原因：默认发布规则已写入 skill、workflow、任务模板和报告模板。
- 扣分原因：尚未把这条规则回填进 6 个历史 todo 补丁任务；那属于下一批任务重写。

## 完成说明 / Completion Note

现在项目默认规则已经调整为：托管 goal/todo 默认发布运行报告页，并套用 `templates/run-report-page-template.html`；除非任务明确写“不发布”，否则不应跳过发布页生成与索引更新。
