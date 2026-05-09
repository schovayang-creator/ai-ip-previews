# Run Report - Codex A Project Index Memory V2 Patch

## Task Metadata

- Task ID: `plans/todo/2026-05-09-codex-a-project-index-memory.md` V2 patch
- Mode: managed / 托管
- Status: finished
- Started: 2026-05-10
- Finished: 2026-05-10
- Agent: Codex
- Report path: `plans/run-reports/2026-05-09-codex-a-project-index-memory-v2-report.md`
- Published report path: `publish/ai-ip-previews/runs/2026-05-09-codex-a-project-index-memory-v2/index.html`
- Published report copy: `publish/ai-ip-previews/runs/2026-05-09-codex-a-project-index-memory-v2/report.md`
- Expected remote URL: `https://schovayang-creator.github.io/ai-ip-previews/runs/2026-05-09-codex-a-project-index-memory-v2/`
- Score: 96/100

## 目标 / Objective

执行 V2 补丁任务，而不是复核旧任务。当前任务文件已明确要求读取顶部固定前置要求、V2 防误判硬规则、当前执行目标，并产生新的 V2 Markdown 报告和新的 V2 HTML 报告页。

本次目标：把已有项目索引和记忆系统补到“新 Codex 只靠 `AGENTS.md` + 当前任务文件就能知道该读哪些索引/记忆文件、如何跑 `/goal 文件路径`、如何验证并发布报告页”的程度。

## V2 必读与输入材料

### 已重新读取的 V2 顶部规则

- `plans/todo/2026-05-09-codex-a-project-index-memory.md` 的 `/goal 启动前置要求（固定）`
- `plans/todo/2026-05-09-codex-a-project-index-memory.md` 的 `V2 防误判硬规则（必须遵守）`
- `plans/todo/2026-05-09-codex-a-project-index-memory.md` 的 `当前执行目标：V2 补丁任务（以本段为准）`

### 已读取的旧产出和原始需求

- `docs/project-index.md`
- `docs/agent-quickstart.md`
- `docs/decision-log.md`
- `docs/project-prd-v2.md`
- `docs/improvement-loop.md`
- `plans/run-reports/2026-05-09-codex-a-project-index-memory-report.md`
- `plans/raw-requests/2026-05-09-system-expansion-raw-reconstructed.md`
- `plans/raw-requests/2026-05-09-system-expansion-interpretation.md`
- `AGENTS.md`
- `plans/tasks/README.md`
- `skills/goal-task-builder.md`
- `workflows/managed-goal-task-v0.md`
- `workflows/run-report-publishing-v0.md`

## 旧产出与原始/V2 要求之间的差距

1. 旧产出有项目索引、quickstart、decision log、PRD、improvement loop，但 `AGENTS.md` 没有足够自然地把新 Agent 引到 `docs/project-index.md`、`docs/agent-quickstart.md`、`docs/decision-log.md`。
2. 旧 quickstart 能做 5 分钟上手，但没有把 `/goal 文件路径` 的前 10 分钟硬流程写成强制执行路径，也没有明确“顶部 V2 要求优先于旧正文”。
3. 旧 decision log 记录了 V3 页面和远程 review，但没有记录用户这次强烈确认的偏好：任务文件自包含、默认中文、托管 goal 默认发布 HTML、旧任务必须回写。
4. 旧 project index 解释了顶层目录，但对 `plans/todo`、`plans/tasks`、`plans/run-reports`、`publish/ai-ip-previews/runs` 的关系还不够具体。
5. 旧 improvement loop 强调小补丁，但没有明确“修改用户已确认流程前必须有理由”“旧入口必须回写”“不能让系统每次用起来陌生”。
6. 旧 run report 和旧 HTML 页面只能证明旧任务完成，不能作为 V2 完成证据；V2 必须生成新的 `-v2` report 和新的 `-v2` HTML 页面。

## 修改文件 / Files Changed

- `AGENTS.md`
  - 增加 fresh agent/project map 入口，直接指向 `docs/agent-quickstart.md`、`docs/project-index.md`、`docs/decision-log.md`。
  - 增加 managed `/goal` or todo task 读取路径。
  - 明确 `/goal <task-file>` 或裸任务文件路径必须把任务文件当自包含入口。
  - 明确固定前置/V2 要求优先于旧正文。
  - 明确托管 goal/todo 默认中文，并“默认发布运行报告页”，除非任务明确写 `不发布`。

- `docs/agent-quickstart.md`
  - 新增 `0A. /goal 文件路径 前 10 分钟硬流程`。
  - 明确读任务全文、读 required skill/workflow、处理新旧正文冲突、回写旧文件、跑验证、写报告、发布 HTML、本地 200、做完成审计。
  - 明确 V2 任务不能拿旧 report 的分数、状态、checklist 当完成证据，必须有新的 V2 report 和新的 V2 HTML。

- `docs/decision-log.md`
  - 新增 2026-05-10 强偏好：任务文件自包含、默认中文、托管 goal/todo 默认发布 HTML、旧任务必须回写。
  - 新增 avoid：只按旧正文判断任务范围，漏读顶部固定要求/V2 目标。
  - 新增“用户生气点 / 不可再漏”，解释以后不能再漏什么。

- `docs/project-index.md`
  - 补充 `plans/todo/`、`plans/tasks/`、`plans/run-reports/` 角色。
  - 补充 `publish/ai-ip-previews/runs/<slug>/report.md`、`index.html`、`runs/index.html` 的用途。
  - 明确“本地发布不等于 push/deploy”。

