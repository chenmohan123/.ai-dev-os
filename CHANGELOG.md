# 更新记录

本文记录 ai-dev-os 对外可感知的结构、入口、接入与协作相关变更，便于业务仓库在引用子模块时判断升级影响。

建议从首次对外发布开始维护，后续每个版本都补充“新增 / 调整 / 修复”三类摘要。

## [Unreleased]

- 暂无未发布变更。

## [v0.1.0] - 2026-04-26

### 新增

- 新增 [README.md](README.md)，补充项目定位、设计原则、快速开始和相关文档入口。
- 新增 [INTEGRATION.md](INTEGRATION.md)，说明业务仓库如何以子模块方式接入 ai-dev-os，并提供 AGENTS.md 与 CLAUDE.md 模板。
- 新增 [RELEASE.md](RELEASE.md)，统一分支策略、版本建议和首发检查清单。
- 新增 [CONTRIBUTING.md](CONTRIBUTING.md)，明确协作流程、目录回写约定、提交前自检和 PR 建议说明。

### 调整

- 将规则库正文提升到仓库根目录，根入口调整为 [00_README.md](00_README.md)，不再以 .ai-dev-os 作为本仓库自开发时的包裹目录。
- 更新 [AGENTS.md](AGENTS.md) 与 [CLAUDE.md](CLAUDE.md)，明确当前仓库是在开发 ai-dev-os 本体。
- 更新 [00_README.md](00_README.md)，补充根目录关系与“本体开发 / 子模块接入”两种场景的区分说明。

### 修复

- 清理入口文档中的旧 .ai-dev-os 路径表述，避免继续沿用迁移前目录结构。
- 修正 [11-ai-engineering/27_AI记忆治理样例.md](11-ai-engineering/27_AI记忆治理样例.md) 中的旧根入口路径描述。

## 维护建议

- 每次准备打 tag 前，先把对应版本从 Unreleased 拆出。
- 只记录对外可感知的变化，不记录纯过程性细节。
- 如果一次变更会影响接入方路径、入口、目录或分支引用方式，必须写入本文件。