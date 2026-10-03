# Where is What? A Comprehensive Layer-wise Analysis of Content, Speaker, and Prosody in Speech SSL Models

[![Paper](https://img.shields.io/badge/Paper-Under_Review-orange.svg)]()
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0%2B-ee4c2c.svg)](https://pytorch.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> Official PyTorch repository for the layer-wise diagnostic probing, disentanglement metric formulation, and feature analysis across state-of-the-art Speech Foundation & SSL models.

---

## 📌 Overview

This repository provides the complete framework to analyze the hierarchical representation geometry of speech SSL models:
- **Phonetic Content Retention** (Frame-level linear classification)
- **Speaker Biometrics & Verification** (Utterance-level mean/std pooling & cosine EER)
- **Hierarchical Prosody Decoding** (Frame-level F0, RMS energy, and duration regression)
- **Disentanglement Formulations** ($\Delta L$, $\mathrm{CDI}$, $\mathrm{SDI}$, and $\mathrm{JDC}$)

---

## ⚙️ Model Setup & Checkpoints

Before running the diagnostic probing pipelines, ensure the pre-trained checkpoints are downloaded into the designated directory:
```bash
mkdir -p pretrained_models


Place the respective HuggingFace / Fairseq checkpoints into ./pretrained_models/:


Architecture	Model Key	Model Identifier / Path
WavLM-Base+	"wavlm-base-plus"	microsoft/wavlm-base-plus
HuBERT-Base	"hubert-base"	facebook/hubert-base-ls960
Wav2Vec2-Base	"wav2vec2-base"	facebook/wav2vec2-base
Data2Vec-Audio	"data2vec-audio-base-960h"	facebook/data2vec-audio-base-960h
Whisper-Small (Enc)	"whisper-small"	openai/whisper-small
