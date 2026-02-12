# Bug Triage Policy

Bug triage is a structured decision process for evaluating and prioritizing reported defects.

Its goal is not to fix everything.
Its goal is to manage risk intentionally.

---

## Objectives

Bug triage ensures:

- critical issues are addressed immediately,
- business impact is understood,
- release decisions are informed by real risk,
- defect backlog remains actionable.

---

## Triage ownership

- QA facilitates triage.
- Engineering evaluates technical impact.
- Product assesses business priority.
- Final priority is a shared decision.

---

## Triage frequency

- High-impact systems: at least weekly.
- During active releases: as needed.
- After production incidents: immediate review.

---

## Evaluation criteria

Each defect must be assessed based on:

- Business impact (revenue, reputation, user trust)
- Affected user journeys
- Reproducibility
- Scope (single user vs system-wide)
- Risk of escalation if left unresolved

---

## Possible outcomes

1. Fix immediately (critical/high impact)
2. Fix before next release
3. Schedule for later iteration
4. Accept risk temporarily
5. Close as invalid / duplicate

Risk acceptance must be explicit.

---

## Backlog hygiene

- Stale defects must be reviewed periodically.
- Low-priority issues should not accumulate indefinitely.
- Technical debt must be visible, not hidden.

Unmanaged backlog creates invisible risk.
