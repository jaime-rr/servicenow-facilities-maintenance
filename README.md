<div align="center">

# Facilities & Maintenance Requests

**ServiceNow scoped app** — office repairs without the email chaos

*When an office employee needs a repair — broken AC, broken chair — the request is sent by email or chat, gets lost or delayed, and the problem stays broken until someone complains twice.*

[![Status](https://img.shields.io/badge/Status-MVP%20in%20development-3c9e4e?style=flat&logo=servicenow&logoColor=white)]()

</div>

---

## Who uses it

| Persona | Access |
|---|---|
| **Employee** | Reports repairs from the portal — sees only their own requests |
| **Agent** | Manages all requests — assigns, updates, closes |
| **Manager** | Reads everything — no changes |

---

## What's built so far

- **Facility Request table** — extends Task, reusing the platform's built-in request features: assignment, work notes, activity, priority, state
- **Portal intake** — employees report repairs from Service Portal and Employee Center (`Report a repair`), describing the problem and choosing the building
- **Security** — employees see only their own requests, agents manage all, managers read-only
- **Urgency rule** — the issue category decides priority: water leaks, power outages, safety hazards and HVAC failures land at Critical; cosmetic issues at Low; everything else Moderate. Agents can override

## Design decisions

- **Extends Task** — we reuse Task's built-in features instead of building our own from scratch. Incident was rejected: it's designed for IT incidents, not facilities requests
- **Urgency on Task's priority field, via decision table** — we reuse the OOB priority (Critical…Planning) instead of a custom urgency field. A decision table maps category → priority, called from a Flow Designer flow on insert/category change — policy stays grid-editable, no code.

## Setup & demo

Coming soon — published with the release.
