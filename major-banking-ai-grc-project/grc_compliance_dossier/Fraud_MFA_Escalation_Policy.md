# Operational Policy: Fraud Mitigation and MFA Escalation Thresholds
**System ID:** AI-POLICY-FRAUD-MFA  
**Framework Alignment:** COBIT 2019 (DSS05 - Managed Security Services) & NIST Cybersecurity Framework (Detect & Protect Functions)

## 1. Executive Summary
Technical performance verification of the Transaction Fraud Detection Engine (v1.0) indicated an aggressive over-sensitivity profile. While raw fraud capture rates meet baseline security goals, the resulting **False Positive rate** introduces severe operational bottlenecks by locking non-fraudulent consumer accounts during international or off-hour activity. This policy framework establishes structured operational mitigation thresholds.

## 2. Multi-Tiered Transaction Enforcement Architecture

Instead of allowing the AI model to execute a hard, autonomous block on a customer's banking account, the system must filter output probabilities into an automated three-tier escalation grid.

```text
 ┌─────────────────────────────┐
 │ Transaction Request Initiated│
 └──────────────┬──────────────┘
                │
                ▼
 ┌─────────────────────────────┐
 │  Fraud AI Probability Score │
 └──────────────┬──────────────┘
                │
     ┌──────────┼──────────┐
     ▼ (<30%)   ▼ (30%-75%)▼ (>75%)
 ┌───────┐ ┌─────────────┐ ┌──────────────┐
 │APPROVE│ │ CHALLENGE   │ │ HARD BLOCK   │
 │Transaction│ (Automated  │ │ Route to     │
 │Logs   │ │ SMS / MFA)  │ │ Fraud Ops Team│
 └───────┘ └─────────────┘ └──────────────┘

