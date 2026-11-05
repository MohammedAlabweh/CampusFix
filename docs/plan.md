# Project plan

The project runs in phases (Waterfall): literature review, requirements, system design, then development. The final report is due on 8 March 2027, so development finishes on 11 February, testing by 21 February, and the last two weeks go to writing.

- Supervisor: David Wyatt
- Time budget: 5 to 8 hours a week

## Deadlines

| Milestone | Due | What it needs |
| --- | --- | --- |
| PiP | 21 Jan 2027 | Literature review, requirements, design, plan, and a working demo |
| Development complete | 11 Feb 2027 | MVP loop working end to end |
| Final report | 8 Mar 2027 | Full report |
| Viva | 3 May 2027 | Demo and questions |

## Phases

| Phase | Dates | What it produces |
| --- | --- | --- |
| 1. Literature review | 5 to 29 Nov 2026 | Reading log; written review draft |
| 2. Requirements analysis | 30 Nov to 13 Dec 2026 | Student survey; Estates interview if possible; user stories; prioritised requirements (MoSCoW); use cases |
| 3. System design | 14 Dec 2026 to 3 Jan 2027 | Architecture; database design; API design; wireframes and clickable Figma prototype; AI pipeline design |
| PiP write-up | 4 to 21 Jan 2027 | PiP covering phases 1 to 3, the plan and the demo |
| 4. Development | 4 Jan to 11 Feb 2027 | Core loop first (report, AI, dashboard), then the rest of the MVP |
| 5. Testing and evaluation | 12 to 21 Feb 2027 | Model results; user testing (SUS); bug fixes |
| 6. Final report | 22 Feb to 8 Mar 2027 | Report submitted |
| Viva preparation | 9 Mar to 3 May 2027 | Demo polish; practice questions |

Running alongside: collect and label fault descriptions from late November, so the AI has data by late December.

## PiP demo goals

The demo shows that the riskiest part, the AI, works. Building a proof of concept during design is justified as testing the biggest technical risk early.

- [ ] AI proof of concept: type a description, get category, priority and confidence (baseline model, 300 to 500 labelled descriptions)
- [ ] Clickable Figma prototype of the student app and staff dashboard
- [ ] Optional: one Flutter screen that sends a description to the classifier and shows the result

## Scope

MVP (the project):

- Student app: sign in (flat known), choose My flat or campus, describe the problem, optional photo, review and submit, track status
- AI: classify the description and predict UWE priority (Emergency, Urgent, Routine), with safety rules and an emergency screen
- Staff dashboard: queue by priority, ticket detail, assign, update status, note to student

Future work (only if ahead after development, otherwise discussed in the report):

- Photo recognition model
- Help assistant for problems with nothing to fix
- Duplicate detection, hotspots, push notifications

## Weekly routine

- About 1 hour: literature review, continuing lightly after phase 1
- 4 to 6 hours: work for the current phase
- 10 minutes after each session: a diary entry
- After every supervisor meeting: a meeting log entry the same day
