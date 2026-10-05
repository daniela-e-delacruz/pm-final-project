# B1 One-Click Compliance Checklist, Simplified PRD (RouteLogic)

**Author:** Me · **Status:** Draft · **Target:** High-Fidelity Prototype · **Persona:** The Real-Time Fleet Coordinator, logging compliance checks during her shift

## 1. The Big Picture
- **Vision:** To eliminate the administrative burden that makes real-time fleet coordinators drop the system, by turning a 14.6 minute compliance check across four screens into one pre-filled flow they can finish during their shift.
- **Press release:** Today, RouteLogic launched the One-Click Compliance Checklist for real-time fleet coordinators. Logging a compliance check used to take 14.6 minutes across four screens while other tasks were waiting, so coordinators dropped the system mid shift and used spreadsheets to load the checks later. This meant compliance records reached RouteLogic late and executives didn't have real-time data to make decisions.

With the new checklist, coordinators open the check from the shift view they are already working in, the data RouteLogic already has is pre-filled, and they review, confirm and submit everything in one flow. Advanced enterprise compliance fields are still available, just out of their way. The goal is that coordinators complete their compliance checks inside RouteLogic during their shift, and managers keep getting the complete records they rely on, now in real time.
- **Success metric:** % of coordinators completing Log Compliance Checks: 48% to 71%
- **Guardrail:** Manager CSAT for Compliance stays at 3.9 or higher

## 2. The Details
### User stories
- 1 - As a real-time fleet coordinator, I want to open the compliance check from the shift view I'm already working in, so that I don't have to leave my workflow to log it.
- 2 - As a real-time fleet coordinator, I want the data RouteLogic already has to be pre-filled, so that I only spend time on what needs my input.
- 3 - As a real-time fleet coordinator, I want to complete the whole check in one screen, so that I can finish it during my shift instead of moving it to a spreadsheet.
- 4 - As a real-time fleet coordinator, I want to review pre-filled data before submitting, so that I can trust the record is correct.
- 5 - As a manager, I want the advanced compliance fields to stay available, so that I keep the complete records I rely on.
### Screens to build
- 1 - Home, the coordinator's shift view with a "Log compliance check" action next to each active route
- 2 - Core, the full compliance check in one screen: pre-filled data, pass or fail for each item, a review section and collapsed enterprise fields
- 3 - Confirmation, a success message with the time the check was saved and a button to go back to the shift view
### Functional requirements
- 1 - The system must open the compliance check in one tap from the shift view.
- 2 - The system must pre-fill driver, vehicle, route and date from the active shift.
- 3 - The system must let the coordinator complete the full check without leaving the core screen.
- 4 - The system must require a reason for every failed item before the check can be submitted.
- 5 - The system must show all pre-filled values for review before submitting.
- 6 - The system must keep advanced enterprise compliance fields collapsed by default and open them in one tap.
- 7 - The system must save the check with a timestamp as soon as it is submitted, in the same compliance record managers use today.
### Smart behaviors (Situation → Outcome)
- If an item is marked as failed → a reason field shows up below it and has to be completed
- If she changes a pre-filled value → the field shows as edited in the review section
- If she taps submit and a reason is missing → the field gets highlighted with a message saying what's missing
- If she opens the enterprise section → the advanced fields open in the same screen
- If the check is submitted → the confirmation screen shows the time it was saved and the route shows as checked in the shift view
### Technical constraints
- Single file React prototype; React useState only; no external API calls; no database or real authentication; use mock data for one coordinator shift with 3 routes, drivers and vehicles, and a checklist of 6 compliance items; no AI fill for fields without existing data; no mobile layout; do not remove any enterprise compliance field, keep them collapsed.

## 3. The Logistics
### Features out
- No AI fill for fields that don't have data; no mobile version; no changes to manager reports or audit export; no removing enterprise compliance fields; no login, settings or check history beyond the current shift.
### Edge cases & safety guard
- If a pre-filled field has no data → it shows empty and she completes it; if an enterprise field is required for the account → the section opens and the field is marked before she can submit; if the route was already checked → it shows as checked and can only be viewed; if she leaves before submitting → a message tells her the check isn't saved; if every item fails → she can submit once all the reasons are completed. Safety: never invent values for fields without data, never submit a check without her confirmation, never remove enterprise fields or make them unreachable.
### Decision log
- Pre-filled only the fields RouteLogic already has instead of using AI for the rest, so B1 fits in a 4 week pilot with 2 engineers. Kept enterprise compliance fields collapsed instead of removing them, so the coordinator's flow is simpler without breaking the records managers use.
### Evals
- Accuracy: pre-fill, smart behaviors and edge cases respond correctly in 100% of test scenarios. Time on task: a full check is completed in 3 minutes or less, the benchmark. Safety: 0 checks submitted without her confirmation, with a failed item missing its reason or with a required enterprise field empty, and 0 invented values.

## MoSCoW scope
- **Must:** Open the check from the shift or route view she is already working in; Pre-fill fields that already exist in RouteLogic (vehicle, driver, route, date); Complete the full check in one flow, without moving across four screens; If an item fails, ask for the reason before submitting; Coordinator reviews and confirms pre-filled data before submitting; Advanced enterprise compliance fields stay available but collapsed; The submitted check is saved in real time, in the same record and with the same audit requirements as today
- **Should:** Step Progress Indicator (B5); Save the check as a draft and resume it if she gets interrupted; Completion tracking to measure the 48% to 71% metric; Turn the feature on only for the 3 pilot accounts, with a way to switch it off
- **Could:** Remember the last values each coordinator used; Confirm several checks at once
- **Won't (now):** AI fill for fields with no existing data source; Mobile version (B4); Changes to manager reports or audit export (B9); Removing any enterprise compliance field

---
**Builder hook:** Build a working prototype based on this PRD. Use the User Story as the core flow, Functional Requirements as build constraints, and prioritize speed and clarity over visual complexity.
