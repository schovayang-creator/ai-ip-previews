# Run Report - Codex D Skill And Tool Evaluation Sandbox V2 Patch

## Task Metadata

- Task ID: `2026-05-09-codex-d-skill-tool-eval-v2`
- Mode: managed / 托管
- Status: review
- Started: 2026-05-10
- Finished: 2026-05-10
- Agent: Codex
- Task prompt: `plans/todo/2026-05-09-codex-d-skill-tool-eval.md`

## Objective

基于已有产出继续做 V2 补丁，不是重写旧制度。目标是把工具/技能评估系统从“框架”补到“能真实试用、能隔离、能二次适配评分”的程度，并产出新的 V2 运行报告页与 `/runs/` 索引。

## Context Read

- `AGENTS.md`
- `plans/tasks/README.md`
- `skills/goal-task-builder.md`
- `workflows/managed-goal-task-v0.md`
- `workflows/run-report-publishing-v0.md`
- `plans/todo/2026-05-09-codex-d-skill-tool-eval.md`
- `plans/run-reports/2026-05-09-codex-d-skill-tool-eval-report.md`
- `publish/ai-ip-previews/runs/2026-05-09-codex-d-skill-tool-eval/index.html`
- `publish/ai-ip-previews/runs/2026-05-09-codex-d-skill-tool-eval/report.md`
- `experiments/README.md`
- `experiments/skill-evals/README.md`
- `experiments/tool-evals/README.md`
- `docs/skill-and-tool-evaluation-guide.md`
- `docs/installed-skill-map.md`
- `docs/tool-candidates.md`

## 旧产物与 V2 需求差距

旧任务产物已经把沙盒框架、模板、技能地图、评估指南和旧运行报告搭起来了，但 V2 仍缺三类关键东西：

1. **真实试用等级不够明确**：旧版本只有宽泛的 L0-L5 思路，缺少“进入条件 / 退出条件 / 能做什么 / 不能做什么”的可执行试用梯子。
2. **技能调用时机不够实用**：旧版本有 routing map，但还没有“什么时候必须调用 / 什么时候不该调用”的硬矩阵，尤其 goal、account、trend、XHS、business、publishing、dbskill 这些高频分支。
3. **候选工具评估不够落地**：旧版本列了候选工具和搜索计划，但 V2 需要更明确的非安装型评估路径、理由、以及下一步 L1/L2 测试动作。

旧 run report 和旧 HTML 页面只作为输入材料；本次 V2 不能把它们当完成证据。

## Files Changed

- `experiments/tool-evals/README.md`
- `docs/installed-skill-map.md`
- `docs/skill-and-tool-evaluation-guide.md`

## Files Created

- `plans/run-reports/2026-05-09-codex-d-skill-tool-eval-v2-report.md`
- `publish/ai-ip-previews/runs/2026-05-09-codex-d-skill-tool-eval-v2/report.md` *(published copy, to be generated)*
- `publish/ai-ip-previews/runs/2026-05-09-codex-d-skill-tool-eval-v2/index.html` *(published copy, to be generated)*
- `publish/ai-ip-previews/runs/index.html` *(updated index, to be generated)*

## Deliverables

### 1. 更可执行的沙箱试用梯子

已在 `experiments/tool-evals/README.md` 补充 V2 试用等级：

- `L0 文档审查`
- `L1 本地无网络安全测试`
- `L2 沙箱运行`
- `L3 接入 AI-IP-Studio 样例任务`
- `L4 适配原型`
- `L5 推广候选`

每一级都写了进入条件、退出条件和允许动作，避免以后只靠抽象模板猜步骤。

### 2. 更实用的技能调用矩阵

已在 `docs/installed-skill-map.md` 增补：

- `Must-call / Should-not-call` 矩阵；
- goal、account、trend、XHS、publishing、reports、business、writing 的更细粒度调用边界；
- `dbs-*`、`lark-*`、Office 技能何时该用、何时不该用。

