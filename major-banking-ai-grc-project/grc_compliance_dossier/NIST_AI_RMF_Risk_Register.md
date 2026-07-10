# NIST AI Risk Management Framework (AI RMF 1.0)
**Core Functions Implemented:** Map, Measure, Manage

## 1. Technical Risk Register Matrix
The following matrix documents the empirical vulnerabilities identified during the technical validation phase of the Model Pipeline.

| Risk ID | Risk Characterization | Framework Category | Severity Impact | Engineering Mitigation Strategy |
| :--- | :--- | :--- | :--- | :--- |
| **AI-01** | **Systemic Algorithmic Bias:** Model displays extreme proxy discrimination, yielding a 0.00 Disparate Impact Ratio against applicants over age 60. | **NIST AI RMF:** *Fairness & Bias Management* | **Critical (5/5)** | Pre-processing data re-weighting, optimization parameter constraints, or wholesale removal of age-correlated features from the secondary training iteration. |
| **AI-02** | **Black-Box Model Opacity:** Decision Tree split metrics lack instant interpretability for external financial regulatory compliance reporting. | **NIST AI RMF:** *Transparency & Accountability* | **Medium (3/5)** | Integration of explainable AI (XAI) wrapper tools, such as SHAP or LIME values, to log top-3 definitive financial drivers behind each transaction decision. |
