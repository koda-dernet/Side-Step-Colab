# Side-Step — Google Colab Edition

```
 ░▒▓███████▓▒░▒▓█▓▒░▒▓███████▓▒░░▒▓████████▓▒░░▒▓███████▓▒░▒▓████████▓▒░▒▓████████▓▒░▒▓███████▓▒░ 
░▒▓█▓▒░      ░▒▓█▓▒░▒▓█▓▒░░▒▓█▓▒░▒▓█▓▒░      ░▒▓█▓▒░         ░▒▓█▓▒░   ░▒▓█▓▒░      ░▒▓█▓▒░░▒▓█▓▒░
░▒▓█▓▒░      ░▒▓█▓▒░▒▓█▓▒░░▒▓█▓▒░▒▓█▓▒░      ░▒▓█▓▒░         ░▒▓█▓▒░   ░▒▓█▓▒░      ░▒▓█▓▒░░▒▓█▓▒░
 ░▒▓██████▓▒░░▒▓█▓▒░▒▓█▓▒░░▒▓█▓▒░▒▓██████▓▒░  ░▒▓██████▓▒░   ░▒▓█▓▒░   ░▒▓██████▓▒░ ░▒▓███████▓▒░ 
       ░▒▓█▓▒░▒▓█▓▒░▒▓█▓▒░░▒▓█▓▒░▒▓█▓▒░             ░▒▓█▓▒░  ░▒▓█▓▒░   ░▒▓█▓▒░      ░▒▓█▓▒░       
       ░▒▓█▓▒░▒▓█▓▒░▒▓█▓▒░░▒▓█▓▒░▒▓█▓▒░             ░▒▓█▓▒░  ░▒▓█▓▒░   ░▒▓█▓▒░      ░▒▓█▓▒░       
░▒▓███████▓▒░░▒▓█▓▒░▒▓███████▓▒░░▒▓████████▓▒░▒▓███████▓▒░   ░▒▓█▓▒░   ░▒▓████████▓▒░▒▓█▓▒░       
 by dernet -- BETA
```

Fine-tune music LoRAs with [Side-Step](https://github.com/koda-dernet/Side-Step) directly in Google Colab — no local GPU required.

---

## Notebooks

### Full Suite — `Side_Step_Colab.ipynb`

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/koda-dernet/Side-Step-Colab/blob/main/Side_Step_Colab.ipynb)

The complete Side-Step pipeline: captions, audio analysis, preprocessing, PP++, training, export, and history.

| Section | | Description |
|---------|--|-------------|
| S0 GPU Check | `[REQUIRED]` | Verify GPU runtime |
| S1 Install & Mount | `[REQUIRED]` | Clone Side-Step, mount Google Drive |
| S2 Model Downloads | `[REQUIRED]` | Download ACE-Step checkpoints to Drive |
| S3 Settings | `[OPTIONAL]` | API keys (Gemini, OpenAI, Genius, Music Flamingo) |
| S4 Dataset Prep | `[OPTIONAL]` | Audio scan, AI captions, sidecar tags, dataset build |
| S5 Audio Analysis | `[OPTIONAL]` | BPM, key, time signature extraction |
| S6 Preprocessing | `[REQUIRED]` | Two-pass audio-to-tensor pipeline (VAE + DIT) |
| S7 PP++ Analysis | `[OPTIONAL]` | Adaptive per-module rank assignment |
| S8 Training | `[REQUIRED]` | Train LoRA / DoRA / LoKR / LoHA / OFT adapters |
| S9 Export | `[OPTIONAL]` | ComfyUI `.safetensors` export |
| S10 History | `[OPTIONAL]` | View past training runs |

### Training Only — `Side_Step_Train.ipynb`

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/koda-dernet/Side-Step-Colab/blob/main/Side_Step_Train.ipynb)

Slim notebook for users who already have audio files with sidecars and just want to preprocess + train.

| Section | Description |
|---------|-------------|
| S0 GPU Check | Verify GPU runtime |
| S1 Install & Mount | Clone Side-Step, mount Drive |
| S2 Model Downloads | Download ACE-Step checkpoints |
| S3 Preprocessing | Audio to .pt tensors |
| S4 PP++ Analysis | Adaptive ranks *(optional)* |
| S5 Training | Train adapter + TensorBoard |

## Quick Start

1. Click the **Open in Colab** badge for the notebook you want
2. Set runtime to **GPU** (Runtime > Change runtime type > T4/A100/L4)
3. Run cells top-to-bottom

## Requirements

- Google account (for Colab + Drive)
- GPU runtime (T4 minimum, A100 recommended)
- Audio files to train on

Everything else (Side-Step, dependencies, model weights) is installed and downloaded automatically inside the notebook.

## License

Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0).
See [LICENSE](LICENSE) for full text.
