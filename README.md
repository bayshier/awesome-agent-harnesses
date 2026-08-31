<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=3DDC84&height=120&section=header&text=Awesome%20Agent%20Harnesses&fontSize=42&fontColor=ffffff" width="100%"/>

**The curated map of the agent-harness layer: platforms, sandboxes, self-evolving skills, and multi-agent coordination.**

[![Entries](https://img.shields.io/badge/Entries-60+-blueviolet?style=flat-square)](#--platforms)
[![Data](https://img.shields.io/badge/star%20counts-fetched%202026--08-3DDC84?style=flat-square)](docs/landscape.md)
[![License: MIT](https://img.shields.io/badge/License-MIT-3DDC84?style=flat-square)](LICENSE)
[![Sponsor](https://img.shields.io/badge/Sponsor-GitHub%20Sponsors-ff69b4?style=flat-square)](https://github.com/sponsors/bayshier)

**English** | [简体中文](README.zh-CN.md) | [日本語](README.ja.md)

</div>

---

> **What is a harness?** Not a framework you import — the *production runtime product* around one model loop: the layer connecting the model to tools, permissions, and environment (OpenAI, Feb 2026). This list tracks that layer. Updated irregularly; stars welcome. Star counts fetched live August 2026 — see [landscape notes](docs/landscape.md).

## 📖 Canonical Reading

The five texts that define the discipline, in order:

- [Harness Engineering: Leveraging Codex in an Agent-First World](https://openai.com/index/harness-engineering/) — OpenAI (Ryan Lopopolo), Feb 2026. *The* coining post; harness as an OODA loop over events.
- [Effective Harnesses for Long-Running Agents](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents) — Anthropic, Nov 2025. Filesystem as external state, parallel subagents, structured tool outputs ("context rot"), hooks.
- [Harness Engineering for Self-Improvement](https://lilianweng.github.io/) — Lilian Weng, Jul 2026. The SE-Agent Router reference architecture; skills-as-files with measured gains.
- [Learn Harness Engineering](https://walkinglabs.github.io/) — walkinglabs, May 2026. Free open book.
- [Harness engineering for coding agent users](https://martinfowler.com/) — martinfowler.com, Apr 2026.
- [Why Software Factories Fail](https://github.com/humanlayer/advanced-context-engineering-for-coding-agents) — HumanLayer, Jul 2026 (2.5k★). **The necessary counterpoint**: harness engineering is not enough; you can't backprop incidents to decisions.
- [lopopolo/harness-engineering](https://github.com/lopopolo/harness-engineering) — 2.5k★ — the anthology/field guide companion to the OpenAI post.

## ⚙️ Platforms & Frameworks

- [deepseek-ai/deepseek-harness](https://github.com/deepseek-ai/deepseek-harness) — **188k★** — "Everything is a Plugin" (Node/Cordis). 186k stars in ten days; the platform whose plugin ecosystem spawned its own awesome lists.
- [affaan-m/ECC](https://github.com/affaan-m/ECC) — **242k★** — agent-harness performance optimization: skills, instincts, memory, continuous-learning-v2.
- [PrimeIntellect-ai/prime-agent](https://github.com/PrimeIntellect-ai/prime-agent) — 17.9k★ — self-improving RL agent.
- [xai-org/grok-build](https://github.com/xai-org/grok-build) — 25.9k★ — Rust coding-agent harness/TUI.
- [sandbaseai/sandbase-harness](https://github.com/sandbaseai/sandbase-harness) — 639★ — local-first, self-hosted runtime and MCP bridge with sandboxed sessions, memory, credentials, audit/replay, and a local Console.
- [yc-software/qm](https://github.com/yc-software/qm) — 14.1k★ — multiplayer harness: per-person/per-room scoped memory, files, keychain, permissions.
- [XiaomiMiMo/MiMo-Code](https://github.com/XiaomiMiMo/MiMo-Code) — 12.8k★
- [lidge-jun/opencodex](https://github.com/lidge-jun/opencodex) — 11.8k★ — universal provider proxy for Codex/Claude Code.
- [MoonshotAI/kimi-code](https://github.com/MoonshotAI/kimi-code) — 7.0k★
- [LangGraph](https://github.com/langchain-ai/langgraph) — 40.3k★ — graph/checkpointing niche ("resilient agents"); v1.x line.
- [openai/openai-agents-python](https://github.com/openai/openai-agents-python) — 28.9k★ — the production successor of swarm.
- [openai/swarm](https://github.com/openai/swarm) — 21.9k★ — educational, handoffs pattern; not production.

## 🤖 Coding Agents (harnesses in the wild)

- [openai/codex](https://github.com/openai/codex) — Rust terminal coding agent; its sandbox (Seatbelt/Landlock+seccomp) is a production reference.
- [anthropics/claude-code](https://github.com/anthropics/claude-code) — sandboxed Bash (Seatbelt/bwrap), subagents with tool allowlists, git-worktree isolation, hooks.
- [openai/codex-security](https://github.com/openai/codex-security) — 10.1k★ — security CLI for agents.
- [truefoundry/trueforge](https://github.com/truefoundry/trueforge) — 3.8k★
- [onecli](https://github.com/onecli) — 3.4k★ (YC S26) — sandboxed team harness.

## 🧬 Skills & Self-Improvement

- [obra/superpowers](https://github.com/obra/superpowers) — **277k★** — agentic skills framework; "writing-skills = TDD applied to process documentation".
- [mattpocock/skills](https://github.com/mattpocock/skills) — 234k★ — "Skills for Real Engineers", `.agents` directory.
- [multica-ai/andrej-karpathy-skills](https://github.com/multica-ai/andrej-karpathy-skills) — 205k★
- [karpathy/autoresearch](https://github.com/karpathy/autoresearch) — **94.6k★** — the MCE skills-as-files loop (agents write/merge/delete skills with measured downstream gains; strict pre-filtering *hurt* performance).
- [awesome-dsh-plugin/awesome-dsh-plugin](https://github.com/awesome-dsh-plugin/awesome-dsh-plugin) — 11.9k★ — the plugin registry layer of the DSH ecosystem.
- [anthropics/skills → skill-creator](https://github.com/anthropics/skills) — eval-gated self-editing loop: baseline vs with_skill, blind A/B via independent grader agents.
- [vivekhaldar/seed](https://github.com/vivekhaldar/seed) — 91★ — minimal self-modifying harness; **the only git-versioned self/** (rollback = git revert).
- [KKKKhazix/khazix-skills](https://github.com/KKKKhazix/khazix-skills) — 20k★ — personal-brand skill collection.

## 🏰 Sandboxes & Isolation

From light (process) to heavy (microVM, cloud):

- [daytonaio/daytona](https://github.com/daytonaio/daytona) — **71.9k★** — elastic infra for AI-generated code; the fastest-starred name in the space.
- [firecracker-microvm/firecracker](https://github.com/firecracker-microvm/firecracker) — 36.2k★ — the microVM substrate (E2B's cloud is built on it).
- [google/gvisor](https://github.com/google/gvisor) — 19.1k★ — application kernel / syscall interception.
- [opensandbox-group/OpenSandbox](https://github.com/opensandbox-group/OpenSandbox) — 14.6k★
- [e2b-dev/E2B](https://github.com/e2b-dev/E2B) — 13.5k★ — the default agent code-execution SDK.
- [TencentCloud/CubeSandbox](https://github.com/TencentCloud/CubeSandbox) — 11.3k★
- [superradcompany/microsandbox](https://github.com/superradcompany/microsandbox) — 7.9k★ — embeddable microVMs, <100ms boot, ships Agent Skills + MCP.
- [Tencent/AI-Infra-Guard](https://github.com/Tencent/AI-Infra-Guard) — 5.6k★ — red teaming incl. MCP scan.
- [dylibso/chicory](https://github.com/dylibso/chicory) — 1.1k★ — pure-Java Wasm runtime; the JVM-native play for untrusted in-process code.

> ⚠️ There is **no JVM security sandbox** (Security Manager died with JEP 486). JVM projects should spawn OS runners (Seatbelt/bwrap/Landlock) behind a `confine(argv, policy)` seam — see [landscape notes](docs/landscape.md) for the macOS-26 sandbox-exec obituary.

## 🐜 Multi-Agent Coordination

- Anthropic's multi-agent research system ([post](https://www.anthropic.com/engineering/built-multi-agent-research-system)) — orchestrator-worker in production: **+90.2% over single-agent, ~15× tokens; token budget explains 80% of outcome variance.**
- [NanmiCoder/dsh-agent-teams](https://github.com/NanmiCoder/dsh-agent-teams) — 920★ — captain-led teams, dependency-gated task DAG with atomic claiming, durable state, cold-restart.
- Claude Code subagents ([docs](https://code.claude.com/docs/en/sub-agents)) — tool allowlists, model routing per agent, worktree isolation, 3-layer depth, cap 20 concurrent.
- Named failure modes to design against: duplicate work from vague task specs; agents distracting each other; infinite searches; *50 subagents for a simple question*; the "telephone game" (fix: filesystem artifacts, not context).

## 🛠️ Reference Implementations

- [bayshier/harness-engineering](https://github.com/bayshier/harness-engineering) — **Kotlin** reference implementation of the five components (OODA loop + token budget, sandbox seam with fail-closed probe, git-versioned evolving skills, task DAG, honest boundaries). The only Kotlin-native entry on this list.
- [bayshier/kline-mcp](https://github.com/bayshier/kline-mcp) · [kline-vision](https://github.com/bayshier/kline-vision) · [t1-replay](https://github.com/bayshier/t1-replay) · [android-mcp](https://github.com/bayshier/android-mcp) — a working MCP tool-chain (data → vision → rules → devices) that a harness can drive.
- [bayshier/android-agent-skills](https://github.com/bayshier/android-agent-skills) — battle-tested Android/Kotlin agent skills.

## 🤝 Contributing

PRs welcome. Rules: (1) star counts must be real at PR time — no vibes; (2) one-line positioning that says *what it is*, not marketing; (3) dead/archived projects get removed. See [landscape notes](docs/landscape.md) for how this list's data was gathered.

## License

[MIT](LICENSE) © [Easin](https://github.com/bayshier)
