# STACK_OVERVIEW — Free AI Stack (No API, No Credit Card)

This document explains the **mental model, layers, and design philosophy** of a fully free AI stack that runs **locally or in the browser**, without API keys, accounts, or billing.

Use this to:
- Understand what tools exist
- Choose the right layer for your use case
- Avoid unnecessary complexity or paid services

---

## Core Philosophy

**Local-first > Offline-capable > Free forever**

Principles:
- No external inference APIs
- No paywalls, quotas, or accounts
- Models run on *your* hardware
- Privacy by default
- Simple over clever

If it requires a credit card, API key, or forced signup — it does not belong here.

---

## The Stack at a Glance

┌───────────────────────────────┐
│        Your Application       │
│   (CLI / Desktop / Web App)   │
└───────────────▲───────────────┘
│
┌───────────────┴───────────────┐
│     Frameworks / Glue Code    │
│  (LangChain-local, scripts)  │
└───────────────▲───────────────┘
│
┌───────────────┴───────────────┐
│     Model Runtimes / Engines  │
│ (Ollama, llama.cpp, WebLLM)  │
└───────────────▲───────────────┘
│
┌───────────────┴───────────────┐
│        Models (Weights)       │
│   (LLMs, Vision, Audio)      │
└───────────────▲───────────────┘
│
┌───────────────┴───────────────┐
│         Your Hardware         │
│   CPU / GPU / Apple Silicon  │
└───────────────────────────────┘

Each layer is swappable and independent.

---

## Layer 1 — Hardware

Your constraints define everything above.

### Common Setups

| Hardware | What Works |
|------|------|
| 8GB RAM | 7B models (Q4) |
| 16GB RAM | 7B–13B models |
| Apple Silicon | Excellent performance |
| CPU-only | Slower but viable |
| GPU | Faster inference |

You do **not** need a GPU to use this stack.

---

## Layer 2 — Models (Weights)

These are the actual neural networks.

### Categories

- **Text / LLMs**
  - Llama, Mistral, Qwen, DeepSeek
- **Embeddings**
  - BGE, MiniLM
- **Vision**
  - Stable Diffusion, SDXL
- **Audio**
  - Whisper, Bark, Coqui, XTTS
- **Multimodal**
  - LLaVA, Qwen-VL

Key properties:
- Open or permissive licenses
- Download once, run offline
- Quantized formats (GGUF) for consumer hardware

---

## Layer 3 — Model Runtimes

Runtimes load and execute models efficiently.

### Popular Runtimes

| Runtime | Best For |
|------|------|
| **Ollama** | Simplicity, automation |
| **LM Studio** | GUI, beginners |
| **llama.cpp** | Maximum control |
| **TextGen WebUI** | Power users |
| **WebLLM** | Browser-based AI |

Runtimes expose:
- CLI
- Local HTTP APIs
- GUI interfaces

No authentication required.

---

## Layer 4 — Frameworks & Glue

Optional but useful for building systems.

### Examples

- Local LangChain (no cloud calls)
- Custom Python / Node scripts
- Cron + shell scripts
- SQLite + FAISS for RAG

Rule:
> If a framework defaults to a cloud API, disable it or avoid it.

Simple scripts often outperform heavy frameworks.

---

## Layer 5 — Applications

What you actually build.

### Common App Types

- CLI tools
- Desktop apps
- Local web apps
- Browser-only apps
- Automation scripts

Examples:
- Offline coding assistant
- Local knowledge base (RAG)
- AI-powered notes
- Private chatbot
- Content generator

---

## Browser AI vs Local AI

### Browser AI

Pros:
- Zero install
- Deploy on static hosting
- No backend

Cons:
- Smaller models
- Hardware-dependent

Tech:
- WebGPU
- WASM
- transformers.js

---

### Local AI

Pros:
- Larger models
- More control
- Faster on good hardware

Cons:
- Requires install
- Uses disk + RAM

Tech:
- Ollama
- llama.cpp
- PyTorch

---

## Choosing the Right Path

### Use Browser AI if:
- You want zero install
- You are building demos
- You target non-technical users

### Use Local AI if:
- You want power
- You want privacy
- You need automation or RAG

---

## What This Stack Avoids (Intentionally)

- Cloud inference APIs
- Token-based billing
- Vendor lock-in
- Rate limits
- Usage tracking

This is **anti-fragile** by design.

---

## Typical Architectures

### Minimal
