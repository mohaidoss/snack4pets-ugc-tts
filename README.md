# 🐾 Snack4Pets — French UGC Text-To-Speech (F5-TTS)

Repository with ready-to-run **Google Colab notebooks** designed to generate and fit natural, energetic French UGC (TikTok, Reels, Shorts) voiceovers for **Snack4Pets**.

Powered by [F5-TTS](https://github.com/SWivid/F5-TTS) (Flow-Matching Diffusion Transformer), which outperforms legacy autoregressive and classical acoustic TTS models on cadence, breathing pauses, and natural speech rhythm.

---

## 🎙️ Pre-Packaged French UGC Reference Voice

A real UGC sample extracted from your video is included directly in this repo:
* **Audio file:** `reference_voices/tao_chew_sample.wav` (9.2 seconds, 24kHz mono)
* **Transcript:**
  > *"Tao a mis presque 16 minutes pour la finir. C'est une mastication qui dure entre 10 et 20 minutes en fonction des chiens. Elle fait partie de la catégorie moyenne durée."*
* **Alternative hook file:** `reference_voices/tao_hook_sample.wav` (5.2 seconds)
  > *"Tu t'es déjà demandé combien de temps dure une oreille de veau ? Tao va nous faire la démonstration."*

You can directly load these in Google Colab without uploading anything!

---

## 🚀 Quick Links (Open Directly in Colab)

| Notebook | Purpose | Link |
|---|---|---|
| **01. Voice Fitting (Fine-Tuning)** | Adapt F5-TTS to a specific creator's voice from 3–10 min of French audio. | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mohaidoss/snack4pets-ugc-tts/blob/main/01_snack4pets_voice_fitting.ipynb) |
| **02. Voice Generation** | Zero-shot voice cloning (5s sample) or inference with your fitted checkpoint. | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mohaidoss/snack4pets-ugc-tts/blob/main/02_snack4pets_voice_generation.ipynb) |

---

## 📋 Hardware Requirements

* **Google Colab:** Standard **T4 GPU** (available on free and Pro tiers).
* Ensure your runtime is configured to GPU: `Runtime` ➔ `Change runtime type` ➔ `T4 GPU`.

---

## 🛠️ Notebook 1: Voice Fitting (`01_snack4pets_voice_fitting.ipynb`)

Use this when you want a signature Snack4Pets creator voice that stays 100% consistent across dozens of video ads.

### Dataset Preparation
1. Collect **3 to 10 minutes** of casual, energetic French speech from a single speaker (e.g. phone recordings, voice memos, clean TikTok voice tracks).
2. Avoid heavy background music, loud sirens, or clipping. Natural background room acoustic is fine and actually improves UGC realism.
3. Upload the `.wav` or `.mp3` files into the Colab environment under `/content/raw_audio`.

### Workflow
* **Automatic Whisper Transcription:** The notebook includes a script that normalizes audio to 24 kHz mono and generates the required pipe-delimited `metadata.csv` automatically in French.
* **Gradio WebUI (Option A):** Alternatively, launch the built-in Gradio trainer to inspect clips and adjust transcriptions manually before launching training.
* **Google Drive Archival:** Checkpoints (`.safetensors`) are automatically synchronized to your Google Drive (`/MyDrive/snack4pets_tts_checkpoints`).

---

## 🎙️ Notebook 2: Voice Generation (`02_snack4pets_voice_generation.ipynb`)

Generate production-ready ad voiceovers in seconds.

### Modes
1. **Zero-Shot Mode (No fine-tuning needed):**
   * Upload a single 5 to 10-second audio clip of someone speaking casual French.
   * Provide the transcript of that clip.
   * Enter your Snack4Pets ad copy. F5-TTS matches the voice timbre, speaking tempo, and informal cadence immediately.
2. **Fitted Mode (Using your checkpoint):**
   * Specify the path to your fine-tuned `.safetensors` model stored on Google Drive.
   * Guarantees identical voice identity across every batch of ad creatives.

### Best Practices for French UGC Scripts:
* **Colloquial Punctuation:** Use commas `,`, exclamation marks `!`, and ellipses `...` to force natural pauses, rhythm breaks, and breath timing.
* **Pacing/Speed:** In UGC ads, standard TTS can feel too slow. Set the `speed` parameter to **`1.10` – `1.15`** for high-energy social hooks.
* **Script Tone:** Write in spoken French (*"J'en pouvais plus..."*, *"Franchement..."*, *"Regardez son kiff..."*) rather than formal written French to match UGC visual framing.

---

## 📂 Repository Structure

```
snack4pets-ugc-tts/
├── 01_snack4pets_voice_fitting.ipynb       # Colab notebook for fine-tuning
├── 02_snack4pets_voice_generation.ipynb    # Colab notebook for inference / zero-shot
└── README.md                               # Setup and operational instructions
```
