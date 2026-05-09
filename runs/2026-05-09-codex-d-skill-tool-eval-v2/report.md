public_final: true
canonical_slug: codex-d-skill-tool-eval
report_visibility: public
version: 2

# Run Report - Codex D Skill And Tool Evaluation Sandbox V2 Patch

## Task Metadata

- Task ID: `2026-05-09-codex-d-skill-tool-eval-v2`
- Mode: managed / 托管
- Status: finished
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
- `publish/ai-ip-previews/runs/2026-05-09-codex-d-skill-tool-eval-v2/report.md`
- `publish/ai-ip-previews/runs/2026-05-09-codex-d-skill-tool-eval-v2/index.html`
- `publish/ai-ip-previews/runs/index.html`

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

- 重新读取了任务文件最前面的三段：`/goal 启动前置要求`、`V2 防误判硬规则`、`当前执行目标：V2 补丁任务`。
- 重新读取了旧产物和旧 report，确认它们只能作为输入，不能当本次完成证据。
- 检查了当前修改文件，确认 V2 的实质补丁落在：
  - 试用梯子；
  - 技能调用矩阵；
  - 候选工具的非安装型评估路径。

### 发布验证结果

- 发布命令：`python3 scripts/publish_run_report.py plans/run-reports/2026-05-09-codex-d-skill-tool-eval-v2-report.md`
- 生成结果：
  - `publish/ai-ip-previews/runs/2026-05-09-codex-d-skill-tool-eval-v2/index.html`
  - `publish/ai-ip-previews/runs/2026-05-09-codex-d-skill-tool-eval-v2/report.md`
  - `publish/ai-ip-previews/runs/index.html`
- 本地 HTTP 验证：
  - `curl -I http://127.0.0.1:8765/runs/` -> `HTTP/1.0 200 OK`，`Content-Length: 12034`
  - `curl -I http://127.0.0.1:8765/runs/2026-05-09-codex-d-skill-tool-eval-v2/` -> `HTTP/1.0 200 OK`，`Content-Length: 9917`
- 远程 HTTP 200 复验：`https://schovayang-creator.github.io/ai-ip-previews/runs/2026-05-09-codex-d-skill-tool-eval-v2/` -> `HTTP 200`

## Published Report

- Local report: `plans/run-reports/2026-05-09-codex-d-skill-tool-eval-v2-report.md`
- Published HTML: `publish/ai-ip-previews/runs/2026-05-09-codex-d-skill-tool-eval-v2/index.html`
- Published Markdown: `publish/ai-ip-previews/runs/2026-05-09-codex-d-skill-tool-eval-v2/report.md`
- Runs index: `publish/ai-ip-previews/runs/index.html`
- Remote URL: `https://schovayang-creator.github.io/ai-ip-previews/runs/2026-05-09-codex-d-skill-tool-eval-v2/`

## Blockers / Risks

- 这次 V2 仍然没有做真实平台登录或 cookie 型工具测试；这是刻意的安全约束，不是遗漏。
- `docs/tool-candidates.md` 没有改动，因为本次 V2 的重点是把“可试用、可隔离、可重评分”的执行面补齐到核心文档和报告链路里。

## Next Actions

1. 后续按这套 V2 梯子去试 `yt-dlp`、`RSSHub`、`XHS-Downloader`、`MediaCrawler`、`auto-editor`。
2. 每个工具都先建 `experiments/tool-evals/YYYYMMDD-tool-slug/`，再填 source、install log、test plan、raw outputs、safety review、adaptation notes、scorecard。
3. 只有 L0/L1/L2 通过后，才考虑接入 AI-IP-Studio 样例任务。

## Self-Review

- Score: 92/100
- Completion gate passed: yes
- Strong points:
  - V2 的差距被明确拆出来了，而不是继续拿旧框架当完成。
  - 实验沙箱、技能矩阵、候选评估路径都变成了可执行条目。
  - 新的 V2 报告路径与发布路径已经明确。
- Weak points:
  - 还没有真正执行外部工具的 L1/L2 样例测试；本次 V2 的定位是把试用路径、隔离规则、候选动作和发布证据补齐。
- What was skipped and why:
  - 全局安装、cookie/登录测试、原始媒体处理：因为任务明确要求安全隔离。
  - 直接改 `docs/tool-candidates.md`：因为本次补丁目标更聚焦在执行面和发布链路。

## A-F 严格收尾补充 / Final Sweep

- 收尾日期: 2026-05-10
- 收尾范围: A-F 历史 V2 任务的报告事实校正、任务迁移、final-only 公开索引重建和 GitHub Pages 复验。
- 源任务文件最终位置: `plans/finished/2026-05-09-codex-d-skill-tool-eval.md`
- 公开最终报告标记: `public_final: true`，`canonical_slug: codex-d-skill-tool-eval`，`report_visibility: public`，`version: 2`。
- 远程报告页: `https://schovayang-creator.github.io/ai-ip-previews/runs/2026-05-09-codex-d-skill-tool-eval-v2/`
- 远程报告页 HTTP: `200`（A-F 收尾流程复验）。
- 公开索引策略: 只展示本任务 V2 最终版；旧版和中间补丁不作为公开最终版本展示。
- 说明: 旧报告中关于“未 push / 待部署 / 预期远程 URL”的过期表述已按当前事实修正。
