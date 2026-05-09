# Run Report - Codex D Skill And Tool Evaluation Sandbox

## Task Metadata

- Task ID: `2026-05-09-codex-d-skill-tool-eval`
- Mode: managed / 托管
- Status: finished
- Started: 2026-05-09
- Finished: 2026-05-09
- Agent: Codex
- Task prompt: `plans/todo/2026-05-09-codex-d-skill-tool-eval.md`

## Objective

Create a safe evaluation system for testing external skills/tools related to short-video, social-media research, trend monitoring, account analysis, and content automation. The system needed experiment folder rules, evaluation templates, an installed skill map, a guide for searching/evaluating/adapting tools, an existing skill audit, a future candidate search plan, and this run report.

## Context Read

- `AGENTS.md`
- `docs/engineer-handbook.md`
- `docs/git-policy.md`
- `plans/todo/2026-05-09-codex-d-skill-tool-eval.md`
- `plans/raw-requests/2026-05-09-system-expansion-raw-reconstructed.md`
- `plans/raw-requests/2026-05-09-system-expansion-interpretation.md`
- `docs/tool-candidates.md`
- `skills/dbskill-bridge.md`
- `docs/integrations/dbskill.md`
- Local skill headers under `skills/*.md`
- Visible installed skill list from current Codex session instructions

## Files Created

- `experiments/README.md`
- `experiments/skill-evals/README.md`
- `experiments/tool-evals/README.md`
- `experiments/templates/tool-evaluation-template.md`
- `experiments/templates/safety-review-template.md`
- `docs/skill-and-tool-evaluation-guide.md`
- `docs/installed-skill-map.md`
- `plans/run-reports/2026-05-09-codex-d-skill-tool-eval-report.md`

## Files Changed

- No pre-existing in-scope files were modified.
- No files outside the task write scope were edited.
- `docs/tool-candidates.md` was inspected but intentionally left unchanged to respect the strict write scope.

## Deliverables

### 1. Experiment Folder Rules

Delivered in `experiments/README.md`, `experiments/tool-evals/README.md`, and `experiments/skill-evals/README.md`.

Rules now define:

- one folder per tested project/tool or skill;
- standard naming: `YYYYMMDD-tool-slug` / `YYYYMMDD-skill-slug`;
- required source metadata;
- install log for tools;
- test plan;
- redacted raw outputs;
- safety review;
- adaptation notes;
- scorecard with original score and adapted AI-IP-Studio score;
- safe execution levels from L0 candidate note to L5 promotion candidate;
- stop conditions for credentials, unsafe scraping, unclear license, copying risk, and untraceable outputs.

### 2. Templates

Delivered in `experiments/templates/tool-evaluation-template.md` and `experiments/templates/safety-review-template.md`.

The tool template includes:

- tool evaluation fields;
- source metadata;
- install log;
- test plan;
- raw output index;
- output quality review;
- safety summary;
- adaptation notes;
- scorecard;
- promotion gate;
- skill evaluation addendum;
- adaptation/re-score addendum.

The safety template includes:

- secret/credential checks;
- data handling;
- security review;
- license/commercial-use review;
- platform/legal risk;
- AI-IP-Studio rule check;
- allowed-use decision.

### 3. Installed Skill Map

Delivered in `docs/installed-skill-map.md`.

It maps:

- AI-IP-Studio local skills;
- image generation skills;
- OpenAI/agent/skill infrastructure skills;
- dontbesilent/dbskill suite;
- Lark/Feishu skills;
- Office/document skills;
- business/planning chatroom skills.

It also identifies primary routing for:

- account analysis;
- trend research;
- Xiaohongshu/XHS;
- publishing;
- reports;
- business;
- writing.

Most global skills are marked `needs live test` because this task audited routing and fit, but did not execute live skill prompt tests.

### 4. Skill And Tool Evaluation Guide

Delivered in `docs/skill-and-tool-evaluation-guide.md`.

It documents:

