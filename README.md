# Explanation Distillation for DDoS attack detection


This repository contains the implementation of the thesis work of using explanation distillation in DDoS attack detection (Chapter 6).  
It presents a novel DDoS detection framework that integrates **frequency-domain analysis** of SDN traffic with **explanation distillation (XAI-based knowledge transfer)** to improve the accuracy and interpretability of attack detection.

---

## 🚀 Overview

Software Defined Networking (SDN) improves flexibility and scalability in 5G and beyond but exposes the centralized controller to Distributed Denial of Service (DDoS) attacks.  
This project introduces a two-stage detection pipeline:

1. **Direct Detector**: Classifies traffic (DFT-transformed Packet-In messages) as benign or attack.
2. **XAI Detector**: Uses Shapley feature attributions from the direct detector to train a secondary model.
3. **Ensemble Decision**: Combines outputs of both detectors to enhance detection of unseen attacks and reduce false positives.

Our approach leverages **explanation distillation** — transferring insights from one model’s explanations to another model — to improve generalization and robustness against novel DDoS attacks.

---

## ✨ Key Features

- 📊 **Frequency-Domain Analysis**: Transforms Packet-In time series data to frequency domain (DFT/FFT) to reveal hidden attack signatures.
- 🧠 **XAI-Driven Knowledge Transfer**: Uses SHAP-derived feature attributions as input to train a secondary classifier.
- 🔒 **Ensemble Architecture**: Combines direct and XAI detectors to improve robustness and reduce false positives.
- 🧪 **Zero-Shot Evaluation**: Tests on unseen attack types (DNS, NTP, TCP-SYN floods) to demonstrate generalization.
- ⚡ **Low Latency**: Achieves <4 ms prediction latency, making it suitable for real-time SDN security applications.
