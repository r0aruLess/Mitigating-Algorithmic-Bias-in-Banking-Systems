# NIST AI Risk Management Framework (AI RMF 1.0)
**Core Functions Implemented:** Map, Measure, Manage

## 1. Technical Risk Register Matrix
The following matrix documents the empirical vulnerabilities identified during the technical validation phase of the Model Pipeline.

| Risk ID | Risk Characterization | Framework Category | Severity Impact | Engineering Mitigation Strategy |
| :--- | :--- | :--- | :--- | :--- |
| **AI-01** | **Systemic Algorithmic Bias:** Model displays extreme proxy discrimination, yielding a 0.00 Disparate Impact Ratio against applicants over age 60. | **NIST AI RMF:** *Fairness & Bias Management* | **Critical (5/5)** | Pre-processing data re-weighting, optimization parameter constraints, or wholesale removal of age-correlated features from the secondary training iteration. |
| **AI-02** | **Black-Box Model Opacity:** Decision Tree split metrics lack instant interpretability for external financial regulatory compliance reporting. | **NIST AI RMF:** *Transparency & Accountability* | **Medium (3/5)** | Integration of explainable AI (XAI) wrapper tools, such as SHAP or LIME values, to log top-3 definitive financial drivers behind each transaction decision. |

| Risk ID | Risk Characterization | Framework Category | Severity Impact | Engineering Mitigation Strategy |
| :--- | :--- | :--- | :--- | :--- |
| **AI-03** | **Operational Denial of Service:** Excessive False Positive metrics freeze legitimate customer payment cards during anomalous hours. | **NIST AI RMF:** *Reliability & Safety* | **High (4/5)** *Triggers high customer turnover and floods call centers.* | Restructure model classification thresholds. Transition from binary "Block/Allow" outputs to a probabilistic risk tiering system ($Low/Medium/High$). |
| **AI-04** | **Helpdesk Pipeline Saturation:** Spikes in algorithmic false blocks cause a 400% surge in customer support ticket volumes, breaching service level agreements (SLAs). | **COBIT 2019:** *APO12 (Managed Risk)* | **Medium (3/5)** | Deploy automated API webhook rules that automatically downgrade model enforcement to "Alert Only" mode if helpdesk hold times exceed 15 minutes. |

| Risk ID | Risk Characterization | Framework Category | Severity Impact | Engineering Mitigation Strategy |
| :--- | :--- | :--- | :--- | :--- |
| **AI-05** | **Shadow IT Deployment:** Model runs in an unlogged production loop, failing regulatory data provenance requirements. | **NIST AI RMF:** *Accountability & Transparency* | **High (4/5)** *Triggers severe regulatory compliance fines and audit failure.* | Integrate structural audit logging layers. Every user query, data access token, and classification shift must be saved to an immutable cloud database. |
| **AI-06** | **Silent Model Drift:** Lack of retraining tracking prevents discovery of data drift as macroeconomic client conditions change. | **NIST AI RMF:** *Explainable & Trackable* | **Medium (3/5)** | Schedule automated monthly statistical drift tests (KS-Tests) comparing inference datasets against baseline parameters, auto-flagging drift to engineers. |
