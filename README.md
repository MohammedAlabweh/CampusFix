# CampusFix

AI-assisted fault reporting for UWE Bristol students, in halls and across campus.

Final-year project, BSc (Hons) Computer Science, UWE Bristol.
Student: Mohammed Alabweh · Supervisor: David Wyatt

## The idea

CampusFix is a mobile app that lets UWE students report any problem, in their flat in halls or anywhere on campus, in under a minute. The student signs in with their student number, so the app already knows their flat: they say what is wrong and add a photo if they want. For campus faults they scan a QR code on the room door.

An AI service reads the description, works out what kind of problem it is, predicts its urgency using UWE's own repair priorities (Emergency, Urgent, Routine) and routes it to the right team: Accommodation Services for halls, or the matching Estates team for campus. Staff manage reports on a web dashboard, and the student follows the report until it is fixed.

## Repository structure

| Folder | What it holds | Technology |
| --- | --- | --- |
| `app/` | Student mobile app | Flutter |
| `dashboard/` | Staff web dashboard | React |
| `api/` | Backend API and database | .NET / C#, PostgreSQL |
| `ai/` | Classification models, data and evaluation | Python |
| `docs/` | Plan, proposal, requirements, design and evaluation documents | Markdown |

## Key dates

| Milestone | Date |
| --- | --- |
| PiP (Project in Progress) | 21 January 2027 |
| Development complete | 11 February 2027 |
| Final report | 8 March 2027 |
| Viva | 3 May 2027 |

## Approach

The project follows a phased (Waterfall) approach: literature review, requirements analysis, system design, development, then testing and evaluation. An AI proof of concept is built during design to test the biggest technical risk early.

See [`docs/plan.md`](docs/plan.md) for the full plan and [`docs/proposal.md`](docs/proposal.md) for the approved proposal.

## Current phase

Phase 1: Literature review (5 to 29 November 2026).
