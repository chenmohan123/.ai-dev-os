# 规则库总索引

## 目标

- 为 ai-dev-os 提供一份可直接浏览的总目录和场景导航。
- 当使用者已经知道自己要做什么，但还不知道应该读哪几篇时，直接从本页进入。

## 与总览入口的分工

- [00_README.md](00_README.md) 负责第一跳判断：任务应该先进哪个目录。
- 当前页负责第二跳展开：当任务类型已经比较明确，但阅读顺序、跨目录补读关系和高频场景路径还不清楚时，从这里继续。
- 如果你还在判断“我到底应该进哪个目录”，先回到 [00_README.md](00_README.md)，不要直接在本页展开细节路径。

## 快速边界入口

- 如需先判断移动 Web、小程序和移动 App 三类形态的边界，先读 [01_移动形态边界速查卡.md](01_%E7%A7%BB%E5%8A%A8%E5%BD%A2%E6%80%81%E8%BE%B9%E7%95%8C%E9%80%9F%E6%9F%A5%E5%8D%A1.md)。

## 目录级入口

- [../01-general/00_README.md](../01-general/00_README.md)：通用编码、架构、命名、Git/PR、评审、交付质量和语言分册入口。
- [../02-frontend/00_README.md](../02-frontend/00_README.md)：前端、管理后台、AI 应用、官网落地页、移动 Web、Vue、React 页面与结构规范入口。
- [../03-backend/00_README.md](../03-backend/00_README.md)：通用后端、Java、.NET、Python 服务端规范入口。
- [../04-database/00_README.md](../04-database/00_README.md)：数据库设计、命名、索引和迁移规范入口。
- [../05-tests/00_README.md](../05-tests/00_README.md)：测试设计分层与测试工具落地规范入口。
- [../06-devops/00_README.md](../06-devops/00_README.md)：批量脚本、Docker、Kubernetes、CI/CD 和发布执行规范入口。
- [../07-security/00_README.md](../07-security/00_README.md)：认证授权、接口安全、密钥管理、数据安全和发布前安全检查入口。
- [../08-electron/00_README.md](../08-electron/00_README.md)：Electron 桌面端规范、专题导航与项目落地指引入口。
- [../09-mobile/00_README.md](../09-mobile/00_README.md)：移动应用工程规范入口，面向 Flutter、React Native、原生 iOS、原生 Android 与 App 发布交付。
- [../10-miniapp/00_README.md](../10-miniapp/00_README.md)：小程序与平台型轻应用规范入口，面向微信小程序及后续可扩展的同类宿主内应用形态。
- [../11-ai-engineering/00_README.md](../11-ai-engineering/00_README.md)：AI 执行软件工程规范入口，面向 AI 任务接入、仓库定位、修改协议、验证闭环和执行审计。

## 常见任务阅读路径

### 新项目启动

- 通用约束：先读 [../01-general/01_需求分析与澄清规范.md](../01-general/01_需求分析与澄清规范.md) 和 [../01-general/02_通用架构规范.md](../01-general/02_通用架构规范.md)。
- 技术目录：按项目类型进入前端、后端或 Electron 目录的 00_README。
- 安全补充：涉及登录、接口、敏感数据时补读 [../07-security/00_README.md](../07-security/00_README.md)。

### 接口开发或接口变更

- 服务边界：先读 [../03-backend/01_通用后端规范.md](../03-backend/01_通用后端规范.md)。
- 安全控制：再读 [../07-security/02_应用与接口安全规范.md](../07-security/02_应用与接口安全规范.md)。
- 身份权限：如涉及登录态、角色权限或多租户数据边界，补读 [../07-security/01_身份认证与授权安全规范.md](../07-security/01_身份认证与授权安全规范.md)。
- 落库变更：如涉及表结构或索引，补读 [../04-database/00_README.md](../04-database/00_README.md)。
- 验证：补读 [../05-tests/01_测试设计与分层规范.md](../05-tests/01_测试设计与分层规范.md)。

### 服务端实现或重构

