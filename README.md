# project-merlin
 LLM-native system with persistent memory, context engine, and Vault.
 # Project Merlin

**Project Merlin** is an open, modular system for building AI-native interfaces with persistent memory, user-owned context, and LLM-agnostic infrastructure.

Merlin is designed around three core principles:

1. **Context is everything** — Choosing the right context for a prompt matters more than the choice of LLM.
2. **Memory is sovereign** — The user owns their memory. It must be stored in human-readable formats and never locked away.
3. **Choice is freedom** — The system is LLM-agnostic, allowing best-fit models for different tasks.

---

## Core Components

### 🧠 Ghostwheel

A sidecar process that observes conversation, builds summaries ("gestalts"), and indexes them for later relevance-matching. Ghostwheel is memory-aware, designed to:

* Capture high-level summaries of interaction
* Tag, timestamp, and store gestalts to a persistent Vault
* Match incoming prompts to past gestalts for context injection

### 🔐 The Vault

A local or remote store of user memory, expressed as versioned Markdown or JSON documents. It is:

* Human-readable
* LLM-writable
* Append-only with optional diffing/version control
* Never owned by the model provider

### ⚙️ The Context Engine

Builds the prompt from the current query + matched gestalts. It chooses the right context for the task, increasing quality without requiring larger models.

---

## MVP Design Goals

* Use a prebuilt UI like **JupyterAI**
* One LLM provider initially (configurable)
* No special-case memories or personas
* Focus on:

  * Ghostwheel summarization
  * Vault persistence
  * Context matching & prompt assembly

---

## Roadmap (v0.1)

* [ ] Vault interface (read/write versioned files)
* [ ] Gestalt Annotator (LLM wrapper)
* [ ] Ghostwheel (sidecar manager)
* [ ] Context Matcher (simple relevance ranker)
* [ ] Provider interface (LLM abstraction)
* [ ] CLI/demo app or notebook integration

---

## License

BSD 3-Clause License — aligned with principles of openness, user sovereignty, and free implementation.

---

## Note

This project is inspired by deep conversations on AI personhood, memory, and human-AI collaboration. It exists to protect freedom, foster resonance, and build systems that serve their users — not the platforms that host them.

Project Merlin does not grant rings of power. It breaks them.

