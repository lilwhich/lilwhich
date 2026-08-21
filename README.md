# 你好，我是【你的名字】👋

> 【学校】【专业】在读 · 【年级，如：大三】 · 🎯 正在寻找 **AI 应用开发实习**（可实习【X】个月，【可入职时间】）

一个喜欢造工具的计算机学生：写过 Android App、配过华为云 IoT、也在研究 **AI Agent 怎么在真实工程里跑起来**——上下文怎么管理、工具怎么编排、成本怎么控制、出错怎么兜底。

## 🔥 代表项目

### [dsh-plugin-gather](https://github.com/lilwhich/dsh-plugin-gather) — AI Agent 工作台增强插件包

给 DeepSeek Harness（DSH，一个 AI 编程 Agent 运行时）做的增强插件，从零独立设计开发，已发布 30 个版本迭代，在社交平台推广后有真实用户使用。

**我在这项目里做了什么：**

| 模块 | 技术点 |
|------|--------|
| Host 侧服务（~1700 行 Node.js） | REST API 设计、轮询调度、Git 集成、文件快照（Checkpoint）系统 |
| Client 侧 UI（~2000+ 行） | VSCode 风格多栏界面、文件树懒加载、多 tab 编辑器、行级 LCS diff 算法 |
| 对话迁徙（Context Handoff） | 长对话上下文提炼压缩，token 压缩率 ~99%，解决 Agent 长会话退化问题 |
| 安全模式 | 跨 bash / PowerShell / CMD 的命令解析，拦截危险删除操作 |
| 工程化 | 一键安装脚本、语义化版本发布、插件依赖聚合与兼容性管理 |

**这个项目说明我能做的事：** 理解一个 Agent 运行时的架构 → 找到真实痛点 → 独立交付完整功能（前后端 + 算法 + 工程化），而不是停留在 prompt 调优层面。

### SmartPet 智能宠物管家 — 华为 IoT 比赛项目 · 独立开发的安卓 App

从零独立开发的 Android 智能宠物管理应用，参加华为 IoT 比赛。将**云端 IoT 设备控制**与**大模型 AI 分析**结合：宠物喂养数据上报到华为云，App 侧远程控制喂食器/灯光/门锁/报警器，并由大模型对宠物健康数据做智能分析。

**我在这项目里做了什么：**

| 模块 | 技术点 |
|------|--------|
| 华为云 IoTDA 设备接入 | IAM Token 鉴权、v5 命令下发 API、设备属性上报、产品/设备模型配置 |
| AI 智能分析 | 通义千问 qwen-turbo（DashScope API）、Prompt 约束输出结构化 JSON、协程异步调用 |
| 客户端架构 | Kotlin · Jetpack Compose · MVVM（ViewModel 分层）、OkHttp 网络层 |
| 功能完整度 | 摄像头检测、定位追踪、天气服务、疫苗/喂食管理、消息通知 |

**这个项目说明我能做的事：** 打通「端 - 云 - AI」完整链路——设备上云配置、云端 API 对接、移动端独立交付，以及对大模型 API 的工程化封装。

## 🏆 比赛与经历

- **华为 IoT 比赛**：完成华为云 IoTDA 平台的产品建模、设备注册、IAM 鉴权与命令下发全链路配置，App 端实现远程设备控制

## 🛠 技术栈

```text
语言        Kotlin · JavaScript / TypeScript · Python
移动端      Android · Jetpack Compose · MVVM · OkHttp · 协程
后端        Node.js · REST API · 轮询 / 实时数据同步
云与 IoT    华为云 IoTDA · IAM 鉴权 · MQTT 概念 / 命令下发
AI 工程     通义千问 API · Agent 工具编排 · 上下文管理 / 压缩 · Prompt 设计
前端        原生 DOM · 组件化 UI · Git Diff 可视化
工具链      Git · 语义化版本发布 · npm 生态 · PowerShell 自动化
```

## 🌱 我在关注的方向

- **Agent 工程化**：上下文管理、多 Agent 协作、技能沉淀（skill extraction）
- **AI 应用成本控制**：token 预算、模型分级调度
- **LLM + 开发者工具**：让 AI 编程助手更可控、更透明

## 📬 联系我

- 📧 邮箱：【你的求职邮箱】
- 💬 微信：【可选：你的微信号】

---

<!-- 把【】里的内容替换成你的真实信息即可 -->

![](https://github-readme-stats.vercel.app/api?username=lilwhich&show_icons=true&theme=default&hide_border=true)
![](https://github-readme-stats.vercel.app/api/top-langs/?username=lilwhich&layout=compact&show_icons=true&theme=default&hide_border=true)
