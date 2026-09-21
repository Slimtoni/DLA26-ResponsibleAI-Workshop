# Case 04 — Emergency-department triage

> *Draft for DLA 2026. All numbers are invented for teaching purposes — review before printing.*

## Context
A hospital with 400 beds runs an emergency department receiving ~80 patients/day. Triage nurses decide how urgently each patient is seen. The hospital is deploying an AI triage assistant that computes a triage category from the patient's reported symptoms and vital signs.

## The decision
- **Decision-maker:** the triage nurse (expert, 5–20 years of experience)
- **Output:** triage category 1 (immediate) / 2 (urgent) / 3 (priority) / 4 (standard) / 5 (minor)
- **Time pressure:** ~2 min per patient at the door; the waiting area holds ~30 patients
- **Volume:** ~80 patients/day

## The AI's output
For each patient: a recommended triage category and the two symptoms that contributed most to the score. The nurse can accept the category or override to any other category; overrides are logged.

**What the human sees:** the patient in front of them — history-taking, physical observation, vital signs, the patient's appearance and state.
**What the AI sees:** the structured symptom list and vital signs — nothing more. It does not see the patient.

## Error economy
| Error | Cost | Who bears it |
|---|---|---|
| Under-triage (send a critical patient too late) | Delayed treatment, potentially fatal | Patient + hospital (liability) |
| Over-triage (treat a minor patient too urgently) | Wasted capacity, longer wait for other patients | Hospital (capacity) + other patients |

In a resource-constrained ED, both matter — but under-triage is the catastrophic one.

## AI system card (vendor-provided)
- **Claimed accuracy:** 91% agreement with experienced nurses on a validation cohort
- **Known failure modes:** performs worse for children (fewer training data) and for atypical presentations ("the story that doesn't fit"); no access to the patient's context beyond the structured input
- **What it can't see:** anything that is not typed in — the look of the patient, their distress, inconsistencies in their story

## Regulatory context *(verify before the day)*
- Medical device regulation: the system is likely a **medical device** (MDR) — classification depends on the risk class of the decisions it influences
- AI Act: healthcare use cases are **high-risk**
- Professional norms: the nurse's clinical judgement is legally protected and expected to prevail — but every override is logged and can be reviewed, which creates a subtle pressure to follow the system
