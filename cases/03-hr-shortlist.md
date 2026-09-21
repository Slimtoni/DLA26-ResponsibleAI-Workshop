# Case 03 — HR shortlist ranking (Mittelstand)

> *Draft for DLA 2026. All numbers are invented for teaching purposes — review before printing.*

## Context
A Mittelstand company (350 employees) is recruiting 5 engineers for its production engineering department. The HR department receives ~200 applications. To manage the volume, the company uses an AI-based ranking system to produce a shortlist that a hiring manager reviews.

## The decision
- **Decision-maker:** the hiring manager (senior engineer) + HR
- **Output:** a ranked shortlist of ~10 candidates out of ~200; the hiring manager picks the final 5
- **Time pressure:** the hiring manager has ~30 min to review the shortlist; the full review of all 200 would take ~2 days
- **Volume:** ~40 hiring rounds/year, 5 positions each

## The AI's output
A ranked list with a match score per candidate. The hiring manager sees the score and a one-line summary per candidate; they can also pull the full CV. The system does not reject candidates — it only ranks.

**What the human sees:** the shortlist with scores, one-line summaries, and (on demand) the full CVs.
**What the AI sees:** the full CVs of all 200, plus a job description and historical hiring data.

## Error economy
| Error | Cost | Who bears it |
|---|---|---|
| Good candidate ranked too low (missed) | Lost talent, extended vacancy, the candidate goes to a competitor | Company (vacancy cost) + candidate (lost opportunity) |
| Bad candidate ranked too high (hired) | Hiring cost, poor performance, potential dismissal | Company + the candidate's new colleague |

## AI system card (vendor-provided)
- **Claimed accuracy:** "predicts successful hire 85% of the time" (vendor benchmark, 2025)
- **Known failure modes:** trained on the company's own past hires — may reproduce past hiring patterns, including any biases in them
- **What it can't see:** motivation, culture fit, or anything not written in the CV

## Regulatory context *(verify before the day)*
- AI Act: "significant access to goods and services" and recruitment use cases are **high-risk** (Annex III) — likely applies
- GDPR Art. 22: automated decision with legal effect — candidates must have the right to human review and to know why they were not shortlisted
- Anti-discrimination law: the ranking must not be based on protected characteristics; the vendor's "success" metric is a proxy and may encode bias