- where to search GitHub/social/product sources;
- what GitHub and social evidence to record;
- metrics that matter: stars, maintenance, license, security, output quality, AI-IP-Studio fit, integration cost;
- how to avoid contaminating the project;
- how to adapt tools to AI-IP-Studio output contracts;
- human confirmation gates;
- installed skill evaluation rules;
- a repeatable candidate search plan;
- an initial candidate shortlist.

### 5. Candidate Search Plan And Initial Shortlist

Delivered in `docs/skill-and-tool-evaluation-guide.md`.

The future search plan tells agents to:

1. choose one use case per run;
2. collect 10-20 candidates;
3. record source URL, category, value hypothesis, license, stars/adoption signal, last update, first safety concern, and safe evaluation level;
4. shortlist 3-5 candidates;
5. run sandboxed experiments;
6. adapt or reject based on safety and adapted score.

Initial shortlist recorded from existing project notes plus safe public GitHub metadata checks:

- `yt-dlp`
- `TikTokDownloader`
- `XHS-Downloader`
- `MediaCrawler`
- `RSSHub`
- `faster-whisper`
- `whisper.cpp`
- `whisperX`
- `auto-editor`
- `pyJianYingDraft`
- `MoneyPrinterTurbo`
- `ShortGPT`
- `LangGraph`
- `openai-agents-python`

No unknown tools were installed globally.

## Validation

| Requirement | Evidence | Status |
|---|---|---|
| Required deliverables exist | All required allowed files now exist, including this run report. | pass |
| Required reading inspected | Listed in `Context Read`; task prompt, AGENTS, raw requests, interpretation, git policy, tool candidates, and relevant skill docs were read. | pass |
| Write scope respected | Created only files allowed by the task. Inspected but did not modify `docs/tool-candidates.md`. | pass |
| No unsafe global installs | No package/tool install commands were run. Only docs and public metadata checks were performed. | pass |
| Experiment folders separated | `experiments/tool-evals/` and `experiments/skill-evals/` now have separate rules and layouts. | pass |
| Templates cover tool, skill, safety, adaptation/re-score | Tool template contains tool, skill addendum, and adaptation/re-score addendum; safety template is separate. | pass |
| Original/adapted score required | `experiments/README.md` and template scorecards require both scores. | pass |
| Existing skills mapped | `docs/installed-skill-map.md` maps project and visible global skills by use case, overlap, status, and when not to use. | pass |
| Candidate search plan exists | `docs/skill-and-tool-evaluation-guide.md` contains future search plan and first 5 recommended experiments. | pass |
| Future agents can evaluate consistently | Folder layout, execution levels, scorecard, stop conditions, and promotion gates are documented. | pass |

## Completion Audit

### Prompt-To-Artifact Checklist

