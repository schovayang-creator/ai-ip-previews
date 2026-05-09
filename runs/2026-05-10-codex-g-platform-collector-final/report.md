public_final: true
canonical_slug: codex-g-platform-collector
report_visibility: public
version: 1

# 运行报告 - Codex G 全平台采集层最终公开报告

## 任务信息 / Task Metadata

- 任务 ID: `plans/todo/2026-05-10-codex-g-platform-collector-final-report.md`
- 模式: managed / 托管
- 最终状态: finished
- 分数: 93/100
- 开始时间: 2026-05-10 CST
- 完成时间: 2026-05-10 CST
- Agent: Codex
- 本地 Markdown 报告: `plans/run-reports/2026-05-10-codex-g-platform-collector-final-report.md`
- 本地 HTML 报告页: `publish/ai-ip-previews/runs/2026-05-10-codex-g-platform-collector-final/index.html`
- 发布副本: `publish/ai-ip-previews/runs/2026-05-10-codex-g-platform-collector-final/report.md`
- 公开索引: `publish/ai-ip-previews/runs/index.html`
- 预期远程链接: `https://schovayang-creator.github.io/ai-ip-previews/runs/2026-05-10-codex-g-platform-collector-final/`
- 预期远程索引: `https://schovayang-creator.github.io/ai-ip-previews/runs/`

## 目标 / Objective

本次任务不是重新实现全平台采集系统，而是对 G 任务“全平台采集与信号源适配器”做最终公开审计：检查已有产物是否真实存在、哪些能力已可复用、哪些仍只是设计意图，并生成一个可以给用户看的 final-only 报告页。

最终判断：当前项目已经具备若干可复用基础，例如 `video-collector`、Douyin V3 账号学习、XHS 专项流程、daily trend 高信号采样规则和报告发布器；但 G 任务指定的独立 adapter 产物没有落盘，因此不能声称“全平台自动跑通”。现阶段可以进入“人工/半自动日更信号台”，不能进入“全平台自动采集”。

## 必读与审计输入

### 已读取的固定任务与工作流

- `AGENTS.md`
- `plans/tasks/README.md`
- `skills/goal-task-builder.md`
- `workflows/managed-goal-task-v0.md`
- `workflows/run-report-publishing-v0.md`
- `plans/todo/2026-05-10-codex-g-platform-collector-final-report.md`
- `plans/todo/2026-05-10-codex-g-platform-collector-adapters.md`
- `skills/video-collector.md`
- `skills/account-batch-analyzer.md`
- `workflows/daily-trend-research-v0.md`
- `docs/skill-and-tool-evaluation-guide.md`

### G 任务指定产物检查结果

- `workflows/platform-collector-adapters-v0.md`: 缺失；影响是没有统一的采集层 -> 专项分析层 -> 内容转化层执行手册。
- `research/platforms/README.md`: 缺失；影响是没有平台信号工作区说明。
- `research/platforms/templates/platform-signal-card-template.md`: 缺失；影响是 `PlatformSignalCard` 字段没有正式模板。
- `research/platforms/templates/platform-adapter-spec-template.md`: 缺失；影响是各平台 adapter 规格没有统一写法。
- `research/platforms/templates/platform-collection-run-template.md`: 缺失；影响是采集运行记录不可复盘。
- `research/platforms/examples/2026-05-10-platform-adapter-sample.md`: 缺失；影响是没有最小 5 来源样例。
- `docs/platform-collector-tool-map.md`: 缺失；影响是工具候选状态没有按平台公开归档。
- `docs/platform-collector-risk-policy.md`: 缺失；影响是 G 专项风险边界没有独立文件。
- `plans/run-reports/2026-05-10-codex-g-platform-collector-adapters-report.md`: 缺失；影响是中间版 G 任务没有可审计报告。
- `publish/ai-ip-previews/runs/2026-05-10-codex-g-platform-collector-adapters/report.md`: 缺失；影响是公开中间版报告不存在，也不会进入 final-only 索引。

## G 任务完成度审计

