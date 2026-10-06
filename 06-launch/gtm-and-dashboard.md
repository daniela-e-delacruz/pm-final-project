# GTM Strategy & Success Dashboard (Module 6)

**Scenario:** RouteLogic (B2B)

**Feature:** B1 One-Click Compliance Checklist

## Goal

**Engagement.** Coordinators already use RouteLogic and start logging compliance checks, but they abandon the flow because it doesn't work for them, so today their habit is to leave the feature and use a spreadsheet. The goal is not to make them aware of the product or to win new customers, but to bring an existing behavior back inside RouteLogic: completing compliance checks during their shift.

## Audience

**Primary:** real-time fleet coordinators who log compliance checks (77% of coordinators), starting with the largest accounts, where the enterprise account currently evaluating a competitor is.

**Secondary:** managers who rely on compliance records and the enterprise fields, so they know these fields are still available and only collapsed, and the executive team, who will move from delayed compliance data to real-time data for their decisions.

## Launch tier: M, Targeted

**Reach:** the launch reaches our existing base, the coordinators who log compliance checks (77% of coordinators). New users will learn the new flow from the start, without the spreadsheet habit current users have. We don't need to reach anyone outside our base, so a multi-channel launch with press or paid media isn't justified.

**Revenue impact:** B1 doesn't generate new revenue, but it protects retention. 4 of 5 churned accounts cite complexity, and our largest account is already evaluating a leaner competitor.

**Risk of silence:** B1 moves the compliance check to the shift view. If we don't tell coordinators, they won't find where to log their checks, and they will abandon from the start instead of trying and leaving under time pressure. Managers could also think the enterprise fields were removed, when they are only collapsed.

## Channels

1. **Owned · In-app message in the shift view**, where coordinators work every day. It shows them where to log compliance checks now, so they don't look for the old flow and abandon.
2. **Earned · Word of mouth from pilot coordinators.** In each large account, a coordinator who used B1 during the pilot shares her experience with her peers in the launch session. A coordinator trusts another coordinator more than a message from RouteLogic.
3. **Owned · Direct communication to managers and executives**, by email and in account meetings, explaining that the enterprise fields are still available and that compliance data will reach them in real time. The CS lead covers the enterprise account and the account managers cover the other large accounts; smaller accounts receive it by email.

## Enablement & assets

The CS lead is the key person for this launch, so before going live I will give her a short enablement brief:

- **What it is:** B1 lets coordinators log compliance checks in one flow during their shift, instead of going through four screens.
- **What it does:** it opens in one tap from the shift view, pre-fills the driver, vehicle, route and date, and lets them complete the whole check in one screen. Enterprise fields are still there, just collapsed.
- **What changes and what doesn't:** the compliance check moves to the shift view and replaces the old flow, it is not one more button. The checklist items, the enterprise fields and the record managers use stay the same.
- **If a coordinator asks why she should change a process that works for her:** with B1 she logs the check once, during her shift, instead of writing it in a spreadsheet and loading it later. She meets her daily logging without extra effort and without piling up work when other tasks need her attention.
- **If a manager asks if the enterprise fields were removed:** they are all still available, just collapsed, and checks are saved in the same record as today. The difference is that data now arrives in real time, so analysis is faster and decisions can be made when they're needed.

**Assets we need to build:**

1. An in-app message in the shift view showing coordinators where to log compliance checks now (designer).
2. A short launch session in each large account, led by the CS lead, where a coordinator from the pilot shares her experience (CS lead).
3. A one-page guide for managers explaining what changes and what doesn't (CS lead).
4. A short demo video of the new flow for coordinators who can't join the session (designer).

## Ownership & budget

I own the GTM plan, the launch tracker and the post-launch metrics. The CS lead owns the enablement brief, the launch sessions in the largest accounts, starting with the enterprise account at risk, and the one-page guide for managers. Since she is a single person for every account, the account manager of each large account will support her with the sessions and the communication with managers and executives, and Sales will get the same enablement brief before launch because they are not part of the core team. To make this manageable, only large accounts get a live session with a pilot coordinator sharing her experience, while smaller accounts get the in-app message, an email and the demo video. The designer owns the in-app message and the demo video, and one engineer owns the feature flag rollout and the completion tracking for the 48% to 71% metric. The engineer also tracks how many coordinators open B1 from the shift view, since the bad signal depends on it. The CS lead sends the email to smaller accounts and invites one pilot coordinator per large account, with her manager's approval. If the designer can't produce the demo video, we replace it with a short step-by-step guide with screenshots. No extra budget is needed, since all channels are owned or earned.

## Timeline

Phase 1 is the beta, during weeks 1 to 4: the pilot runs in the largest accounts with the M5 experiment, I read the results on day 15 and confirm Manager CSAT at the end of week 4. We only move to Phase 2 if the experiment meets the ship criteria. Phase 2 is the launch, during weeks 5 to 8: in week 5 the CS lead and the account managers get the enablement brief, and the in-app message, the manager guide and the demo video are ready. From week 6, the CS lead runs the launch sessions in the large accounts, starting with the enterprise account, while smaller accounts receive the in-app message, the email and the video. Phase 3 is post-launch, from week 9 onward: I track adoption velocity, error rate and Manager CSAT for Compliance, and decide whether to double down, iterate or adjust the rollout.

## Success metrics

The main metric is the percentage of coordinators who complete Log Compliance Checks inside RouteLogic during their shift, from 48% to 71%, the same metric I validated in the experiment. I will also track the average time to log a compliance check, from 14.6 minutes toward the 3-minute benchmark, and the time to first completed check after launch: each coordinator should complete her first check with B1 within one week of launch in her account, which covers the daily changes in logging volume. Manager CSAT for Compliance stays as the guardrail at 3.9 or higher.

## Bad signal to watch for

Fewer than 48% of coordinators open B1 within two weeks of launch in their account, fewer than reach the compliance step today = resistance to change or they can't find it. I interview coordinators to understand which one and iterate on training and communication.

## Most likely post-launch decision

Iterate, because solving this problem is necessary: the data and the problem hook prove it, the value proposition is solid and the cost is low for the reach we identified. The trigger would be completion moving above the 48% baseline but staying below 58%, my MDE from M5. In that case I would only change the communication, with more training and pilot coordinators sharing their experience in more accounts.
