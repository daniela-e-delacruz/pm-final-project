# Experimentation Plan (Module 5)

## Get your documents ready
- **From M3, your hypothesis sentence:** Based on the M2 persona dropping the system for spreadsheets when logging compliance checks during their shift, and on that step taking 14.6 minutes against a 3 minute benchmark with only 48% completion and a Compliance CSAT of 2.2, I believe that reducing the administrative burden of logging compliance checks for real-time fleet coordinators will result in them completing the checks inside RouteLogic, giving executives real-time data and reducing the complexity that 4 of 5 churned accounts cite. This will be measured by a 23 point increase in the percentage of coordinators who complete Log Compliance Checks, from 48% to 71%. I will protect Manager CSAT for Compliance at 3.9 or higher and will make a go/no-go decision 15 days after launch.
- **From M3, your primary success metric & guardrail metric:** Primary: The percentage of real-time fleet coordinators who complete Log Compliance Checks inside the daily workflow, moving from 48% to 71%. Supporting signal: average time to log compliance checks dropping from 14.6 minutes toward the 3 minute benchmark.
Guardrails: Manager CSAT for Compliance stays at 3.9 or higher, and Compliance Checklist adoption among coordinators stays at 77% or higher.
- **From M4, the feature you scoped in your PRD this is what you're testing:** B1 One-Click Compliance Checklist: coordinators open the compliance check from the shift view they are already working in, with the data RouteLogic already has pre-filled, and review, confirm and submit everything in one flow. Advanced enterprise compliance fields stay available but collapsed.

## Define your experiment parameters
- **Feature under test pull from your M4 PRD:** B1 One-Click Compliance Checklist, with the B5 Step Progress Indicator as part of its design. The coordinator opens the compliance check in one tap from the shift view she is already working in. Driver, vehicle, route and date are pre-filled from the active shift. She completes the whole check in one screen: pass or fail for each item, a reason for every failed item, and a review of the pre-filled data before submitting. Advanced enterprise compliance fields stay available but collapsed.
- **Persona pull your M2 persona:** A real-time fleet coordinator who keeps daily operations running and is responsible for logging compliance checks during her shift.
- **Expected outcome the behaviour change you expect, from your M3 hypothesis:** Coordinators complete their compliance checks inside RouteLogic during their shift, instead of leaving the flow and moving them to a spreadsheet. This way compliance records reach RouteLogic in real time and executives have the data they need to make decisions.
- **Primary success metric the one number that defines success, from M3:** The percentage of real-time fleet coordinators who complete Log Compliance Checks inside RouteLogic during their shift.
- **Baseline rate today's rate of your primary metric, from your M3 data:** 48%, the share of coordinators who reach the Log Compliance Checks step in the M3 data. The real completion rate can only be the same or lower, so the control group will confirm the actual baseline during the test.
- **Guardrail metric & boundary what must not break, and how far it can move before you investigate:** Manager CSAT for Compliance must stay at 3.9 or higher, and Compliance Checklist adoption among coordinators must stay at 77% or higher. If either one drops below its limit, I will investigate before making a decision.
- **Minimum Detectable Effect (MDE) the smallest improvement worth shipping, your floor:** +10 percentage points, from 48% to 58%. A smaller increase would not justify the effort and risk of changing the flow. If the result reaches 10 points but not more, I would still ship and analyze the segments to understand why it wasn't higher.
- **Sample size per arm use the calculator in the builder, baseline + MDE:** 390 coordinators per arm, 780 in total. The pilot starts with the 3 largest accounts. If they have fewer than 780 coordinators, I will add the next largest accounts until the sample is reached, since extending the test doesn't add new coordinators and the feature flag keeps the risk low.
- **Traffic split & test duration 50/50 standard · cover ≥ 2 weekly cycles:** 50/50 between control and variant, randomized by coordinator. This split needs the smallest total sample to reach 390 coordinators per arm, and the risk is low: the feature flag allows instant rollback, enterprise fields stay available, and no check is submitted without the coordinator's confirmation. The test runs for 15 days to cover two full weekly cycles and avoid day-of-week and novelty effects. Manager CSAT will be read at the end of the 4-week pilot, since it takes longer to update.
- **Significance threshold p < 0.05 is standard, explain any deviation:** p < 0.05. I'm not using a stricter threshold because the feature flag allows an immediate rollback, so a wrong decision is easy to reverse technically. I'm not relaxing it either, because a wrong rollout still has a cost: the CS lead would have communicated and trained the accounts on a change that doesn't work, coordinators would have to relearn the old flow, and the enterprise account already evaluating a competitor would lose trust in RouteLogic.

