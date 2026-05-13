# 运行报告 - 专利撰写全流程 + 体系自优化

- Task ID：TASK-20260512-201
- 模式：managed
- 最终状态：review
- 自评分：93/100
- 更新时间：2026-05-13
- public_final：false
- report_visibility：internal
- canonical_slug：marathon-patent-drafting-system

## 目标

继续执行 AI-IP-Studio 马拉松任务，基于本地旧专利资料和学术工作台专利 workflow，选择一个资料充分且风险可控的 pilot 技术主题，完成专利撰写全流程 v1/v2、两轮评分、附图 prompt、系统优化包和交付草案。

## 完成度

已完成到“可交发明人/代理师复核的本地草案包”阶段；没有标记 finished，原因是正式检索、申请人/发明人信息、代理师复核和专利质量 95+ 门槛仍未满足。发布页作为 review 直链生成，不进入公开最终版 `/runs/` 索引。

## 必读与来源

- 已读 AI-IP-Studio：`AGENTS.md`、`plans/tasks/README.md`、`skills/goal-task-builder.md`、`workflows/managed-goal-task-v0.md`、`workflows/marathon-goal-task-v0.md`、`workflows/run-report-publishing-v0.md`。
- 已读学术工作台：`AGENTS.md`、`README.md`、`profile/confidential-boundaries.md`、`profile/patent-applicant-info.md`、`workflows/patent-workflow.md`、`skills/patent-drafting.md`。
- 已本地只读盘点旧资料路径，记录于学术项目的 `source-materials/source-inventory.md` 和 `source-materials/source-paths.tsv`。

## 交付物

- 学术项目目录：`/Users/yang/Desktop/学术/projects/patents/20260513-multiview-delivery-access-gate/`
- `working/v1/01-technical-disclosure.md`：v1 技术交底整理。
- `working/v1/02-invention-mining.md`：v1 发明点挖掘。
- `working/v1/03-prior-art-map.md`：v1 现有技术检索计划与初步公开检索记录。
- `working/v1/04-claims.md`：v1 权利要求书。
- `working/v1/05-specification.md`：v1 说明书。
- `working/v1/06-figure-list.md`：v1 附图清单与 prompt。
- `working/v1/07-abstract.md`：v1 摘要。
- `review/07-patent-self-check-v1.md`：v1 自检。
- `review/v1-score.md`：v1 评分，折算 77/100。
- `system-improvement/trial-v1/`：试行版系统优化包。
- `working/v2/04-claims.md`：v2 权利要求书。
- `working/v2/05-specification.md`：v2 说明书。
- `working/v2/06-figure-list.md`：v2 附图清单与图文一致性表。
- `working/v2/07-abstract.md`：v2 摘要。
- `figures/figure-prompts.md`：统一附图 prompt。
- `review/support-matrix-v2.md`：权利要求-说明书支撑矩阵。
- `review/07-patent-self-check-v2.md`：v2 自检。
- `review/v2-score.md`：v2 评分，93/100。
- `review/system-comparison.md`：旧系统 / 当前系统 / 试行版对比。
- `review/source-risk-v2.md`：来源与风险说明。
- `deliverables/`：v2 代理师复核草案包。

## 轮次日志

### v1

- 基于旧 PAT05 草稿和当前学术工作台 `patent-workflow`，完成交底、发明点、现有技术地图、权利要求、说明书、摘要和附图 prompt。
- v1 评分：77/100。主要扣分点是区别特征不够集中，质量契约、披露规则和结构化事件流字段不够清楚。

### 试行版系统

- 创建 `system-improvement/trial-v1/`，包含专利评分表、图生成规范、权利要求-说明书支撑检查表、代理师复核清单、tech facts 模板和交付包清单模板。
- 没有硬改正式 `skills/`、`workflows/` 或 `templates/`。

### v2

- 按试行版重构权利要求和说明书，突出材料研发事件流、多视图交付、敏感等级到处理动作、质量契约和审计轨迹。
- 建立图号、编号、说明书位置和 prompt 的一致性表。
- 建立支撑矩阵和来源风险说明。
- v2 评分：93/100。达到高质量 review 草案，但因正式检索和申请信息缺失，不能诚实标记 95+ finished。

## 多 Agent 分工

- 主 agent：PM/integrator，负责读取任务、盘点现状、补齐 v1/v2 交付物、写运行报告和收尾。
- explorer Peirce：只读审查项目完成度，指出 v1 后半、v2、附图、自检、交付稿和发布页缺失。
- explorer Popper：只读审查旧/当前/试行版系统差异，建议试行版系统包字段和最终报告写法。
- 说明：未让 worker 直接写入文件，避免并行覆盖；子 agent 只做审查和建议。

## 系统对比

见学术项目 `review/system-comparison.md`。摘要结论：旧系统是规则和案例库，优势在模板、评分和事实源；当前系统是轻量工作台骨架，优势是路径清晰；试行版作为迁移桥，把事实源、类型分流、D1-D5 评分、支撑矩阵和交付清单嵌入当前系统。

## 验证

- 文件存在性检查：30 个核心交付物全部存在，`MISSING_COUNT 0`。
- 本地发布页验证：`curl -I http://127.0.0.1:9876/runs/` 和 `curl -I http://127.0.0.1:9876/runs/2026-05-12-marathon-patent-drafting-system/` 均返回 `HTTP/1.0 200 OK`。
- 目录清单：学术项目 `run-evidence/project-file-list.txt`。
- 图像边界：未调用外部图像服务，未上传 Confidential 技术细节；仅生成图号、编号、图意和黑白线稿 prompt。
- 保密边界：公开/发布报告不包含完整权利要求、说明书或实施例正文；正文留在本地项目目录，按 Confidential 处理。

