# Root Cause Analysis (RCA) Template

This template is used after a production incident has been stabilized.

The purpose is learning and system improvement, not blame.

---

## 1. Incident Summary

- Date and time:
- Duration:
- Affected systems:
- Affected user journeys:
- Business impact (revenue, reputation, operations):

---

## 2. Timeline

Chronological sequence of events:

- Detection time:
- First response:
- Mitigation applied:
- Resolution confirmed:

Focus on facts, not assumptions.

---

## 3. Root Cause

Describe:

- What failed?
- Why did it fail?
- Why was it not detected earlier?

If useful, apply the "5 Whys" technique to reach systemic cause.

---

## 4. Contributing Factors

Examples:

- Missing test coverage
- Monitoring gaps
- Configuration error
- Communication delay
- Release pressure

Identify process weaknesses, not just technical failure.

---

## 5. Detection Analysis

- How was the issue detected?
- Could it have been detected earlier?
- Was monitoring sufficient?

If detection failed, define what signal was missing.

---

## 6. Preventive Actions

Define concrete improvements:

- Add/adjust automated test?
- Improve contract validation?
- Strengthen monitoring?
- Update quality gate?
- Update release checklist?

Each action must have:
- Owner
- Due date

---

## 7. Risk Register Update

- Does this incident change risk priority?
- Does a new risk need to be added?
- Should test strategy be adjusted?

Incident learning must feed back into the quality system.
