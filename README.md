# 🧠 EEG Rhythm Extraction & Spectral Analysis

## Project Overview
This repository contains a specialized Python pipeline for processing and analyzing raw **EEG (Electroencephalography)** data. The project bridges the gap between raw voltage-time series and meaningful neurological insights by leveraging **Fast Fourier Transforms (FFT)** to map the Power Spectral Density (PSD) of brain activity.

A key highlight of this implementation is the identification of **60Hz line noise**, a common environmental artifact in North American datasets, and the characterization of standard neural rhythms (Alpha, Beta, Delta, Theta).



---

## 🛠️ Technical Workflow
The analysis follows a rigorous signal-processing sequence:

1. **Temporal Inspection:** Visualization of raw 10-channel data to observe signal morphology and amplitude.
2. **Statistical Characterization:** Computing mean, variance, and standard deviation to establish a baseline for signal quality.
3. **DC Offset Removal:** Centering the signal by subtracting the mean to eliminate the 0Hz component before spectral decomposition.
4. **Spectral Analysis:** - Implementation of the FFT algorithm.
   - Scaling the power spectrum to account for sampling interval and duration.
   - Mapping the Nyquist-limited frequency axis for real-world interpretation in Hertz (Hz).

---

## 📊 Key Findings
* **60Hz Artifact:** The spectral plot reveals a high-magnitude, narrow-band spike at 60Hz. This confirms that the data contains electrical interference from the power grid, requiring further notch filtering.
* **Neural Signatures:** Beyond the noise, the pipeline is designed to isolate rhythmic activity associated with different cognitive states, such as the 8-13Hz Alpha band.



---

## 🚀 Getting Started

### 1. Requirements
Ensure you have the following scientific Python libraries installed:
```bash
pip install numpy scipy matplotlib
