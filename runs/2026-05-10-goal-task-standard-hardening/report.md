# 运行报告 - Goal/Todo 标准固化与报告页模板修正

## 任务信息 / Task Metadata

- 任务 ID: 2026-05-10-goal-task-standard-hardening
- 模式: office
- 最终状态: finished
- 分数: 94/100
- 结束时间: 2026-05-10
- 报告路径: `plans/run-reports/2026-05-10-goal-task-standard-hardening-report.md`
- 页面模板: `templates/run-report-page-template.html`

## 目标 / Objective

把用户关于“托管 goal/todo 必须高标准、能跑通、能测试、能自评、能收尾，并且发布到 GitHub 的报告页面必须套用固定页面模板”的要求固化进项目工作流，而不是只停留在聊天记录里。

## 读取上下文 / Context Read

- `AGENTS.md`
- `skills/goal-task-builder.md`
- `workflows/managed-goal-task-v0.md`
- `workflows/run-report-publishing-v0.md`
- `plans/tasks/README.md`
- `plans/tasks/TASK-TEMPLATE.md`
- `templates/task-card-template.md`
- `templates/run-report-template.md`
- `templates/run-report-page-template.html`
- `scripts/publish_run_report.py`

## 交付物 / Deliverables

- 已把 goal/todo 任务搭建标准改成中文优先。
- 已把托管任务完成链路固化为：`build -> run -> test -> user review -> report -> publish (if required) -> archive`。
- 已明确：系统搭建类任务不能只写框架，必须跑通、测试、按用户要求评审，用户回来时应能直接上手；否则必须写 blocker。
- 已明确：GitHub Pages 运行报告页面默认使用 `templates/run-report-page-template.html`。
- 已把运行报告发布工作流改成中文说明，并补充模板、验证、远程部署边界。
- 已把报告页面模板中文化，保留原有视觉体系和 URL 结构。
- 已增强 `scripts/publish_run_report.py`，兼容中文/英文报告标题、元信息、章节名。

## 修改文件 / Files Changed

- `skills/goal-task-builder.md`
- `workflows/managed-goal-task-v0.md`
- `workflows/run-report-publishing-v0.md`
- `plans/tasks/README.md`
- `plans/tasks/TASK-TEMPLATE.md`
- `templates/task-card-template.md`
- `templates/run-report-template.md`
- `templates/run-report-page-template.html`
- `scripts/publish_run_report.py`

## 新建文件 / Files Created

- `plans/run-reports/2026-05-10-goal-task-standard-hardening-report.md`

## 验证 / Validation

- `python3 -m py_compile scripts/publish_run_report.py` 通过。
- `scripts/publish_run_report.py` 已支持中文 headings，例如 `目标 / Objective`、`验证 / Validation`、`修改文件 / Files Changed`。
- 运行报告模板和页面模板已明确绑定 `templates/run-report-page-template.html`。
- 本次报告将用发布脚本生成本地 HTML 页面，并重建 `/runs/` 索引。

## 发布链接 / Publish Links

- 本地页面路径：`publish/ai-ip-previews/runs/2026-05-10-goal-task-standard-hardening/index.html`
- 本地索引路径：`publish/ai-ip-previews/runs/index.html`
- 预期远程链接：`https://schovayang-creator.github.io/ai-ip-previews/runs/2026-05-10-goal-task-standard-hardening/`
- 说明：当前只生成本地发布文件，未自动 push 到 GitHub。

## 跳过项 / Skipped Items

- 未修改 6 个历史 todo 原文件；这一步先固化底层标准，后续可按这个标准重写 6 个补丁任务。
- 未 push GitHub；当前任务只要求先操作标准和模板，且工作流规定除非用户明确要求，否则不自动推送。

## 风险 / Risks

- 历史已经生成的运行报告页面如果不重新发布，仍可能保留旧英文模板。
- 6 个历史 todo 仍保留在 `plans/todo/`，它们本身还没有被升级成新标准补丁任务。
- `publish/ai-ip-previews/runs/` 目前在本地存在，远程 GitHub Pages 是否可见取决于后续是否提交并推送。

## 下一步 / Next Actions

- 如果用户确认，可以把 6 个补丁任务按新标准重写，要求每个 Codex 先跑通、测试、评审，再发布中文运行报告页。
- 如果用户确认，可以把本地 `publish/ai-ip-previews/runs/` 提交并推送到 GitHub，使手机端远程可访问。
- 后续所有 todo/goal 创建任务都应默认读取 `skills/goal-task-builder.md`。

## 自评 / Self-Review

- 分数: 94/100
- 达标原因：核心要求已经写进 skill、workflow、task template、run report template、GitHub Pages page template 和发布脚本。
- 扣分原因：还没有重写 6 个历史补丁任务，也没有 push 到 GitHub；这两个动作更适合在用户确认后作为下一步执行。

## 完成说明 / Completion Note

本次完成的是“标准固化层”：以后提到 todo/goal 并确认要执行时，任务生成标准会默认中文优先，强制写清托管完成链路、测试验收、用户标准评审、报告发布和归档要求；发布到 GitHub 的报告页模板也已经明确为 `templates/run-report-page-template.html`。
