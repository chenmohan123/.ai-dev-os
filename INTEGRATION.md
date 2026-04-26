# ai-dev-os 接入说明

English version: [INTEGRATION.en.md](INTEGRATION.en.md)

本文说明如何把 ai-dev-os 作为子模块接入到业务仓库，并在 AGENTS.md 与 CLAUDE.md 中声明入口。

## 推荐接入方式

建议把本仓库作为 Git 子模块挂载到业务仓库的 .ai-dev-os/ 目录下：

```bash
git submodule add <your-repo-url> .ai-dev-os
git submodule update --init --recursive
```

如果你不想使用隐藏目录，也可以挂载到 ai-dev-os/，但后续所有入口路径都要同步改成 ai-dev-os/00_README.md。

## 接入后的目录示例

```text
your-project/
  AGENTS.md
  CLAUDE.md
  .ai-dev-os/
    00_README.md
    00-overview/
    01-general/
    02-frontend/
    ...
    11-ai-engineering/
    README.md
    LICENSE
```

说明：

- 子模块根目录保留 README.md、LICENSE、AGENTS.md、CLAUDE.md 是正常的。
- 这些文件不会破坏子模块使用方式。
- 业务仓库真正需要引用的规则入口，是 .ai-dev-os/00_README.md。

## 接入方 AGENTS.md 模板

如果你的业务仓库使用 .ai-dev-os/ 作为子模块目录，可使用下面模板：

```md
# AGENTS.md

本项目接入 ai-dev-os 作为 AI 软件工程操作系统。
AI 在处理任务前，必须先阅读 .ai-dev-os/00_README.md，再结合本项目文档、代码和约束执行。

如果任务涉及技术选型、框架选型、组件库选型、架构选型或模板选型，先询问用户，由用户确认后再继续。

## 语言要求

- 所有回复、文档、注释与说明内容使用简体中文。
```

如果你的目录名是 ai-dev-os/，只需要把路径替换成 ai-dev-os/00_README.md。

## 接入方 CLAUDE.md 模板

```md
# CLAUDE.md

本仓库将 AGENTS.md 视为首要且唯一的主规范文件。

处理本仓库时，请先阅读并遵循 AGENTS.md。

补充约束：

- 如果 CLAUDE.md 与 AGENTS.md 存在差异，以 AGENTS.md 为准
- 本文件应故意保持精简，只做兼容入口，避免规则重复和后续漂移
```

## 更新子模块

拉取最新规则时，可在业务仓库中执行：

```bash
git submodule update --remote --recursive
```

如果团队希望固定到某个提交，再按普通 Git 提交流程提交子模块指针变更即可。

## 开发 ai-dev-os 本体时

如果当前仓库根目录直接包含 00_README.md、00-overview/、01-general/ 到 11-ai-engineering/ 等目录，表示当前正在开发 ai-dev-os 本身。

在这种场景下：

- 根目录就是规则库根目录。
- 入口应直接写根目录 00_README.md。
- 不应再写成 .ai-dev-os/00_README.md。