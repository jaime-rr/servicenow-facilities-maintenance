<div align="center">

# Facilities & Maintenance Requests

**ServiceNow scoped app** — office repairs without the email black hole

*When an office employee needs a repair — broken AC, broken chair — the request
goes by email or chat, gets lost or delayed, and the problem stays broken until
someone complains twice.*

[![Status](https://img.shields.io/badge/Status-MVP%20in%20development-3c9e4e?style=flat&logo=servicenow&logoColor=white)]()

</div>

---

## What this app does

Employees request repairs through the portal. Urgent problems are flagged by rules —
not by the loudest requester. Small repairs auto-approve while costly ones wait for
the facilities agent. Requests route to the right vendor by location. A dashboard
gives management cost and workload visibility.

## Roles

| Role | What they do |
|---|---|
| **Employee** | Submits requests from the portal, tracks their own status |
| **Facilities agent** | Triage, approval of costly repairs, vendor assignment |
| **Manager** | Read-only dashboard: workload, costs, anything slipping |

## The three rules

| Rule | How it works |
|---|---|
| **Money** | ≤ €150 auto-approved · > €150 agent approval · emergencies skip approval, flagged for review |
| **Urgency** | Facts decide: urgent ← leaks, power outages, safety hazards, HVAC failure · low ← cosmetic · normal ← the rest |
| **Routing** | Location suggests the vendor · agent confirms in one click · nothing sits unassigned |

## Design decisions

Added at decision time — decision, rejected alternative, why.

## Setup & demo

Pending — published with the release.
