# ai-dev-os 发布与协作说明

English version: [RELEASE.en.md](RELEASE.en.md)

本文用于统一 ai-dev-os 的分支策略、版本建议和首次发布前检查项。

## 推荐分支策略

建议采用一条稳定主分支加一条长期开发分支的方式：

- main：稳定、可对外引用的分支。外部仓库作为子模块引用时，默认跟随该分支或其标签。
- develop：日常集成开发分支。规则调整、目录回写、README 更新等改动先进入这里，再合并到 main。
- feature/*：短期功能分支，用于新增规范目录、补齐样例、完善模板等。
- docs/*：短期文档分支，用于 README、接入文档、发布说明等非规则正文类文档更新。
- fix/*：短期修复分支，用于修正错误路径、失效链接、目录漂移和明显文案问题。

如果当前仓库由单人维护，也可以简化为 main + feature/*；但只要开始有持续维护节奏，仍建议保留 develop。

## 推荐协作流

1. 从 develop 拉出短期分支。
2. 在短期分支完成修改与自检。
3. 合并回 develop，确认入口、索引和样例链路没有漂移。
4. 当 develop 达到一个稳定节点，再合并到 main。
5. 在 main 上打标签，作为外部仓库可引用的稳定版本。

## 分支命名建议

- develop：长期开发分支。
- feature/root-entry-cleanup：规则入口或目录结构类新增。
- feature/integration-guide：接入说明或模板类新增。
- docs/readme-polish：README 或说明文档优化。
- fix/path-drift：旧路径、失效引用或结构漂移修复。

## 版本建议

如果开始对外提供稳定引用，建议采用语义化版本标签：

- v0.x.y：仍在快速演进，结构和目录可能继续调整。
- v1.x.y：规则入口、主要目录结构和接入方式相对稳定。

当前仓库更适合先从 v0.1.0 开始，再根据目录结构和接入方式是否稳定决定何时进入 v1.0.0。

## 首次发布前检查清单

### 仓库结构

- 根目录是否直接包含 00_README.md、00-overview/ 到 11-ai-engineering/。
- 是否已经清理旧的 .ai-dev-os/ 包裹路径表述。
- AGENTS.md 与 CLAUDE.md 是否明确声明“当前仓库是在开发 ai-dev-os 本体”。

### 入口与导航

- [00_README.md](00_README.md) 是否仍是唯一根入口。
- [00-overview/00_README.md](00-overview/00_README.md) 与 [00-overview/library-index.md](00-overview/library-index.md) 是否还能正确承担分流职责。
- 新增目录或文档后，是否已同步回写入口和索引。

### 对外说明

- [README.md](README.md) 是否能说明项目定位、快速开始、接入方式和相关文档。
- [INTEGRATION.md](INTEGRATION.md) 是否能指导业务仓库完成子模块接入。
- LICENSE 是否已确认使用的开源协议。

### 发布口径

- 是否明确 main 是稳定引用分支，develop 是日常开发分支。
- 是否约定首次对外标签，例如 v0.1.0。
- 是否确认业务仓库应引用 main 还是某个固定 tag。

## 作为子模块被引用时的建议

- 业务仓库如果追求稳定，优先锁定到某个 tag 或明确提交，而不是长期漂移跟随 develop。
- 只有在你愿意让接入方承受规则持续变化时，才让他们直接跟随 main 最新提交。
- 不建议让业务仓库引用 develop。

## 后续可以继续补充的内容

- 示例仓库：演示业务仓库如何以子模块方式接入 ai-dev-os。

当前仓库已经提供 [CONTRIBUTING.md](CONTRIBUTING.md)，用于说明目录调整、规范补充、索引回写和提交流程。

当前仓库已经提供 [CHANGELOG.md](CHANGELOG.md)，用于记录每个版本的主要变化和接入影响。