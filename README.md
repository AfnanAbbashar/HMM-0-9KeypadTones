# HMM-0-9KeypadTones
Speech Recognition of Keypad Tones using Hidden Markov Models (HMM)
Full Google Colab code



# Project Report

## Project Title
**Speech Recognition of Keypad Tones using Hidden Markov Models (HMM)**

## Dataset Description
The dataset consists of recorded audio tones corresponding to each number on a telephone keypad (0-9). Each number class has multiple `.wav` audio samples representing the Dual-Tone Multi-Frequency (DTMF) sound of pressing that number.

- **Number of classes (digits):** 10 (0 through 9)
- **Number of total samples:** 300 audio files
- **Structure:** Organized in subfolders named 0, 1, 2, ..., 9

## Methodology
1. **Feature Extraction:**
   - We extracted **Mel-Frequency Cepstral Coefficients (MFCCs)** from each audio sample to capture its spectral characteristics.

2. **Model:**
   - We trained **one Hidden Markov Model (HMM)** for each digit using the **GaussianHMM** implementation from the `hmmlearn` library.
   - Each model used 5 hidden states and diagonal covariance matrices.

3. **Training and Testing:**
   - Dataset was split into 80% for training and 20% for testing.
   - For prediction, we computed the log-likelihood of each test sample for all HMMs and selected the model with the highest likelihood as the predicted digit.

## Results
- **Test Accuracy:** 96.67%
- **Classes detected:** 0, 1, 2, 3, 4, 5, 6, 7, 8, 9

## Conclusion
- The HMM-based speech recognition system performed with **high accuracy** in recognizing keypad tones.
- The system can be extended for real-time applications or larger datasets.

## Requirements Used
- `Python`, `Google Colab`
- Libraries: `hmmlearn`, `librosa`, `scikit-learn`, `joblib`
