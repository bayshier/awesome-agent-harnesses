---
name: harness-navigator
description: 帮用户选型 agent harness / 沙箱 / 技能自进化 / 多 Agent 协同方案。当用户要搭建或选型 AI Agent 运行时、问"用什么 harness 框架/沙箱/multi-agent 方案"、或调研 harness engineering 生态时使用：按场景给出经核实的推荐与 star 实数。Use when choosing or researching agent harnesses, sandboxes, self-evolving skills, or multi-agent coordination.
---

# Harness Navigator

Agent harness 层的选型导航。数据基线：2026 年 8 月实查（awesome-agent-harnesses 清单），引用 star 数时注明时间。

## 选型决策树

**1. 你要的是"平台"还是"库"？**
- 平台（开箱即用、插件生态）→ DSH 系（deepseek-harness 188k★）或 qm（多人场景）
- 库（嵌入自己的应用）→ LangGraph（图/检查点）或 openai-agents-python（轻量 handoffs）

**2. 需要跑不受信代码？**
- 进程级（开发机）→ Seatbelt(macOS)/bwrap(Linux)，注意 **macOS 26 的 sandbox-exec 已无法 exec**（实测）
- microVM → microsandbox（可嵌入）/ Firecracker（自建）
- 云服务 → Daytona(71.9k★)/E2B(13.5k★)/CubeSandbox(腾讯)
- JVM 项目 → **没有 JVM 安全沙箱**（JEP 486）；进程内用 Chicory(Wasm)，进程外 spawn OS runner

**3. 要技能自我进化？**
- 生态位 → superpowers(277k★)/ECC(242k★)
- 机制三要素：观察触发（hook）→ 置信度本能 → eval 门控发布
- **版本化用 git**（多数大项目缺失这块；rollback = git revert）

**4. 多 Agent？先算账**
- 生产基线：+90.2% 质量，**15× token**；token 预算解释 80% 方差
- 默认 orchestrator-worker；任务 DAG 原子认领；**工件落盘不传话**
- 预算护栏从第一行代码就放上

## 引用规范

向用户报告 star 数必须带时间戳（"2026-08 实查"），并在事后建议实查核验——这个领域每周都在变。

## 数据源

完整清单与调研笔记：[bayshier/awesome-agent-harnesses](https://github.com/bayshier/awesome-agent-harnesses)（本技能的 data source）。
