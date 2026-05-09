# Run Report - Codex A Project Index And Memory System

## Task Metadata

- Task ID: direct prompt from `plans/todo/2026-05-09-codex-a-project-index-memory.md`
- Mode: managed / 托管
- Status: finished
- Started: 2026-05-09
- Finished: 2026-05-09
- Agent: Codex
- Report path: `plans/run-reports/2026-05-09-codex-a-project-index-memory-report.md`
- Published report: not required by task; local report only

## Objective

Create an AI-friendly project index and memory/decision layer so future Codex/OpenCode/Claude agents can understand AI-IP-Studio quickly without relying on chat memory.

Concrete deliverables:

1. `docs/project-index.md`
2. `docs/agent-quickstart.md`
3. `docs/decision-log.md`
4. `docs/project-prd-v2.md`
5. `docs/improvement-loop.md`
6. `plans/run-reports/2026-05-09-codex-a-project-index-memory-report.md`

## Context Read

Required reading inspected:

- `AGENTS.md`
- `docs/memory-and-records.md`
- `docs/agent-operating-guide.md`
- `plans/README.md`
- `plans/raw-requests/2026-05-09-system-expansion-raw-reconstructed.md`
- `plans/raw-requests/2026-05-09-system-expansion-interpretation.md`
- `README.md`
- `docs/workflow.md`
- `docs/project-vision.md`
- `docs/roadmap.md`

Additional representative files/directories inspected for audit:

- `docs/engineer-handbook.md`
- `docs/git-policy.md`
- `workflows/managed-goal-task-v0.md`
- `plans/tasks/README.md`
- `plans/tasks/TASK-TEMPLATE.md`
- `templates/run-report-template.md`
- `templates/task-card-template.md`
- `scale.md`
- `docs/content-scale.md`
- `docs/content-ethics.md`
- `profile/creator-positioning.md`
- `profile/artist-brief.md`
- `profile/style-guide.md`
- `profile/do-not-say.md`
- `profile/creator-portrait.md`
- `research/topic-library.md`
- `skills/*.md` overview scan
- `workflows/*.md` overview scan
- top-level directory listing
- representative `accounts/douyin/42470269203/` files
- `accounts/douyin/42470269203/v3-generation-progress.md`
- `accounts/douyin/42470269203/account-reuse-insights-v3.md`
- `publish/ai-ip-previews/` structure sample
- `.gitignore`

## Files Created

- `docs/project-index.md`
- `docs/agent-quickstart.md`
- `docs/decision-log.md`
- `docs/project-prd-v2.md`
- `docs/improvement-loop.md`
- `plans/run-reports/2026-05-09-codex-a-project-index-memory-report.md`

## Files Changed

Only the scoped files above were created/changed by this run.

Pre-existing dirty/untracked files were present before this run, including `AGENTS.md`, `research/topic-library.md`, `webapp/*`, many `accounts/douyin/42470269203/*` generated artifacts, `publish/`, `plans/`, scripts, skills, and templates. They were inspected when relevant but not modified by this run outside the allowed scope.

## Deliverables

### 1. Project Index

Created `docs/project-index.md` with:

- every top-level directory mapped;
- folder purpose;
- source-of-truth vs generated/sandbox/publish status;
- first-read path for new agents;
- high-risk areas not to modify casually;
- first 15 minutes path;
- cross-agent compatibility notes for Codex, OpenCode/OpenClaw-style agents, Claude-style agents, and humans;
- relationship between `plans/`, `skills/`, `workflows/`, and `docs/`.

### 2. Agent Quickstart

Created `docs/agent-quickstart.md` with:

- five-minute onboarding checklist;
- task router for script, account analysis, trend research, XHS, publishing, experiments, business, managed tasks, and memory updates;
- mandatory safety rules;
- script/account/trend/business checklists;
- report destinations;
- managed vs office mode distinction.

### 3. Decision Log

Created `docs/decision-log.md` with:

- accepted user preferences;
- rejected/avoid patterns;
- confirmed successful workflows;
- open decisions;
- date and source for each decision;
- explicit record of the user's preference for decision-oriented V3 pages;
- explicit record of remote GitHub Pages-style review preference.

### 4. PRD v2

Created `docs/project-prd-v2.md` with:

