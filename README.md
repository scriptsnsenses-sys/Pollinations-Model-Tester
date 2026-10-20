# 🧪 Pollinations Models Tester

A single-file, browser-based playground for testing [Pollinations](https://pollinations.ai) text models side-by-side. Enter one or more model IDs, connect your Pollinations account, and instantly compare latency, capabilities, pricing, and live responses.

> ⚠️ **Running a test consumes pollen from your Pollinations balance.** Each click of **Test Model** sends a real chat-completion request.

---

## ✨ Features

- **Multi-model comparison** — add as many cards as you want and test models in parallel.
- **Live model resolution** — pulls the public model registry from `gen.pollinations.ai/v1/models` for accurate metadata.
- **Graceful handling of unknown models** — unregistered IDs (e.g. `community/.../custom-model`) still go through to the API; metadata fields just show *Unknown*.
- **Rich per-model details** shown after each test:
  - ⏱️ **Time** — end-to-end latency in seconds and milliseconds
  - 🧠 **Reasoning** — Yes / No
  - 📏 **Context** — context window (when reported by the publisher)
  - 🏢 **Publisher** — the org that owns the model
  - 🗂️ **Type** — text / image / video / 3D / audio
  - 💰 **Price** — pollen cost per token (prompt or completion, whichever is published)
  - 💬 **Response** — the raw model reply, plus `reasoning_content` when present
- **BYOP (Bring Your Own Pollen)** — connect via Pollinations' official OAuth redirect flow.
- **Manual key fallback** — paste a `pk_…` or `sk_…` key if redirects aren't available.
- **Session persistence** — the key lives in `sessionStorage`, so it survives a reload but clears when the tab closes.
- **Glassmorphism UI** with blue glow accents, ambient floating orbs, and smooth animations.
- **Zero build step** — one HTML file, no dependencies, no bundler.

[![Made with pollinations.ai](https://raw.githubusercontent.com/pollinations/pollinations/main/packages/ui/src/brand/badge-made-with.svg)](https://pollinations.ai/?ref=badge)
