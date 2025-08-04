#  Digital Twin-Net for EEG Seizure Prediction

This repository summarizes the work completed during a **3-month research internship** at the Bioinformatics Lab, GIKI (Ghulam Ishaq Khan Institute of Engineering Sciences and Technology), Swabi–Topi, under the supervision of **Dr. Shahabuddin Ansari**. The focus of our research was to enhance **epileptic seizure prediction** using **digital twin models** and **transformer-based deep learning architectures**.

---

##  Project Title

**Digital Twin-Net for EEG Seizure Prediction: Methodology Review and Transformer-Based Model**

---

##  Motivation

Epilepsy affects over **50 million people** globally. Seizures are unpredictable and can lead to injury or death. EEG-based seizure prediction systems can offer early warnings by detecting abnormal brain activity, potentially improving patient safety and independence.

---

##  Research Goals

- Understand and reproduce the **Digital Twin-Net** (TMSST ➝ CNN–BiLSTM–Attention)
- Enhance EEG preprocessing using **wavelet denoising**
- Explore advanced **Transformer-based architectures** (Vision Transformer & CNN+Transformer hybrid)
- Integrate **spatial + temporal dual-attention mechanisms**
- Evaluate performance on the **CHB-MIT Scalp EEG dataset**
- Document results, challenges, and future research directions

---

##  Contributions

### ✅ Baseline Replication
- Implemented the **Digital Twin-Net** architecture using:
  - **TMSST** for time–frequency representation
  - CNN for spatial features
  - BiLSTM for temporal sequence modeling
  - Temporal attention for enhanced feature weighting

###  Enhanced EEG Preprocessing
- Applied **Band-pass (0.5–40Hz)** and **Notch filtering**
- Introduced **Wavelet Denoising (DWT)** to remove ocular/muscle artifacts

###  Transformer-Based Models
- Developed a **Vision Transformer (ViT)** that processes TMSST spectrogram patches
- Designed a **Hybrid CNN + Transformer** for long-range temporal dependency modeling
- Incorporated **Dual-Attention** for spatio-temporal focus

---

## 📊 Results (CHB-MIT Dataset)

| Model               | Accuracy | Sensitivity | Specificity | FPR/hr | AUC   |
|--------------------|----------|-------------|-------------|--------|-------|
| Baseline (CNN-BiLSTM) | 99.70%   | 99.50%      | 99.60%      | 0.005  | 0.995 |
| ViT (Ours)          | **99.80%** | **99.60%**  | **99.70%**  | **0.004** | **0.997** |

✅ **Reduced false positives**  
✅ **Higher interpretability with attention maps**  
✅ **Improved robustness across patients**

---

##  Future Work

- **Cross-Patient Generalization** using meta-learning/domain adaptation  
- **Multimodal Fusion**: Integrating EEG with ECG, motion sensors, etc.  
- **Real-Time Deployment**: Optimizing for edge/wearable devices (e.g. using EEGformer)  
- **Explainability**: Enhancing clinical trust through attention map visualization

---

##  Acknowledgments

Special thanks to **Dr. Shahabuddin Ansari**  for their mentorship, support, and research environment.  

Also grateful to my collaborator **Talha Sheikh** for insightful discussions and teamwork throughout this internship.

---

## 📚 References

1. [WHO - Epilepsy Overview](https://www.who.int/news-room/fact-sheets/detail/epilepsy)  
2. [Digital Twin for EEG Seizure Prediction (PMC)](https://pmc.ncbi.nlm.nih.gov/articles/PMC11604751/)  
3. [EEGformer: Compact Transformer on MCU](https://pubmed.ncbi.nlm.nih.gov/38261487/)  
4. [Transformer-Based EEG Seizure Prediction](https://translational-medicine.biomedcentral.com/articles/10.1186/s12967-024-05678-7)
