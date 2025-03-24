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
```

Verify:

```bash
python --version
```

---

### 2. Install Git

```bash
brew install git
```

---

### 3. Clone the Forge Repository

```bash
git clone https://github.com/lllyasviel/stable-diffusion-webui-forge.git
cd stable-diffusion-webui-forge
```

---

### 4. Set Up a Virtual Environment (optional)

```bash
python -m venv venv
source venv/bin/activate
```

---

### 5. Install Dependencies and Launch

```bash
python launch.py --skip-torch-cuda-test --no-half
```

- `--skip-torch-cuda-test`: Skips CUDA tests, not needed on macOS
- `--no-half`: Disables FP16 mode (not well supported on M1/M2)

---

### 6. Download a Model (e.g., SD 1.5)

Place a model file into the `models/Stable-diffusion/` folder.

Example (via `curl`):

```bash
curl -L -o models/Stable-diffusion/v1-5-pruned.safetensors \
https://civitai.com/api/download/models/11145
```

Or download a `.ckpt`/`.safetensors` file from [Hugging Face](https://huggingface.co/) or [Civitai](https://civitai.com/).

---

### 7. Run the Web UI

```bash
python launch.py --skip-torch-cuda-test --no-half --listen
```

Then open your browser at:

```
http://localhost:7860
```

---

### ⚙️ Apple Silicon (M1/M2) Users

Forge will automatically use **MPS** (Metal Performance Shaders) if you're on Apple Silicon.

If needed, manually reinstall PyTorch with MPS support:

```bash
pip install torch torchvision torchaudio
```

---

### 🧠 Tips

- To use **SDXL**, download SDXL base and refiner models and place them in `models/Stable-diffusion/`
- Customize the UI using Forge’s config files or web settings
- Explore extensions and LoRA models for enhanced generation

---

Happy generating! 🖼️✨
