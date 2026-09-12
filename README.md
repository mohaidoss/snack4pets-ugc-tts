# 🐾 Snack4Pets — French UGC Text-To-Speech

Production-ready **Google Colab notebooks** designed to generate natural, energetic French UGC (TikTok, Instagram Reels, Shorts) voiceovers for **Snack4Pets**.

Powered by **XTTS-v2** with explicit French phonetic modeling (`language="fr"`), eliminating English accent bleeding while cloning the authentic vocal timbre and tempo of your UGC video.

---

## 🎙️ Pre-Packaged French UGC Reference Voice

Extracted directly from your real pet UGC video:
* **Reference Audio:** `reference_voices/tao_chew_sample.wav` (9.2 seconds, 24kHz mono)
* **Hook Reference:** `reference_voices/tao_hook_sample.wav` (5.2 seconds)

---

## 🚀 Quick Links (Open Directly in Colab)

| Notebook | Purpose | Link |
|---|---|---|
| **02. French Voice Generation** | Zero-shot French voice cloning with native `fr` language model. | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mohaidoss/snack4pets-ugc-tts/blob/main/02_snack4pets_voice_generation.ipynb) |
| **01. Voice Fitting (Fine-Tuning)** | Adapt base checkpoint to a permanent creator persona on Google Drive. | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mohaidoss/snack4pets-ugc-tts/blob/main/01_snack4pets_voice_fitting.ipynb) |

---

## 🛠️ Usage in Colab

1. Open **[02_snack4pets_voice_generation.ipynb](https://colab.research.google.com/github/mohaidoss/snack4pets-ugc-tts/blob/main/02_snack4pets_voice_generation.ipynb)**.
2. Select **Runtime -> Change runtime type -> T4 GPU**.
3. Run all cells:
   ```python
   tts.tts_to_file(
       text=ad_script,
       speaker_wav="/content/snack4pets-ugc-tts/reference_voices/tao_chew_sample.wav",
       language="fr",
       speed=1.12,
       file_path="snack4pets_ad_fr.wav"
   )
   ```
4. Output is generated in native French with the voice identity from your reference video.
