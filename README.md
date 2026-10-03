
markdown
# Where is What? A Comprehensive Layer-wise Analysis of Content, Speaker, and Prosody in Speech SSL Models

[![Python 3.9+](https://img.shields.io/badge/python-3.9%2B-blue.svg)](https://www.python.org/downloads/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0%2B-orange.svg)](https://pytorch.org/)
[![HuggingFace](https://img.shields.io/badge/%F0%9F%A4%97-Transformers-yellow.svg)](https://huggingface.co/transformers)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

This repository contains the official implementation, diagnostic probing benchmarks, and disentanglement evaluation scripts for the paper:

> **"Where is What? A Comprehensive Layer-wise Analysis of Content, Speaker, and Prosody in Speech SSL Models"**

---

## ⚙️ Model Setup & Checkpoints

Before running the diagnostic probing pipelines, ensure the pre-trained checkpoints are downloaded into the designated directory:
```bash
mkdir -p pretrained_models
📥 Pre-trained Models Configuration
The following models are utilized in this diagnostic study. Please ensure they are downloaded and placed in the ./pretrained_models/ directory:


Architecture	Model Key	HuggingFace Identifier / Path
WavLM-Base+	"wavlm-base-plus"	microsoft/wavlm-base-plus
HuBERT-Base	"hubert-base"	facebook/hubert-base-ls960
Wav2Vec2-Base	"wav2vec2-base"	facebook/wav2vec2-base
Data2Vec-Audio	"data2vec-audio-base-960h"	facebook/data2vec-audio-base-960h
Whisper-Small (Enc)	"whisper-small"	openai/whisper-small
Note: For Whisper, we specifically analyze the Encoder representations to maintain consistency with the other self-supervised backbones.

🚀 Execution Pipeline
To reproduce the experiments and extract layer-wise diagnostics, execute the Jupyter notebooks sequentially in numbered order (01 → 04):


Order	Notebook	Description
01	MRH_01_Prepare_14050711.ipynb	Downloads pre-trained speech checkpoints, prepares VCTK datasets, and extracts layer-wise representations.
02	MRH_02_Prosody_14050711.ipynb	Performs linear regression probing for prosodic attributes (
𝐹
0
F 
0
​
 
, RMS energy, and phone duration).
03	MRH_03_Speaker_14050711.ipynb	Evaluates speaker identity retention via 100-speaker classification (Macro-F1) and cosine-similarity verification (EER).
04	MRH_04_Content_14050711.ipynb	Conducts frame-level phonetic content probing, manner of articulation analysis, and calculates Disentanglement Indices (
SDI
SDI
, 
JDC
JDC
).
To run via command line:

bash
jupyter notebook MRH_01_Prepare_14050711.ipynb
📖 Citation
If you find this codebase, diagnostic framework, or disentanglement metrics useful in your research, please consider citing:

bibtex
@article{heydari2024whereiswhat,
  title   = {Where is What? A Comprehensive Layer-wise Analysis of Content, Speaker, and Prosody in Speech SSL Models},
  author  = {Heydari, Mohammadreza and others},
  journal = {arXiv preprint / Under Review},
  year    = {2024},
  url     = {https://github.com/MohammdReza2020/Speech-SSL-Models}
}
