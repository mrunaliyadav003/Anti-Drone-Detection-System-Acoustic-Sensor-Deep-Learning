# Anti-Drone Detection System — Acoustic Sensor + Deep Learning

> AI-driven drone detection using acoustic sensors and deep learning models, developed during an internship at **Paras Anti Drone Technologies**. Achieved **75% reduction in false positives** over the baseline system.

---

## Overview

This project implements a real-time drone detection system that uses acoustic sensor data and deep learning to identify the presence of drones. Unlike visual detection systems that fail in low-visibility conditions, acoustic detection works at night, through fog, and at range.

The system processes audio signals from microphone arrays, extracts spectral features, and classifies them using trained neural network models to determine whether a drone is present in the environment.

---

## Key Results

| Metric | Baseline | This System | Improvement |
|---|---|---|---|
| False Positive Rate | High | Reduced by 75% | 75% reduction |
| Detection Method | Visual only | Acoustic + ML | Multi-modal |
| Visibility Requirement | Clear conditions | All conditions | All-weather |

---

## Notebooks

| File | Description |
|---|---|
| `drone_detection.ipynb` | Main detection pipeline — feature extraction, model training, inference |
| `drone_audio_detection.ipynb` | Audio signal processing and classification |
| `Antidrone.ipynb` | Full anti-drone system integration |
| `featureextract&normalization.ipynb` | Feature engineering — MFCC, spectral features, normalisation |
| `check_dataset.ipynb` | Dataset exploration and validation |
| `check_threshold.ipynb` | Threshold tuning to minimise false positives |
| `Farm_Pest_detection.ipynb` | Transfer learning applied to agricultural pest detection (B.Tech thesis domain) |
| `rasabot.ipynb` | Rasa conversational AI integration |

---

## Technical Approach

### 1. Audio Feature Extraction
- **MFCC (Mel-Frequency Cepstral Coefficients)** — captures the acoustic signature of drone rotors
- **Spectral centroid, bandwidth, rolloff** — characterises the frequency distribution
- **Zero crossing rate** — distinguishes mechanical from ambient noise
- Normalisation pipeline to handle varying recording conditions

### 2. Deep Learning Model
- Deep Neural Network trained on labelled drone / non-drone audio samples
- Binary classification: drone present vs. ambient noise
- Threshold optimisation to reduce false positives while maintaining sensitivity

### 3. Detection Pipeline
```
Acoustic Sensor Input
       ↓
Audio Preprocessing (noise reduction, normalisation)
       ↓
Feature Extraction (MFCC, spectral features)
       ↓
Deep Neural Network Classifier
       ↓
Threshold Decision
       ↓
Alert: Drone Detected / Clear
```

---

## Tech Stack

| Layer | Technology |
|---|---|
| Language | Python 3 |
| Deep Learning | TensorFlow / Keras |
| Audio Processing | librosa, scipy |
| Data Analysis | NumPy, Pandas |
| Visualisation | Matplotlib, Seaborn |
| Notebooks | Jupyter |

---

## Research Foundation

This work builds on published research in acoustic drone detection:

- [Drone Detection Using Acoustic Sensors — MDPI Sensors 2021](https://www.mdpi.com/1424-8220/21/15/4953)
- [Acoustic-Based Drone Detection — EasyChair Preprint](https://easychair.org/publications/preprint_open/93TN)
- [Guide to Audio Classification Using Deep Learning — Analytics Vidhya](https://www.analyticsvidhya.com/blog/2022/04/guide-to-audio-classification-using-deep-learning/)

---

## Related Work

The `Farm_Pest_detection.ipynb` notebook extends the audio/ML pipeline to agricultural pest detection — the domain of the B.Tech thesis project at Pillai College of Engineering, Mumbai, which applied ML and Big Data to pesticide detection at scale.

---

## Context

- **Developed during:** AI/ML Engineer Internship at Paras Anti Drone Technologies (Mar 2023 - Jul 2023)
- **Role:** Designed and implemented the detection system; optimised detection logic to reduce false positives by 75%
- **Application:** Security and surveillance — detecting unauthorised drones in restricted airspace

---

*Part of the AI/ML portfolio at [github.com/mrunaliyadav003](https://github.com/mrunaliyadav003)*
