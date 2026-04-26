# ai-dev-os

English summary:
- This file is the single root entry for the ai-dev-os rule library.
- Start here if you are entering the repository for the first time or if you are not sure which topic directory to read next.
- For a high-level router, continue to [00-overview/00_README.md](00-overview/00_README.md). For scenario-based reading paths, continue to [00-overview/library-index.md](00-overview/library-index.md).

当前 00_README.md 是本仓库规则库的唯一根入口。
AI 在进入本规则库时，应先阅读本文件，再按索引进入对应子目录。

## 目标

- 为整个 ai-dev-os 提供最顶层入口，先说明这套规则库该怎么进入、怎么分流、什么时候补读其他目录。
- 避免一上来只看到目录名，却不知道先看总览、总索引还是直接进入专题目录。

## 什么时候先读本页

- 第一次进入 ai-dev-os，还不确定整体结构和阅读顺序。

## 当前目录关系

- 当前仓库根目录直接承载规则库正文，00-overview/、01-general/ 到 11-ai-engineering/ 都是第一层目录。
- 因此当前仓库是在开发 ai-dev-os 本体，而不是在某个业务仓库中通过 .ai-dev-os/ 子目录消费它。
- 如果其他仓库以子模块方式引入本项目，建议把整个仓库挂载到目标仓库的 .ai-dev-os/ 目录下，再由接入方在自己的 AGENTS.md 和 CLAUDE.md 中指向该目录下的 00_README.md。
- 当前任务可能跨多个目录，例如“接口 + 数据 + 安全 + 发布”。
- 需要从根入口快速判断是去总览页、总索引，还是直接进入某个专题目录。

## 使用原则

- 如果任务里存在技术选型、框架选型、组件库选型、架构选型或模板选型，先询问用户，由用户确认后再继续。
- 进入各目录后，首先阅读对应的 00_README.md，再继续阅读其他文档。
- 如果还不确定任务应该进入哪个目录，先去 [00-overview/00_README.md](00-overview/00_README.md)。
- 如果已经知道自己要做什么，但不知道该按什么顺序阅读，优先去 [00-overview/library-index.md](00-overview/library-index.md)。
- 如果要新增、调整或重组规则库结构，先读 [00-overview/library-maintenance.md](00-overview/library-maintenance.md)。

## 最短进入路径

- 不确定入口：先读 [00-overview/00_README.md](00-overview/00_README.md)。
- 不确定是移动 Web、小程序还是移动 App：先读 [00-overview/01_移动形态边界速查卡.md](00-overview/01_%E7%A7%BB%E5%8A%A8%E5%BD%A2%E6%80%81%E8%BE%B9%E7%95%8C%E9%80%9F%E6%9F%A5%E5%8D%A1.md)。
- 已明确任务类型：直接进入对应专题目录的 00_README.md。
- 已明确场景但不清楚阅读顺序：进入 [00-overview/library-index.md](00-overview/library-index.md)。
- 要维护规则库本身：进入 [00-overview/library-maintenance.md](00-overview/library-maintenance.md)。

## 根入口与总览分工

- 本页负责说明整套规则库怎么进入，以及顶层目录分别负责什么。
- [00-overview/00_README.md](00-overview/00_README.md) 负责按任务类型做第一层分流。
- [00-overview/library-index.md](00-overview/library-index.md) 负责给出更细的高频场景阅读路径。
- [00-overview/library-maintenance.md](00-overview/library-maintenance.md) 负责约束目录结构、编号和命名维护方式。

## 与其它目录的配合方式

- 根入口负责回答“整套规则库该怎么进入、先去哪里判断、再去哪里细化”。
- [00-overview/00_README.md](00-overview/00_README.md) 负责第一层任务分流，[00-overview/library-index.md](00-overview/library-index.md) 负责高频场景阅读顺序。
- 具体规则仍落在各专题目录自己的 00_README 和分册正文中，本页不替代任何专题目录。
- 如需维护规则库结构和新增文档路径，统一回到 [00-overview/library-maintenance.md](00-overview/library-maintenance.md)。