### 3. 候选工具非安装型评估路径

已在 `docs/skill-and-tool-evaluation-guide.md` 增补：

- 5 个重点候选：`yt-dlp`、`XHS-Downloader`、`MediaCrawler`、`RSSHub`、`auto-editor`；
- 每个候选为什么值得看、为什么暂时不直接下载运行；
- 下一步安全测试命令/动作；
- 继续坚持“不全局安装、不碰 cookie/token、不污染主项目”。

### 4. V2 报告与发布页

本次任务要求新的 V2 Markdown 报告、HTML 报告页、`report.md` 副本和 `/runs/` 索引。

这些产物需要通过本地发布脚本和 HTTP 验证后，才能算 V2 证据完整。

## Validation

### 已完成的审计动作

- 重新读取了任务文件最前面的三段：`goal` 启动前置要求、`V2 防误判硬规则`、`当前执行目标：V2 补丁任务`。
- 重新读取了旧产物和旧 report，确认它们只能作为输入，不能当本次完成证据。
- 检查了当前修改文件，确认 V2 的实质补丁落在：
  - 试用梯子；
  - 技能调用矩阵；
  - 候选工具的非安装型评估路径。

### 待执行的发布验证

- 运行 `python3 scripts/publish_run_report.py plans/run-reports/2026-05-09-codex-d-skill-tool-eval-v2-report.md`。
- 启动本地 HTTP 服务并验证：
  - `curl -I http://127.0.0.1:8765/runs/`
  - `curl -I http://127.0.0.1:8765/runs/2026-05-09-codex-d-skill-tool-eval-v2/`
- 若返回 `HTTP/1.0 200 OK`，再把状态从 `review` 改为 `finished`。

## Published Report

- Local report: `plans/run-reports/2026-05-09-codex-d-skill-tool-eval-v2-report.md`
- Published HTML: `publish/ai-ip-previews/runs/2026-05-09-codex-d-skill-tool-eval-v2/index.html`
- Published Markdown: `publish/ai-ip-previews/runs/2026-05-09-codex-d-skill-tool-eval-v2/report.md`
- Runs index: `publish/ai-ip-previews/runs/index.html`
- Expected remote URL: `https://schovayang-creator.github.io/ai-ip-previews/runs/2026-05-09-codex-d-skill-tool-eval-v2/`

## Blockers / Risks

- 目前还没完成本地 HTTP 200 验证，所以最终状态暂时保留为 `review`。
- 这次 V2 仍然没有做真实平台登录或 cookie 型工具测试；这是刻意的安全约束，不是遗漏。
- `docs/tool-candidates.md` 没有改动，因为本次 V2 的重点是把“可试用、可隔离、可重评分”的执行面补齐到核心文档和报告链路里。

## Next Actions

1. 运行发布脚本生成 V2 HTML 报告页与 `/runs/` 索引。
2. 用本地 HTTP 服务验证 `runs/` 和具体报告页都返回 200。
3. 如果验证通过，把报告状态改成 `finished`，并刷新发布页。
4. 后续再按这套 V2 梯子去试 `yt-dlp`、`RSSHub`、`XHS-Downloader`、`MediaCrawler`、`auto-editor`。

## Self-Review

- Score: 92/100
- Completion gate passed: no
- Strong points:
  - V2 的差距被明确拆出来了，而不是继续拿旧框架当完成。
  - 实验沙箱、技能矩阵、候选评估路径都变成了可执行条目。
  - 新的 V2 报告路径与发布路径已经明确。
- Weak points:
  - 还缺最终发布验证和 HTTP 200 证据。
  - 还没有真正执行外部工具的 L1/L2 样例测试，只是把试用路径补齐了。
- What was skipped and why:
  - 全局安装、cookie/登录测试、原始媒体处理：因为任务明确要求安全隔离。
  - 直接改 `docs/tool-candidates.md`：因为本次补丁目标更聚焦在执行面和发布链路。
