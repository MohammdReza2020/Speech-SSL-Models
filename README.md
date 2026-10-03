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