- 通用边界：先读 [../03-backend/01_通用后端规范.md](../03-backend/01_通用后端规范.md)。
- 语言分册：按实际栈补读 [../03-backend/02_Java服务端规范.md](../03-backend/02_Java服务端规范.md)、[../03-backend/03_.NET服务端规范.md](../03-backend/03_.NET服务端规范.md) 或 [../03-backend/04_Python服务端规范.md](../03-backend/04_Python服务端规范.md)。
- 通用实现约束：补读 [../01-general/03_通用编码规范.md](../01-general/03_通用编码规范.md) 和 [../01-general/06_代码评审规范.md](../01-general/06_代码评审规范.md)。
- 交付验证：补读 [../05-tests/00_README.md](../05-tests/00_README.md) 和 [../01-general/08_交付质量规范.md](../01-general/08_交付质量规范.md)。

### 管理后台页面开发

- 前端总入口：先读 [../02-frontend/00_README.md](../02-frontend/00_README.md)。
- 页面分流：如还不确定是否属于后台页面，先读 [../02-frontend/13_前端页面场景选型规范.md](../02-frontend/13_前端页面场景选型规范.md)。
- 页面模板：再读 [../02-frontend/03_管理后台页面模板规范.md](../02-frontend/03_管理后台页面模板规范.md)。
- 接口联动：如页面依赖后端接口，补读 [../03-backend/01_通用后端规范.md](../03-backend/01_通用后端规范.md)。
- 权限与敏感信息：补读 [../07-security/01_身份认证与授权安全规范.md](../07-security/01_身份认证与授权安全规范.md) 和 [../07-security/04_数据安全与隐私保护规范.md](../07-security/04_数据安全与隐私保护规范.md)。

### AI 应用前端开发

- 前端总入口：先读 [../02-frontend/00_README.md](../02-frontend/00_README.md)。
- 页面分流：如场景还不确定，先读 [../02-frontend/13_前端页面场景选型规范.md](../02-frontend/13_前端页面场景选型规范.md)。
- AI 交互页面：再读 [../02-frontend/11_AntDesignX智能应用前端规范.md](../02-frontend/11_AntDesignX智能应用前端规范.md)。
- 页面模板：如需直接生成页面骨架，再读 [../02-frontend/14_智能应用与官网页面模板规范.md](../02-frontend/14_智能应用与官网页面模板规范.md)。
- 如页面嵌入后台工作台：补读 [../02-frontend/02_管理后台页面通用规范.md](../02-frontend/02_管理后台页面通用规范.md) 和 [../02-frontend/08_AntDesignReact管理后台前端规范.md](../02-frontend/08_AntDesignReact管理后台前端规范.md)。
- 接口与安全：按需补读 [../03-backend/01_通用后端规范.md](../03-backend/01_通用后端规范.md) 和 [../07-security/00_README.md](../07-security/00_README.md)。

### 官网或落地页开发

- 前端总入口：先读 [../02-frontend/00_README.md](../02-frontend/00_README.md)。
- 页面分流：如场景还不确定，先读 [../02-frontend/13_前端页面场景选型规范.md](../02-frontend/13_前端页面场景选型规范.md)。
- 官网与营销页：再读 [../02-frontend/12_AntDesignLanding官网与落地页规范.md](../02-frontend/12_AntDesignLanding官网与落地页规范.md)。
- 页面模板：如需直接生成页面骨架，再读 [../02-frontend/14_智能应用与官网页面模板规范.md](../02-frontend/14_智能应用与官网页面模板规范.md)。
- 如涉及埋点、转化表单或内容来源：结合项目现有规范补充统计、内容管理和交付要求。
- 如同项目还包含后台，不把官网区块体系直接复用为后台模板。

### 移动 Web 页面开发

