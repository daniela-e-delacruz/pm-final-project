# RouteLogic Velocity · One-Click Compliance Checklist

> Real-time fleet coordinators log their compliance checks in one flow during their shift, without the administrative burden and without losing the enterprise features.

**Daniela De La Cruz** · Product Management Cohort · Sep 2026 (Weekdays)

- **Repo:** https://github.com/daniela-e-delacruz/pm-final-project
- **Prototype:** https://daniela-e-delacruz.github.io/pm-final-project/04-roadmap/b1-compliance-checklist-prototype.html
- **Deck (HTML):** https://daniela-e-delacruz.github.io/pm-final-project/06-launch/final-presentation.html

---

## Slide 5 · Strategy

**Problem hook**

We must stop the lack of engagement of real-time fleet coordinators because logging compliance checks is such an administrative burden that they drop the system by the 4th screen and switch to spreadsheets, delaying compliance records and the real-time tracking that executives need.

**Value proposition**

For real-time fleet coordinators, we will allow them to register compliance checks within RouteLogic, keeping advanced enterprise features available but out of their way, because this process is an administrative burden that affects real-time operations and the statistics the executive team uses to make decisions now, giving competitors an opportunity to win our biggest account.

**Data-backed hypothesis**

> Based on the M2 persona dropping the system for spreadsheets when logging compliance checks during their shift, and on that step taking 14.6 minutes against a 3 minute benchmark with only 48% completion and a Compliance CSAT of 2.2, I believe that reducing the administrative burden of logging compliance checks for real-time fleet coordinators will result in them completing the checks inside RouteLogic, giving executives real-time data and reducing the complexity that 4 of 5 churned accounts cite. This will be measured by a 23 point increase in the percentage of coordinators who complete Log Compliance Checks, from 48% to 71%. I will protect Manager CSAT for Compliance at 3.9 or higher and will make a go/no-go decision 15 days after launch.

---

## Slide 6 · Research

**Competitive analysis / workaround**

Today, when coordinators log a compliance check during their shift, they drop RouteLogic at the fourth screen and use a spreadsheet as a shadow compliance log. They write the check there to get back to operations, and later they have to load it again into RouteLogic. The work is done twice and the system stays out of date in the meantime. The interviews don't talk about compliance directly, but they show the same pattern: users move core tasks to texting, WhatsApp groups and paper manifests (UXR-01, UXR-02, UXR-12). That's why this still needs new interviews to be validated.

**Journey map**

- **Today:** the compliance check is due during her shift → she goes through the logging screens while other tasks are waiting → at the fourth screen, under time pressure, she leaves RouteLogic (**the moment of misery**) → she writes the check in a spreadsheet → later she loads it again into RouteLogic.
- **With B1:** the check is due → she opens it in one tap from the shift view → she completes it in one screen with the data already pre-filled → she goes back to operations with nothing pending → executives see the record in real time.

---

## Slide 7 · Blueprint

**Prioritisation / roadmap**

I scored 10 features by value and effort for a team of 2 engineers, 1 designer and 1 CS lead.

| Now (4-week pilot in 3 accounts) | Next (GA, weeks 5-8) | Later | Cut |
|---|---|---|---|
| B1 One-Click Compliance Checklist, the quick win that directly moves the 48% to 71% metric, with B5 Step Progress Indicator bundled into its design. | B9 Compliance Audit Trail Export, which doesn't move completion but protects the manager CSAT guardrail. | B2 Smart Daily Report Auto-Fill, B3 Shift Handoff Wizard and B4 Mobile-First Coordinator Dashboard, useful but outside the compliance step or too big for the pilot. | B6, B7, B8 and B10, because they don't address the coordinator's logging friction. |

**PRD highlights**

The coordinator opens the compliance check in one tap from the shift view she is already working in. Driver, vehicle, route and date are pre-filled, and she completes the whole check in one screen: pass or fail for each item, a required reason for every failed item, and a review before submitting. Enterprise compliance fields stay available but collapsed. Success metric: coordinators completing Log Compliance Checks from 48% to 71%, protecting Manager CSAT at 3.9 or higher. Key decision: we only pre-fill data RouteLogic already has, with no AI fill, so B1 fits in a 4-week pilot, and we never invent values or submit a check without her confirmation.