| 模块 | 状态 | 证据 | 影响判断 |
|---|---:|---|---|
| YouTube adapter | 部分完成 | `workflows/daily-trend-research-v0.md` 有 YouTube 高信号样本字段；G 专项 adapter 文件缺失。 | 可人工记录公开链接、标题、指标、hook、视觉证据建议；不能说自动采集已跑通。 |
| X/Twitter adapter | 部分完成 | daily trend 中有 X/Twitter 高互动样本字段；无 X 专项 adapter、无授权/API 测试。 | 只能手动记录公共帖子或走官方授权；不做未授权登录态抓取。 |
| GitHub adapter | 部分完成 | daily trend 有 GitHub 高星/快增长样本模块；项目曾有 GitHub 趋势研究素材；G 专项模板缺失。 | 最适合先做自动化 MVP，可用公开 GitHub API/search，但仍需写 adapter 和测试样例。 |
| XHS adapter | 部分完成 | 项目存在 XHS 专项 workflow 和样例体系；G 专项 adapter 缺失。 | 适合账号/笔记深扒和引流路径分析；真实采集优先人工导入或授权导出。 |
| Douyin adapter | 部分完成 | `skills/account-batch-analyzer.md` 和本地 Douyin V3 账号沉淀存在；G 专项 adapter 缺失。 | 适合账号深扒；自动下载/评论采集必须单独授权和沙箱评估。 |
| Bilibili adapter | 未完成 | 没有发现 Bilibili 专项 adapter、样例或报告。 | 可作为第二批视频平台 adapter；当前仅能参考 `yt-dlp` 候选能力，不可宣称已支持。 |
| News/RSS adapter | 部分完成 | daily trend workflow 有国内/国际新闻源、RSS/公开源思路；G 专项 adapter 缺失。 | 最适合日更热点自动化 MVP；需要把源、抓取频率、可信度字段落成模板。 |
| 平台专项分析层 | 部分完成 | Douyin V3、XHS 专项、daily trend 高信号采样各自存在。 | 缺统一路由：信号卡应明确进入 Douyin / XHS / YouTube / GitHub / X discourse 等分析层。 |
| 内容转化层 | 部分完成 | AGENTS 和本地技能已有脚本、口播、小红书、图文、发布包规则。 | 缺从 `PlatformSignalCard` 到内容包的标准桥接步骤。 |
| 风险边界 | 部分完成 | AGENTS、`docs/skill-and-tool-evaluation-guide.md`、已有合规文档提供通用边界。 | G 专项 `docs/platform-collector-risk-policy.md` 缺失；视觉证据公开/内部使用还需文件化。 |
| 最小测试样例 | 未完成 | G 指定 example 文件缺失。 | 没有 5 来源信号卡样例，无法证明 adapter 字段可用。 |
| 失败 fallback | 部分完成 | `video-collector` 要求 blocker 记录；daily trend 强调人工采样和来源记录。 | G 专项 fallback 表未落地，需要把“自动失败 -> 手动导入 -> 摘要记录”写成模板。 |

## 全平台采集层最终结构

建议把全平台系统稳定拆成三层，而不是把所有平台混成一个爬虫：

```text
全平台采集层
  -> PlatformSignalCard
  -> 只保存可公开复核的 URL、标题、时间、指标、摘要和风险判断
  -> 对 raw media、完整截图、评论隐私数据默认不保存/不公开

平台专项分析层
  -> Douyin V3 account distillation
  -> XHS lead-gen / note analysis
  -> YouTube topic/video packaging analysis
  -> GitHub product-trend analysis
  -> X discourse / opinion spread analysis
  -> News/RSS trend thesis and credibility check

内容转化层
  -> 口播脚本
  -> 小红书笔记
  -> 图文/轮播
  -> 封面钩子
  -> 私域引流
  -> 选题库与复盘
```

核心字段仍应使用 G 任务设定的 `PlatformSignalCard`：`platform`、`source_url`、`source_type`、`captured_at`、`title_or_caption`、`creator_or_repo`、`public_metrics`、`age_of_signal`、`topic`、`hook_or_claim`、`visual_evidence_suggestion`、`rights_risk`、`privacy_risk`、`credibility`、`content_mechanism`、`platform_specific_notes`、`recommended_analysis_route`、`recommended_output_route`、`do_not_copy`、`next_action`。

## 各 adapter 能做什么、不能做什么