| Explicit Requirement | Artifact / Evidence | Result |
|---|---|---|
| Create safe evaluation system for external skills/tools | `experiments/README.md`, `docs/skill-and-tool-evaluation-guide.md` | complete |
| Experiment folder rules: one folder per tested project/tool | `experiments/README.md`, `experiments/tool-evals/README.md`, `experiments/skill-evals/README.md` | complete |
| Source metadata | Required in experiment READMEs and templates | complete |
| Install log | Required for tool experiments and template | complete |
| Test plan | Required in experiment READMEs and templates | complete |
| Raw outputs | Required with redaction rules | complete |
| Safety review | Dedicated template and required file | complete |
| Adaptation notes | Required in experiment READMEs and template | complete |
| Original score and adapted score | Required scorecard and guide thresholds | complete |
| Tool evaluation template | `experiments/templates/tool-evaluation-template.md` | complete |
| Skill evaluation template | Skill addendum in `experiments/templates/tool-evaluation-template.md` | complete |
| Safety review template | `experiments/templates/safety-review-template.md` | complete |
| Adaptation/re-score template | Adaptation/re-score addendum in `experiments/templates/tool-evaluation-template.md` | complete |
| Installed skill map | `docs/installed-skill-map.md` | complete |
| Group skills by use case | Routing summary, skill categories, specific use-case call map | complete |
| Explain likely best use | Tables in installed skill map | complete |
| Identify overlaps | Overlap columns and overlap rules | complete |
| Mark needs live test | Global skills and dbskill/lark/office helpers marked where not tested | complete |
| Guide: search GitHub/social sources | Search source sections in guide | complete |
| Metrics: stars, maintenance, license, security, output quality, fit | Metrics sections and scorecard | complete |
| Avoid project contamination | Sandbox discipline and isolation rules | complete |
| Adapt a tool to AI-IP-Studio | Adapter behavior and output mapping | complete |
| Existing skill audit: account analysis, trend, XHS, publishing, reports, business, writing | `docs/installed-skill-map.md` specific use-case call map | complete |
| Candidate search plan | `docs/skill-and-tool-evaluation-guide.md` | complete |
| Live search initial shortlist if safe/available | Public GitHub metadata was checked; shortlist recorded; no installs | complete |
| Sandbox discipline | `experiments/README.md` and tool/skill eval READMEs | complete |
| Run report exists | This file | complete |
| If from plans/todo, do not delete; leave completion note | This report states task is finished and leaves todo archival to user/task-board agent | complete |

### Verification Commands Used

- `git status --short`
- `sed -n` inspections of required reading and generated files
- `rg --files skills`
- `rg -n` keyword checks across generated docs/templates
- Python file existence and content checks for required terms
- Public GitHub API metadata check for candidate shortlist; timed out for a few entries and those were marked accordingly in the guide

## Self-Review

- Score: 94/100
- Completion gate passed: yes
- Status: finished

Strong points:

- The sandbox is operationally specific, not just conceptual.
- Folder rules and templates require safety review, source metadata, logs, raw output redaction, adaptation notes, and dual scores.
- The installed skill map gives practical routing and overlap rules for AI-IP-Studio's current visible skills.
- The guide separates discovery, safety, evaluation, adaptation, and promotion.
- No unknown tools were installed and no raw media/secrets were touched.

Weak points:

- No live skill prompt tests were run; global skills are correctly marked `needs live test` rather than over-claimed.
- Initial candidate shortlist used lightweight public metadata checks and existing notes, not a full multi-source social discovery run.
- The skill evaluation and adaptation/re-score templates are addenda inside the tool evaluation template rather than separate files, because the task write scope listed only two template files.

What was skipped and why:

- Global installs: skipped because explicitly unsafe/out of scope.
- Credentialed platform tests: skipped because not approved and not needed for this sandbox design run.
- Publishing a remote HTML report: not required by this task's write scope; local run report was required and created.
- Moving/deleting the todo prompt: skipped because the prompt is under `plans/todo/` and explicitly says to leave final archival to the user or task-board agent.

## Published Report

- Local report: `plans/run-reports/2026-05-09-codex-d-skill-tool-eval-report.md`
- Remote report: not published in this run; no publishing path was in write scope.

## Blockers / Risks

- Future tool candidates that require cookies, QR login, browser profile access, or platform scraping must stay at documentation review until the user approves a controlled test.
- GPL/AGPL/missing-license tools may be fine for local experiments but need review before product/service integration.
- A dedicated trend-engine local skill/workflow still needs to be created in a future task.

## Next Recommended Action

1. Run a first L1/L3 experiment for `yt-dlp` using a public, non-private sample URL.
2. Run L1 documentation/safety reviews for `TikTokDownloader`, `XHS-Downloader`, and `MediaCrawler` before any login/cookie-based use.
3. Run an L1/L3 `RSSHub` test for public trend feeds to seed the domestic/international trend engine.
4. Live-test `dbs-hook`, `dbs-ai-check`, and `dbs-xhs-title` through `skills/dbskill-bridge.md` on a non-sensitive sample script/package.
5. Create a dedicated trend-engine workflow once candidate collection and feed experiments are validated.