## 修改文件

- `/Users/yang/Desktop/学术/projects/patents/20260513-multiview-delivery-access-gate/README.md`
- `/Users/yang/Desktop/学术/projects/patents/20260513-multiview-delivery-access-gate/run-log.md`
- `/Users/yang/Desktop/学术/run-reports/marathon-patent-drafting-system-report.md`
- `/Users/yang/Desktop/AI-IP-Studio/plans/run-reports/2026-05-12-marathon-patent-drafting-system-report.md`
- `/Users/yang/Desktop/AI-IP-Studio/plans/tasks/running/TASK-20260512-201-marathon-patent-drafting-system.md`

## 新建文件

- `/Users/yang/Desktop/学术/projects/patents/20260513-multiview-delivery-access-gate/working/v1/04-claims.md`
- `/Users/yang/Desktop/学术/projects/patents/20260513-multiview-delivery-access-gate/working/v1/05-specification.md`
- `/Users/yang/Desktop/学术/projects/patents/20260513-multiview-delivery-access-gate/working/v1/06-figure-list.md`
- `/Users/yang/Desktop/学术/projects/patents/20260513-multiview-delivery-access-gate/working/v1/07-abstract.md`
- `/Users/yang/Desktop/学术/projects/patents/20260513-multiview-delivery-access-gate/working/v2/04-claims.md`
- `/Users/yang/Desktop/学术/projects/patents/20260513-multiview-delivery-access-gate/working/v2/05-specification.md`
- `/Users/yang/Desktop/学术/projects/patents/20260513-multiview-delivery-access-gate/working/v2/06-figure-list.md`
- `/Users/yang/Desktop/学术/projects/patents/20260513-multiview-delivery-access-gate/working/v2/07-abstract.md`
- `/Users/yang/Desktop/学术/projects/patents/20260513-multiview-delivery-access-gate/figures/figure-prompts.md`
- `/Users/yang/Desktop/学术/projects/patents/20260513-multiview-delivery-access-gate/review/07-patent-self-check-v1.md`
- `/Users/yang/Desktop/学术/projects/patents/20260513-multiview-delivery-access-gate/review/v1-score.md`
- `/Users/yang/Desktop/学术/projects/patents/20260513-multiview-delivery-access-gate/review/07-patent-self-check-v2.md`
- `/Users/yang/Desktop/学术/projects/patents/20260513-multiview-delivery-access-gate/review/v2-score.md`
- `/Users/yang/Desktop/学术/projects/patents/20260513-multiview-delivery-access-gate/review/support-matrix-v2.md`
- `/Users/yang/Desktop/学术/projects/patents/20260513-multiview-delivery-access-gate/review/system-comparison.md`
- `/Users/yang/Desktop/学术/projects/patents/20260513-multiview-delivery-access-gate/review/source-risk-v2.md`
- `/Users/yang/Desktop/学术/projects/patents/20260513-multiview-delivery-access-gate/system-improvement/trial-v1/`
- `/Users/yang/Desktop/学术/projects/patents/20260513-multiview-delivery-access-gate/deliverables/`

## 发布链接

- 本地 Markdown：`plans/run-reports/2026-05-12-marathon-patent-drafting-system-report.md`
- 本地 HTML：`publish/ai-ip-previews/runs/2026-05-12-marathon-patent-drafting-system/index.html`
- 预期远程直链：`https://schovayang-creator.github.io/ai-ip-previews/runs/2026-05-12-marathon-patent-drafting-system/`
- 公开索引：不进入最终版公开索引，因为状态为 `review` 且 `public_final:false`。
- GitHub Pages commit：`d3513ec`（首次发布）；`006a86c`（补充远程验证说明）。
- 远程验证：2026-05-13 `https://schovayang-creator.github.io/ai-ip-previews/runs/2026-05-12-marathon-patent-drafting-system/` 返回 HTTP 200；`/runs/` 返回 HTTP 200；`/runs/` 不包含本 review 报告入口，符合 final-only 规则。

## 风险

- 未完成正式 CNIPA / WIPO / 中文专利数据库检索，不能形成正式新颖性或创造性结论。
- 申请人、发明人、地址、权属和公开时点均待确认。
- v2 仍需代理师确认“质量契约”术语、权利要求数量、客体风险和最接近现有技术。
- 未生成正式附图，仅生成可供制图参考的黑白线稿 prompt。

## 下一步

1. 用户/发明人确认申请人、发明人、权属和保密边界。
2. 代理师或检索人员完成正式检索，并反馈最接近现有技术。
3. 根据检索结果调整独立权利要求宽度和从属层级。
4. 提供一组完全脱敏的演示数据或日志，补强实施例和技术效果。
5. 由制图人员按学术项目 `figures/figure-prompts.md` 绘制正式附图。

## 自评

- v1 评分：77/100。
- v2 评分：93/100。
- 任务要求 finished 需要 >=95、发布/push/远程 HTTP 200 和无重大人工阻塞；本次诚实进入 review。

## 完成说明

本地专利核心交付物已补齐，并完成两轮评分和系统优化包。任务不应进入 finished，而应进入 review：可交发明人/代理师复核，但正式检索、申请信息和代理师意见仍是阻塞 finished 的关键条件。
