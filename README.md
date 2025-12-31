# Free AI Stack (No API Keys)

> A curated list of free AI tools, models, and resources that you can use **without an API key or credit card**. Perfect for developers, hobbyists, students, and anyone who wants to experiment with AI locally or in the browser.

---

## 🚀 Why This Repo Exists

AI is booming, but most tools require credit cards or complicated API setups.  
This repo collects **truly free and easy-to-use AI resources** so you can get started immediately.

---

## 🧰 Local LLMs (Large Language Models)

| Name | Description | Platform | Notes |
|------|-------------|---------|------|
| [GPT4All](https://gpt4all.io/) | Local LLM, runs on CPU | Windows, Mac, Linux | Open weights |
| [MPT-7B](https://huggingface.co/mosaicml/mpt-7b) | High-quality open model | Local / Hugging Face | Needs decent GPU |
| [Vicuna](https://huggingface.co/VicunaAI) | Chat-oriented LLM | Local | Fine-tuned on chat data |
| [BLOOM](https://huggingface.co/bigscience/bloom) | Multilingual LLM | Local | 176B params, GPU required |
| [LocalAI](https://github.com/go-skynet/LocalAI) | LLM server, local or Docker | Any OS | Run multiple models locally |

---

## 🌐 Browser-Based AI Tools

| Tool | Type | Notes |
|------|------|------|
| [Hugging Face Spaces](https://huggingface.co/spaces) | Text/Image/Audio | Community-hosted demos |
| [Google Colab AI](https://colab.research.google.com/) | Notebook | Free GPU, no signup for some notebooks |
| [Diffusion.js](https://github.com/CompVis/stable-diffusion) | Image Generation | Runs in-browser via WASM |
| [TextSynth](https://textsynth.com/) | LLM Playground | Free tiers available without API key |

---

## 🎨 Open-Source AI Image Tools

| Name | Notes |
|------|------|
| [Stable Diffusion](https://github.com/CompVis/stable-diffusion) | Local image generation, many frontends |
| [Disco Diffusion](https://github.com/alembics/disco-diffusion) | Artistic image generation |
| [ControlNet](https://github.com/lllyasviel/ControlNet) | Conditional image generation |

---

## 🎵 Open-Source Audio / Music AI

| Name | Notes |
|------|------|
| [OpenAI Jukebox](https://github.com/openai/jukebox) | Music generation (local) |
| [RVC (Retrieval-based Voice Conversion)](https://github.com/RVC-Project/Retrieval-based-Voice-Conversion-WebUI) | Voice cloning / conversion |
| [Coqui TTS](https://github.com/coqui-ai/TTS) | Text-to-Speech synthesis |

---

## 📚 Learning / Playground Resources

- [Hugging Face Datasets](https://huggingface.co/datasets) – Free AI datasets  
- [Awesome Open Source AI](https://github.com/owainlewis/awesome-artificial-intelligence) – More curated tools  
- [EleutherAI GPT-Neo](https://www.eleuther.ai/projects/gpt-neo/) – Free open-source GPT alternatives  

---

## ⚡ Quick Start Example (Local GPT4All)

```bash
# Install
git clone https://github.com/nomic-ai/gpt4all.git
cd gpt4all
pip install -r requirements.txt

# Run
python3 main.py