| Adapter | 当前可做 | 当前不能做 | 推荐采集方式 |
|---|---|---|---|
| YouTube | 人工/半自动记录公开视频、标题、发布时间、观看量、评论方向、前 5-15 秒 hook、缩略图承诺。 | 未完成批量频道采集、字幕/评论自动化测试、公开视觉素材授权判断。 | 先用手动 URL + 元数据卡；后续沙箱测试 `yt-dlp` 只做公开元数据/字幕。 |
| X/Twitter | 人工记录公共帖子、互动指标、争议点、可转述问题。 | 不做绕登录、不抓取付费/私密内容、不保存大规模评论或头像。 | 官方 API 或人工导入；没有授权时只做手动摘要。 |
| GitHub | 公开 repo / release / search 结果可结构化；stars、forks、license、pushed_at 适合做证据。 | 不能把开发者热度直接说成大众消费趋势；不能忽略许可证和安全风险。 | 优先做自动化 MVP：GitHub API/search + 速率限制 + Markdown 信号卡。 |
| XHS | 可用账号/笔记链接、标题、封面承诺、评论方向、私域路径做人工分析。 | 不做未授权登录态采集、不保存头像和评论隐私、不把平台原图公开复用。 | 手动浏览器导出/用户提供素材；工具候选必须先沙箱评估。 |
| Douyin | 可接入已有 Douyin V3 账号深扒思路，记录视频指标、选题、结构、复用风险。 | 不宣称全自动抓取；不下载/公开 raw mp4；评论采集需授权和脱敏。 | 用户提供链接/导出文件；工具候选仅在隔离实验中评估。 |
| Bilibili | 可人工记录视频/UP 主/分区热度和评论方向。 | 当前无专项 adapter，无测试样例。 | 作为 YouTube 后的第二视频平台；先测公开元数据和字幕可用性。 |
| News/RSS | 可基于公开新闻、官方源、RSS 源做日更热点输入。 | 不能把单一媒体叙述当事实；不能忽略发布时间和来源等级。 | 最适合自动化：RSS/站点公开页 + 来源可信度 + 交叉验证。 |

## 自动化程度与人工导入边界

- 可优先自动化：GitHub、News/RSS。理由是公开源结构稳定、风险较低、指标可复核。
- 可半自动化：YouTube、Bilibili。理由是公开视频元数据可以结构化，但字幕、评论、缩略图和版权边界需要逐项确认。
- 默认人工导入：X/Twitter、XHS、Douyin。理由是登录态、平台 ToS、评论隐私、反爬和版权风险更高；没有明确授权时只做公共链接摘要和人工记录。
- 需要人工授权：任何登录态、批量账号采集、评论明细采集、下载视频/图片、使用 cookies/session 的流程。
- 绝对不做：绕过反爬、保存凭据、全量扒取、付费墙内容、私密评论/头像、raw mp4 公开发布。

## 每天热点与账号深扒分工

| 适合每天热点 | 原因 | 输出建议 |
|---|---|---|
| News/RSS | 来源多、发布时间清晰、可交叉验证。 | 今日趋势 brief、可信度说明、口播事实底稿。 |
| GitHub | 指标公开，适合 AI 工具、创作者工具、开发者趋势。 | “海外早期信号”口播、工具观察、小红书图文。 |
| YouTube | 能看包装、hook、缩略图和观看指标。 | 选题包装拆解、标题/封面机制，不直接搬运画面。 |
| X/Twitter | 适合捕捉争论、观点扩散、国外 creator 语境。 | 转述争议问题和反方观点，不照搬原帖。 |
| Douyin/XHS 热点 | 贴近国内情绪与生活方式语言。 | 小红书标题、口播开头、私域承接角度；优先人工采样。 |

| 适合账号深扒 | 原因 | 输出建议 |
|---|---|---|
| Douyin | 已有 V3 决策页和账号级洞察体系。 | 拆爆款机制、拍摄优先级、账号选题库。 |
| XHS | 适合 lead-gen、标题封面、评论需求和转化路径分析。 | 笔记结构、私域路径、账号漏斗。 |
| YouTube/Bilibili | 适合频道内容结构、系列栏目、缩略图承诺。 | 频道包装学习、系列化选题。 |
| GitHub org/repo | 适合产品趋势和工具生态分析。 | 产品趋势 memo、AI 工具观察。 |

## 如何进入内容转化层

建议后续每条信号按以下路径进入内容生产，而不是从平台材料直接写脚本：

```text
PlatformSignalCard
  -> 风险检查：rights_risk / privacy_risk / credibility / do_not_copy
  -> 路由：recommended_analysis_route
  -> 机制抽象：content_mechanism / hook_or_claim / audience pain
  -> 内容标尺：是否适合创作者定位、是否有原创观点、是否可拍
  -> 输出路由：recommended_output_route
  -> 生成：口播脚本 / 小红书笔记 / 图文 / 封面钩子 / 私域引流
  -> 复盘：发布表现进入 topic library 和 performance review
```

国外热点尤其要保留“可用于口播转述的视觉证据切片思路”，但默认只记录切片建议和来源信息：例如 repo stars 区域、发布页排名、公开视频前 5 秒结构、公开帖子指标区。公开发布时优先重绘成原创文字卡或口播描述，不直接发布完整截图。

