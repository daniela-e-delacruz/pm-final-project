# Feature Roadmap, Module 4 · RouteLogic Velocity

**Team:** 2 engineers + 1 designer + 1 CS lead

## Strategic anchors
- **Persona:** The Real-Time Fleet Coordinator, logging compliance checks during her shift
- **Primary metric:** % of coordinators completing Log Compliance Checks in the workflow: 48% to 71%
- **Moment of misery:** Compliance logging takes 14.6 min vs 3 min benchmark, so she drops the system mid shift
- **Guardrail:** Manager CSAT for Compliance stays at 3.9 or higher

## Scoring
| Feature | Value | Effort | Quadrant | Decision | Rationale |
|---|---|---|---|---|---|
| B1 One-Click Compliance Checklist | 5 | 2 | Quick Win | Now | Directly moves the 48% to 71% metric; pilot scoped to fields that can already be pre-filled. |
| B2 Smart Daily Report Auto-Fill | 3 | 4 | Time Sinker | Later | Helps the 18% daily report rate, but it's not where coordinators drop off. |
| B3 Shift Handoff Wizard | 2 | 3 | Time Sinker | Later | Saves 6.8 min/day, but outside the compliance step. |
| B4 Mobile-First Coordinator Dashboard | 3 | 5 | Time Sinker | Later | Only feature tied to M2 evidence (BUG-2079, UXR-11), but too big for a 4 week pilot |
| B5 Step Progress Indicator | 3 | 1 | Fill-In | Now | Knowing how many steps are left can reduce abandonment; bundled into B1's design. |
| B6 Driver Alert Notifications | 1 | 4 | Time Sinker | Cut | Serves drivers, not the coordinator's logging friction. |
| B7 Contextual AI ETA Display | 1 | 3 | Time Sinker | Cut | ETA has nothing to do with compliance; 11% adoption shows low relevance. |
| B8 Fleet Analytics Manager View | 1 | 5 | Time Sinker | Cut | The real-time data executives need comes from coordinators logging on time, which B1 solves; a new dashboard would only show late data faster. |
| B9 Compliance Audit Trail Export | 2 | 2 | Fill-In | Next | Doesn't move completion, but can protect the manager CSAT guardrail. |
| B10 In-App Coordinator Training | 1 | 3 | Time Sinker | Cut | No data shows onboarding drives the drop-off. |

## Roadmap
### NOW, Pilot (4 weeks, 3 accounts)
- **B1 One-Click Compliance Checklist**, Directly moves the 48% to 71% metric; pilot scoped to fields that can already be pre-filled.
- **B5 Step Progress Indicator**, Knowing how many steps are left can reduce abandonment; bundled into B1's design.

### NEXT, GA Release (weeks 5-8)
- **B9 Compliance Audit Trail Export**, Doesn't move completion, but can protect the manager CSAT guardrail.

### LATER, backlog
- **B2 Smart Daily Report Auto-Fill**, Helps the 18% daily report rate, but it's not where coordinators drop off.
- **B3 Shift Handoff Wizard**, Saves 6.8 min/day, but outside the compliance step.
- **B4 Mobile-First Coordinator Dashboard**, Only feature tied to M2 evidence (BUG-2079, UXR-11), but too big for a 4 week pilot

### ✂ Cut List
- **B6 Driver Alert Notifications**, Serves drivers, not the coordinator's logging friction.
- **B7 Contextual AI ETA Display**, ETA has nothing to do with compliance; 11% adoption shows low relevance.
- **B8 Fleet Analytics Manager View**, The real-time data executives need comes from coordinators logging on time, which B1 solves; a new dashboard would only show late data faster.
- **B10 In-App Coordinator Training**, No data shows onboarding drives the drop-off.
