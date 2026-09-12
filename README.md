# 🐾 Snack4Pets — French UGC Text-To-Speech (F5-TTS French)

Colab notebook for high-converting French UGC voice generation using **F5-TTS** paired with the community-trained French weights from [F5-TTS Issue #434](https://github.com/SWivid/F5-TTS/issues/434) ([`RASPIAUDIO/F5-French-MixedSpeakers-reduced`](https://huggingface.co/RASPIAUDIO/F5-French-MixedSpeakers-reduced)).

- **Model:** F5-TTS (Flow-Matching Diffusion Transformer).
- **French Vocabulary & Weights:** Dedicated French tokenizer and weights trained on 120k French multi-speaker samples.
- **Natural UGC Voiceover:** Preserves natural breath pauses, fast cadence, and authentic French pronunciation.
- **Reference Voice Included:** Auto-loads your dog chew demonstration voice sample (`reference_voices/tao_chew_sample.wav`).

---

## 🚀 Quick Link

| Notebook | Purpose | Link |
|---|---|---|
| **French UGC Voice Generation** | F5-TTS French community checkpoint with zero-shot cloning. | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mohaidoss/snack4pets-ugc-tts/blob/main/02_snack4pets_voice_generation.ipynb) |

---

## 🛠️ How It Works in Colab

1. Open **[02_snack4pets_voice_generation.ipynb](https://colab.research.google.com/github/mohaidoss/snack4pets-ugc-tts/blob/main/02_snack4pets_voice_generation.ipynb)**.
2. Ensure GPU is active (`Runtime -> Change runtime type -> T4 GPU`).
3. Click **Runtime -> Run all**.
   - Installs F5-TTS cleanly from git.
   - Downloads `model_last_reduced.pt` and `vocab.txt` from Hugging Face.
   - Generates the Snack4Pets French ad script in Tao's owner's voice at `speed=1.12`.
