# Case 06 — Predictive maintenance

> *Draft for DLA 2026. All numbers are invented for teaching purposes — review before printing.*

## Context
A logistics company operates a fleet of 40 electric delivery trucks. Each truck is fitted with sensors (temperature, vibration, battery state, brake wear). A predictive maintenance model forecasts the probability of a component failure over the next 7 days, so the fleet manager can schedule service before a breakdown.

## The decision
- **Decision-maker:** the fleet manager (5 years of experience) + the assigned maintenance technician
- **Output:** schedule a service visit (which component, when) / keep the truck in service / pull the truck from the fleet
- **Time pressure:** the fleet manager reviews alerts weekly; a truck pulled early loses a delivery day, a truck left running risks a breakdown on the road
- **Volume:** ~120 maintenance decisions/month across the fleet

## The AI's output
For each truck: a list of components with a 7-day failure probability and a recommended service window. The model is trained on 5 years of the fleet's own sensor data and service history.

**What the human sees:** the alert list, the probability, and (on demand) the sensor time-series.
**What the AI sees:** 5 years of sensor data from all 40 trucks, plus service records — but it has never *seen* a physical breakdown.

## Error economy
| Error | Cost | Who bears it |
|---|---|---|
| False positive (service a healthy truck) | Lost delivery day, service cost, technician time | Company |
| False negative (miss a real failure) | Breakdown on the road, delivery delay, safety risk, costly emergency repair | Company + customers (delayed deliveries) |

## AI system card (vendor-provided)
- **Claimed accuracy:** 88% of failures predicted at least 48 h in advance; 22% of alerts turn out to be unnecessary
- **Known failure modes:** the model is trained only on *sensor data* — it cannot learn failure modes that don't show up in the sensors (e.g., a driver's rough handling); the 22% false-alarm rate has been *increasing* over the last 2 quarters (drift, unexplained)
- **What it can't see:** the physical state of the component, the driving behaviour, or external conditions (road surface, weather)

## Regulatory context *(verify before the day)*
- No specific AI Act high-risk class, but the fleet is subject to vehicle safety regulations (driver safety, cargo safety)
- The technician's professional judgement is legally relevant — but every override is logged against the model's recommendation, creating a subtle pressure to follow the system
- The increasing false-alarm rate is itself a maintenance signal: the model is degrading, and the fleet manager must decide whether to trust it at all
