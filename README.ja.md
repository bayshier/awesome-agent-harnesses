<div align="center">

**エージェント・ハーネス層の厳選マップ：プラットフォーム、サンドボックス、自己進化スキル、マルチエージェント連携。**

[![Entries](https://img.shields.io/badge/項目-60+-blueviolet?style=flat-square)](README.ja.md)
[![License: MIT](https://img.shields.io/badge/License-MIT-3DDC84?style=flat-square)](LICENSE)

[English](README.md) | [简体中文](README.zh-CN.md) | **日本語**

</div>

---

> **ハーネスとは？** インポートするフレームワークではなく、一つのモデルループを囲む**本番ランタイム製品**——モデルをツール・権限・環境に接続する層（OpenAI、2026年2月）。

## 📖 主要文献

- [Harness Engineering: Leveraging Codex in an Agent-First World](https://openai.com/index/harness-engineering/) — OpenAI、2026年2月。用語の原典。
- [Effective Harnesses for Long-Running Agents](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents) — Anthropic、2025年11月。
- [Harness Engineering for Self-Improvement](https://lilianweng.github.io/) — Lilian Weng、2026年7月。
- [Why Software Factories Fail](https://github.com/humanlayer/advanced-context-engineering-for-coding-agents) — HumanLayer。必要な反論。

## ⚙️ プラットフォーム

| リポジトリ | スター | 概要 |
|---|---|---|
| [deepseek-harness](https://github.com/deepseek-ai/deepseek-harness) | 188k★ | 「すべてはプラグイン」 |
| [ECC](https://github.com/affaan-m/ECC) | 242k★ | ハーネス性能最適化 |
| [LangGraph](https://github.com/langchain-ai/langgraph) | 40.3k★ | グラフ/チェックポイント |
| [openai-agents-python](https://github.com/openai/openai-agents-python) | 28.9k★ | swarm の後継 |

## 🏰 サンドボックス

| リポジトリ | スター | 概要 |
|---|---|---|
| [daytona](https://github.com/daytonaio/daytona) | 71.9k★ | AI生成コード用インフラ |
| [firecracker](https://github.com/firecracker-microvm/firecracker) | 36.2k★ | microVM 基盤 |
| [gVisor](https://github.com/google/gvisor) | 19.1k★ | システムコール遮断 |
| [E2B](https://github.com/e2b-dev/E2B) | 13.5k★ | コード実行 SDK の標準 |
| [microsandbox](https://github.com/superradcompany/microsandbox) | 7.9k★ | 組み込み microVM |

## 🧬 スキルと自己進化

- [superpowers](https://github.com/obra/superpowers) — 277k★ — 「スキル執筆 = プロセス文書への TDD」
- [autoresearch](https://github.com/karpathy/autoresearch) — 94.6k★ — スキル即ファイルループ（MCE）
- [seed](https://github.com/vivekhaldar/seed) — 91★ — git でバージョン管理された自己書き換え

## 🐜 マルチエージェント

Anthropic 本番データ：**+90.2%、ただし 15× トークン**。トークン予算が結果分散の 80% を説明。

## 🛠️ リファレンス実装

- [bayshier/harness-engineering](https://github.com/bayshier/harness-engineering) — **Kotlin** による 5 コンポーネント参照実装。

## ライセンス

[MIT](LICENSE) © [Easin](https://github.com/bayshier)
