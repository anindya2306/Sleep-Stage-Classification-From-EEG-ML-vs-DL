# Sleep Stage Prediction from Raw EEG Signals

In the modern age of rapid technological advancements and fast-paced lifestyles, sleep disorders have become increasingly common, negatively impacting health, productivity, and overall quality of life. Traditional diagnostic methods are expensive and time-consuming, leaving many vulnerable without timely intervention. This project aims to address this issue by utilizing machine learning models to analyze EEG recordings of patients, enabling efficient assessment of sleep quality and accurate diagnosis of sleep disorders.

## Data

The input data consists of sequences of 30-second EEG epochs recorded from a single channel "Fpz-Cz", following the standards set by the AASM and R&K manuals. Each epoch is labeled as "W" (Wake), "N1" (Non-REM Stage 1), "N2" (Non-REM Stage 2), "N3" (Non-REM Stage 3), or "REM" (Rapid Eye Movement). The objective is to transform the raw time-series EEG data into a coherent hypnogram.

## Methods

Two main approaches were adopted for sleep stage prediction:

1. **Feature-based Machine Learning Approach:**
   Hand-crafted time and frequency domain features, including Cross Wavelet features, were extracted from each 30-second epoch. A LightGBM model was trained on these features to classify sleep stages based on their time-invariant properties.

2. **Hybrid CNN-LSTM Architecture:**
   A hybrid model combining Convolutional Neural Networks (CNNs) and Long Short-Term Memory (LSTM) networks was developed. CNNs learned to extract time-invariant features from raw single-channel EEG signals, while bidirectional LSTMs captured temporal information and sleep stage transition patterns.

The uniqueness of the hybrid model lies in its ability to adapt to various EEG datasets with different properties and scoring standards (e.g., AASM and R&K) without requiring manual feature engineering.

## Results

Sample visualizations of sleep stage predictions are provided below:

[Insert sample photos of results here]

## Reference

This project draws inspiration from the research paper:
"DeepSleepNet: A Model for Automatic Sleep Stage Scoring based on Raw Single-Channel EEG" by Akara Supratak, Hao Dong, Chao Wu, Yike Guo.

[Read the full paper here](https://arxiv.org/pdf/1703.04046.pdf)

This repository serves as a demonstration of utilizing machine learning techniques to predict sleep stages from raw EEG signals, contributing towards a more accessible and efficient method of diagnosing sleep disorders.
