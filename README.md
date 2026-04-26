# ai-dev-os

English version: [README.en.md](README.en.md)

ai-dev-os 是一套面向 AI 软件工程执行的规则库与操作系统，用于统一任务接入、目录分流、最小变更实施、验证闭环和治理约束。

当前仓库就是 ai-dev-os 本体。仓库根目录直接承载规则正文，AI 在进入本仓库时应先阅读 [00_README.md](00_README.md)，再按索引进入对应专题目录。

说明：当前规则正文与样例仍以中文为主；英文说明当前优先覆盖项目概览、接入方式、协作入口和支持说明。

## 设计原则

- 根入口清晰：先判断入口，再进入专题目录，不把规则库当作无结构的文档堆。
- 最小变更优先：优先做局部、可验证、可回退的修改，而不是大面积扩写或重构。
- 验证闭环前置：修改后优先做最小范围验证，而不是靠主观判断认为“应该没问题”。
- 规则与样例并存：既提供规范正文，也提供可直接照搬的样例和模板。
- 治理信息外显：把接入方式、目录关系、审计与记忆治理规则明确写出来，而不是依赖口口相传。

## 适用场景

- 希望为 AI 编程代理提供统一的任务接入、阅读分流和执行约束。
- 希望在多个项目之间复用同一套工程规范，而不是把规则散落在各仓库里。
- 希望把“最小变更、先验证、失败恢复、审计留痕”等 AI 工程实践沉淀为统一入口。

## 仓库目录关系

- 根目录的 [00_README.md](00_README.md) 是唯一根入口。
- [00-overview](00-overview) 负责全局总览、总索引和规则库维护约定。
- [01-general](01-general) 到 [11-ai-engineering](11-ai-engineering) 是各专题规则目录。
- [AGENTS.md](AGENTS.md) 和 [CLAUDE.md](CLAUDE.md) 用于声明当前仓库是在开发 ai-dev-os 本身时的入口约束。

## 快速开始

如果你是第一次进入本仓库，建议按下面顺序阅读：

1. [00_README.md](00_README.md)
2. [00-overview/00_README.md](00-overview/00_README.md)
3. [00-overview/library-index.md](00-overview/library-index.md)
4. 按任务类型进入对应专题目录的 00_README.md

## 作为子模块引入

建议其他仓库把本项目作为子模块引入到自己的 .ai-dev-os/ 目录下。

推荐优先使用 .ai-dev-os/ 作为目录名，这样可以明确表示它是项目内嵌的规则子模块，而不是业务代码目录。

添加子模块示例：

```bash
git submodule add <your-repo-url> .ai-dev-os
git submodule update --init --recursive
```

示例：

```text
your-project/
  AGENTS.md
  CLAUDE.md
  .ai-dev-os/
    00_README.md
    00-overview/
    01-general/
    ...
    11-ai-engineering/
```

子模块根目录保留 README.md、LICENSE、AGENTS.md、CLAUDE.md 是正常的，不会影响子模块使用；真正的规则入口仍然是子模块目录下的 00_README.md。

更完整的接入步骤、命令和模板见 [INTEGRATION.md](INTEGRATION.md)。

## 接入方 AGENTS.md 建议文案

```md
# AGENTS.md

本项目接入 ai-dev-os 作为 AI 软件工程操作系统。
AI 在处理任务前，必须先阅读 .ai-dev-os/00_README.md，再结合本项目文档、代码和约束执行。

如果任务涉及技术选型、框架选型、组件库选型、架构选型或模板选型，先询问用户，由用户确认后再继续。

## 语言要求

- 所有回复、文档、注释与说明内容使用简体中文。
```

## 接入方 CLAUDE.md 建议文案

```md
# CLAUDE.md

本仓库将 AGENTS.md 视为首要且唯一的主规范文件。

处理本仓库时，请先阅读并遵循 AGENTS.md。

补充约束：

- 如果 CLAUDE.md 与 AGENTS.md 存在差异，以 AGENTS.md 为准
- 本文件应故意保持精简，只做兼容入口，避免规则重复和后续漂移
```

## 开发 ai-dev-os 本身时

当仓库根目录直接包含 [00_README.md](00_README.md)、[00-overview](00-overview)、[01-general](01-general) 到 [11-ai-engineering](11-ai-engineering) 时，表示当前正在开发 ai-dev-os 本体。

在这种场景下：

- 入口路径直接写根目录的 [00_README.md](00_README.md)。
- 不应再写成 .ai-dev-os/00_README.md 这类额外包裹路径。
- [AGENTS.md](AGENTS.md) 和 [CLAUDE.md](CLAUDE.md) 应明确说明当前是在维护规则库本身。

## 支持项目

如果这个项目对你有帮助，欢迎支持持续维护。

查看 [SUPPORT.md](SUPPORT.md)。

## 相关文档

- [00_README.md](00_README.md)：规则库根入口。
- [00-overview/00_README.md](00-overview/00_README.md)：全局总览入口。
- [00-overview/library-index.md](00-overview/library-index.md)：高频场景阅读路径。
- [INTEGRATION.md](INTEGRATION.md)：子模块接入说明与模板。
- [RELEASE.md](RELEASE.md)：分支策略、版本建议与首发清单。
- [CONTRIBUTING.md](CONTRIBUTING.md)：协作流程、目录回写约定与提交前自检。
- [CHANGELOG.md](CHANGELOG.md)：版本变更记录与升级影响摘要。
- [SUPPORT.md](SUPPORT.md)：支持方式与赞助说明。