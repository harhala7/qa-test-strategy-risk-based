# Severity and Priority Guide

This guide defines how defects are classified to ensure consistent and risk-based decision making.

Severity and priority are not the same.

- Severity = technical and user impact.
- Priority = business urgency.

---

## Severity Levels

### Critical

- System-wide failure
- Payment/checkout blocked
- Data corruption
- Security vulnerability

Impact: immediate revenue or trust damage.

---

### High

- Major feature not working
- Significant degradation of core flow
- Frequent user-visible errors

Impact: strong user frustration or operational overhead.

---

### Medium

- Partial feature malfunction
- Workaround exists
- Non-critical flow degradation

Impact: limited user impact.

---

### Low

- Cosmetic issues
- Minor UI inconsistencies
- Edge case with minimal exposure

Impact: negligible business risk.

---

## Priority Levels

### P1 – Immediate

- Must be fixed before release or immediately in production.
- Direct business risk.

---

### P2 – High

- Fix in current or next planned release.
- Noticeable impact but not blocking revenue.

---

### P3 – Normal

- Schedule based on capacity.
- Low risk of escalation.

---

### P4 – Deferred

- Acceptable to postpone.
- Minimal impact.

---

## Decision Principles

- Critical severity does not always equal P1 priority.
- Priority is influenced by business context (campaigns, peak season, SLAs).
- Classification must be consistent and transparent.

Clear classification reduces emotional decision-making.
