# Regression Policy – After Production Incidents

This policy defines how production incidents influence future testing and quality decisions.

An incident must result in a system improvement, not only a fix.

---

## Principle

Every production incident triggers evaluation of:

- Was this scenario covered by automated tests?
- Should it have been?
- Was monitoring sufficient?
- Did quality gates fail to detect the risk?

If the answer to any of these is "yes", the system must be adjusted.

---

## Mandatory evaluation after each incident

1. Should a new automated test be added?
2. Should an existing test be strengthened?
3. Should a new monitoring alert be created?
4. Should risk priority be increased?
5. Should release validation criteria be updated?

At least one improvement action must be identified.

---

## When automation is required

Automation should be added when:

- the incident impacted revenue or critical flows,
- the scenario is reproducible,
- the failure could have been detected earlier.

High-impact regressions must not rely solely on manual validation.

---

## When monitoring is preferred

Monitoring improvements may be prioritized when:

- the issue is environment-specific,
- third-party instability is involved,
- failure depends on production-scale traffic.

Detection speed may be more valuable than prevention.

---

## Risk Register Feedback Loop

After each incident:

- Risk register is reviewed and updated.
- Risk priority may be adjusted.
- Test strategy may be refined.

Incidents are treated as data for improving the quality model.

---

## Ownership

QA owns the evaluation of regression strategy changes.

Implementation may be shared with engineering, but quality responsibility remains explicit.
