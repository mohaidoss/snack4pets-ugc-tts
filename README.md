# 🐾 Snack4Pets — French UGC Text-To-Speech (Kokoro ONNX)

Ultra-lightweight, zero-dependency French TTS notebook for **Snack4Pets**.

- **Zero Dependency Hell:** Built on **Kokoro ONNX** (`kokoro-onnx` + `soundfile`).
- **No PyTorch / CUDA version mismatch:** Runs instantly out of the box in 5 seconds on Colab.
- **Native French Support:** Configured with `lang="fr-fr"` and the `ff_siwis` voice.
- **UGC Pacing:** Tuned to `speed=1.15` for fast, punchy TikTok and Reels ad delivery.

---

## 🚀 Quick Link

| Notebook | Purpose | Link |
|---|---|---|
| **French Voice Generation** | Fast, hassle-free French audio generation. | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mohaidoss/snack4pets-ugc-tts/blob/main/02_snack4pets_voice_generation.ipynb) |

---

## 🛠️ Usage

1. Open **[02_snack4pets_voice_generation.ipynb](https://colab.research.google.com/github/mohaidoss/snack4pets-ugc-tts/blob/main/02_snack4pets_voice_generation.ipynb)** in Google Colab.
2. Run all cells:
   ```python
   !pip install -q kokoro-onnx soundfile
   ```
3. Type your French copy and listen to the audio output directly in your browser.
