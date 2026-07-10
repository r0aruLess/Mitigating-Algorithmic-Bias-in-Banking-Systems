# Human-in-the-Loop (HITL) Operational Policy Framework
**System ID:** AI-POLICY-HITL-CREDIT  
**Framework Alignment:** COBIT 2019 (MEA02 - Managed Internal Controls) & NIST AI RMF (Manage Function)  
**Regulatory Context:** EU AI Act High-Risk System Obligations (Article 14 - Human Oversight)

---

## 1. Objective & Purpose
Technical validation of the Automated Credit-Scoring Engine (v1.0) revealed a catastrophic structural vulnerability: a **Disparate Impact Ratio of 0.00** against applicants over the age of 60. While the model maintains a deceptive 97.50% overall classification accuracy, its autonomous deployment presents an unacceptable legal, financial, and reputational liability. 

This policy establishes an enforceable **Human-in-the-Loop (HITL)** oversight framework. It strips the autonomous machine learning model of unilateral final decision-making authority over loan denials, mitigating algorithmic bias through structured human intervention.

---

## 2. Structural Governance Hierarchy

The workflow enforces a strict division of authority between the automated risk pipeline and certified banking personnel.

```text
 ┌───────────────────────────┐
 │   Lending Dataset Input   │
 └─────────────┬─────────────┘
               │
               ▼
 ┌───────────────────────────┐
 │   Decision Tree Model     │
 └─────────────┬─────────────┘
               │
               ├─────────────────────────┐
               ▼ (Confidence > 90%)      ▼ (Confidence < 90% OR Denied)
 ┌───────────────────────────┐ ┌───────────────────────────┐
 │   Automated Fast-Track    │ │   Escalation Queue        │
 │     Credit Approval       │ │ (Mandatory HITL Lockout)  │
 └───────────────────────────┘ └───────────┬───────────────┘
                                           │
                                           ▼
                               ┌───────────────────────────┐
                               │   Human Credit Officer    │
                               │  Manual Audit & Override  │
                               └───────────────────────────┘
