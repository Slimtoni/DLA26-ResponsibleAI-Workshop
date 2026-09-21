# Case 02 — Production-line defect detection

> *Draft for DLA 2026. All numbers are invented for teaching purposes — review before printing.*

## Context
A Mittelstand manufacturer (200 employees) produces mechanical components on a high-speed production line. Quality control is done at two points: one inline camera inspection at 120 parts/min, and a manual spot check by operators. The company is deploying an AI vision system on the inline camera to flag defects.

## The decision
- **Decision-maker:** the line operator at the inline station
- **Output:** part continues on the line (pass) / part is diverted to rework (fail)
- **Time pressure:** the line runs at 120 parts/min; each part gets ~3 s of the operator's attention
- **Volume:** ~300,000 parts/day across 3 shifts

## The AI's output
For each part: a pass/fail flag. On "fail", the part is automatically diverted to a rework bin. The operator sees the flag appear on a small screen and can override the diversion if they disagree.

**What the human sees:** one part on the conveyor, a pass/fail flag on the screen.
**What the AI sees:** a high-resolution image of the part from multiple angles.

## Error economy
| Error | Cost | Who bears it |
|---|---|---|
| False positive (divert a good part) | Rework labour, scrap of a good part, line slowdown | Factory (labour, material) |
| False negative (let a defective part through) | Customer complaint, recall, safety risk if the component is safety-relevant | Factory (reputation, cost) + customer (safety) |

## AI system card (vendor-provided)
- **Claimed accuracy:** 98.2% pass/fail on the vendor's test set
- **Known failure modes:** struggles with defects that only appear after assembly (not visible pre-assembly); occasionally flags parts with surface scratches that are within tolerance
- **What it can't see:** defects that develop later in the process; the functional behaviour of the part

## Regulatory context *(verify before the day)*
- If the component is safety-relevant (e.g., automotive), the quality process is subject to industry quality standards (e.g., IATF 16949) and liability rules
- Operator override is a logged event; the deployer remains accountable for the system's output
- No specific AI Act class, but the system is a high-stakes industrial quality gate
