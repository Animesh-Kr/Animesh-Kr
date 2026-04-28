<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=700&size=30&duration=3000&pause=800&color=00D4FF&center=true&vCenter=true&multiline=true&width=900&height=100&lines=Hi+there%2C+I'm+Animesh+Kumar+%F0%9F%91%8B;AI+Researcher+%7C+MLOps+Engineer+%7C+PhD+Aspirant" alt="Typing SVG" />

<br/>

[![Portfolio](https://img.shields.io/badge/Portfolio-akumar--tech.me-00D4FF?style=for-the-badge&logo=vercel&logoColor=white)](https://akumar-tech.me/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-animeshakumar-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/animeshakumar/)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-animeshakr-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)](https://huggingface.co/animeshakr)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0003--0608--7004-brightgreen?style=for-the-badge)](https://orcid.org/0009-0003-0608-7004)
[![Twitter](https://img.shields.io/badge/Twitter-@AnimeshKumar__-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/AnimeshKumar_)
[![Credly](https://img.shields.io/badge/Credly-Certifications-FF6B00?style=for-the-badge&logo=credly&logoColor=white)](https://www.credly.com/users/animesh-kumar.d87a7137)

![Profile Views](https://komarev.com/ghpvc/?username=Animesh-Kr&color=00D4FF&style=for-the-badge&label=PROFILE+VIEWS)

</div>

---

## 🧠 About Me

```python
animesh = {
    "role"       : "AI Researcher & MLOps Engineer",
    "education"  : ["MSc Advanced Computer Science @ Newcastle University (2025–26, on track for Distinction)",
                    "B.Tech CSE (AI Specialization) @ AKTU, India"],
    "research"   : ["Medical Image Analysis", "Computer Vision",
                    "Generative AI", "Clinical AI Safety",
                    "Uncertainty Quantification"],
    "goal"       : "Funded PhD in AI/Medical Imaging (Germany, 2026) — targeting TU Munich, DKFZ, FAU",
    "location"   : "Newcastle upon Tyne, UK 🇬🇧",
    "visa"       : "Eligible: UK Graduate Visa & Netherlands Orientation Year Visa (2026)",
    "fun_fact"   : "I turn retinal scans into decisions — one attention map at a time 🔬"
}
```

---

## 🚀 Featured Projects

### 🔬 [OCT Retinal Fluid Segmentation](https://github.com/Animesh-Kr/oct-fluid-segmentation) &nbsp; [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19808008.svg)](https://doi.org/10.5281/zenodo.19808008) &nbsp; [![Live Demo](https://img.shields.io/badge/🤗%20Live%20Demo-HuggingFace-FFD21E?style=flat-square)](https://huggingface.co/spaces/animeshakr/oct-fluid-segmentation) &nbsp; [![Model Weights](https://img.shields.io/badge/🤗%20Model%20Weights-HuggingFace-orange?style=flat-square)](https://huggingface.co/animeshakr/oct-fluid-segmentation)

> **PhD-level independent research — multi-class retinal fluid segmentation with clinical uncertainty triage**

- **Architecture:** Dual AttentionTransUNetL ensemble (EfficientNetV2L encoder, 127M params each) + Transformer bottleneck (d_model=512, 16 heads) + 4× Attention Gates + Source-Adaptive BatchNorm
- **Dataset:** 4 independent OCT sources — DUKE DME, AROI, UMN AMD, UMN DME (4983 training slices)
- **Results:** V2L val Dice **0.784 ± 0.006** across 3 seeds · IRF 0.916 · SRF 0.856 · PED 0.581
- **Novel:** UCUS — Uncertainty-Weighted Clinical Urgency Score (Monitor / Review / Urgent triage)
- **Clinical Safety:** Uncertainty **1.34× higher** at inter-grader disagreement pixels (p=3.77e-05) · SRF volume r=0.778 · PED volume r=0.841
- **Deployment:** INT8 quantised (510MB → 132MB, 3.9×) · ONNX export · Streamlit dashboard · FastAPI endpoint
- **Targeting:** arXiv preprint + OMIA 2027 Workshop at MICCAI

`PyTorch` `EfficientNetV2L` `TransUNet` `MC Dropout` `ONNX` `Streamlit` `FastAPI` `HuggingFace`

---

### 🔬 [OCT Retinal Disease Classification](https://github.com/Animesh-Kr/Human-Eye-Disease-Prediction) &nbsp; [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19224303.svg)](https://doi.org/10.5281/zenodo.19224303) &nbsp; [![Live Demo](https://img.shields.io/badge/🤗%20Live%20Demo-HuggingFace-FFD21E?style=flat-square)](https://huggingface.co/spaces/animeshakr/oct-retinal-ai) &nbsp; [![Model Weights](https://img.shields.io/badge/🤗%20Model%20Weights-HuggingFace-orange?style=flat-square)](https://huggingface.co/animeshakr/oct-retinal-weights)

> **Production-grade clinical AI system for automated retinal disease detection**

- **Architecture:** EfficientNetV2L + 4× Multi-Head Attention + Learnable Positional Encoding + XGBoost hybrid head
- **Dataset:** Kermany et al. (84K OCT images — CNV, DME, DRUSEN, NORMAL)
- **Results:** 5-seed validated · **95.43% ± 0.27% Accuracy** · **Macro AUC 0.9941 ± 0.0006** · ECE 0.0024
- **RETFound comparison:** Matches 303M-parameter foundation model while being 5× more stable across seeds
- **Clinical Safety:** Mahalanobis OOD Detection · MC Dropout · Temperature Scaling · Grad-CAM · SHAP
- **Deployment:** ONNX 237MB · ~62.9ms CPU · Streamlit + Gradio + FastAPI on HuggingFace

`TensorFlow` `EfficientNetV2L` `XGBoost` `Optuna` `SHAP` `Streamlit` `HuggingFace`

---

### 🔗 [OCT Complete Diagnostic Pipeline] [![Live Demo](https://img.shields.io/badge/🤗%20Live%20Demo-HuggingFace-FFD21E?style=flat-square)](https://huggingface.co/spaces/animeshakr/oct-complete-pipeline)

> **End-to-end clinical pipeline connecting both retinal AI projects**

- Stage 1: Classification (CNV / DME / DRUSEN / NORMAL) via ONNX inference
- Stage 2: Fluid segmentation (IRF / SRF / PED) with live ONNX dual ensemble
- UCUS clinical triage score computed end-to-end from raw scan to urgency band

---

### 🌿 [Plant Disease Prediction](https://github.com/Animesh-Kr/Plant-Disease-Prediction) &nbsp;[![Live Demo](https://img.shields.io/badge/🤗%20Live%20Demo-HuggingFace-FFD21E?style=flat-square)](https://huggingface.co/spaces/animeshakr/plant-disease-detection1) [![Model Weights](https://img.shields.io/badge/🤗%20Model%20Weights-HuggingFace-orange?style=flat-square)](https://huggingface.co/animeshakr/plant-disease-efficientnetv2s)

> **Research-grade plant pathology classification — 38 diseases, 54,306 images**

- **Results:** **99.57% Test Accuracy** · **99.48% Macro F1** · McNemar p = 3.27 × 10⁻¹⁸²
- **Architecture:** EfficientNetV2S · two-stage transfer learning · TFLite float16 (~45 MB)

`TensorFlow` `EfficientNetV2S` `TFLite` `Streamlit` `UMAP` `HuggingFace`

---

### 🤖 [AI-Powered Social Media Caption Generator](https://github.com/Animesh-Kr/AI-Powered-Social-Media-Post-Caption-Generator)

> **Automated content creation pipeline with RAG + fine-tuned Llama-2**

- ~70% reduction in manual writing time · LangChain RAG · vector store retrieval

`LangChain` `RAG` `Llama-2` `Python`

---

## 🛠️ Tech Stack

### Languages & Frameworks
![Python](https://img.shields.io/badge/Python-Advanced-3776AB?style=for-the-badge&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white)
![CUDA](https://img.shields.io/badge/CUDA-76B900?style=for-the-badge&logo=nvidia&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white)

### AI / ML / CV
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-Transformers-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-189AB4?style=for-the-badge&logo=xgboost&logoColor=white)

### MLOps & Cloud
![AWS](https://img.shields.io/badge/AWS-Solutions%20Architect-FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-0078D4?style=for-the-badge&logo=microsoft-azure&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)

### Data & Explainability
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![SHAP](https://img.shields.io/badge/SHAP-Explainability-8B0000?style=for-the-badge)
![Tableau](https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=tableau&logoColor=white)

---

## 🏆 Certifications

| Certification | Issuer | Badge |
|---|---|---|
| Oracle Generative AI Professional | Oracle | ![Oracle](https://img.shields.io/badge/Oracle-GenAI%20Professional-F80000?style=flat-square&logo=oracle&logoColor=white) |
| AWS Solutions Architect | Amazon Web Services | ![AWS](https://img.shields.io/badge/AWS-Solutions%20Architect-FF9900?style=flat-square&logo=amazon-aws&logoColor=white) |
| Azure Fundamentals (AZ-900) | Microsoft | ![Azure](https://img.shields.io/badge/Azure-AZ--900-0078D4?style=flat-square&logo=microsoft-azure&logoColor=white) |
| Oracle AI Vector Search | Oracle | ![Oracle](https://img.shields.io/badge/Oracle-AI%20Vector%20Search-F80000?style=flat-square&logo=oracle&logoColor=white) |

🔗 [View all credentials on Credly →](https://www.credly.com/users/animesh-kumar.d87a7137)

---

## 💼 Experience

**🔷 IBM — AI/ML Intern** *(Summer 2025)*
> LLMs & Transformer architectures — fine-tuning, deployment, and prompt engineering at enterprise scale

**🔷 IIT Kanpur — Deep Learning Intern** *(May–June 2023)*
> Retinal disease detection with DL + AWS cloud infrastructure

**🔷 MedTourEasy — Data Analyst** *(October 2022)*
> Healthcare data analytics and reporting

---

## 📊 GitHub Stats

<div align="center">

<img height="180em" src="https://github-readme-stats.vercel.app/api?username=Animesh-Kr&show_icons=true&theme=tokyonight&include_all_commits=true&count_private=true&hide_border=true&bg_color=0D1117&title_color=00D4FF&icon_color=00D4FF&text_color=FFFFFF"/>
<img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Animesh-Kr&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00D4FF&text_color=FFFFFF"/>

</div>

---

## 🎯 Current Focus

- 🔬 **OCT Fluid Segmentation** — arXiv preprint submission (targeting cs.CV / eess.IV)
- 🔬 **OCT Classification** — arXiv preprint submission
- 🎓 **PhD Applications** — targeting funded positions at TU Munich · DKFZ · FAU (Sept/Oct 2026)
- 📖 **MSc Dissertation** — Newcastle University (2025–26)

---

## 🔬 Research Interests

`Medical Image Analysis` &nbsp;`Computer Vision` &nbsp;`Generative AI` &nbsp;`Clinical AI Safety`
`Uncertainty Quantification` &nbsp;`Explainable AI (XAI)` &nbsp;`Transformer Architectures` &nbsp;`MLOps`

---

<div align="center">

### 📬 Let's Connect

*Open to research collaborations, PhD discussions, and interesting problems in medical AI.*

[![Email](https://img.shields.io/badge/Email-Get%20In%20Touch-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:animesh@akumar-tech.me)
[![Portfolio](https://img.shields.io/badge/Portfolio-akumar--tech.me-00D4FF?style=for-the-badge&logo=vercel&logoColor=white)](https://akumar-tech.me/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/animeshakumar/)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-Follow-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)](https://huggingface.co/animeshakr)

---

*"Building AI that doctors can trust and researchers can build on."*

</div>
```