**[View prototype](https://daniela-e-delacruz.github.io/pm-final-project/04-roadmap/b1-compliance-checklist-prototype.html)**

---

## Slide 8 · Validation

A/B test inside the largest accounts, randomized by coordinator, 50/50 split, 15 days, with a feature flag for instant rollback.

**Hypothesis:** I believe the B1 One-Click Compliance Checklist for real-time fleet coordinators will result in them completing compliance checks inside RouteLogic during their shift, measured by a 23-point increase (48% to 71%) in coordinators who complete Log Compliance Checks within 15 days.

| Element | Detail |
|---|---|
| Control (A) | The current four-screen flow. |
| Variant (B) | B1, with the B5 Step Progress Indicator in its design. |
| Primary metric | % of coordinators who complete Log Compliance Checks (baseline 48%, MDE +10 points). |
| Guardrails | Manager CSAT for Compliance at 3.9 or higher and Compliance Checklist adoption at 77% or higher. |
| Sample | 390 coordinators per arm, p < 0.05. |

**Decision rules**

- **Ship** if completion improves by at least 10 points and no guardrail breaks.
- **Iterate** if it improves less or isn't significant.
- **Investigate** if a guardrail breaks or a segment gets worse, especially the enterprise account.
- **Kill** if there's no improvement.

Results are read only at the end of the 15 days.

---

## Slide 9 · Launch

**GTM strategy**

`Goal: Engagement` `Tier: M` `Owned: in-app message` `Earned: word of mouth` `Owned: managers & executives`

Goal: engagement. Coordinators already use RouteLogic, but their habit is to abandon the compliance flow and use a spreadsheet, so the goal is to bring that behavior back inside the system. Audience: coordinators who log compliance checks (77%), starting with the largest accounts and the enterprise account evaluating a competitor; managers and executives who rely on compliance records as secondary. Tier: M, because we only need to reach our existing base, and B1 protects retention instead of generating new revenue. Channels: an in-app message in the shift view (owned), word of mouth from pilot coordinators in the large accounts (earned), and direct communication to managers and executives (owned). The CS lead gets an enablement brief before launch, supported by the account managers.

**Success metrics**

I track the % of coordinators who complete Log Compliance Checks (48% to 71%), the average time to log a check (14.6 minutes toward 3), and the time to first completed check, which should happen within one week of launch in each account. Manager CSAT for Compliance stays at 3.9 or higher.

> **Bad signal:** fewer than 48% of coordinators open B1 within two weeks of launch in their account, which means resistance to change or they can't find it. In that case I interview coordinators and iterate on training and communication.

---

## Slide 10 · Story

**Friction points + aha moment**

The hardest part was M1, which I iterated three times. The qualitative research didn't cover my case, and later the quantitative data didn't support my second one, so I had to decide which analysis was more representative. Since I needed to understand behavior, I went with the quantitative data and made it explicit that the interviews didn't support it, because people don't complain about a workaround they think works. My aha moment was realizing that I already knew what I was doing, just in a different way. I was frozen and overwhelmed by the data until I started making decisions, and from that moment the work flowed and I learned to trust my own judgment.

**Key takeaways / what I would do next**

I already did the work of a PM in my current role, but without technique or documentation, and the course confirmed it. I'll start every initiative with a clear problem and value proposition, use a PRD to bring everything together, and run experiments with structure, since in my company we do A/B testing based on intuition, without defining the metric, the minimum lift or the decision rules first. Next, I would run new interviews with coordinators to validate the spreadsheet workaround and the compliance friction, which today is supported by the data but not yet by the qualitative research.

---

## Thank you

**Repo:** https://github.com/daniela-e-delacruz/pm-final-project · **Cohort:** Product Management Cohort · Sep 2026 (Weekdays)

**Submit to the learning platform.**