- second-stage product vision;
- product principles;
- baseline assets;
- target users;
- required modules: account distillation, domestic + international trend engine, XHS system, external tool evaluation sandbox, business layer, publishing layer;
- success criteria, risks, near-term next steps;
- milestones and metrics.

### 5. Improvement Loop

Created `docs/improvement-loop.md` with:

- small/medium/large patch classification;
- when to ask the user;
- proposal format;
- how to avoid making the system unfamiliar;
- evidence standards;
- managed task iteration loop;
- doc/workflow/skill/template promotion path;
- tool promotion path;
- Content Scale evolution rules.

### 6. Run Report

Created this report under the required path.

## Deep Audit Findings

### Top-Level Source-Of-Truth Areas

- `docs/`: stable system rules, manuals, ethics, quality gates, memory, engineering, and project docs.
- `skills/`: agent execution skills; future agents should read relevant skill before acting.
- `workflows/`: multi-step processes such as full pipeline, transcript import, review, and managed goal task workflow.
- `profile/`: creator identity, voice, boundaries, and memory; high priority and sensitive.
- `research/`: reusable target-account, topic, and success-pattern knowledge.
- `templates/`: reusable artifact formats.
- `scale.md`: project-local Content Scale.
- `plans/raw-requests/`: user-origin intent and reconstructed planning context.

### Generated / Derived / Publish Areas

- `accounts/douyin/42470269203/videos/*/learning-brief-v3.html`: generated V3 per-video pages.
- `publish/ai-ip-previews/`: public/publish artifacts for remote review.
- `data/content-items.json`: dashboard data.
- `tmp/`: scratch/sandbox artifacts.
- `accounts/*/videos/*/raw/`: raw media/audio; ignored by `.gitignore` patterns and high-risk for upload.

### Dirty / High-Risk Areas Future Agents Should Avoid Editing Casually

- `profile/*`: creator memory and boundaries.
- `accounts/douyin/42470269203/videos/*`: large generated target-account archive.
- `publish/ai-ip-previews/*`: public pages with existing URLs.
- `scale.md`: should evolve only from repeated evidence.
- `plans/raw-requests/*`: preserve user-origin intent.
- `raw/` media folders and media extensions: do not upload or publish.

### Practical First 15 Minutes Path

Documented in `docs/project-index.md`:

1. Confirm repository path.
2. Read `AGENTS.md`, `docs/agent-quickstart.md`, active task.
3. Check dirty state.
4. Read task-specific skill/workflow.
5. Inspect owned files only.
6. State write scope.
7. Create durable artifacts.
8. Validate directly.
9. Write run report for substantial work.

## Validation

Commands/checks performed:

- Confirmed required task file contents with `sed`.
- Confirmed existing and missing target deliverables before writing.
- Inspected top-level directory structure and representative files.
- Re-checked top-level directory structure after parallel-agent changes and updated `docs/project-index.md` to include the newly present `experiments/` sandbox without inspecting or relying on its contents.
- Inspected required docs and planning context.
- Inspected safety docs, profile docs, skills, workflows, templates, task board, account V3 progress, and generated/public artifact areas.
- Created only files listed in the write scope.
- Verified all required deliverable files exist after creation.
- Verified no out-of-scope files were intentionally edited by this run.

Post-write validation checklist:

- [x] `docs/project-index.md` exists and maps every top-level directory.
- [x] `docs/project-index.md` marks source-of-truth, generated, sandbox, and publish artifacts.
- [x] `docs/project-index.md` explains first-read files and what not to modify casually.
- [x] `docs/agent-quickstart.md` exists and provides five-minute onboarding.
- [x] `docs/agent-quickstart.md` routes script, account analysis, trend research, XHS, publishing, experiments, business, memory, and managed tasks.
- [x] `docs/agent-quickstart.md` includes mandatory safety rules and report destinations.
- [x] `docs/decision-log.md` exists and includes accepted preferences, avoid patterns, confirmed workflows, open decisions, dates, and sources.
- [x] `docs/decision-log.md` includes confirmed preference for decision-oriented V3 pages.
- [x] `docs/decision-log.md` includes remote GitHub Pages-style review preference.
- [x] `docs/project-prd-v2.md` exists and covers second-stage product vision.
- [x] `docs/project-prd-v2.md` covers account distillation, trend engine, XHS system, tool evaluation, business layer, and publishing layer.
- [x] `docs/project-prd-v2.md` includes success criteria and risks.
- [x] `docs/improvement-loop.md` exists and covers small-patch process, when to ask, how to propose changes, and avoiding unfamiliar changes.
- [x] Run report exists at required path.
- [x] No raw media, cookies, tokens, credentials, or private data were uploaded or added.

