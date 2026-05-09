# 运行报告 - 六个旧 Todo 自包含化与 HTML 发布补丁

## 任务信息 / Task Metadata

- 任务 ID: 2026-05-10-six-todo-self-contained-publish-fix
- 模式: office
- 最终状态: finished
- 分数: 95/100
- 结束时间: 2026-05-10
- 报告路径: `plans/run-reports/2026-05-10-six-todo-self-contained-publish-fix-report.md`
- 页面模板: `templates/run-report-page-template.html`

## 目标 / Objective

纠正此前只把 `/goal + 任务文件路径` 标准写进 skill/模板、但没有回写到 6 个已存在 `plans/todo/*.md` 的问题；同时补齐 6 个旧任务缺失的 HTML 运行报告页。

## 交付物 / Deliverables

- 已给 6 个 `plans/todo/2026-05-09-codex-*.md` 增加固定 `/goal` 启动前置要求。
- 已在每个任务文件中写入绝对路径形式的必读文件。
- 已在每个任务文件中写入：托管模式、默认发布报告页、跑通/测试/用户评审/收尾、不达标进 review/blocked。
- 已把 6 个已有 Markdown 运行报告发布成本地 HTML 报告页。
- 已更新 `publish/ai-ip-previews/runs/index.html`。

## 修改文件 / Files Changed

- `plans/todo/2026-05-09-codex-a-project-index-memory.md`
- `plans/todo/2026-05-09-codex-b-trend-engine.md`
- `plans/todo/2026-05-09-codex-c-xhs-system.md`
- `plans/todo/2026-05-09-codex-d-skill-tool-eval.md`
- `plans/todo/2026-05-09-codex-e-business-prd.md`
- `plans/todo/2026-05-09-codex-f-run-report-publisher.md`
- `publish/ai-ip-previews/runs/index.html`

## 新建文件 / Files Created

- `publish/ai-ip-previews/runs/2026-05-09-codex-a-project-index-memory/index.html`
- `publish/ai-ip-previews/runs/2026-05-09-codex-a-project-index-memory/report.md`
- `publish/ai-ip-previews/runs/2026-05-09-codex-b-trend-engine/index.html`
- `publish/ai-ip-previews/runs/2026-05-09-codex-b-trend-engine/report.md`
- `publish/ai-ip-previews/runs/2026-05-09-codex-c-xhs-system/index.html`
- `publish/ai-ip-previews/runs/2026-05-09-codex-c-xhs-system/report.md`
- `publish/ai-ip-previews/runs/2026-05-09-codex-d-skill-tool-eval/index.html`
- `publish/ai-ip-previews/runs/2026-05-09-codex-d-skill-tool-eval/report.md`
- `publish/ai-ip-previews/runs/2026-05-09-codex-e-business-prd/index.html`
- `publish/ai-ip-previews/runs/2026-05-09-codex-e-business-prd/report.md`
- `plans/run-reports/2026-05-10-six-todo-self-contained-publish-fix-report.md`

## 验证 / Validation

- `rg` 验证 6 个 todo 文件均已包含 `/goal 启动前置要求（固定）`。
- `rg` 验证 6 个 todo 文件均已包含 `默认发布运行报告页`、`用户评审`、`不准硬写 finished`、`run-report-publishing-v0.md`。
- 使用 `scripts/publish_run_report.py` 成功发布 6 个已有 Markdown 报告。
- 本地 HTTP 验证全部通过：6 个任务报告页均返回 `HTTP/1.0 200 OK`。
- 本地 `/runs/` 索引返回 `HTTP/1.0 200 OK`。

## 发布链接 / Publish Links

- `publish/ai-ip-previews/runs/2026-05-09-codex-a-project-index-memory/index.html`
- `publish/ai-ip-previews/runs/2026-05-09-codex-b-trend-engine/index.html`
- `publish/ai-ip-previews/runs/2026-05-09-codex-c-xhs-system/index.html`
- `publish/ai-ip-previews/runs/2026-05-09-codex-d-skill-tool-eval/index.html`
- `publish/ai-ip-previews/runs/2026-05-09-codex-e-business-prd/index.html`
- `publish/ai-ip-previews/runs/2026-05-09-codex-f-run-report-publisher/index.html`
- `publish/ai-ip-previews/runs/index.html`

## 风险 / Risks

- 这次补的是旧任务文件和旧报告的本地 HTML 页面；远程 GitHub Pages 是否可见仍取决于是否提交并 push `publish/ai-ip-previews`。
- 旧报告正文里仍可能写着“当时不要求 publish”；但页面已补发，任务文件也已更新，后续重跑会按新标准执行。

## 下一步 / Next Actions

- 如果要手机远程看这些报告，需要提交并推送 `publish/ai-ip-previews/runs/`。
- 后续新 todo 必须从一开始就是自包含 `/goal` 文件，不能只靠模板或 skill 间接约束。

## 自评 / Self-Review

- 分数: 95/100
- 达标原因：6 个旧任务文件本体已补强，6 个旧报告 HTML 页已生成并本地 200 验证。
- 扣分原因：尚未 push 到 GitHub；旧报告正文没有逐篇改写为“新版完成标准”，只是补发了 HTML 和任务文件入口标准。

## 完成说明 / Completion Note

这次纠偏的核心是承认之前漏做：只改模板不等于改已有任务文件。现在 6 个 `plans/todo` 任务已经可以直接用 `/goal + 文件路径` 启动，并且任务文件本身写死了必读、托管、默认发布、用户评审和不达标处理要求。
