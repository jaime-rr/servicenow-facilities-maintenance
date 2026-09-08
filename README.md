<div align="center">

# Facilities & Maintenance Requests

**ServiceNow scoped app** — office repairs without the email black hole

*When an office employee needs a repair — broken AC, broken chair — the request
goes by email or chat, gets lost or delayed, and the problem stays broken until
someone complains twice.*

[![Status](https://img.shields.io/badge/Status-MVP%20in%20development-3c9e4e?style=flat&logo=servicenow&logoColor=white)]()

</div>

---

## Built so far

A `Facility Request` table that extends Task, with the standard work-item
machinery inherited — number, assignment, work notes, activity, priority, state.

- Records start at **Open** (OOB default) and move through the Task state
  lifecycle: Open → Work in Progress → Closed Complete
- **Building** is a mandatory choice (Building A / Building B / Other), stored
  as stable keys (`building_a`) for the routing logic that will read it later

## Design decisions

**Extends Task (not standalone, not Incident)**

- **Decision:** inherit Task's generic work-item machinery — number, assignment,
  work notes, activity, priority, state
- **Rejected:** standalone table (rebuilds all of it); Incident (ITSM process semantics)
- **Why:** platform-first reuse — the inherited priority field feeds the urgency
  rule when it lands

## Setup & demo

Pending — published with the release.