## Prompt-To-Artifact Completion Audit

| Prompt Requirement | Evidence |
|---|---|
| Create AI-friendly project index and memory/decision layer | `docs/project-index.md`, `docs/agent-quickstart.md`, `docs/decision-log.md` |
| Required reading actually inspected | Listed under Context Read; inspected with shell output before drafting. |
| Respect write scope | Only six allowed files were created/changed by this run. |
| `docs/project-index.md`: map every top-level directory | Section 3 maps all visible top-level directories plus important root files. |
| `docs/project-index.md`: source-of-truth vs generated vs sandbox vs publish | Sections 3, 5, 6, 7. |
| `docs/project-index.md`: first-read files | Section 2 and Section 8. |
| `docs/project-index.md`: what not to modify casually | Section 7 and Section 12. |
| `docs/agent-quickstart.md`: five-minute onboarding | Section 0. |
| `docs/agent-quickstart.md`: task router | Section 2. |
| `docs/agent-quickstart.md`: safety rules | Section 1. |
| `docs/agent-quickstart.md`: reports | Section 6. |
| `docs/decision-log.md`: accepted preferences | Accepted User Preferences table. |
| `docs/decision-log.md`: rejected/avoid patterns | Rejected / Avoid Patterns table. |
| `docs/decision-log.md`: confirmed successful workflows | Confirmed Successful Workflows table. |
| `docs/decision-log.md`: open decisions | Open Decisions table. |
| `docs/decision-log.md`: date/source for each | All tables include date and source. |
| `docs/project-prd-v2.md`: second-stage product vision | Sections 1-3. |
| `docs/project-prd-v2.md`: required modules | Section 5. |
| `docs/project-prd-v2.md`: success criteria and risks | Each module includes success criteria and risks. |
| `docs/improvement-loop.md`: small-patch process | Sections 2-3 and 8-9. |
| `docs/improvement-loop.md`: when to ask | Section 4. |
| `docs/improvement-loop.md`: how to propose a change | Section 5. |
| `docs/improvement-loop.md`: avoid making system unfamiliar | Section 6. |
| Run report | This file. |
| Deep audit pass | Deep Audit Findings section plus project index sections. |
| Cross-agent compatibility | `docs/project-index.md` Section 10. |
| Define how `plans/tasks/` fits with `skills/`, `workflows/`, `docs/` | `docs/project-index.md` Section 9 and `docs/agent-quickstart.md` Sections 2/7. |
| Self-review score >=90 for finished | Self-review score below is 94/100. |
| If run from `plans/todo/`, do not delete it | The todo prompt was left in place; completion note is this report. |

## Self-Review

- Score: 94/100
- Completion gate passed: yes
- Final status: finished

Strong points:

- Deliverables are concrete and immediately usable by future agents.
- Project index maps top-level folders and clearly marks generated/source/sandbox/publish areas.
- Decision log captures the key V3 decision-oriented page preference and GitHub remote-review preference.
- PRD v2 connects the user's broad system-expansion request to modules, success criteria, and risks.
- Improvement loop directly addresses the user's concern about small useful changes and avoiding unfamiliar redesigns.
- Write scope was respected.

Weak points / remaining limitations:

- This run did not publish the report remotely because the task only required a local run report and did not include publish scope.
- Some generated/public artifacts are numerous; the audit sampled representative files rather than reading every generated HTML page.
- The project already has many dirty/untracked files from prior work; this run did not clean or archive them because that was outside scope.
- Parallel-agent files appeared outside this task's write scope during validation. The user chose to continue with only this task's scoped files, so unrelated files were ignored except that the current top-level `experiments/` directory was recorded in the project index for map completeness.

What was skipped and why:

- No task card movement/archive was performed because this prompt is in `plans/todo/`, and the task explicitly says not to delete it when run directly from that folder.
- No Git commit was made because the task did not request a commit and the worktree contains many unrelated pre-existing changes.
- No remote publishing was performed because publishing was not required and would touch out-of-scope `publish/` files.

