# DLA 2026 — Scenario Task: Design a Responsible AI Decision-Support System

## Your task

Your team (4–5 people) is the project team of a company that is deploying an **AI-based decision-support system (DSS)**.

**Main task:** design a **responsible DSS** for your scenario. The design must address **stakeholder needs** and **socio-technical requirements** — legal, ethical, and organisational — and apply the concepts from the theory input: **appropriate reliance, (X)AI literacy, and responsible application of Explainable AI (XAI)**.

**Output:** one **A2 poster** per team. The poster is the basis for the red team and your final 1-minute deployment pitch.

## How the day works

- Session 2 (from 11:10): **P1** decision & risks (20 min) → theory input → **P2** predict behaviour (25 min)
- Lunch — a real break
- Session 3: morning's results + what they mean for your design → **P3** design (40 min) → **P4 red team** — another team writes attacks on your poster (15 min) → **P5** one revision (10 min) → plenary: **1-min deployment pitch** per team

Theory input comes in short pulses — right before you need each concept.

## Working principles

1. **Red line first.** Before designing anything, write one statement: *"This system must never ___."* Everything else is checked against it.
2. **Affected person is a mandatory input.** Design for the decision-maker, *and* answer what the affected person (rejected applicant, patient, denied borrower) is entitled to know and influence.
3. **Filled in backwards.** Outcome and error economy first, target reliance behaviour second, the human as they are, and only then the explanation. Left alone, teams start at the explanation and design a dashboard.
4. **Design for the human as they are** — realistic literacy, realistic time pressure, realistic incentives.
5. **Roles.** Each team member takes one role card (decision-maker / affected person / regulator / skeptic). Your design must satisfy all four.

## Poster structure

Structure your A2 around these zones:

| Zone | Contents |
|---|---|
| **P1 Decision & risks** | Stakeholders · decision without AI · error economy (cost of FP vs FN, who bears each) · **red line statement** |
| **P2 Predict behaviour** | The 2×2: which quadrant failure is the real risk here · what the user *actually* does at their realistic (X)AI literacy |
| **P3 Design** | XAI: whom/what/when, which form, **what NOT to show and why** · beyond explanation: legal, training, workflow friction, defaults, timing, accountability |
| **Evidence** | One *behavioural* indicator that would show it worked (not satisfaction, not trust) + how you would measure it |
| **Attack surface** | *(filled by another team in the red team)* |
| **Revision** | One change in response to the strongest attack |

## Guiding questions

### All teams

- Who are the stakeholders?
- How does the decision look like without an AI-based DSS?
- Which risks when using an AI-based DSS?
- Which human behaviour do you expect in the interaction with the AI (under-reliance, over-reliance)?

### XAI-related questions

- **Whom** do you explain to, **what**, and **when** — at the decision moment, in training/onboarding, in audit, or to the *affected person* (explanation duty)?
- **What will you NOT show, and why** — explanation overload, explanation wrongness, cost of the user's attention?
- **Explanation wrongness:** if the explanation is wrong or misleading, can the user detect that? What protects them?
- **Uncertainty:** should the system display uncertainty — and can this user actually use it?
- **Literacy match:** what does "understood" mean for *this* user at *their* realistic (X)AI literacy — not the idealised one?
- **Method choice:** instance-based (saliency, SHAP) vs concept-based (SemanticLens) vs plain language — which fits which stakeholder?

### Further questions

- How could **(X)AI literacy** help — and whose job is it to build: training, UX, or regulation?
- **Accountability:** when the system errs, who is liable — operator, deployer, vendor? How is that distributed?
- **Red lines:** what would you *refuse* to deploy in this scenario, and why?
- **Longevity:** what breaks in 3 years — model drift, staff turnover, regulation change?

## Your case

Your case is **assigned, not chosen** (each pulls in a different direction: over- vs. under-reliance). Your case consists of two files:

- `cases/0X-<case>.md` — the case brief: context, decision, AI output, error economy, what the human sees vs. what the AI sees, the AI system card (vendor-provided), and regulatory context
- `stakeholder-cards/0X-<case>-stakeholders.md` — stakeholder cards: goals, fears, what they want to know, what they are entitled to

> **No solution hints in the case briefs** — that is deliberate. The design is yours.
