# Enterprise AI Governance: Mitigating Algorithmic Bias in Banking Systems

A Mini Project implementing a 30% AI Engineering and 70% GRC (Governance, Risk, and Compliance) architecture using **COBIT 2019** and the **NIST AI Risk Management Framework (AI RMF)**.

---

## 📌 Project Overview
This project addresses a major corporate challenge: **the deception of high model accuracy masking catastrophic compliance and ethical risks.** By simulating a real-world financial deployment, this project demonstrates how a credit-scoring model boasting **97.50% overall accuracy** secretly codified systemic age discrimination—resulting in a legally indefensible **Disparate Impact Ratio of 0.00** against applicants over the age of 60.

The core objective of this project is to implement an enterprise safety net using industry-standard GRC frameworks to identify, assess, govern, and remediate systemic AI risks within a commercial banking environment.

### 📐 Project Architecture Split
* **30% AI Engineering:** Scripting, mock data generation, automated model training, and quantitative bias discovery via Google Colab.
* **70% IT Governance & Risk Management:** Structural asset mapping, enterprise risk profiling, human-in-the-loop operational policy generation, and remediation strategies.

---

## 🧠 Frameworks & Standards Utilized
* **COBIT 2019 (ISACA):** Applied to govern enterprise asset accountability, create structural IT ownership pipelines, and outline internal control evaluation methods (**APO01, APO12, MEA02**).
* **NIST AI RMF 1.0:** Utilized to map technical system boundaries, quantitatively measure algorithmic bias metrics, and construct an actionable risk mitigation register (**Map, Measure, Manage**).
* **The 80% Rule (Disparate Impact Standard):** Used as the technical compliance threshold for identifying systemic discrimination.

---

## 📁 Repository Structure
```text
├── 📓 credit_scoring_model_pipeline.ipynb   # 30% AI: Model training & bias logging
├── 📁 grc_compliance_dossier/              # 70% GRC Artifacts
│   ├── 📄 COBIT_AI_Asset_Inventory.xlsx      # APO01: Structural accountability matrix
│   ├── 📄 NIST_AI_RMF_Risk_Register.xlsx     # Map & Measure: Technical risk mapping
│   └── 📄 Human_In_The_Loop_Policy.md        # MEA02: Operational override standard
└── 📄 README.md                            # Executive Project summary