- 前端总入口：先读 [../02-frontend/00_README.md](../02-frontend/00_README.md)。
- 页面分流：先读 [../02-frontend/15_移动端页面场景选型规范.md](../02-frontend/15_移动端页面场景选型规范.md)。
- 技术栈规范：再读 [../02-frontend/16_AntDesignMobile前端规范.md](../02-frontend/16_AntDesignMobile前端规范.md)。
- 页面模板：如需直接生成业务 H5、移动 Web 工作台或移动 Web AI 助手页骨架，再读 [../02-frontend/17_移动端页面模板规范.md](../02-frontend/17_移动端页面模板规范.md)。
- 如页面同时依赖桌面后台能力或 AI 助手能力，按需补读 [../02-frontend/08_AntDesignReact管理后台前端规范.md](../02-frontend/08_AntDesignReact管理后台前端规范.md) 和 [../02-frontend/11_AntDesignX智能应用前端规范.md](../02-frontend/11_AntDesignX智能应用前端规范.md)。

### 移动应用工程开发

- 目录入口：先读 [../09-mobile/00_README.md](../09-mobile/00_README.md)。
- 边界判断：先确认主体是 App 工程、原生容器和设备能力，而不是移动 Web、H5 或 WebView 页面。
- 通用约束：再读 [../09-mobile/11_移动端通用规范.md](../09-mobile/11_移动端通用规范.md)。
- 技术选型：如需判断 Flutter、React Native、原生 iOS、原生 Android 方案，再读 [../09-mobile/12_移动端技术选型规范.md](../09-mobile/12_移动端技术选型规范.md)；如属于真正的新建双端 App 工程，默认先从 Flutter 的优先评估与转出规则开始。
- 目录规划：如需确定 App 工程目录、模块边界、桥接层和构建发布资源位置，再读 [../09-mobile/13_移动端目录结构规范.md](../09-mobile/13_移动端目录结构规范.md)。
- 原生能力：如需接入相机、定位、蓝牙、推送、深链、文件、通知、分享和生物识别，再读 [../09-mobile/14_移动端原生能力接入规范.md](../09-mobile/14_移动端原生能力接入规范.md)。
- 发布交付：如需处理签名、渠道、商店上架、灰度、回滚和发布前后观察，再读 [../09-mobile/15_移动端发布交付规范.md](../09-mobile/15_移动端发布交付规范.md)。
- 测试验收：如需覆盖单元测试、集成测试、真机验收、安装升级和发布前门禁，再读 [../09-mobile/16_移动端测试与验收规范.md](../09-mobile/16_移动端测试与验收规范.md)。
- 交付清单：如需直接执行版本发布前检查、自测、真机验收、出包和回滚准备，再读 [../09-mobile/17_移动端项目交付清单模板.md](../09-mobile/17_移动端项目交付清单模板.md)。
- 验收记录：如需留档发布验收结论、上线确认和灰度放量建议，再读 [../09-mobile/18_移动端发布验收记录模板.md](../09-mobile/18_移动端发布验收记录模板.md)。
- 事故复盘：如需留档线上故障、发布异常、灰度事故和后续行动项，再读 [../09-mobile/19_移动端事故复盘模板.md](../09-mobile/19_移动端事故复盘模板.md)。
- 交叉补读：如应用内还承载 H5 页面，按需补读 [../02-frontend/00_README.md](../02-frontend/00_README.md)。
- 安全与发布：涉及登录、隐私、设备权限、签名、分发和发布校验时，补读 [../07-security/00_README.md](../07-security/00_README.md)、[../05-tests/00_README.md](../05-tests/00_README.md) 和 [../06-devops/00_README.md](../06-devops/00_README.md)。

### 小程序或平台型轻应用开发