## 目录索引

- [00-overview/](00-overview/)：全局使用说明、阅读导航、场景索引与规则库维护约定。
- [01-general/](01-general/)：通用需求、架构、编码、命名、Git/PR、评审、测试和交付质量规范。
- [02-frontend/](02-frontend/)：前端、移动 Web 页面、Vue、React、官网、AI 应用、管理后台与组件库相关规范。
- [03-backend/](03-backend/)：通用后端、Java、.NET、Python 服务端规范。
- [04-database/](04-database/)：数据库设计、命名、索引和迁移规范。
- [05-tests/](05-tests/)：测试设计分层、测试工具与自动化实现规范。
- [06-devops/](06-devops/)：批量脚本、Docker、Kubernetes、CI/CD 和发布执行规范。
- [07-security/](07-security/)：认证授权、接口安全、敏感信息、数据安全、运行安全和安全发布规范。
- [08-electron/](08-electron/)：Electron 桌面端规范、专题导航、模板与项目落地指引。
- [09-mobile/](09-mobile/)：真正的移动端应用工程规范，包括 Flutter、React Native、原生 iOS、原生 Android 与应用发布交付边界。
- [10-miniapp/](10-miniapp/)：小程序与平台型轻应用规范入口，面向微信小程序及后续可扩展的同类宿主内应用形态。
- [11-ai-engineering/](11-ai-engineering/)：AI 执行软件工程规范入口，面向 AI 任务接入、仓库定位、最小变更、验证闭环、权限边界、阻塞处理与执行审计。

## 常见进入方式

- 做需求、架构、编码、命名、评审或交付质量判断：进入 [01-general/00_README.md](01-general/00_README.md)。
- 做页面、前端结构、移动 Web 页面或管理后台开发：进入 [02-frontend/00_README.md](02-frontend/00_README.md)。
- 做接口开发、服务端实现或后端重构：进入 [03-backend/00_README.md](03-backend/00_README.md)。
- 做库表设计、索引优化或数据库迁移：进入 [04-database/00_README.md](04-database/00_README.md)。
- 做测试分层、回归范围或测试工具落地：进入 [05-tests/00_README.md](05-tests/00_README.md)。
- 做容器化、Kubernetes、流水线或发布交付：进入 [06-devops/00_README.md](06-devops/00_README.md)。
- 做认证授权、接口安全、密钥、隐私或安全整改：进入 [07-security/00_README.md](07-security/00_README.md)。
- 做 Electron 桌面端设计、实现或项目落地：进入 [08-electron/00_README.md](08-electron/00_README.md)。
- 做 Flutter、React Native、原生 iOS、原生 Android 或移动应用工程设计：进入 [09-mobile/00_README.md](09-mobile/00_README.md)。
- 做微信小程序或同类平台型轻应用设计：进入 [10-miniapp/00_README.md](10-miniapp/00_README.md)。
- 做 AI 工程代理、AI 自动修复、AI 仓库执行协议、AI 验证闭环或 AI 工程治理：进入 [11-ai-engineering/00_README.md](11-ai-engineering/00_README.md)。
- 做移动 Web、小程序和移动 App 的边界判断：进入 [00-overview/01_移动形态边界速查卡.md](00-overview/01_%E7%A7%BB%E5%8A%A8%E5%BD%A2%E6%80%81%E8%BE%B9%E7%95%8C%E9%80%9F%E6%9F%A5%E5%8D%A1.md)。

## 不建议的做法

- 把根入口当成完整规则正文使用，不继续进入总览页或专题目录。
- 只看目录名就直接开始写规则或做实现，不先判断当前任务真正属于哪个目录。
- 在没有先看维护规则前，直接新增目录、改编号或重组整套规则库结构。
