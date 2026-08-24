<div align="center">

**Agent Harness 层的精选地图：平台、沙箱、自进化技能与多 Agent 协同。**

[![Entries](https://img.shields.io/badge/条目-60+-blueviolet?style=flat-square)](README.zh-CN.md)
[![Data](https://img.shields.io/badge/star%20数-2026--08%20实查-3DDC84?style=flat-square)](docs/landscape.md)
[![License: MIT](https://img.shields.io/badge/License-MIT-3DDC84?style=flat-square)](LICENSE)

[English](README.md) | **简体中文** | [日本語](README.ja.md)

</div>

---

> **什么是 Harness？** 不是你 import 的框架——而是围绕一个模型循环的**生产运行时产品**：连接模型与工具、权限、环境的那一层（OpenAI，2026 年 2 月）。本清单跟踪这一层。不定期更新，欢迎 Star。所有 star 数为 2026 年 8 月实查——见[调研笔记](docs/landscape.md)。

## 📖 定义学科的五篇原文（按顺序读）

- [Harness Engineering: Leveraging Codex in an Agent-First World](https://openai.com/index/harness-engineering/) — OpenAI（Ryan Lopopolo），2026-02，**定名之作**；harness = 事件之上的 OODA 循环
- [Effective Harnesses for Long-Running Agents](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents) — Anthropic，2025-11；文件系统即外部状态、结构化工具输出（"上下文腐烂"）、hooks
- [Harness Engineering for Self-Improvement](https://lilianweng.github.io/) — Lilian Weng，2026-07；SE-Agent Router 参考架构
- [Learn Harness Engineering](https://walkinglabs.github.io/) — walkinglabs 免费开放书，2026-05
- [Why Software Factories Fail](https://github.com/humanlayer/advanced-context-engineering-for-coding-agents) — HumanLayer，2026-07（2.5k★），**必要的反方**：harness 不能解决模型训练问题

## ⚙️ 平台与框架

- [deepseek-ai/deepseek-harness](https://github.com/deepseek-ai/deepseek-harness) — **188k★** — "一切皆插件"；10 天 18.6 万星，插件生态自成体系
- [affaan-m/ECC](https://github.com/affaan-m/ECC) — **242k★** — harness 性能优化：skills / instincts / memory，continuous-learning-v2
- [PrimeIntellect-ai/prime-agent](https://github.com/PrimeIntellect-ai/prime-agent) — 17.9k★ — 自我改进 RL Agent
- [xai-org/grok-build](https://github.com/xai-org/grok-build) — 25.9k★ — Rust 编码 Agent harness/TUI
- [yc-software/qm](https://github.com/yc-software/qm) — 14.1k★ — 多人 harness：按人/房间隔离的记忆、文件、钥匙串与权限
- [LangGraph](https://github.com/langchain-ai/langgraph) — 40.3k★ — 图/检查点生态位
- [openai/openai-agents-python](https://github.com/openai/openai-agents-python) — 28.9k★ — swarm 的生产继任者

## 🏰 沙箱与隔离（轻 → 重）

- [daytonaio/daytona](https://github.com/daytonaio/daytona) — **71.9k★** — 该赛道涨星最快
- [firecracker-microvm/firecracker](https://github.com/firecracker-microvm/firecracker) — 36.2k★ — microVM 基石（E2B 云的底座）
- [google/gvisor](https://github.com/google/gvisor) — 19.1k★ — 系统调用拦截的应用内核
- [e2b-dev/E2B](https://github.com/e2b-dev/E2B) — 13.5k★ — Agent 代码执行的事实标准 SDK
- [superradcompany/microsandbox](https://github.com/superradcompany/microsandbox) — 7.9k★ — 可嵌入 microVM，<100ms 启动

> ⚠️ **JVM 没有安全沙箱**（Security Manager 随 JEP 486 永久禁用）。JVM 项目应在 `confine(argv, policy)` 接缝后 spawn OS 级运行器——macOS 26 的 sandbox-exec 已无法执行 exec（实测），见[调研笔记](docs/landscape.md)。

## 🧬 技能与自我改进

- [obra/superpowers](https://github.com/obra/superpowers) — **277k★** — "写技能 = TDD 应用于流程文档"
- [karpathy/autoresearch](https://github.com/karpathy/autoresearch) — **94.6k★** — MCE 技能即文件循环；实测：过严过滤反而降低下游性能
- [anthropics/skills → skill-creator](https://github.com/anthropics/skills) — eval 门控的自我改写：基线对比 + 盲测 A/B
- [vivekhaldar/seed](https://github.com/vivekhaldar/seed) — 91★ — 极简自我改写 harness，**唯一用 git 版本化自我目录的实现**

## 🐜 多 Agent 协同（生产实账）

Anthropic 生产数据：**+90.2% 但 15× token；token 预算解释 80% 的结果方差**。已命名翻车现场：任务含糊→重复劳动、Agent 互相打扰、**简单问题爆 50 个 subagent**、"电话游戏"（修复=工件落盘不传话）。

- [NanmiCoder/dsh-agent-teams](https://github.com/NanmiCoder/dsh-agent-teams) — 920★ — 依赖门控任务 DAG + 原子认领 + 断点续跑
- Claude Code subagents（[文档](https://code.claude.com/docs/en/sub-agents)）— 工具白名单、按 Agent 路由模型、worktree 隔离、并发上限 20

## 🛠️ 参考实现

- [bayshier/harness-engineering](https://github.com/bayshier/harness-engineering) — **Kotlin** 五组件参考实现（OODA+预算护栏 / fail-closed 沙箱接缝 / git 版本化自进化技能 / 任务 DAG / 诚实边界）。本清单唯一的 Kotlin 原生条目
- [bayshier/kline-mcp](https://github.com/bayshier/kline-mcp) · [kline-vision](https://github.com/bayshier/kline-vision) · [t1-replay](https://github.com/bayshier/t1-replay) · [android-mcp](https://github.com/bayshier/android-mcp) — 可被 harness 驱动的 MCP 工具链（数据→视觉→规则→设备）

## 🤝 贡献

欢迎 PR。规则：(1) star 数必须是 PR 时实查——不收体感数据；(2) 一句话说清"是什么"而非营销话术；(3) 弃坑项目会被移除。

## 许可证

[MIT](LICENSE) © [Easin](https://github.com/bayshier)
