# 全局总览入口

English summary:
- This page is the high-level router for the ai-dev-os rule library.
- Read this page when you know the task area only roughly and need help deciding which topic directory to enter.
- If you already know the task type but need a more detailed reading path, continue to [library-index.md](library-index.md).

## 目标

- 为整个 ai-dev-os 提供统一阅读入口，避免使用者只看到目录名但不知道该先读什么。
- 当任务跨多个技术目录，或还不确定应该进入哪个分册时，先从本页判断阅读路径。
- 为新增目录提供统一挂载点，保证像 07-security 这类共性规范能被总览层发现。
- 如需看全库文档清单和按场景的快捷跳转，可继续阅读 [library-index.md](library-index.md)。

## 什么时候先读本页

- 你还不确定任务应该归到前端、后端、数据库、测试、DevOps、安全、Electron 还是小程序。
- 任务跨多个目录，例如“接口 + 数据 + 安全 + 发布”。
- 你要做团队 onboarding、规范导读或补齐文档导航。

## 推荐进入路径

- 做通用编码、命名、架构、Git/PR 或语言分册：进入 [../01-general/00_README.md](../01-general/00_README.md)。
- 做前端、移动 Web 页面、Vue、React、官网、AI 应用或管理后台：进入 [../02-frontend/00_README.md](../02-frontend/00_README.md)。
- 做服务端、Java、.NET、Python 或通用后端设计：进入 [../03-backend/00_README.md](../03-backend/00_README.md)。
- 做库表设计、索引、命名和迁移：进入 [../04-database/00_README.md](../04-database/00_README.md)。
- 做测试策略、测试分层、工具选型和验收：进入 [../05-tests/00_README.md](../05-tests/00_README.md)。
- 做 Docker、Kubernetes、脚本、流水线和交付：进入 [../06-devops/00_README.md](../06-devops/00_README.md)。
- 做鉴权授权、接口安全、敏感信息、数据安全、供应链和发布前安全检查：进入 [../07-security/00_README.md](../07-security/00_README.md)。
- 做 Electron 桌面端规范、模板或项目落地：进入 [../08-electron/00_README.md](../08-electron/00_README.md)。
- 做 Flutter、React Native、原生 iOS、原生 Android 或移动应用工程：进入 [../09-mobile/00_README.md](../09-mobile/00_README.md)。
- 做微信小程序或同类平台型轻应用：进入 [../10-miniapp/00_README.md](../10-miniapp/00_README.md)。
- 做 AI 执行软件工程、AI 工程代理工作流、执行协议、验证闭环和失败恢复：进入 [../11-ai-engineering/00_README.md](../11-ai-engineering/00_README.md)。

## 高频任务快速分流

- 新项目启动：先读 [../01-general/01_需求分析与澄清规范.md](../01-general/01_需求分析与澄清规范.md) 和 [../01-general/02_通用架构规范.md](../01-general/02_通用架构规范.md)，再进入对应技术目录。
- 接口开发或接口变更：先读 [../03-backend/01_通用后端规范.md](../03-backend/01_通用后端规范.md)，再补读 [library-index.md](library-index.md) 中“接口开发或接口变更”路径。
- 服务端实现或重构：先读 [../03-backend/00_README.md](../03-backend/00_README.md)，再按语言进入 Java、.NET 或 Python 分册。
- 管理后台页面开发：先读 [../02-frontend/00_README.md](../02-frontend/00_README.md)，再按页面模板或技术选型分流。
- 移动 Web 页面开发：先读 [../02-frontend/00_README.md](../02-frontend/00_README.md)，再按移动 Web 场景、技术栈规范和页面模板分流。
- 移动应用工程开发：先读 [../09-mobile/00_README.md](../09-mobile/00_README.md)，先判断是否属于 App 工程而不是移动 Web 页面；如属于真正的新建双端 App 工程，默认先评估 Flutter。
- 小程序或平台型轻应用开发：先读 [../10-miniapp/00_README.md](../10-miniapp/00_README.md)，先判断是否属于平台宿主内应用而不是浏览器页面或真正 App 工程。
- 数据库设计或迁移：先读 [../04-database/00_README.md](../04-database/00_README.md)，涉及上线迁移时必须补读迁移规范。
- 测试设计与测试落地：先读 [../05-tests/00_README.md](../05-tests/00_README.md)，再补读通用测试和交付质量规范。
- 容器化、流水线或上线发布：先读 [../06-devops/00_README.md](../06-devops/00_README.md)，涉及放行判断时补读安全发布检查单。
- 安全评审或安全整改：先读 [../07-security/00_README.md](../07-security/00_README.md)，再按身份、接口、数据、密钥或基础设施继续分流。
- Electron 桌面端开发：先读 [../08-electron/00_README.md](../08-electron/00_README.md)，如需更细导航再看其总览导航文件。
- 做 AI 自动完成代码修改、评审、排障、文档维护或仓库执行治理：先读 [../11-ai-engineering/00_README.md](../11-ai-engineering/00_README.md)，再回到对应技术目录落地实现。
- 做 11-ai-engineering 的入口判断、团队导读或首次阅读顺序选择：先读 [../11-ai-engineering/15_AI软件工程操作系统使用说明.md](../11-ai-engineering/15_AI%E8%BD%AF%E4%BB%B6%E5%B7%A5%E7%A8%8B%E6%93%8D%E4%BD%9C%E7%B3%BB%E7%BB%9F%E4%BD%BF%E7%94%A8%E8%AF%B4%E6%98%8E.md)。
- 做 AI 软件工程术语统一、培训前口径对齐或评审前关键词解释：先读 [../11-ai-engineering/16_AI软件工程术语表.md](../11-ai-engineering/16_AI%E8%BD%AF%E4%BB%B6%E5%B7%A5%E7%A8%8B%E6%9C%AF%E8%AF%AD%E8%A1%A8.md)。
- 做新仓库接入 AI 软件工程操作系统、最小接入顺序或阶段落地计划：先读 [../11-ai-engineering/14_AI软件工程新项目接入指引.md](../11-ai-engineering/14_AI%E8%BD%AF%E4%BB%B6%E5%B7%A5%E7%A8%8B%E6%96%B0%E9%A1%B9%E7%9B%AE%E6%8E%A5%E5%85%A5%E6%8C%87%E5%BC%95.md)。
- 做 11-ai-engineering 的目录分层理解、后续扩写归类或结构演进说明：先读 [../11-ai-engineering/31_AI目录分层与演进说明.md](../11-ai-engineering/31_AI%E7%9B%AE%E5%BD%95%E5%88%86%E5%B1%82%E4%B8%8E%E6%BC%94%E8%BF%9B%E8%AF%B4%E6%98%8E.md)。
- 做 11-ai-engineering 的首次 onboarding、压缩版导读或最短阅读路径选择：先读 [../11-ai-engineering/32_AI最短上手路径.md](../11-ai-engineering/32_AI%E6%9C%80%E7%9F%AD%E4%B8%8A%E6%89%8B%E8%B7%AF%E5%BE%84.md)。