## 现阶段能不能直接投入日更

不能以“全平台自动跑通”的方式直接投入日更。原因是 G 任务指定的 workflow、模板、工具地图、风险政策、最小样例和中间报告都缺失。

可以以“人工/半自动日更信号台”的方式开始试运行：每天手动/半自动采 10-20 条高信号素材，其中 GitHub 和 News/RSS 可先自动化，YouTube/Bilibili 可半自动记录，X/Twitter/XHS/Douyin 先人工导入。每条只产出信号卡、风险判断、内容机制和下一步，不下载 raw media，不公开平台原图和评论隐私。

## 下一批建议派发的 Codex 任务

1. `codex-g1-platform-adapter-docs`: 补建 `workflows/platform-collector-adapters-v0.md`、`research/platforms/README.md` 和三个模板，先不接真实平台。
2. `codex-g2-github-rss-mvp`: 做 GitHub + News/RSS 两个低风险自动 adapter，生成 10 条真实 `PlatformSignalCard`，并记录命令和失败 fallback。
3. `codex-g3-video-platform-sandbox`: 沙箱评估 YouTube/Bilibili 公开元数据与字幕采集，只测试公开链接，不保存 raw mp4。
4. `codex-g4-domestic-manual-import`: 给 XHS/Douyin 建人工导入模板和脱敏规范，明确哪些字段必须用户提供。
5. `codex-g5-signal-to-content-pilot`: 从 10 条信号卡中挑 3 条进入内容标尺，分别产出口播、小红书、图文的低风险样稿。
6. `codex-g6-risk-policy-final`: 单独补 `docs/platform-collector-risk-policy.md`，把视觉证据、评论、头像、raw media、登录态边界写成硬规则。

## 修改文件 / Files Changed

- `plans/run-reports/2026-05-10-codex-g-platform-collector-final-report.md`
- `publish/ai-ip-previews/runs/2026-05-10-codex-g-platform-collector-final/index.html`
- `publish/ai-ip-previews/runs/2026-05-10-codex-g-platform-collector-final/report.md`
- `publish/ai-ip-previews/runs/index.html`

## 新建文件 / Files Created

- `plans/run-reports/2026-05-10-codex-g-platform-collector-final-report.md`
- `publish/ai-ip-previews/runs/2026-05-10-codex-g-platform-collector-final/index.html`
- `publish/ai-ip-previews/runs/2026-05-10-codex-g-platform-collector-final/report.md`

## 验证 / Validation

本报告生成后执行并记录以下验证：

- 本地 Markdown 报告存在：`plans/run-reports/2026-05-10-codex-g-platform-collector-final-report.md`
- 本地 HTML 报告存在：`publish/ai-ip-previews/runs/2026-05-10-codex-g-platform-collector-final/index.html`
- 本地报告副本存在：`publish/ai-ip-previews/runs/2026-05-10-codex-g-platform-collector-final/report.md`
- `python3 scripts/publish_run_report.py --check plans/run-reports/2026-05-10-codex-g-platform-collector-final-report.md`
- `python3 scripts/publish_run_report.py --rebuild-index`
- `git add runs/2026-05-10-codex-g-platform-collector-final/index.html runs/2026-05-10-codex-g-platform-collector-final/report.md runs/index.html`
- `git commit -m "reports: publish platform collector final report"`
- `git push`
- 远程最终报告页 HTTP 200：`https://schovayang-creator.github.io/ai-ip-previews/runs/2026-05-10-codex-g-platform-collector-final/`
- 远程 `/runs/` HTTP 200：`https://schovayang-creator.github.io/ai-ip-previews/runs/`

## 发布链接 / Publish Links

- 本地 Markdown 报告：`plans/run-reports/2026-05-10-codex-g-platform-collector-final-report.md`
- 本地 HTML 报告页：`publish/ai-ip-previews/runs/2026-05-10-codex-g-platform-collector-final/index.html`
- 本地发布副本：`publish/ai-ip-previews/runs/2026-05-10-codex-g-platform-collector-final/report.md`
- 本地 final-only 索引：`publish/ai-ip-previews/runs/index.html`
- 远程最终报告页：`https://schovayang-creator.github.io/ai-ip-previews/runs/2026-05-10-codex-g-platform-collector-final/`
- 远程 final-only 索引：`https://schovayang-creator.github.io/ai-ip-previews/runs/`

## 公开索引说明

