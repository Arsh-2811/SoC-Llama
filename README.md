<!-- prettier-ignore -->
<h1 align="center">SoC-Llama</h1>
<p align="center">
  <a href="https://ieeexplore.ieee.org/document/10719268"><img src="https://img.shields.io/badge/DOI-10719268-blue.svg?style=flat-square" alt="IEEE DOI"/></a>
  <a href="LICENSE"><img src="https://img.shields.io/github/license/Arsh-2811/SoC-Llama?style=flat-square" alt="License"/></a>
  <a href="https://pypi.org/project/torch/"><img src="https://img.shields.io/badge/PyTorch-%3E%3D1.13-lightgrey?style=flat-square" alt="PyTorch"/></a>
</p>

---

## 🔍 Overview
SoC-Llama is a *transformer-based* research implementation for **State of Charge (SoC)** estimation in EV batteries. It adapts the streamlined LLaMA decoder, enriched with:
- **RoPE** for relative positional encoding  
- **GQA** for parameter-efficient attention  
- **SiLU** activations and **RMSNorm**  
- Custom warm-up & decay schedule (à la **“Attention Is All You Need”**)  

_All code reproduces the experiments and plots from our IEEE paper._

---

## ✨ Features
| Component               | Description                                                      |
|:------------------------|:-----------------------------------------------------------------|
| 🔧 **Architecture**     | Lightweight LLaMA-style decoder                                   |
| 📐 **RoPE**             | Rotary embeddings for scalable, relative token dependencies      |
| ⚙️ **GQA**              | Grouped multi-query attention for fewer heads, same expressivity |
| 🌊 **SiLU + RMSNorm**   | Smooth activations & stable normalization                        |
| 🚀 **Scheduler**        | Warm-up + cosine decay (Adam optimizer)                          |

---

## 📊 Results
- **Final MSE:** \(0.345\)  
- **Training Config:**  
  - Epochs: 4000  
  - Adam β₁=0.9, β₂=0.98, ε=1e-9
  - Warm-up steps: 2  
- **Illustrative Plots:**  
  <ul>
    <li>Training vs. Validation Loss</li>
    <li>Predicted vs. Actual SoC</li>
  </ul>

## 📑 Paper & Assets

> **Full details & theory:**
> [SOC-Llama: Estimation of SOC using LLaMA](https://ieeexplore.ieee.org/document/10719268)

---

## 👥 Authors & Acknowledgments

* **Aditi Garg** — *([aditigarg@dtu.ac.in](mailto:aditigarg_ee20a12_52@dtu.ac.in))*
* **Arsh Sharan** — *([arshsharan@dtu.ac.in](mailto:arshsharan_ee20a13_04@dtu.ac.in))*
* **Aryan Garg** — *([aryangarg@dtu.ac.in](mailto:aryangarg_ee20a13_07@dtu.ac.in))*
* **Krishna Dutt** — *([krishna@dtu.ac.in](mailto:krishna@dtu.ac.in))*
* **Anshul Arora** — *([anshularora@dtu.ac.in](mailto:anshularora@dtu.ac.in))*

Supported by the Department of Electrical Engineering, Delhi Technological University.
