# Cross-Lingual Speech Emotion Recognition with Wav2Vec2: Bengali–English Emotion Transfer

[![Paper](https://img.shields.io/badge/IEEE%20Xplore-ICCMRAI%202026-blue.svg)](https://ieeexplore.ieee.org/document/11723515)
[![DOI](https://img.shields.io/badge/DOI-10.1109%2FICCMRAI67732.2026.11723515-orange.svg)](https://doi.org/10.1109/ICCMRAI67732.2026.11723515)
[![Framework](https://img.shields.io/badge/PyTorch-Hugging%20Face-yellow.svg)](https://pytorch.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Official PyTorch implementation of the paper **"Cross-Lingual Speech Emotion Recognition with Wav2Vec2: Bengali–English Emotion Transfer"**, presented at the *2026 1st International Conference on Computer, Mechatronics, Robotics & Artificial Intelligence (ICCMRAI)*, Pune, India.

---

## 📌 Abstract

Speech Emotion Recognition (SER) is gaining importance in human-computer interaction systems to make machines sound more humane. However, SER for low-resourced languages is under-researched due to limited availability of annotated data. This study investigates cross-lingual SER using the self-supervised **Wav2Vec 2.0** pretrained model between Bengali and English to examine whether emotion representations learned in one language can be transferred to another.

Our findings demonstrate that fine-tuning Wav2Vec2 yields:
- **90.77% accuracy** on merged English speech benchmarks (SAVEE & CREMA-D).
- **97.17% accuracy** on the SUBESCO Bengali dataset.
- **79.11% accuracy** in cross-lingual transfer (trained on Bengali, evaluated on English), exceeding the chance baseline by **+64.38 percentage points**.
- Acoustic-prosodic analysis shows that high-arousal emotions (*Anger*, *Surprise*) transfer significantly better across language barriers than low-arousal emotions (*Fear*, *Sad*).

---

## 📊 Empirical Results

| Training Regime | Source Language / Dataset | Target Language / Dataset | Accuracy (%) |
| :--- | :--- | :--- | :---: |
| Monolingual Baseline | Bengali (SUBESCO) | Bengali (SUBESCO) | **97.17%** |
| Monolingual Baseline | English (SAVEE + CREMA-D) | English (SAVEE + CREMA-D) | **90.77%** |
| Cross-Lingual Transfer | Bengali (SUBESCO) | English (SAVEE + CREMA-D) | **79.11%** |
| Random Guess Baseline | — | English (SAVEE + CREMA-D) | ~14.73% |