- 保留在 `/runs/` final-only 索引：`2026-05-10-codex-g-platform-collector-final`。
- 隐藏旧 G 中间报告：`2026-05-10-codex-g-platform-collector-adapters`。当前本地未发现该中间报告目录或 report.md，因此无需删除；索引也不应展示它。
- 其他历史 run 报告如果没有 `public_final: true`、`report_visibility: public`、`status: finished`，默认不进入 final-only 索引。

## 跳过项 / Skipped Items

- 未重新创建 G adapter 全套 workflow、模板、工具地图和风险政策，因为本任务写入范围要求产出最终公开报告，而不是重做 G 平台系统。
- 未进行任何真实平台登录、批量抓取、下载 raw media、评论采集或截图发布。
- 未修改主页 `publish/ai-ip-previews/index.html`，因为任务说明主页已有 `/runs/` 固定入口，且本次没有发现必须改主页的证据。

## 风险 / Risks

- 当前 G 系统的最大风险是“概念上想要全平台，但独立 adapter 产物缺失”。如果直接安排日更，容易让执行者误以为所有平台都已自动化。
- 国内平台和 X/Twitter 的采集边界高风险：没有人工授权或官方 API 前，只能做公共链接摘要和人工导入。
- 视觉证据只能作为内部转述线索；公开页面不应发布完整 copyrighted screenshots、头像、评论隐私或 raw mp4。
- 现有工作区存在大量其他任务未提交/未跟踪文件；本次发布仓库只提交 G final run 目录和 `runs/index.html`，不顺手提交并行任务目录。

## 下一步 / Next Actions

- 先派 `codex-g1-platform-adapter-docs` 补齐缺失的 workflow、README、模板和 G 专项风险政策。
- 再派 `codex-g2-github-rss-mvp` 做低风险真实样例，把“设计”推进到“可跑”。
- 之后再分平台处理 YouTube/Bilibili 半自动、XHS/Douyin 人工导入、X/Twitter 官方授权/手动摘要。
- 在第一个真实日更试运行前，必须有至少 10 条信号卡、1 份采集 run log、1 份失败 fallback 记录。

## 完成审计清单

| 要求 | 证据 | 结果 |
|---|---|---:|
| 读取任务和固定工作流 | 报告列出 AGENTS、任务卡、managed workflow、发布 workflow、绑定技能 | 通过 |
| 审计 G 已有产出 | 已列出 10 个指定产物缺失清单和影响判断 | 通过 |
| 覆盖 7 个 adapter | 审计表覆盖 YouTube、X/Twitter、GitHub、XHS、Douyin、Bilibili、News/RSS | 通过 |
| 覆盖平台专项分析层 | 已说明 Douyin/XHS/daily trend 等部分可复用但缺统一路由 | 通过 |
| 覆盖内容转化层 | 已给出 PlatformSignalCard 到口播/小红书/图文的转换路径 | 通过 |
| 覆盖风险边界 | 已列明自动/人工/授权边界和禁止项 | 通过 |
| 覆盖最小测试样例 | 明确样例缺失，不能宣称跑通 | 通过 |
| 覆盖失败 fallback | 明确缺统一模板，建议自动失败后人工导入/摘要记录 | 通过 |
| 报告顶部公开字段 | 文件顶部含 `public_final: true`、`canonical_slug`、`report_visibility: public`、`version: 1` | 通过 |
| final-only 索引 | `publish_run_report.py` 默认 final-only 索引，仅公开本最终报告 | 通过 |
| 不改主页 | 本任务未修改主页 | 通过 |
| 不做危险采集 | 未登录平台、未抓取、未下载 raw media、未保存隐私数据 | 通过 |
| GitHub push 与远程 HTTP 200 | 收尾阶段执行并在最终回复记录 commit hash 与 HTTP 200 | 待命令验证 |

## 自评 / Self-Review

- 分数: 93/100
- 达标原因：最终报告如实区分了“已有基础能力”“G 专项产物缺失”“可人工试运行”和“不可宣称全平台自动跑通”，并进入 final-only 发布链路。
- 扣分原因：由于 G adapter 中间产物本身缺失，本报告只能完成最终审计和下一步调度，不能替代真实 adapter MVP。

## 完成说明 / Completion Note

本次最终报告完成的是“公开、可信、可继续安排任务”的收尾：G 全平台采集层目前不应被包装成已自动化系统，而应作为下一批 Codex 任务拆分推进。公开索引只展示这份 final 报告，隐藏缺失的中间版 G 报告，避免用户手机端误读旧过程页。
