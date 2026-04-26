# ai-dev-os 贡献说明

English version: [CONTRIBUTING.en.md](CONTRIBUTING.en.md)

本文说明如何为 ai-dev-os 提交规范补充、目录调整、样例扩展和文档修订，目标是让协作过程稳定、可回溯、可维护。

## 开始之前

在动手修改前，建议先按下面顺序阅读：

1. [00_README.md](00_README.md)
2. [00-overview/00_README.md](00-overview/00_README.md)
3. [00-overview/library-index.md](00-overview/library-index.md)
4. [00-overview/library-maintenance.md](00-overview/library-maintenance.md)
5. 你准备修改的目标目录的 00_README.md

如果你修改的是 AI 执行软件工程相关内容，再补读 [11-ai-engineering/00_README.md](11-ai-engineering/00_README.md)。

## 贡献范围

欢迎提交以下类型的改动：

- 补齐缺失的 00_README.md、导航页、样例页和模板页。
- 完善已有规范中的入口、边界、阅读顺序和验证要求。
- 修正失效链接、旧路径、目录漂移和明显错误表述。
- 增加接入说明、发布说明和协作说明等配套文档。

不建议在同一轮改动中混入下列内容：

- 大规模目录重命名。
- 无明确边界的一次性全库重写。
- 规则新增、历史清理、目录迁移和文案润色同时并行推进。

## 核心协作原则

- 最小变更：一次只解决一个明确主题，避免把多个无关调整揉进同一个提交。
- 入口优先：新增目录或分册时，先补入口，再补正文。
- 索引回写：新增目录、入口或高频路径后，必须同步回写对应导航文件。
- 路径稳定：在没有完整回链检查前，不做大规模改名。
- 文案收敛：优先统一正文口径，再考虑是否调整文件名或目录名。
- 全文中文：所有说明、文档和新增注释使用简体中文。

## 分支建议

推荐按照 [RELEASE.md](RELEASE.md) 中的分支策略协作：

- develop：长期开发分支。
- feature/*：新增规范、模板、样例或目录能力。
- docs/*：README、接入说明、贡献说明等文档优化。
- fix/*：路径漂移、链接失效、入口不一致等修复。

示例：

```bash
git checkout develop
git pull
git checkout -b docs/contributing-guide
```

## 修改规则目录时必须遵守的约定

### 新增一级目录

- 使用两位编号前缀加主题名，例如 12-something。
- 先创建该目录的 00_README.md，再继续补正文。
- 同步回写 [00_README.md](00_README.md) 和 [00-overview/00_README.md](00-overview/00_README.md)。
- 如涉及高频阅读路径，再同步回写 [00-overview/library-index.md](00-overview/library-index.md)。

### 新增专题分册

- 采用“编号_主题规范.md”或“编号_主题模板.md”的命名方式。
- 编号优先表达阅读顺序或职责顺序，不随意插号。
- 同步回写该目录自己的 00_README.md。
- 如影响跨目录路径，再补写总索引或相关导航页。

### 修改历史内容

- 优先修正文案和入口，不轻易改动历史文件名。
- 如果必须改路径，先确认引用范围，再一起更新回链。
- 不要把目录重构和正文扩写混在同一轮完成。

## 提交前自检

提交前至少检查以下内容：

- 是否仍以 [00_README.md](00_README.md) 作为唯一根入口。
- 是否给新增目录补齐了 00_README.md。
- 是否回写了目标目录入口、总览入口或总索引。
- 是否引入了旧路径、断链或与现有口径冲突的表述。
- 是否把一次性临时说明错误地写成长期规则。
- 是否把多个不相关主题塞进一个提交。

## 提交信息建议

提交信息不必过度复杂，但应能看出这次改动的主要目标：

- docs: 补充 CONTRIBUTING 和接入说明
- docs: 修正根入口与子模块接入口径
- feat: 新增 11-ai-engineering 样例导航
- fix: 清理旧 .ai-dev-os 路径引用

## Pull Request 建议说明

提交 PR 时，建议至少写清楚：

- 本次改动解决什么问题。
- 改了哪些入口、目录或样例。
- 是否回写了对应索引和导航。
- 是否存在需要重点复核的路径或结构调整。

## 不建议的做法

- 只补正文，不补入口和索引。
- 只改 README，不同步修正规则库内的真实导航。
- 未检查引用范围就直接大规模重命名目录或文件。
- 把“当前这一轮的临时结论”写成长期稳定规范。

## 相关文档

- [README.md](README.md)：项目首页与快速理解。
- [INTEGRATION.md](INTEGRATION.md)：业务仓库接入说明。
- [RELEASE.md](RELEASE.md)：分支策略与发布建议。
- [00-overview/library-maintenance.md](00-overview/library-maintenance.md)：目录结构与命名约定。