---
title: 'Projects'
date: 2023-10-24
type: landing

design:
  spacing: '5rem'

sections:
  - block: markdown
    content:
      title: 'Selected Projects'
      subtitle: ''
      text: |

        ### SC GenAI Splunk — Supply Chain Alert Monitoring
        - 📅 **Period**: Jan 2026 — Apr 2026

        - **Stack**: Python · FastAPI · LangGraph · LangChain · Azure OpenAI · LangSmith · PyYAML · OAuth2 · Webex Adaptive Card · Snowflake · SMTP · pytest · Docker · Jenkins · Conjur

        Supply Chain GenAI Splunk alert monitoring platform. Receives Splunk alerts via **FastAPI Webhook**,
        applies app identification, pattern matching, and **LangGraph AI Agent** analysis, then sends intelligent
        notifications through email + Webex dual channels.

        - Upgraded Control-M and general Splunk alerts to **Webex Adaptive Cards** with structured display
        - Integrated **Confluence Wiki** troubleshooting summaries into cards
        - Scheduled CronJob to read Run/Trace data from **LangSmith** and write to **Snowflake** for AI observability
        - Added `custom_fields` support in component YAML, extracting business fields from Splunk `result` dynamically

        ---

        ### GenAI Self Service Hub Service
        - 📅 **Period**: Feb 2026 — Apr 2026

        - **Stack**: Python 3.11+ · FastAPI · Pydantic · PyYAML · Alation REST API · boto3 · S3 · Poetry · pytest

        Backend microservice for Cisco GenAI's **Self Service Hub**, providing business teams with self-service
        capabilities for knowledge bases, documents, Agent Workflows, and MCP Registry. Owned the **Semantic Layer** build-out.

        - Implemented **Alation Cloud REST Client** (token refresh, table retrieval, column-level metadata extraction)
        - Built Semantic Model YAML generation with **PyYAML** (dimension/fact splitting, relationships, Verified Queries); exposed via FastAPI `/generate` endpoint
        - Completed YAML validation and **S3 upload** with component/app naming and versioning
        - Delivered `/generate`, `/validate`, `/save` REST endpoints with Pydantic Schemas; added **pytest** unit tests

        ---

        ### Cisco IT Supply Chain GenAI Platform
        - 📅 **Period**: Jun 2025 — Jan 2026

        - **Stack**: Python · Streamlit · Duo SSO · GPU (CUDA) · OpenStack · HTTPS/TLS · Poetry · CI/CD · Ansible

        Internal AI Q&A and automation platform for Cisco Supply Chain based on **RAG + LangGraph**,
        integrated with multiple enterprise systems.

        - Integrated **Duo SSO** with Streamlit UI for unified user authentication
        - Installed and configured **NVIDIA GPU drivers** for embedding-vectorization acceleration
        - Configured HTTPS and TLS certificates across Dev/Stage/Prod on **OpenStack**
        - Migrated dependency management from pip to **Poetry**; built CI/CD pipeline
        - Installed and configured **Ansible** for multi-VM automation foundation

        ---

        ### API Maestro — Cisco IT Hackathon 2025
        - 📅 **Period**: May 2025 — Jun 2025

        - **Stack**: Python 3.12 · LangChain · LangGraph · FastMCP · Streamlit · FastAPI · OpenAPI/Swagger · BridgeIT · Docker Compose · PyYAML · Requests · ReAct Agent

        **Solo project** for Cisco IT Hackathon 2025. Drives any OpenAPI application with natural language:
        automatically parses OpenAPI/Swagger specs, understands endpoints and workflows, and translates
        conversational instructions into precise HTTP API calls.

        - Independently delivered architecture, coding, demo, and containerized deployment in ~2 months
        - Built NL → API orchestration chain with **LangGraph ReAct Agent**, dynamically mapping OpenAPI endpoints to LangChain Tools
        - Implemented OpenAPI spec parsing and runtime endpoint tool generation, supporting live spec switching
        - Evolved Agent capabilities into **FastMCP**-based MCP server with standardized Tools for Cursor/IDE integration
        - Delivered **Streamlit** conversational Web UI and **FastAPI HTTP Bridge** with Mock API Server

        ---

        ### Supply Chain Finance Miscellaneous Tools
        - 📅 **Period**: Sep 2023 — Apr 2026

        - **Stack**: Java 21 · Spring Boot 4.0 · Spring Security · OAuth2 · Angular 21 · Gradle (Kotlin DSL) · Docker · Jenkins · Spinnaker · Conjur

        Lightweight tools platform for the Supply Chain Finance team, hosting multiple high-frequency
        internal business tools with Excel/CSV uploads, cost-data downloads, and email notifications.

        - Monolithic Angular SPA + Spring Boot with **Gradle (Kotlin DSL)** unified build
        - SSO and dual-layer RBAC on **Spring Security + OAuth2 + Cisco LDAP**
        - API-First with **OpenAPI v3** contract and code generation pipeline
        - Drove **Spring Boot 2 → 4.0** and **Angular → 21** upgrades via **OpenRewrite**
        - Built DevSecOps pipeline with **Jenkins + SonarQube + SAST + Spinnaker**

        ---

        ### CART-Kafka — CBM Data Ingestion Microservice
        - 📅 **Period**: Jul 2024 — Apr 2026

        - **Stack**: Java 21 · Spring Boot 4.0 · Spring Kafka · Oracle · OAuth2 · Conjur · Docker · Jenkins · Spinnaker · OpenShift

        Upstream data-ingestion microservice consuming the CBM Kafka stream from Oracle Cloud,
        replicating component business data into enterprise ESM interface tables.

        - Tech Lead driving "independent microservice + dual Oracle data sources" layered architecture
        - Built Kafka consumer framework, dual-datasource auto-configuration, CBM entity model
        - Batch insert performance optimization via Hibernate batching + sliced `saveAll` strategy
        - Drove **Spring Boot 2.x → 4.0** and **Java → 21** upgrades via **OpenRewrite**
        - Migrated from Cert Auth to OAuth2; integrated **Conjur**; built on Cisco IT **Golden Pipeline**

        ---

        ### CART — Cost Analysis and Reconciliation Tool
        - 📅 **Period**: Sep 2020 — Apr 2026

        - **Stack**: Java 21 · Spring Boot 4.0 · Spring Security · OAuth2 · Oracle · Redis · OpenAPI v3 · AWS S3 · Angular 21 · AG Grid · Docker · Jenkins · Spinnaker · OpenShift

        Core Supply Chain Finance system automating day-end close — cost variance analysis and
        three-source reconciliation across Sub-Ledger / General Ledger / Cloud.

        - Bootstrapped full-stack frontend/backend scaffolding, evolved into team reference implementation
        - Implemented SSO, RBAC, and service-to-service auth on **Spring Security + OAuth2 + LDAP**
        - Designed and built **Cisco COS / AWS S3** integration with unified object-storage abstraction
        - Drove **Spring Boot → 4.0**, **Java → 21**, **Angular → 21** upgrades via **OpenRewrite**
        - Built DevSecOps pipeline: **Jenkins + SonarQube + SAST + PMD + JaCoCo + Spinnaker**

        ---

        ### Earlier Projects (2003 — Present)

        | Period | Project | Highlights |
        |---|---|---|
        | 2018/7 — 2026/4 | RCE — Royalty Calculation Engine | Tech Lead (9-person cross-border team); Cisco's enterprise royalty calculation system (30+ modules); Cloud Native + API-First; first Blue-Green zero-downtime deployment in department; Nx Monorepo with @scf/common-lib; upgraded to Spring Boot 4/Java 21/Angular 21 via OpenRewrite |
        | 2014/11 — 2018/1 | Self Service Model | Streamlined build/deploy workflows; Build-Once/Deploy-Many; Dev/QA self-service; Continuous Delivery Portal |
        | 2013/11 — 2014/10 | Continuous Delivery Transformation | Cisco IT CDT unified platform; migrated Git/Jenkins/Artifactory; uDeploy/uRelease feasibility study |
        | 2012/7 — 2013/10 | Data Center Migration | WebEx DC → Cisco DC app migration; US architecture discussions & POC; WLST automation scripts |
        | 2011/7 — 2012/6 | Git Migration | CVS → Git migration; POC & technical planning; trained developers on Git (in English) |
        | 2009/9 — 2010/10 | Continuous Integration | Refactored CruiseControl; migrated to Hudson (Jenkins) |
        | 2008/8 — 2009/8 | WebEx Elvis | Maintained lifecycle management system (PHP + MySQL) |
        | 2008/7 — 2009/8 | Myify | Lead developer of PHP/Zend/Dojo task-tracking app (90%+ code) |
        | 2007/10 — 2008/5 | Y!China NBS Platform | Lead frontend engineer for Yahoo's site-builder platform |
        | 2007/5 — 2007/7 | Y!China Blog UGC | Frontend architecture for Yahoo blog aggregation |
        | 2006/2 — 2007/5 | Y!China Photo Service | Lead frontend engineer; grew PV from <1M to 20M+ |
        | 2003/10 — 2004/2 | National Foreign Investment Inspection | .NET system for Ministry of Commerce + 7 ministries |
  - block: markdown
    content:
      title: 'Side Projects'
      subtitle: ''
      text: |

        ### RCE UI Rewrite in React
        - 📅 **Period**: Apr 2026 — May 2026

        - **Stack**: React 19 · TypeScript 6 · Vite 8 · Vitest · Playwright · React Router 7 · TanStack Query v5 · AG Grid Enterprise · Orval · OIDC · Cisco Atmosphere v4 · Tailwind CSS · pnpm Monorepo · Docker

        A personal exploration initiative pursuing multiple compounding goals: validate the
        **Vibe Coding** paradigm with AI Harness methodology, align UI/UX with the latest
        Cisco Design System (Atmosphere v4), lift code quality, and optimize performance.

        - **22 business pages rewritten** in ~2 months — validating Vibe Coding for end-to-end architecture migration
        - Produced reusable **pnpm Monorepo + React 19 + Vite + Orval + TanStack Query** scaffold
        - Landed **OIDC SSO**, **AG Grid Enterprise**, runtime env-config injection, **Docker**, and **Playwright E2E** tests
        - Harnessed AI Coding Agents with **Superpowers plugin** and custom-built **Skills** for reusable Agent workflows

        ---

        ### Playwright Test Automation
        - 📅 **Period**: 2025 — 2026

        - **Stack**: Playwright · TypeScript · Page Object Model · oracledb · TA JWT (RSA) · DUO OIDC · OAuth2 JWT · Express · Docker · Jenkins · Conjur

        Cross-project E2E automation initiative introducing a modern, reusable testing framework for the team.

        - Built cross-app framework from scratch covering **CART (E2E + API)** and **RCE (E2E / Regression / Smoke)**
        - Designed **TA JWT (RSA-signed)** auth mechanism to solve enterprise SSO blocking unattended automation
        - Built and maintain custom **Playwright Docker image**; CI orchestrated via **Jenkins parameter matrix**
        - Self-hosted **Test Report Server** (Express + Multer) with DUO OIDC + OAuth2 JWT protection
        - Adopted as reusable template by multiple team projects

        ---

        ### Video Downloader
        - 📅 **Period**: Jun 2025 — Jul 2025

        - **Stack**: Python 3.12 · yt-dlp · PyYAML · Docker · Docker Compose · GitHub Actions · GHCR · Bash
        - **Open Source**: [github.com/zpkx/video-downloader](https://github.com/zpkx/video-downloader)

        Personal open-source project for multi-platform batch video downloading and archiving.
        Supports YAML-driven URL management, category-based directory organization, rate-limit avoidance,
        and auto-download on config change for NAS/container environments.

        - Built `VideoDownloader` class on **yt-dlp** with single/multi-URL, category batch download, and info-only/dry-run modes
        - YAML-driven config: urls.yaml for categories and URL lists, config.yaml for centralized yt-dlp options
        - **Dockerfile + docker-compose** with watcher/oneshot/manual service modes; URL change triggers auto-download
        - Published image to **GHCR** via **GitHub Actions** for home NAS deployment
    design:
      columns: '1'
---