- 目录入口：先读 [../10-miniapp/00_README.md](../10-miniapp/00_README.md)。
- 边界判断：先确认主体是平台宿主内应用、小程序运行时和平台 API，而不是浏览器页面、H5 或真正 App 工程。
- 通用约束：再读 [../10-miniapp/11_小程序通用规范.md](../10-miniapp/11_小程序通用规范.md)。
- 技术选型：如需判断原生小程序方案、Taro、uni-app 或同类方案，再读 [../10-miniapp/12_小程序技术选型规范.md](../10-miniapp/12_小程序技术选型规范.md)；如属于真正以微信小程序为主交付形态的新项目，默认先从原生小程序方案的优先评估与转出规则开始。
- 目录规划：如需确定小程序工程目录、分包边界、平台能力模块和提审发布资源位置，再读 [../10-miniapp/13_小程序目录结构规范.md](../10-miniapp/13_小程序目录结构规范.md)。
- 平台能力：如需接入登录授权、支付、订阅消息、分享、定位、扫码、文件和其它宿主 API，再读 [../10-miniapp/14_小程序平台能力接入规范.md](../10-miniapp/14_小程序平台能力接入规范.md)。
- 发布交付：如需处理构建、提审、灰度、正式发布、回退和发布前后观察，再读 [../10-miniapp/15_小程序发布交付规范.md](../10-miniapp/15_小程序发布交付规范.md)。
- 测试验收：如需覆盖自动化验证、体验版冒烟、平台能力验收和发布前门禁，再读 [../10-miniapp/19_小程序测试与验收规范.md](../10-miniapp/19_小程序测试与验收规范.md)。
- 交付清单：如需直接执行版本发布前检查、自测、体验版验证、提审、灰度和回退准备，再读 [../10-miniapp/16_小程序项目交付清单模板.md](../10-miniapp/16_小程序项目交付清单模板.md)。
- 验收记录：如需留档发布验收结论、上线确认和灰度放量建议，再读 [../10-miniapp/17_小程序发布验收记录模板.md](../10-miniapp/17_小程序发布验收记录模板.md)。
- 事故复盘：如需留档线上故障、发布异常、灰度事故和后续行动项，再读 [../10-miniapp/18_小程序事故复盘模板.md](../10-miniapp/18_小程序事故复盘模板.md)。
- 交付形态：先确认当前任务是否涉及微信小程序登录授权、支付、订阅消息、审核提审、平台 API 或平台发布链路。
- 交叉补读：如同时承载 Web 页面或 WebView 页面，按需补读 [../02-frontend/00_README.md](../02-frontend/00_README.md)。
- 安全与接口：涉及登录、支付、敏感信息和服务协同时，补读 [../07-security/00_README.md](../07-security/00_README.md) 和 [../03-backend/00_README.md](../03-backend/00_README.md)。

### AI 执行软件工程任务

#### 先判断怎么进入

- 目录入口：先读 [../11-ai-engineering/00_README.md](../11-ai-engineering/00_README.md)。
- 入口判断：如还不清楚目录入口、总览导航和新项目路线的分工，先读 [../11-ai-engineering/15_AI软件工程操作系统使用说明.md](../11-ai-engineering/15_AI%E8%BD%AF%E4%BB%B6%E5%B7%A5%E7%A8%8B%E6%93%8D%E4%BD%9C%E7%B3%BB%E7%BB%9F%E4%BD%BF%E7%94%A8%E8%AF%B4%E6%98%8E.md)。
- 术语统一：如需先统一执行闭环、多代理、阻塞、证据链等术语口径，先读 [../11-ai-engineering/16_AI软件工程术语表.md](../11-ai-engineering/16_AI%E8%BD%AF%E4%BB%B6%E5%B7%A5%E7%A8%8B%E6%9C%AF%E8%AF%AD%E8%A1%A8.md)。
- 分层说明：如需理解 11-ai-engineering 为什么拆成正文层、样例层和样例导航层，继续读 [../11-ai-engineering/31_AI目录分层与演进说明.md](../11-ai-engineering/31_AI%E7%9B%AE%E5%BD%95%E5%88%86%E5%B1%82%E4%B8%8E%E6%BC%94%E8%BF%9B%E8%AF%B4%E6%98%8E.md)。
- 最短上手：如需第一次进入 11-ai-engineering 时的最短阅读路线，继续读 [../11-ai-engineering/32_AI最短上手路径.md](../11-ai-engineering/32_AI%E6%9C%80%E7%9F%AD%E4%B8%8A%E6%89%8B%E8%B7%AF%E5%BE%84.md)。

#### 再看一次执行闭环

