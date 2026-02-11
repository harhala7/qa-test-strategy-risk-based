# Incident Triage – Production Failures

This document defines how incidents are handled when a production issue is detected.

The goal of triage is not to assign blame.
The goal is to quickly assess impact, stabilize the system, and restore service.

---

## Step 1 – Confirm and classify

- Confirm the issue is reproducible or visible in monitoring.
- Identify affected user journeys.
- Classify impact level:

  - Critical – payment/checkout broken, revenue blocked
  - High – major feature degraded
  - Medium – partial degradation
  - Low – minor or cosmetic issue

---

## Step 2 – Assess business impact

- Is revenue directly affected?
- Are customers blocked from completing purchases?
- Is data integrity at risk?
- Is this impacting an active campaign or peak traffic window?

Impact drives response urgency.

---

## Step 3 – Immediate containment

Options include:

- rollback release,
- feature flag disable,
- configuration hotfix,
- traffic rerouting,
- temporary service degradation.

Speed is prioritized over elegance.

---

## Step 4 – Communication

- Notify product and engineering leads.
- Clarify current impact and mitigation plan.
- Avoid speculation.
- Provide time-bound updates.

Clear communication reduces chaos.

---

## Step 5 – Evidence collection

Capture:

- logs,
- error messages,
- monitoring graphs,
- recent deployment details.

This ensures proper root cause analysis later.

---

## Triage principles

- Contain first, analyze second.
- Focus on customer impact, not technical curiosity.
- Escalate early if impact is unclear.
- Avoid hiding or downplaying risk.

Incident response is a quality responsibility, not only an operations task.