- `docs/improvement-loop.md`
  - 新增 `3A. 已确认流程的小补丁纪律`。
  - 明确小补丁必须少而准、修改确认流程前必须有理由、旧任务路径必须回写、默认中文/默认发布报告页/HTML 本地 200 是托管任务完成门槛。

## 新建文件 / Files Created

- `plans/run-reports/2026-05-09-codex-a-project-index-memory-v2-report.md`
- `publish/ai-ip-previews/runs/2026-05-09-codex-a-project-index-memory-v2/report.md`
- `publish/ai-ip-previews/runs/2026-05-09-codex-a-project-index-memory-v2/index.html`

## 发布链接 / Publish Links

- 本地 V2 Markdown 报告：`plans/run-reports/2026-05-09-codex-a-project-index-memory-v2-report.md`
- 本地 V2 发布副本：`publish/ai-ip-previews/runs/2026-05-09-codex-a-project-index-memory-v2/report.md`
- 本地 V2 HTML 报告：`publish/ai-ip-previews/runs/2026-05-09-codex-a-project-index-memory-v2/index.html`
- `/runs/` 索引：`publish/ai-ip-previews/runs/index.html`
- 预期远程 URL：`https://schovayang-creator.github.io/ai-ip-previews/runs/2026-05-09-codex-a-project-index-memory-v2/`

## 验证 / Validation

### 内容覆盖验证

- [x] 已重新读取任务文件最前面的 `/goal 启动前置要求（固定）`。
- [x] 已重新读取 `V2 防误判硬规则（必须遵守）`。
- [x] 已重新读取 `当前执行目标：V2 补丁任务（以本段为准）`。
- [x] 已读取旧产出和原始需求，且旧产出只作为输入材料。
- [x] 已指出旧产出与原始/V2 要求之间的差距。
- [x] 已完成至少一个与 V2 补丁目标直接相关的实质文件改动；实际改动为 `AGENTS.md`、`docs/agent-quickstart.md`、`docs/decision-log.md`、`docs/project-index.md`、`docs/improvement-loop.md`。
- [x] 已创建新的 V2 Markdown report，不复用旧 report 作为完成证据。
- [x] 已创建新的 V2 HTML report，不复用旧 HTML 作为完成证据。
- [x] 已更新 `/runs/` 索引。

### 本地 HTTP 验证

已通过本地 HTTP server 验证：

```text
200 http://127.0.0.1:8787/publish/ai-ip-previews/runs/2026-05-09-codex-a-project-index-memory-v2/index.html
200 http://127.0.0.1:8787/publish/ai-ip-previews/runs/index.html
```

### 安全验证

- [x] 未上传 raw media。
- [x] 未新增 cookie、token、credential、private key。
- [x] 未编辑视频分析页、账号数据、原始媒体、profile 文件。
- [x] 本地发布不等于 push/deploy；本次未执行 git push。

## Prompt-To-Artifact V2 审计

| V2 要求 | 新证据 |
|---|---|
| 新的 V2 Markdown 运行报告 | `plans/run-reports/2026-05-09-codex-a-project-index-memory-v2-report.md` |
| 新的 V2 HTML 报告页 | `publish/ai-ip-previews/runs/2026-05-09-codex-a-project-index-memory-v2/index.html` |
| 新的 V2 report.md 发布副本 | `publish/ai-ip-previews/runs/2026-05-09-codex-a-project-index-memory-v2/report.md` |
| 更新 `/runs/` 索引 | `publish/ai-ip-previews/runs/index.html` |
| 至少一个 V2 实质改动 | `AGENTS.md`、`docs/agent-quickstart.md`、`docs/decision-log.md`、`docs/project-index.md`、`docs/improvement-loop.md` |
| 新 Codex 只读 AGENTS + 本任务文件知道读哪些索引/记忆文件 | `AGENTS.md` Read First 区域 + 任务文件 V2 必读列表 |
| decision-log 能回答用户为什么生气、以后不能漏什么 | `docs/decision-log.md` 的 `2026-05-10 - 用户生气点 / 不可再漏` |
| quickstart 能回答拿到 `/goal 文件路径` 后怎么跑 | `docs/agent-quickstart.md` 的 `0A. /goal 文件路径 前 10 分钟硬流程` |
| project-index 解释 plans/publish runs | `docs/project-index.md` 的 `plans/ Subfolder Rules` 与 `publish/ai-ip-previews/runs/ Rules` |
| improvement-loop 强调小补丁少而准 | `docs/improvement-loop.md` 的 `3A. 已确认流程的小补丁纪律` |
| HTML 本地 200 | 本报告“本地 HTTP 验证”记录 |

## 自评 / Self-Review

- Score: 96/100
- Completion gate passed: yes
- Final status: finished

强项：

- 没有再把旧 report 或旧 HTML 当成 V2 完成证据。
- 产出了新的 V2 report、V2 HTML、V2 published report copy。
- 对用户指出的误判原因做了制度化记录：任务自包含、顶部 V2 优先、默认中文、默认发布、旧入口回写。
- 做了本地 HTTP 200 验证。

剩余风险：

- 当前工作区仍有多项并行任务产生的未跟踪文件；本次没有清理，因为不属于本 V2 补丁目标。
- 预期远程 URL 需要后续 push/deploy 后才会在线更新；本次只生成本地发布产物。

## 下一步 / Next

- 用户可以直接打开 `publish/ai-ip-previews/runs/2026-05-09-codex-a-project-index-memory-v2/index.html` 做本地查看。
- 如果需要远程查看，下一步由用户或发布任务执行 GitHub Pages 推送/部署。