## Define your control and variant
- **Control (A) the current experience, reference your M2 moment of misery and M3 funnel/workflow data:** The current compliance logging flow. When the coordinator logs a compliance check during her shift, she has to go through four screens while other operational tasks are waiting. By the fourth screen, time pressure pushes her out of RouteLogic, and she switches to a spreadsheet to load the checks later (M2 moment of misery). In the M3 data, Log Compliance Checks takes 14.6 minutes against a 3-minute benchmark, only 48% of coordinators reach the step, and coordinators rate Compliance at 2.2 CSAT.
- **Variant (B) your single change, copy the relevant screens & functional requirements from your M4 PRD:** B1 One-Click Compliance Checklist, with the B5 Step Progress Indicator as part of its design. The test measures the impact of the package; it can't separate the contribution of each feature.

Screens:

- Home: the coordinator's shift view with a "Log compliance check" action next to each active route.
- Core: the full compliance check in one screen: pre-filled data, pass or fail for each item, a review section and collapsed enterprise fields.
- Confirmation: a success message with the time the check was saved and a button to go back to the shift view.

Functional requirements:

- The system must open the compliance check in one tap from the shift view.
- The system must pre-fill driver, vehicle, route and date from the active shift.
- The system must let the coordinator complete the full check without leaving the core screen.
- The system must require a reason for every failed item before the check can be submitted.
- The system must show all pre-filled values for review before submitting.
- The system must keep advanced enterprise compliance fields collapsed by default and open them in one tap.
- The system must save the check with a timestamp as soon as it is submitted, in the same compliance record managers use today.
- **Isolation check, what has NOT changed? list everything identical between arms (app version, recommendation engine, notifications, onboarding). If something changed inadvertently, your test is compromised.:** Everything except the compliance logging flow stays identical between both groups:

- Product: same RouteLogic version, same features outside compliance, same notifications and same shift view (except the new "Log compliance check" action in B).
- Checklist content: the same compliance items to review and the same required fields, including the enterprise fields, which are only collapsed in B, not removed.
- Data: both groups save the check in the same compliance record managers use today, and completion is measured the same way in both groups.
- Workload: random assignment by coordinator should keep the amount of data to load and the active hours similar between groups. I will check that both groups are balanced before reading the results.
- Communication: no training or announcements about the new flow during the test. The CS lead only supports the B group with the new flow if needed, and does not tell coordinators in group A about the change, so their behavior doesn't change.

## Formalize your hypothesis & shipping criteria
- **Your hypothesis (filled in):** I believe that the B1 One-Click Compliance Checklist for real-time fleet coordinators will result in them completing compliance checks inside RouteLogic during their shift instead of moving them to a spreadsheet, as measured by a 23 percentage point increase (from 48% to 71%) in the percentage of coordinators who complete Log Compliance Checks within 15 days. We will protect Manager CSAT for Compliance (3.9 or higher) and Compliance Checklist adoption among coordinators (77% or higher) throughout the test.
- **Your shipping criteria (filled in):** We will SHIP if the percentage of coordinators who complete Log Compliance Checks improves by at least 10 percentage points at p < 0.05, and Manager CSAT for Compliance does not drop below 3.9 and Compliance Checklist adoption does not drop below 77% after 15 days (with Manager CSAT confirmed at the end of the 4-week pilot).

We will ITERATE if the direction is positive but the lift is below 10 percentage points or not significant.

We will INVESTIGATE if the primary metric meets the ship criteria but a guardrail crosses its boundary, or a segment gets worse, especially the enterprise account at risk.

We will KILL if the primary metric shows no improvement or moves negatively.

The read date is fixed at the end of the 15 days; no results reviewed before this date.
- **Hardest parameter to define, and did it change your hypothesis? quick debrief:** The hardest parameter was the traffic split, but not because of the concept: my first instinct was 50/50, and I changed it because it seemed too obvious. Working through it, I realized the standard answer was right for my case: the risk is low and any other split would need more coordinators. It didn't change my hypothesis. Defining the MDE made me separate two things: my hypothesis is what I believe will happen (+23 points, from 48% to 71%), while the MDE is the floor for my decision to ship (+10 points). One is a prediction, the other is a decision rule.