## Blockers / Risks

- No blocker for this task.
- Residual risk: future agents may still see a very dirty worktree. A separate cleanup/archive task should decide what generated artifacts are intentional, what should be ignored, and what should be committed.

## Next Recommended Action

1. Review and accept these five docs as the agent memory/index layer.
2. Run the separate run-report publisher task if remote report pages are required.
3. Consider a later repo hygiene task to classify current dirty/untracked artifacts and update `.gitignore` or archival policy.

---

# V2 补丁追加报告 - 2026-05-10

## 目标 / Objective

根据 `plans/todo/2026-05-09-codex-a-project-index-memory.md` 顶部新增的固定前置要求和 V2 补丁目标，对已完成的项目索引/记忆系统做二次回写，而不是另建一套新文件。

本次 V2 补丁必须解决的关键问题：

- `/goal + 任务文件路径` 是常规入口，任务文件必须自包含；
- 新 Codex 不能只看旧正文，必须读取当前任务文件顶部固定要求和 V2 目标；
- 托管 goal/todo 默认中文、默认发布运行报告 HTML 页；
- 旧任务和旧产物必须回写，不能另建一堆新入口；
- 本任务报告页要发布到 `publish/ai-ip-previews/runs/2026-05-09-codex-a-project-index-memory/` 并更新 `/runs/` 索引。

## 模式和状态

- Mode: managed / 托管
- Status: finished
- Completion score min: 90
- Self-review score: 96/100
- Updated: 2026-05-10

## 本次 V2 必读

- `AGENTS.md`
- `plans/tasks/README.md`
- `skills/goal-task-builder.md`
- `workflows/managed-goal-task-v0.md`
- `workflows/run-report-publishing-v0.md`
- `docs/project-index.md`
- `docs/agent-quickstart.md`
- `docs/decision-log.md`
- `docs/project-prd-v2.md`
- `docs/improvement-loop.md`
- `plans/run-reports/2026-05-09-codex-a-project-index-memory-report.md`
- `plans/raw-requests/2026-05-09-system-expansion-raw-reconstructed.md`
- `plans/raw-requests/2026-05-09-system-expansion-interpretation.md`

## 修改 / 新建文件

本次 V2 补丁更新：

- `AGENTS.md`
  - 增加 Fresh agent / project map 入口：`docs/agent-quickstart.md`、`docs/project-index.md`、`docs/decision-log.md`。
  - 增加 managed `/goal` / todo task 读取路径。
  - 明确 `/goal <task-file>` 或裸任务文件路径要把任务文件当自包含入口，顶部固定要求/V2 要求优先于旧正文。
  - 明确托管 goal/todo 默认中文和默认发布运行报告页，除非任务明确写 `不发布`。

- `docs/agent-quickstart.md`
  - 增加 `0A. /goal 文件路径 前 10 分钟硬流程`。
  - 覆盖读任务全文、读 skill/workflow、处理新旧正文冲突、回写旧文件、验证、写报告、发布 HTML、本地 200、完成审计、中文最终回复。

- `docs/decision-log.md`
  - 新增用户强偏好：任务文件自包含、默认中文、托管 goal 默认发布 HTML、旧任务必须回写而不是另建替代文件。
  - 新增“用户生气点 / 不可再漏”：不能只按旧正文判断任务范围；必须重新读取当前任务文件顶部固定前置要求和 V2 补丁目标。

- `docs/project-index.md`
  - 补充 `plans/todo/`、`plans/tasks/`、`plans/run-reports/` 的职责区别。
  - 补充 `publish/ai-ip-previews/runs/<slug>/report.md`、`index.html`、`runs/index.html` 的作用。
  - 明确本地发布不等于 push/deploy。

- `docs/improvement-loop.md`
  - 增加“已确认流程的小补丁纪律”。
  - 明确少而准、修改用户已确认流程前要有理由、旧入口必须回写、托管任务默认中文/默认发布/HTML 本地 200 是完成门槛。

- `plans/run-reports/2026-05-09-codex-a-project-index-memory-report.md`
  - 追加本 V2 补丁报告、验证清单和自评。

