# 你好，我是 lilwhich 👋

> 人工智能专业 · 大三在读 · 🎯 正在寻找 **AI 应用开发实习**

人工智能专业，大三在读。写过 Android 应用（Kotlin + Jetpack Compose），接过华为云 IoTDA 的设备接入与命令下发，发布过 30 个版本的 DSH 插件，另有几个 CV 与语音方向的课程项目。日常用 Claude Code、Codex、DSH 这类 Agent 工具写代码，关心的是上下文怎么管、工具怎么编排、token 怎么控。

## ✨ 我的特质

- **关注 AI 前沿**：持续看大模型 / Agent / 多模态的进展，新工具出来后会上手试用，并拆解它的实现方式
- **边学边做**：Android、华为云 IoT、Agent 插件这几套技术栈都是边学边写，靠项目推进掌握
- **长期使用 Agent 工具**：一直用 **Claude Code、Codex、DSH** 等工具做开发，在上下文管理、Prompt 编写、token 成本控制上有实际经验

## 🤖 AI 辅助开发工作流

熟练使用 **Cursor / Claude Code / WorkBuddy / Codex** 等编码智能体：传入业务约束与开发规范，让 Agent 生成样板代码，借助它排查漏洞、生成测试与文档。

**「AI 生成 + 人工把关」工作流：**

```text
1. AI 起稿     传入业务约束、开发规范 → Agent 生成样板代码、测试与文档
2. 人工校验     重点核对并发、权限、SQL 注入等安全问题，甄别 AI 幻觉
3. 核心自写     核心业务逻辑自己实现，不依赖 AI 输出
```

> 原则：**样板代码和重复劳动交给 AI，安全和核心逻辑自己写。**

## 🔥 代表项目

### [dsh-plugin-gather](https://github.com/lilwhich/dsh-plugin-gather) — AI Agent 工作台增强插件包

给 DeepSeek Harness（DSH，一个 AI 编程 Agent 运行时）做的增强插件。长期使用 DSH 的过程中按实际遇到的问题设计开发，目前已发布 30 个版本，在社交平台推广后有用户在使用。

**我在这项目里做了什么：**

| 模块 | 技术点 |
|------|--------|
| Host 侧服务（~1700 行 Node.js） | REST API 设计、轮询调度、Git 集成、文件快照（Checkpoint）系统 |
| Client 侧 UI（~2000+ 行） | VSCode 风格多栏界面、文件树懒加载、多 tab 编辑器、行级 LCS diff 算法 |
| 对话迁徙（Context Handoff） | 长对话上下文提炼压缩，token 压缩率约 99%，缓解 Agent 长会话后的上下文退化 |
| 安全模式 | 跨 bash / PowerShell / CMD 的命令解析，拦截危险删除操作 |
| 工程化 | 一键安装脚本、语义化版本发布、插件依赖聚合与兼容性管理 |

**项目形态：** 一个可安装的 DSH 插件包，Host 侧 Node.js 服务与 Client 侧界面相互分离，通过 REST 通信。

**顺手搭的小东西**：给这个仓库加了 AI Issue 自动分诊工作流（GitHub Actions + 大模型）——新 issue 一来就自动摘要、分类打标签、生成回复草稿，省去手动分类；大模型调用失败时自动降级为关键词分类，流程不会中断。

### SmartPet 智能宠物管家 — 华为 IoT 比赛项目 · Android App

参加华为 IoT 比赛的 Android 应用。宠物喂养数据上报华为云，App 侧远程控制喂食器、灯光、门锁与报警器。

**我在这项目里做了什么：**

| 模块 | 技术点 |
|------|--------|
| 华为云 IoTDA 设备接入 | IAM Token 鉴权、v5 命令下发 API、设备属性上报、产品/设备模型配置 |
| 客户端架构 | Kotlin · Jetpack Compose · MVVM（ViewModel 分层）、OkHttp 网络层 |

**链路：** 设备上云配置 → 云端 API 对接 → 移动端远程控制。

### [classroom-cv](https://github.com/lilwhich/course-projects/tree/main/computer-vision/classroom-cv) — 教室在室人数与停留时长统计 · 主从分布式

课程设计，两台电脑 + 网络摄像头。从机接摄像头做人脸检测与识别，把进出事件经 HTTP 上报；主机落 SQLite 账本，Web 看板展示在室人数与每人停留时长。

**我在这项目里做了什么：**

| 模块 | 技术点 |
|------|--------|
| 从机识别 | OpenCV YuNet 检测 + SFace 特征比对；一个摄像头只开一次，推流与识别共用 capture（Windows 下重复打开会失败） |
| 设备发现 | UDP 广播（8766）自动发现主机，换教室不用手填 IP |
| 去抖与去重 | 四道过滤：框尺寸阈值 → 同轨迹累计 3 帧 → 同身份同机位 20 秒窗口 → 断网落本地队列；事件带 uuid，多机合并不重复记账 |
| 数据模型 | 不存「在室表」，在室名单由 `status='OPEN'` 的会话实时推导，避免与事件流水打架 |
| 服务端 | FastAPI + SQLite，双路 MJPEG 预览、CSV 导出（进/出/时长） |

**完整链路：** 摄像头采集 → 检测识别 → 事件上报 → 账本落库 → 看板展示。两台机器各自识别后合并，断网补传不重复记账；没有稳定身份 ID 时按先进先出配对。

> 📚 课程与实验课的小实践另有归档：**[course-projects](https://github.com/lilwhich/course-projects)** —— 按学科分目录，每个项目自带 README、依赖清单与结果图，可独立复现。

## 🏆 比赛与经历

- **2026 大学生创新创业训练计划（大创）三等奖** ——《农田病虫害智能监测与生态防治系统》
- **华为 IoT 比赛**：完成华为云 IoTDA 的产品建模、设备注册、IAM 鉴权与命令下发配置，App 端实现远程设备控制

## 🛠 技术栈

```text
语言        Kotlin · JavaScript / TypeScript · Python
移动端      Android · Jetpack Compose · MVVM · OkHttp · 协程
后端服务    Node.js · FastAPI · REST API · SQLite · 轮询 / 实时数据同步
云与 IoT    华为云 IoTDA · IAM 鉴权 · 设备命令下发
AI 工程     Agent 工具编排 · 上下文管理 / 压缩
AI 编码工具  Cursor · Claude Code · WorkBuddy · Codex · DSH
计算机视觉  OpenCV · YuNet / SFace · SIFT / RANSAC · 柱面投影
前端        原生 DOM · 组件化 UI · Git Diff 可视化
分布式      UDP 广播服务发现 · 事件幂等 · 断网补传
工具链      Git · GitHub Actions（CI 自动化） · 语义化版本发布 · PowerShell 自动化
```

## 🌱 我在关注的方向

- **Agent 前沿动态**：MCP / Function Calling 生态、多 Agent 协作、技能沉淀（skill extraction）、Computer Use
- **Agent 落地场景**：关注 Agent 能力嵌进具体行业时，哪些环节真的能省下人力、哪些还存在明显错误率
- **AI 应用成本控制**：token 预算、模型分级调度、长上下文压缩
- **LLM + 开发者工具**：让 AI 编程助手更可控、更透明

## 📬 联系我

- 📧 3077271883@qq.com · lilwhich122@gmail.com
- 💬 微信：lilwhich

---

![](https://github-readme-stats.vercel.app/api?username=lilwhich&show_icons=true&theme=default&hide_border=true)
![](https://github-readme-stats.vercel.app/api/top-langs/?username=lilwhich&layout=compact&show_icons=true&theme=default&hide_border=true)
