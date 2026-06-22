---
title: '项目经验'
date: 2023-10-24
type: landing

design:
  spacing: '5rem'

sections:
  - block: markdown
    content:
      title: '项目经验'
      subtitle: ''
      text: |

        ### SC GenAI Splunk — Supply Chain Alert Monitoring
        - 📅 **项目周期**：2026/1 — 2026/4

        - **技术栈**: Python · FastAPI · LangGraph · LangChain · Azure OpenAI · LangSmith · PyYAML · OAuth2 · Webex Adaptive Card · Snowflake · SMTP · pytest · Docker · Jenkins · Conjur

        供应链 GenAI Splunk 告警监控平台，基于 **FastAPI Webhook** 接收 Splunk 告警，
        经应用识别、模式匹配与 **LangGraph AI Agent** 分析后，通过邮件 + Webex 双通道智能通知。

        - 将 Control-M 及通用 Splunk 告警通知升级为 **Webex Adaptive Card**（作业详情、Oracle 异常、可折叠区块等结构化展示）
        - 集成 **Confluence Wiki 故障排查** 摘要并渲染至卡片
        - 通过 CronJob 定时从 **LangSmith** 读取 Run/Trace 数据，写入 **Snowflake** 支撑 AI 告警可观测性
        - 在组件级 YAML 支持 `custom_fields`，从 Splunk `result` 动态提取业务字段，贯通全链路展示

        ---

        ### GenAI Self Service Hub Service
        - 📅 **项目周期**：2026/2 — 2026/4

        - **技术栈**: Python 3.11+ · FastAPI · Pydantic · PyYAML · Alation REST API · boto3 · S3 · Poetry · pytest

        Cisco GenAI 平台的 **Self Service Hub** 后端微服务，为业务团队提供知识库、文档、Agent Workflow、MCP Registry 等自助能力。
        本人负责 **Semantic Layer（语义层）** 能力建设。

        - 实现 **Alation Cloud REST Client**（Token 刷新、表检索、列级元数据拉取），映射为结构化规格
        - 基于 **PyYAML** 实现语义模型文档组装与校验（维度/事实拆分、关系与 Verified Queries），通过 FastAPI `/generate` 接口一键生成 Semantic Model YAML
        - 完成生成结果的校验与落盘，将 YAML **上传至 S3**（按组件/应用命名与版本化管理）
        - 交付 `/generate`、`/validate`、`/save` 等 REST 端点及 Pydantic Schema；补充 **pytest** 单元测试

        ---

        ### Cisco IT Supply Chain GenAI Platform
        - 📅 **项目周期**：2025/6 — 2026/1

        - **技术栈**: Python · Streamlit · Duo SSO · GPU (CUDA) · OpenStack · HTTPS/TLS · Poetry · CI/CD · Ansible

        基于 **RAG + LangGraph** 为 Cisco 供应链构建的企业内部 AI 问答与自动化平台，集成多个企业系统，
        实现智能问答与业务自动化。

        - 完成 **Duo SSO** 与 Streamlit UI 的集成，填补统一用户登录能力
        - 在生产 VM 上完成 **Nvidia GPU 驱动安装与配置**，为 Embedding 向量化加速提供算力底座
        - 在 **OpenStack** 上为 Dev/Stage/Prod 环境完成 HTTPS 与 TLS 证书配置
        - 将依赖管理从 pip 迁移至 **Poetry**，并完成 **CI/CD Pipeline** 搭建
        - 完成 **Ansible** 安装与配置，建立多 VM 自动化运维基础

        ---

        ### API Maestro — Cisco IT Hackathon 2025
        - 📅 **项目周期**：2025/5 — 2025/6

        - **技术栈**: Python 3.12 · LangChain · LangGraph · FastMCP · Streamlit · FastAPI · OpenAPI/Swagger · BridgeIT · Docker Compose · PyYAML · Requests · ReAct Agent

        **Solo 独立完成** 的 Cisco IT Hackathon 2025 参赛作品，用自然语言驱动任意 OpenAPI 应用：
        系统自动解析 OpenAPI/Swagger 规范，将用户的口语化指令翻译为精准的 HTTP API 调用。

        - 从 0 到 1 独立交付：架构设计、核心编码、Demo 与容器化部署，约 2 个月完成完整作品
        - 基于 **LangGraph ReAct Agent** 构建 NL → API 编排链路，动态将 OpenAPI 端点映射为 LangChain Tools
        - 实现 OpenAPI 规范解析与端点工具化，支持运行时加载/切换 API Spec
        - 将 Agent 能力重构为基于 **FastMCP** 的 MCP 服务，提供标准化 Tool，支持 Cursor/IDE 接入
        - 交付 **Streamlit** 对话式 Web UI 与 **FastAPI HTTP Bridge**，配套 Mock API Server

        ---

        ### Supply Chain Finance Miscellaneous Tools
        - 📅 **项目周期**：2023/9 — 2026/4

        - **技术栈**: Java 21 · Spring Boot 4.0 · Spring Security · OAuth2 · Angular 21 · Gradle (Kotlin DSL) · Docker · Jenkins · Spinnaker · Conjur

        面向供应链财务团队的轻量级工具集平台，承载多个高频内部业务工具，
        覆盖 Excel/CSV 批量上传、成本数据下载、邮件通知等场景。

        - Monolithic Angular SPA + Spring Boot 同仓共建，**Gradle (Kotlin DSL)** 统一编排
        - 基于 **Spring Security + OAuth2 + Cisco LDAP** 实现 SSO 与 RBAC
        - API-First 维护 OpenAPI v3 规范并落地代码自动生成
        - 通过 **OpenRewrite** 主导 Spring Boot 2 → 4.0、Angular → 21 升级
        - 搭建 **Jenkins + SonarQube + SAST + Spinnaker** 自动化交付链路

        ---

        ### CART-Kafka — CBM 数据接入微服务
        - 📅 **项目周期**：2024/7 — 2026/4

        - **技术栈**: Java 21 · Spring Boot 4.0 · Spring Kafka · Oracle · OAuth2 · Conjur · Docker · Jenkins · Spinnaker · OpenShift

        CART 项目的上游数据接入微服务，消费 Oracle Cloud 的 CBM Kafka 数据流，
        将组件业务数据近实时复制到企业 ESM 系统的 XXCART schema 接口表中。

        - Tech Lead 主导从 0 到 1 的架构设计，确立"独立微服务 + 双 Oracle 数据源"分层架构
        - 完成 Kafka Consumer 框架、双数据源自动配置、CBM 实体模型与持久化层
        - 通过 Hibernate Batch + 按 batch_size 切片调用 saveAll 实现批量写入性能优化
        - 通过 **OpenRewrite** 主导 Spring Boot 2.x → 4.0、Java → 21 多轮升级
        - 完成 Cert Auth → OAuth2 迁移；密钥托管接入 **Conjur**；迁移至 Cisco IT **Golden Pipeline**

        ---

        ### CART — Cost Analysis and Reconciliation Tool
        - 📅 **项目周期**：2020/9 — 2026/4

        - **技术栈**: Java 21 · Spring Boot 4.0 · Spring Security · OAuth2 · Oracle · Redis · OpenAPI v3 · AWS S3 · Angular 21 · AG Grid · Docker · Jenkins · Spinnaker · OpenShift

        供应链财务核心业务系统，自动化日结流程中的成本差异分析与子账/总账/Cloud 三源对账，
        后端 22 个 Controller/43 个 Service，前端 17 个业务模块。

        - 主导搭建前后端分离的全栈脚手架，演进为团队参考实现
        - 基于 **Spring Security + OAuth2 + LDAP** 实现 SSO、RBAC 与服务间鉴权
        - 完成 **Cisco COS / AWS S3** 集成，统一抽象对象存储能力
        - 通过 **OpenRewrite** 主导 Spring Boot → 4.0、Java → 21、Angular → 21 升级
        - 负责 **Jenkins + SonarQube + SAST + PMD + JaCoCo + Spinnaker** 交付链路

        ---

        ### 早期项目 (2003 — 至今)

        | 时间 | 项目 | 角色与亮点 |
        |---|---|---|
        | 2018/7 — 2026/4 | RCE — Royalty Calculation Engine | Tech Lead（9 人跨国团队）；Cisco 专利税核心业务系统（30+ 模块）；Cloud Native + API-First；部门首个 Blue-Green 零停机部署；Nx Monorepo 与 @scf/common-lib 共享库；OpenRewrite 演进至 Spring Boot 4/Java 21/Angular 21 |
        | 2014/11 — 2018/1 | Self Service Model | 优化构建/部署流程，实现 Build-Once/Deploy-Many 与 Dev/QA Self Service 上线；开发 Continuous Delivery Portal |
        | 2013/11 — 2014/10 | Continuous Delivery Transformation | Cisco IT CDT 统一交付平台；主导 Git/Jenkins/Artifactory 迁移至新平台；uDeploy/uRelease 可行性研究与美印平台团队协作 |
        | 2012/7 — 2013/10 | Data Center Migration | WebEx DataCenter → Cisco DataCenter 应用迁移；赴美参与架构讨论与 POC；编写 WLST 自动化脚本 |
        | 2011/7 — 2012/6 | Git Migration | CVS → Git 迁移；完成 POC 与技术方案；英语培训 Dev 团队 Git 技能；带领 DevOps 成员按计划完成迁移 |
        | 2009/9 — 2010/10 | Continuous Integration | 重构 CruiseControl 脚本；主导从 CruiseControl 迁移至 Hudson（Jenkins） |
        | 2008/8 — 2009/8 | WebEx Elvis | 维护内部生命周期管理系统（PHP + MySQL），完成 Bug 修复与功能开发 |
        | 2008/7 — 2009/8 | Myify | PHP/Zend/Dojo 任务跟踪 Web 应用主开发，完成 90%+ 代码 |
        | 2007/10 — 2008/5 | Y!China NBS Platform | 雅虎站长天下建站平台前端主开发，主导 symfony 框架落地与后台管理模块 |
        | 2007/5 — 2007/7 | Y!China Blog UGC | 雅虎博客聚合前端架构设计与开发（PHP + PostgreSQL） |
        | 2006/2 — 2007/5 | Y!China Photo Service | 雅虎相册前端主开发，配合运营将 PV 从 <100 万提升至 2000 万+ |
        | 2003/10 — 2004/2 | 国家外资年检系统 | 商务部联合 7 部委的 .NET 系统 |
  - block: markdown
    content:
      title: '业余项目'
      subtitle: ''
      text: |

        ### RCE UI 重写为 React
        - 📅 **项目周期**：2026/4 — 2026/5

        - **技术栈**: React 19 · TypeScript 6 · Vite 8 · Vitest · Playwright · React Router 7 · TanStack Query v5 · AG Grid Enterprise · Orval · OIDC · Cisco Atmosphere v4 · Tailwind CSS · pnpm Monorepo · Docker

        个人主导的探索性 Initiative，验证 **Vibe Coding** 模式与 AI Harness 实践，
        对齐最新 Cisco Design System (Atmosphere v4)，提升代码质量与性能。

        - 约 2 个月独立完成 **22 个业务页面** 的全量重写，验证 Vibe Coding 可行性
        - 沉淀 **pnpm Monorepo + React 19 + Vite + Orval + TanStack Query** 现代前端脚手架
        - 完成 **OIDC SSO**、**AG Grid Enterprise**、Docker 容器化、Playwright E2E 测试
        - 综合运用 **Superpowers 插件**与自建 **Skills** 形成可复用的 Agent 工作流

        ---

        ### Playwright Test Automation
        - 📅 **项目周期**：2025 — 2026

        - **技术栈**: Playwright · TypeScript · Page Object Model · oracledb · TA JWT (RSA) · DUO OIDC · OAuth2 JWT · Express · Docker · Jenkins · Conjur

        为团队引入现代化、可复用、跨项目通用的端到端自动化测试体系。

        - 基于 **Playwright + TypeScript + Page Object Model** 从 0 搭建跨应用测试框架
        - 设计 **TA JWT (RSA 签名)** 认证方案，解决企业 SSO 阻塞自动化测试的难题
        - 自构建并维护专用 Playwright Docker 镜像；通过 Jenkins Pipeline + 矩阵参数调度
        - 自建 Test Report Server（Express + Multer），DUO OIDC + OAuth2 JWT 保护
        - 作为可复用模板被团队多个项目采纳

        ---

        ### Video Downloader
        - 📅 **项目周期**：2025/6 — 2025/7

        - **技术栈**: Python 3.12 · yt-dlp · PyYAML · Docker · Docker Compose · GitHub Actions · GHCR · Bash
        - **开源仓库**: [github.com/zpkx/video-downloader](https://github.com/zpkx/video-downloader)

        个人业余开源项目，解决多平台视频批量下载与归档痛点：手工维护 URL 列表、按类别分目录保存、避免触发限流，支持 NAS/容器环境改配置即自动下载。

        - 基于 **yt-dlp** 封装 `VideoDownloader` 类，支持单 URL、多 URL、按类别批量下载及 info-only/dry-run 模式
        - YAML 驱动配置：urls.yaml 定义分类与 URL 列表，config.yaml 集中管理 yt-dlp 选项
        - 提供 **Dockerfile + docker-compose**（watcher/oneshot/manual 多服务模式），实现 urls.yaml 变更即触发下载
        - 通过 **GitHub Actions** 构建并发布镜像至 **GHCR**，便于家庭 NAS 长期拉取运行
    design:
      columns: '1'
---