- 任务接入：如需判断当前任务是否可直接执行、是否需要最小澄清或是否存在高风险边界，先读 [../11-ai-engineering/01_AI任务接入与澄清规范.md](../11-ai-engineering/01_AI%E4%BB%BB%E5%8A%A1%E6%8E%A5%E5%85%A5%E4%B8%8E%E6%BE%84%E6%B8%85%E8%A7%84%E8%8C%83.md)。
- 仓库定位：如需从文件、符号、报错、测试或行为描述快速收敛到直接控制路径，先读 [../11-ai-engineering/03_AI仓库定位与上下文收集规范.md](../11-ai-engineering/03_AI%E4%BB%93%E5%BA%93%E5%AE%9A%E4%BD%8D%E4%B8%8E%E4%B8%8A%E4%B8%8B%E6%96%87%E6%94%B6%E9%9B%86%E8%A7%84%E8%8C%83.md)。
- 代码修改：如需实施最小改动、修复根因并保护用户已有改动，继续读 [../11-ai-engineering/04_AI代码修改与最小变更规范.md](../11-ai-engineering/04_AI%E4%BB%A3%E7%A0%81%E4%BF%AE%E6%94%B9%E4%B8%8E%E6%9C%80%E5%B0%8F%E5%8F%98%E6%9B%B4%E8%A7%84%E8%8C%83.md)。
- 验证闭环：如需定义改后第一步验证、完成判定和环境受限时的替代验证，继续读 [../11-ai-engineering/05_AI验证与完成判定规范.md](../11-ai-engineering/05_AI%E9%AA%8C%E8%AF%81%E4%B8%8E%E5%AE%8C%E6%88%90%E5%88%A4%E5%AE%9A%E8%A7%84%E8%8C%83.md)。

#### 按需补治理与导航

- 权限与阻塞：如需处理工具权限边界、删除与批量修改限制、连续失败或环境不可用，继续读 [../11-ai-engineering/06_AI工具调用与权限边界规范.md](../11-ai-engineering/06_AI%E5%B7%A5%E5%85%B7%E8%B0%83%E7%94%A8%E4%B8%8E%E6%9D%83%E9%99%90%E8%BE%B9%E7%95%8C%E8%A7%84%E8%8C%83.md) 和 [../11-ai-engineering/10_AI失败恢复与阻塞处理规范.md](../11-ai-engineering/10_AI%E5%A4%B1%E8%B4%A5%E6%81%A2%E5%A4%8D%E4%B8%8E%E9%98%BB%E5%A1%9E%E5%A4%84%E7%90%86%E8%A7%84%E8%8C%83.md)。
- 总览导航：如需按任务类型、执行阶段或治理主题组织阅读顺序，继续读 [../11-ai-engineering/13_AI软件工程操作系统总览导航.md](../11-ai-engineering/13_AI%E8%BD%AF%E4%BB%B6%E5%B7%A5%E7%A8%8B%E6%93%8D%E4%BD%9C%E7%B3%BB%E7%BB%9F%E6%80%BB%E8%A7%88%E5%AF%BC%E8%88%AA.md)。
- 新仓库接入：如需把这套规范接入一个新仓库或规划阶段性接入路线，继续读 [../11-ai-engineering/14_AI软件工程新项目接入指引.md](../11-ai-engineering/14_AI%E8%BD%AF%E4%BB%B6%E5%B7%A5%E7%A8%8B%E6%96%B0%E9%A1%B9%E7%9B%AE%E6%8E%A5%E5%85%A5%E6%8C%87%E5%BC%95.md)。

#### 需要演练时再进入样例层

