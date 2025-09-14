# Vocoder Benchmarking in Text-to-Speech 🎙️

## Overview
This project benchmarks three popular vocoders used in modern text-to-speech (TTS) pipelines:  
- **Griffin-Lim**  
- **WaveGlow**  
- **WaveRNN**

The goal was to evaluate **speed, efficiency, and audio quality** when generating speech from the same input text.  

## Motivation
Text-to-Speech is everywhere → from voice assistants to accessibility tools.  
But not all vocoders are created equal — some are **fast but noisy**, others are **clear but slow**.  
This project explores that trade-off and provides measurable benchmarks.  

## Methodology
1. Used a single consistent text input for fairness.  
2. Measured **generation time** for each vocoder.  
3. Analyzed **spectrogram outputs** for qualitative comparison.  
4. Evaluated **subjective audio quality** (naturalness, clarity, noise).  

## Results
| Vocoder     | Time (s)   | Notes                                      |
|-------------|-----------:|--------------------------------------------|
| Griffin-Lim | 61.09      | Baseline, robotic, slow                    |
| WaveGlow    | 0.31       | Very fast, slightly fuzzy without denoiser |
| WaveRNN     | 61.35     | Clearer & natural, but slow & resource-heavy |

**Trade-off observed:**  
- WaveGlow = **real-time speed**  
- WaveRNN = **better clarity, slower**  
- Griffin-Lim = **benchmark baseline**  

## Next Steps
- Add **HiFi-GAN** and compare with these baselines  
- Fine-tune Tacotron2 on custom data for personalized voice  
- Explore MOS (Mean Opinion Score) evaluation with more listeners  

## Tech Stack
- **PyTorch** (TorchAudio, TorchHub models)  
- **NumPy, Pandas, Matplotlib** for analysis & plotting  
- **Jupyter Notebook** or **colab** for experiments  

