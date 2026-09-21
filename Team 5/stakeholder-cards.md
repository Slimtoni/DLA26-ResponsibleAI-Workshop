# Stakeholder cards — Payments fraud review

### Card A: Fraud analyst (decision-maker)
- **Goal:** clear the queue in 4 h without letting fraud through
- **Fear:** cancelling a legitimate order and getting the complaint; releasing fraud and getting the loss
- **Wants to know:** whether the one-line reason is real; what the model actually saw
- **Entitled to:** the full order history; a system whose reasons they can verify; no queue that grows faster than they can clear

### Card B: Customer (affected person)
- **Goal:** get their product; if the order is cancelled, know why and get their money back
- **Fear:** being treated like a criminal for a legitimate purchase — or having their identity stolen and *not* being believed
- **Wants to know:** the reason for the cancellation; how to contest it; that their data wasn't the cause
- **Entitled to:** GDPR Art. 22 rights — human review, contestation, a reason

### Card C: Company management
- **Goal:** keep fraud loss and customer harm in balance
- **Fear:** the false-flag rate creeping up (vendor says 3%, their own data says 5%); the generated reasons being *wrong* in a way that misleads analysts into the wrong direction
- **Wants to know:** the actual error rates on *their* data; why the reason text doesn't always match the data
- **Entitled to:** (as deployer) honest vendor benchmarks, monitoring, and a documented escalation path
