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
| **Agent** | Manages all requests — triages, picks the vendor, updates, closes |
| **Manager** | Approves costs above the threshold; otherwise reads everything |

---

## What's built so far

- **Facility Request table** — extends Task, reusing the platform's built-in request features: assignment, work notes, activity, priority, state
- **Portal intake** — employees report repairs from Service Portal and Employee Center (`Report a repair`), describing the problem and choosing the building
- **Security** — employees see only their own requests, agents manage all, managers read-only apart from cost approvals
- **Urgency rule** — the issue category decides priority: water leaks, power outages, safety hazards and HVAC failures land at Critical; cosmetic issues at Low; everything else Moderate. Agents can override. A Critical priority also flags the request as emergency-approved for later spend review
- **Cost approval rule** — the agent sets the cost during triage: up to €150 proceeds, above it waits for the manager's approval; Critical requests skip approval
- **Vendor routing** — every request belongs to the facilities team from the moment it's created, so nothing sits unassigned; the agent picks the vendor during triage from those covering that kind of issue, and a coverage mapping lets one contractor handle several trades
- **ATF tests** — the core behaviours are covered by automated tests: default state, priority assignment, emergency flagging and cost approvals

## Design decisions

- **Extends Task** — we reuse Task's built-in features instead of building our own from scratch. Incident was rejected: it's designed for IT incidents, not facilities requests
- **Cost estimated by the agent during triage, not by the employee** — pricing a repair is expert input; an untrusted number driving money decisions is worse than a short triage step
- **Urgency on Task's priority field, via decision table** — we reuse the OOB priority (Critical…Planning) instead of a custom urgency field. A decision table maps category → priority, called from a Flow Designer flow on insert/category change — policy stays grid-editable, no code.

## Setup & demo

Coming soon — published with the release.