本次 V2 补丁发布后生成/更新：

- `publish/ai-ip-previews/runs/2026-05-09-codex-a-project-index-memory/report.md`
- `publish/ai-ip-previews/runs/2026-05-09-codex-a-project-index-memory/index.html`
- `publish/ai-ip-previews/runs/index.html`

## Prompt-To-Artifact V2 审计

| V2 要求 | 证据 |
|---|---|
| 审核现有 5 个文档是否覆盖三次原始需求 | 本报告“本次 V2 必读”和原报告 Deep Audit；`docs/project-prd-v2.md` 覆盖商业化、趋势、XHS、工具评估，`docs/decision-log.md` 覆盖决策，`docs/improvement-loop.md` 覆盖持续优化。 |
| AGENTS 自然引导新 agent 读取索引/quickstart/decision-log | `AGENTS.md` 的 `Fresh agent / project map` 行。 |
| 记录用户强偏好：任务自包含、默认中文、托管 goal 默认发布、旧任务回写 | `docs/decision-log.md` 2026-05-10 accepted rows 与“用户生气点 / 不可再漏”。 |
| quickstart 回答拿到 `/goal 文件路径` 后怎么跑 | `docs/agent-quickstart.md` `0A. /goal 文件路径 前 10 分钟硬流程`。 |
| project-index 解释新增目录和产物，尤其 plans/todo、plans/tasks、plans/run-reports、publish runs | `docs/project-index.md` 顶层表和 `plans/ Subfolder Rules` / `publish/ai-ip-previews/runs/ Rules`。 |
| improvement-loop 明确小补丁少而准、修改确认流程前要有理由 | `docs/improvement-loop.md` `3A. 已确认流程的小补丁纪律`。 |
| 生成/更新运行报告并默认发布 HTML | 本报告追加段落；发布路径见下方“发布链接”。 |
| 本任务报告 HTML 本地 200 | 见最终验证命令记录。 |

## 验证 / Validation

验证项：

- [x] 任务文件当前 V2 顶部要求已重新读取。
- [x] V2 必读文件已检查。
- [x] 只回写既有文档和本任务报告/报告页，没有另建替代入口。
- [x] `AGENTS.md` 已能引导新 Agent 读取 `docs/project-index.md`、`docs/agent-quickstart.md`、`docs/decision-log.md`。
- [x] `docs/decision-log.md` 能回答“用户为什么生气、以后不能再漏什么”。
- [x] `docs/agent-quickstart.md` 能回答“拿到 `/goal 文件路径` 后怎么跑”。
- [x] `docs/project-index.md` 解释 `plans/todo`、`plans/tasks`、`plans/run-reports`、`publish/ai-ip-previews/runs`。
- [x] `docs/improvement-loop.md` 明确小补丁少而准，改确认流程前要有理由。
- [x] 运行报告已追加 V2 补丁说明。
- [x] 发布页将由 `scripts/publish_run_report.py` 生成并更新 `/runs/index.html`。
- [x] 未上传 raw media、cookie、token、credential。

## 发布链接

- 本地 Markdown 报告：`plans/run-reports/2026-05-09-codex-a-project-index-memory-report.md`
- 本地发布 Markdown：`publish/ai-ip-previews/runs/2026-05-09-codex-a-project-index-memory/report.md`
- 本地 HTML 报告：`publish/ai-ip-previews/runs/2026-05-09-codex-a-project-index-memory/index.html`
- 本地 `/runs/` 索引：`publish/ai-ip-previews/runs/index.html`
- 预期远程 URL：`https://schovayang-creator.github.io/ai-ip-previews/runs/2026-05-09-codex-a-project-index-memory/`

## 风险 / Risks

- 本次只生成本地发布页并更新本地 `/runs/` 索引，不执行 git commit 或 push；远程 URL 只有在用户后续部署/推送后才会更新。
- 工作区仍有多个并行任务留下的 untracked/modified 文件；本次只处理本任务写入范围和固定发布范围。

## 下一步 / Next

- 用户可直接打开本地 HTML 报告，或在推送 GitHub Pages 后使用预期远程 URL 查看。
- 后续类似 `/goal 文件路径` 任务应先按 `docs/agent-quickstart.md` 的 `0A` 流程执行，避免再次漏读顶部固定要求。
