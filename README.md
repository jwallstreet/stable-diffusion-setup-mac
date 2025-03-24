# stable-diffusion-setup-mac

# Stable Diffusion Forge on macOS

## ✨ What is Stable Diffusion?

[Stable Diffusion](https://stability.ai/stable-diffusion) is a deep learning text-to-image model released by Stability AI. It generates photorealistic images based on text prompts using a process called **latent diffusion**.

### 🔥 Perks of Stable Diffusion:

- **High-quality images** from text prompts
- **Runs locally** – no internet or cloud APIs needed
- **Fully open source**
- **Highly customizable** with community-made models, extensions, and fine-tuning
- **Fast and optimized** when using forks like Forge or Automatic1111

---

## 🚀 Installing Stable Diffusion Forge on macOS

This guide walks you through setting up **Stable Diffusion Forge** on macOS, a fast and feature-rich fork of the Automatic1111 web UI.

### ✅ Requirements

- macOS 12+ (Monterey or later)
- Python 3.10.x
- Git
- (Optional but recommended) Miniconda or pyenv

---

### 1. Install Python 3.10

Using `pyenv`:

```bash
brew install pyenv
pyenv install 3.10.13
pyenv global 3.10.13
