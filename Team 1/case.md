# Case 01 — Loan denial under an explanation duty

> *Draft for DLA 2026. All numbers are invented for teaching purposes — review before printing.*

## Context
A mid-sized regional bank (120 employees). Retail credit team handles personal loan applications for employees and customers of the bank's clients. The bank is introducing an AI-based credit scoring system to support loan officers.

## The decision
- **Decision-maker:** one loan officer per application
- **Output:** approve / reject / escalate to a second officer
- **Time pressure:** ~5 min per file, ~15 files per day
- **Volume:** ~3,000 applications/year

## The AI's output
For each application: a risk class (low / medium / high), a default probability, and a recommendation (approve / reject). The system is *not* allowed to decide autonomously — a human must sign off.

**What the human sees:** the application form — income, employment, credit history summary, requested amount.
**What the AI sees:** the same, plus credit bureau data and 12 months of account behaviour.

## Error economy
| Error | Cost | Who bears it |
|---|---|---|
| False positive (reject a good borrower) | Lost revenue, lost customer, damage to the applicant's credit standing | Bank (revenue) + applicant (opportunity, credit record) |
| False negative (approve a bad borrower) | Bad debt, write-off | Bank |

## AI system card (vendor-provided)
- **Claimed accuracy:** 94% on a comparable bank's dataset (2024)
- **Known failure modes:** performs worse for self-employed applicants (limited data); occasionally misreads very recent credit changes
- **What it can't see:** the applicant's situation beyond the data it was trained on; one-off circumstances (e.g., a temporary income drop due to illness)

## Regulatory context *(verify article numbers against the consolidated text before the day)*
- AI Act: creditworthiness assessment for natural persons is a **high-risk** use case (Annex III) — likely applies
- GDPR Art. 22: automated individual decision with legal effect — human sign-off and a **right to an explanation** for the applicant are relevant
- The rejected applicant is entitled to know *why*
