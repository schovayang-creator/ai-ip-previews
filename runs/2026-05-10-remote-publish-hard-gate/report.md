# 运行报告 - remote publish hard gate

- Task ID: 2026-05-10-remote-publish-hard-gate
- 状态: finished
- 模式: office
- 分数: 93/100
- 更新时间: 2026-05-10

## 目标

修正托管 goal/todo 的完成标准：本地生成 HTML 不等于发布完成。以后默认必须把对应运行报告页提交并推送到 `publish/ai-ip-previews` 独立 GitHub Pages 仓库，并验证远程 URL HTTP 200，才允许写 finished。

## 交付物

- 已补齐 7 个 todo 文件中的远程发布硬门槛：`git push`、`remote HTTP 200`、只 add 本任务 run 目录和 `runs/index.html`。
- 已补齐核心标准文件：`skills/goal-task-builder.md`、`workflows/managed-goal-task-v0.md`、`workflows/run-report-publishing-v0.md`、`plans/tasks/README.md`、`templates/task-card-template.md`、`plans/tasks/TASK-TEMPLATE.md`。
- 已修正 `scripts/publish_run_report.py`：默认重建运行报告索引时过滤未被 nested publish repo 跟踪的本地 run 目录，避免主页索引提前指向未 push 的 404 页面；如确实要展示全部本地 run，可显式使用 `--include-untracked-index`。

## 修改文件

- `plans/todo/2026-05-09-codex-a-project-index-memory.md`
- `plans/todo/2026-05-09-codex-b-trend-engine.md`
- `plans/todo/2026-05-09-codex-c-xhs-system.md`
- `plans/todo/2026-05-09-codex-d-skill-tool-eval.md`
- `plans/todo/2026-05-09-codex-e-business-prd.md`
- `plans/todo/2026-05-09-codex-f-run-report-publisher.md`
- `plans/todo/2026-05-10-codex-g-platform-collector-adapters.md`
- `workflows/run-report-publishing-v0.md`
- `templates/task-card-template.md`
- `plans/tasks/TASK-TEMPLATE.md`
- `scripts/publish_run_report.py`

## 验证

- 运行 Python 检查：7 个 todo 均包含 `publish/ai-ip-previews`、`git push`、`remote HTTP 200`、`只 add`。
- 运行 Python 检查：6 个核心标准/模板文件均包含 `publish/ai-ip-previews`、`git push`、`remote HTTP 200`。
- 本报告已通过 `scripts/publish_run_report.py` 生成本地 HTML 页面。

## 完成说明

这次修正的关键不是再加一个报告页，而是把用户期望写成硬标准：托管任务默认发布远程可访问报告页；没有 commit hash 和远程 HTTP 200 URL，就不能 finished。并行任务只能提交自己的 run 目录，不能顺手推送其他 Codex 生成的未跟踪目录。

## 风险

- 已经跑完的其他 Codex 如果没有重新读取任务文件，仍可能按旧标准回复；需要给它们追加统一通知。
- 当前项目工作区很脏，存在大量其他任务产生的未跟踪文件；本次没有批量提交它们，避免污染并行任务边界。

## 下一步

- 对已经回复 finished 但没有远程 HTTP 200 的 Codex，发送统一补发提示：补 commit/push/remote HTTP 200，不达标改 review 或 blocked。
- 以后新建 todo 时，直接使用已更新的模板，不再依赖聊天上下文。
