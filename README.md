# Patient Participation Tokenomics (Non-PHI)

**Rights Reserved, Unlicensed**

---

## Overview
This repository defines a **privacy-preserving tokenomics model** designed to incentivize consistent participation in health and wellness programs without storing **protected health information (PHI)** on-chain.  

The framework demonstrates how **streak-based rewards, inactivity penalties, and capped emissions** can align participant incentives with program sustainability. It is intended as a **reference model** for researchers, developers, and stakeholders exploring **Web3-enabled healthcare participation**.

---

## Purpose
- Encourage patients to attend and engage consistently in approved health sessions.  
- Reward healthy behavior streaks through milestone-based NFTs.  
- Protect program sustainability with conservative token issuance and decay rules.  
- Preserve privacy by keeping PHI completely off-chain.  

---

## Mechanism
- **Session → Token emission** per compliant session.  
- **Streaks → Milestone NFTs** unlock discount tiers (0%, 3%, 6%, 9%).  
- **Inactivity decay:**  
  \( D(t) = base \times e^{-k t} \)  
- **No-show penalty window** reduces subsequent emissions.  
- **Monthly emission cap** per participant.  
- **Treasury bound:** ensures sustainability over rolling 12 months.  

---

## Key Parameters
- `tiers`: [0, 3, 6, 9] (percent discounts)  
- `thresholds`: tokens required to unlock tiers  
- `penalty`: no-show penalty percent  
- `decay_k`: exponential decay rate per inactivity unit  
- `cap_monthly`: max tokens per month per participant  

---

## Data & Privacy
- **Verifiable Credentials (VCs)** attest session attendance (date, type enum only).  
- **No diagnoses, no notes, no PHI** are recorded.  
- Credentials follow **privacy-preserving issuance and revocation patterns**.  

---

## Repository Contents
- **`config.json`** — tokenomics parameters (tiers, decay, penalties, caps).  
- **`simulation.ipynb`** — Jupyter notebook simulating participant types (adherent, irregular, attrition) and treasury outcomes.  
- **`.gitignore`** — excludes system and notebook artifacts.  

---

## Key Performance Indicators (KPIs)
- Retention uplift vs. baseline  
- Discount liability vs. revenue margin  
- Token float and monthly issuance  
- Break-even month and 12-month treasury bound  

---

## Roadmap
- **Phase 1:** Simulation & KPI validation (current repo)  
- **Phase 2:** Pilot integration with non-PHI verifiable credential flows  
- **Phase 3:** Evaluation of large-scale applicability in healthcare/wellness ecosystems  

---

## Notes
- This repository contains **models and rules only**; it does **not mint tokens or NFTs**.  
- Designed for use with verifiable credentials frameworks (e.g., Aries/Indy).  
- Example only; not production financial advice.  

---

## Audience
This repo is intended for:  
- **Healthcare innovators** exploring tokenized incentives  
- **Web3 researchers** validating sustainability models  
- **Policy and grant stakeholders** evaluating privacy-preserving engagement approaches  

---

## Contact
For collaboration or research inquiries, please submit an **Issue** or reach out via the organization page.  

---