- 样例导航：如需先判断样例层如何进入或按任务目标如何组合样例，继续读 [../11-ai-engineering/29_AI样例层总览导航.md](../11-ai-engineering/29_AI%E6%A0%B7%E4%BE%8B%E5%B1%82%E6%80%BB%E8%A7%88%E5%AF%BC%E8%88%AA.md) 和 [../11-ai-engineering/30_AI跨样例组合路径.md](../11-ai-engineering/30_AI%E8%B7%A8%E6%A0%B7%E4%BE%8B%E7%BB%84%E5%90%88%E8%B7%AF%E5%BE%84.md)。
- 样例演练：如需快速看到接入判断、多代理协作、阻塞升级、仓库定位、验证闭环、最小变更、失败恢复分流、计划管理、审计证据链、记忆治理、评估指标和结果输出长什么样，继续读 [../11-ai-engineering/17_AI任务接入样例.md](../11-ai-engineering/17_AI%E4%BB%BB%E5%8A%A1%E6%8E%A5%E5%85%A5%E6%A0%B7%E4%BE%8B.md)、[../11-ai-engineering/18_AI多代理协作样例.md](../11-ai-engineering/18_AI%E5%A4%9A%E4%BB%A3%E7%90%86%E5%8D%8F%E4%BD%9C%E6%A0%B7%E4%BE%8B.md)、[../11-ai-engineering/19_AI阻塞升级样例.md](../11-ai-engineering/19_AI%E9%98%BB%E5%A1%9E%E5%8D%87%E7%BA%A7%E6%A0%B7%E4%BE%8B.md)、[../11-ai-engineering/20_AI输出模板实例.md](../11-ai-engineering/20_AI%E8%BE%93%E5%87%BA%E6%A8%A1%E6%9D%BF%E5%AE%9E%E4%BE%8B.md)、[../11-ai-engineering/21_AI仓库定位样例.md](../11-ai-engineering/21_AI%E4%BB%93%E5%BA%93%E5%AE%9A%E4%BD%8D%E6%A0%B7%E4%BE%8B.md)、[../11-ai-engineering/22_AI验证闭环样例.md](../11-ai-engineering/22_AI%E9%AA%8C%E8%AF%81%E9%97%AD%E7%8E%AF%E6%A0%B7%E4%BE%8B.md)、[../11-ai-engineering/23_AI最小变更样例.md](../11-ai-engineering/23_AI%E6%9C%80%E5%B0%8F%E5%8F%98%E6%9B%B4%E6%A0%B7%E4%BE%8B.md)、[../11-ai-engineering/24_AI失败恢复分流样例.md](../11-ai-engineering/24_AI%E5%A4%B1%E8%B4%A5%E6%81%A2%E5%A4%8D%E5%88%86%E6%B5%81%E6%A0%B7%E4%BE%8B.md)、[../11-ai-engineering/25_AI计划管理样例.md](../11-ai-engineering/25_AI%E8%AE%A1%E5%88%92%E7%AE%A1%E7%90%86%E6%A0%B7%E4%BE%8B.md)、[../11-ai-engineering/26_AI审计证据链样例.md](../11-ai-engineering/26_AI%E5%AE%A1%E8%AE%A1%E8%AF%81%E6%8D%AE%E9%93%BE%E6%A0%B7%E4%BE%8B.md)、[../11-ai-engineering/27_AI记忆治理样例.md](../11-ai-engineering/27_AI%E8%AE%B0%E5%BF%86%E6%B2%BB%E7%90%86%E6%A0%B7%E4%BE%8B.md) 和 [../11-ai-engineering/28_AI评估指标样例.md](../11-ai-engineering/28_AI%E8%AF%84%E4%BC%B0%E6%8C%87%E6%A0%87%E6%A0%B7%E4%BE%8B.md)。
- 技术落地：如任务最终落到前端、后端、数据库、测试、安全或 DevOps 具体改动，仍需回到对应技术目录继续实施，而不是停留在 AI 执行协议层。

### 数据库设计或迁移

- 建模：先读 [../04-database/01_数据库设计规范.md](../04-database/01_数据库设计规范.md)。
- 命名与索引：再读 [../04-database/02_数据库命名规范.md](../04-database/02_数据库命名规范.md) 和 [../04-database/03_数据库索引规范.md](../04-database/03_数据库索引规范.md)。
- 上线迁移：变更前必须读 [../04-database/04_数据库迁移规范.md](../04-database/04_数据库迁移规范.md)。
- 回归验证：补读 [../05-tests/01_测试设计与分层规范.md](../05-tests/01_测试设计与分层规范.md)。

### 上线发布或变更交付

- 通用质量：先读 [../01-general/08_交付质量规范.md](../01-general/08_交付质量规范.md)。
- 数据变更：如涉及库表变更，补读 [../04-database/04_数据库迁移规范.md](../04-database/04_数据库迁移规范.md)。
- 安全检查：补读 [../07-security/08_安全评审与发布检查清单.md](../07-security/08_安全评审与发布检查清单.md)。
- DevOps 执行：进入 [../06-devops/00_README.md](../06-devops/00_README.md)，按脚本、流水线或发布执行主题继续阅读。

