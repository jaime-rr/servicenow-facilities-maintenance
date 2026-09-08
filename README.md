<div align="center">

# Facilities & Maintenance Requests

**ServiceNow scoped app** — office repairs without the email chaos

*When an office employee needs a repair — broken AC, broken chair — the request is sent by email or chat, gets lost or delayed, and the problem stays broken until someone complains twice.*

[![Status](https://img.shields.io/badge/Status-MVP%20in%20development-3c9e4e?style=flat&logo=servicenow&logoColor=white)]()

</div>

---

## What's built so far

- **Facility Request table** — extends Task, reusing the platform's built-in request features: assignment, work notes, activity, priority, state
- **Portal intake** — employees report repairs from Service Portal and Employee Center, describing the problem and choosing the building

## Design decisions

- **Extends Task** — we reuse Task's built-in features instead of building our own from scratch. Incident was rejected: it's designed for IT incidents, not facilities requests

## Setup & demo

Coming soon — published with the release.