## 跨目录任务判断法

- 如果任务先要判断规则边界和共性约束，先读对应技术目录的 00_README，再进入具体分册。
- 如果任务同时涉及接口、数据和权限边界，优先补读 [../07-security/00_README.md](../07-security/00_README.md)。
- 如果任务包含新项目选型、框架选型、组件库选型、架构选型或模板选型，先询问用户确认，再继续进入具体目录。

## 与其它目录的配合方式

- 当前页负责先判断“任务属于哪一类、该先进哪个目录”。
- 进入某个专题后，应回到该目录自己的 00_README 继续分流，再进入具体分册。
- 如果已经明确高频场景但不清楚阅读顺序，继续看 [library-index.md](library-index.md)。
- 如果是在维护规则库结构、索引和编号口径，继续看 [library-maintenance.md](library-maintenance.md)。

## 总览与总索引分工

- 当前页负责先判断“应该进哪个目录、哪类任务”。
- [library-index.md](library-index.md) 负责给出更细的按场景阅读路径和跨目录跳转顺序。
- 如果已经确定自己要做什么，但不知道该按什么顺序读，优先继续看 [library-index.md](library-index.md)。

## 什么时候停在总览页，什么时候进入总索引

- 你还在判断任务属于哪个目录、哪个专题，先停在本页，不要过早跳进总索引。
- 你已经知道任务大致属于前端、后端、数据库、测试、DevOps、安全、Electron、移动端、小程序或 AI 工程执行，再进入对应目录的 00_README。
- 你已经明确任务类型，但需要更细的阅读顺序、跨目录补读关系或高频场景路径，再进入 [library-index.md](library-index.md)。
- 本页只负责第一跳分流，不负责展开每一种任务的完整阅读链。

## 最短阅读顺序

- 单目录任务：本页判断目录后，直接进入目标目录的 00_README。
- 跨目录任务：本页判断主目录后，补读相关的安全、测试或 DevOps 目录。
- 不确定入口：先看根入口 [../00_README.md](../00_README.md)，再回到本页按场景分流。
- 已经明确高频场景但需要更细路线：从本页直接跳到 [library-index.md](library-index.md)。

## 补充入口

- 如需先快速判断移动 Web、小程序和移动 App 的边界，继续看 [01_移动形态边界速查卡.md](01_%E7%A7%BB%E5%8A%A8%E5%BD%A2%E6%80%81%E8%BE%B9%E7%95%8C%E9%80%9F%E6%9F%A5%E5%8D%A1.md)。
- 如需按“接口变更、页面开发、数据库迁移、上线发布、新项目启动”这类任务直接找阅读路径，继续看 [library-index.md](library-index.md)。
- 如需从全局总览直接进入 11-ai-engineering 的最短 onboarding 路线或分层解释，优先结合 [library-index.md](library-index.md) 中 AI 执行软件工程任务条目继续分流。
- 如需维护规则库自身的目录结构、编号和命名口径，继续看 [library-maintenance.md](library-maintenance.md)。

## 不建议的做法

- 把总览页当成最终落地规范使用，不继续进入专题目录和具体分册。
- 任务已经明确属于具体专题，却仍停留在总览层反复横跳，不进入目标目录。
- 在没有区分总览、总索引和维护规则分工前，把三者混写成同一类文档使用。
