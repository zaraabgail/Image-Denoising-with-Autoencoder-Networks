# Image Denoising with Convolutional Autoencoders

## 🧠 Project Description
This project focuses on applying **deep learning** techniques for **image denoising** using **Convolutional Autoencoders (CAEs)**.  
Autoencoders are neural networks designed to learn efficient representations of data, allowing them to reconstruct clean images from noisy inputs.  

The goal of this project is to compare two autoencoder models—**a baseline model** and a **modified version** using LeakyReLU activation—to evaluate improvements in image reconstruction quality.  
Through this comparison, the project demonstrates how small architectural and activation function changes can significantly enhance model performance in low-level vision tasks.

---

## 📋 Overview
The workflow involves:
1. **Data Loading and Preprocessing** – Extracting, resizing, and normalizing RGB images from the dataset.  
2. **Model Development** – Building and training two convolutional autoencoder models.  
3. **Training and Evaluation** – Measuring performance using **SSIM (Structural Similarity Index)** and **MSE (Mean Squared Error)**.  
4. **Comparison and Analysis** – Evaluating how the modified architecture improves reconstruction quality.

---

## ⚙️ Methodology
- **Baseline Autoencoder:** A simple convolutional model using ReLU activation functions.  
- **Modified Autoencoder:** Replaces ReLU with LeakyReLU to improve gradient propagation and reduce dead neuron problems.  
- Both models are trained to reconstruct denoised images from noisy inputs using **MSE loss** and the **Adam optimizer**.  
- Performance is compared on the same dataset using quantitative and visual evaluations.

---

## 📊 Results
| Model            | SSIM      | MSE       |
|------------------|------------|------------|
| Baseline Model   | **0.9356** | **0.001232** |
| Modified Model   | **0.9485** | **0.000941** |

**Result Summary:**
- The **Modified Autoencoder** achieved a **1.4% improvement in SSIM** and a **23.6% reduction in MSE** compared to the baseline.  
- Visual inspection confirms sharper, cleaner reconstructions and better color preservation.  
- The experiment highlights the impact of activation function selection in deep learning image tasks.
