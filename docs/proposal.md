# CampusFix – Project proposal

Approved by the supervisor on 4 November 2026. The formatted version is [`CampusFix-Proposal.pdf`](CampusFix-Proposal.pdf).

## 1. The problem

Students in UWE halls can already report repairs online, but students have no online route for campus buildings, and no existing route is a photo-first mobile app with automatic triage.

| Who | Area | Current route | Gap |
| --- | --- | --- | --- |
| Students in UWE halls | Accommodation | Online student repairs portal with a job tracker | Halls only; no photo upload or app mentioned |
| Staff | Campus buildings | Facilities Online work requests | Staff login required |
| Students | Campus buildings | General Estates contact page, switchboard or Facilities phone line | No mobile, photo-based or trackable route |

In April 2023 a student proposed on the Students' Union ideas board that the UWE app should let students report broken plug sockets by building and room. The idea received no comments and shows no recorded outcome.

CampusFix covers both areas in one app. For campus buildings it fills the gap outright. For halls it improves on the existing portal, which becomes the baseline for evaluation. It would not replace Facilities Online: it is a student-facing front end that could feed the existing staff workflow.

## 2. How it works

Example: a student types "the oven in our kitchen won't turn on" with no photo. The flat is already known from their profile, the AI suggests Kitchen appliances and Urgent, and the report goes to Accommodation Services.

Main flow:

1. Student signs in (flat known)
2. Chooses My flat or Somewhere on campus
3. Describes the problem, optionally adds a photo
4. AI classifies the fault and predicts the UWE priority
5. Student reviews, confirms and submits
6. Staff see it in a queue sorted by priority, assign a team and start work
7. Staff mark it fixed with a note
8. Student confirms it is fixed, or reopens it

Branches:

- **Somewhere on campus:** the student scans the room QR code or picks the building and room; the report goes to the matching Estates team.
- **Emergency:** if the AI or the safety rules suggest Emergency, the app shows the UWE emergency number and asks the student to call.
- **Unsure:** a low-confidence result enters the queue flagged "Needs review".

## 3. MVP scope

| Part | MVP |
| --- | --- |
| Student app (Flutter) | Sign in with student number; My flat or campus; QR or building/room picker; description and optional photo; review screen; emergency screen; reference number; My reports with status timeline |
| AI service (Python) | Classify the description with a confidence score; predict UWE priority with safety rules; route to Accommodation Services or Estates; flag low confidence; log corrections |
| Staff dashboard (React) | Sign in; queue by priority and age with filters; ticket detail; time left against UWE response targets; correct, assign, update status, add a note |
| Admin set-up | Halls, flats, buildings, rooms, teams and sample students from a config file; printable room QR codes |

Future work: photo recognition model, help assistant for problems with nothing to fix, duplicate detection, hotspots, push notifications.

Out of scope: integration with UWE's live Facilities Online system, real deployment, and emergency reporting.

## 4. AI and data

About 1,000 labelled fault descriptions, each with a category and one of UWE's three priorities (Emergency = attend within 4 hours, Urgent = within 8 hours, Routine = within 7 days).

| Category | Example faults | Typical UWE priority |
| --- | --- | --- |
| Plumbing and water | Leaks, blocked toilet or sink, flooding | Routine to Emergency |
| Heating and hot water | No heating, no hot water | Urgent |
| Electrical and lighting | Dead sockets, broken lights, exposed wiring, power loss | Routine to Emergency |
| Kitchen appliances | Oven, hob, fridge or freezer not working | Urgent |
| Doors, windows and locks | Faulty lock, broken window | Urgent or Routine |
| Furniture and fittings | Broken chair, desk, wardrobe, blind | Routine |
| IT and AV | Projector, screen, lecture-room PC | Routine |
| Cleaning and pests | Spills, overflowing bins, pests | Routine |
| Safety | Blocked fire exit, wedged fire door, trip hazard | Emergency |

Evaluation: accuracy, precision, recall and a confusion matrix per category and priority, comparing a baseline model, a fine-tuned model and a general AI API. Emergency recall is the key safety metric. Usability is measured with SUS and task times.

## 5. Ethics

Low risk: adult student participants for usability testing and a short survey, no sensitive topics, sample data only in the app, photos with no people in shot. Supervisor confirmed no ethics issues on 4 November 2026.