### 安全评审或安全整改

- 总入口：先读 [../07-security/00_README.md](../07-security/00_README.md)。
- 身份与接口：按需补读 [../07-security/01_身份认证与授权安全规范.md](../07-security/01_身份认证与授权安全规范.md) 和 [../07-security/02_应用与接口安全规范.md](../07-security/02_应用与接口安全规范.md)。
- 数据与密钥：如涉及敏感字段、导出、凭据或配置，补读 [../07-security/03_敏感信息与密钥管理规范.md](../07-security/03_敏感信息与密钥管理规范.md) 和 [../07-security/04_数据安全与隐私保护规范.md](../07-security/04_数据安全与隐私保护规范.md)。
- 运行与发布：如涉及基础设施、漏洞、审计或事件响应，补读 [../07-security/05_依赖与供应链安全规范.md](../07-security/05_依赖与供应链安全规范.md)、[../07-security/06_基础设施与运行环境安全规范.md](../07-security/06_基础设施与运行环境安全规范.md)、[../07-security/07_安全审计与事件响应规范.md](../07-security/07_安全审计与事件响应规范.md) 和 [../07-security/08_安全评审与发布检查清单.md](../07-security/08_安全评审与发布检查清单.md)。

### 容器化与部署交付

- 镜像构建：先读 [../06-devops/02_Docker与镜像规范.md](../06-devops/02_Docker与镜像规范.md)。
- 集群部署：如使用 Kubernetes，再读 [../06-devops/03_Kubernetes部署规范.md](../06-devops/03_Kubernetes部署规范.md)。
- 流水线门禁：补读 [../06-devops/04_CI_CD规范.md](../06-devops/04_CI_CD规范.md)。
- 发布执行：上线前补读 [../06-devops/05_发布与变更执行规范.md](../06-devops/05_发布与变更执行规范.md)。

### 测试设计与测试落地

- 测试分层：先读 [../05-tests/01_测试设计与分层规范.md](../05-tests/01_测试设计与分层规范.md)。
- 工具实现：再读 [../05-tests/02_测试工具与实现规范.md](../05-tests/02_测试工具与实现规范.md)。
- 通用验证口径：补读 [../01-general/07_通用测试规范.md](../01-general/07_通用测试规范.md) 和 [../01-general/08_交付质量规范.md](../01-general/08_交付质量规范.md)。

### 语言层实现规范

- 语言入口：先读 [../01-general/languages/00_README.md](../01-general/languages/00_README.md)。
- Java：进入 [../01-general/languages/01_Java语言规范.md](../01-general/languages/01_Java语言规范.md)。
- .NET：进入 [../01-general/languages/02_.NET语言规范.md](../01-general/languages/02_.NET语言规范.md)。
- Python：进入 [../01-general/languages/03_Python语言规范.md](../01-general/languages/03_Python语言规范.md)。
- JavaScript/TypeScript：进入 [../01-general/languages/04_JavaScript_TypeScript语言规范.md](../01-general/languages/04_JavaScript_TypeScript语言规范.md)。


### Electron 桌面端开发

- 目录入口：先读 [../08-electron/00_README.md](../08-electron/00_README.md)。
- 专题定位：如还不确定读哪些分册，再读 [../08-electron/31_Electron桌面端规范总览导航.md](../08-electron/31_Electron桌面端规范总览导航.md)。
- 安全补充：涉及权限、敏感信息和外链控制时，补读 [../07-security/00_README.md](../07-security/00_README.md)。

## 使用规则

- 如果任务涉及技术选型、框架选型、组件库选型、架构选型或模板选型，先询问用户确认后再继续。
- 如任务跨多个目录，优先确定主目录，再补读安全、测试、数据库或 DevOps 目录。
- 每次进入某个目录后，优先先读该目录的 00_README，再进入具体分册。
- 如需新增、调整或重组规则库文档，先读 [library-maintenance.md](library-maintenance.md)。
