# Patient Participation Tokenomics (Non-PHI)

All rights reserved, unlicensed.

## Purpose
Incentivize consistent participation in health programs without storing PHI on-chain. Rewards favor streaks and verified attendance, with conservative emissions and treasury protection.

## Mechanism Overview
- Session → Token emission (per compliant session).
- Streaks → Milestone NFTs unlock discount tiers (0%, 3%, 6%, 9%).
- Inactivity decay: D(t) = base * e^{-k t}.
- No-show penalty window reduces subsequent emissions.
- Monthly emission cap per participant.
- Treasury sustainability bound over rolling 12 months.

## Key Parameters
- tiers: [0, 3, 6, 9] (percent discounts)
- thresholds: tokens required to unlock tiers
- penalty: no-show penalty percent
- decay_k: exponential decay rate per inactivity unit
- cap_monthly: max tokens per month per participant

## Data & Privacy
- Use verifiable credentials (VCs) to attest attendance (no diagnoses, no notes).
- PHI stays off-chain; credentials carry minimal claims (date, attendance, type enum).

## Files
- config.json — parameters for tiers, thresholds, emission, decay, penalties.
- simulation.ipynb — cohort simulation for adherence/irregular/attrition and treasury impact.
- .gitignore — ignores OS and notebook artifacts.

## KPIs
- Retention uplift vs baseline
- Discount liability vs revenue margin
- Token float and monthly issuance
- Break-even month and 12-month bound

## Notes
- This repo defines rules and math; it does not mint tokens or NFTs.
- Attendance should be proven via VCs (e.g., Aries/Indy patterns) without PHI.
