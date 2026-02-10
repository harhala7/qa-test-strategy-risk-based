# Test Matrix – Product A (E-commerce)

This test matrix maps **key product risks** to **testing and monitoring signals**.

Its purpose is to make testing decisions transparent and defensible.

---

## Risk-to-signal mapping

| Risk area | Primary test level | Test type | Signal timing | Notes |
|----------|-------------------|-----------|---------------|-------|
| Payment failures | API | Functional + contract | Pre-release + production | High-impact area, monitored continuously |
| Incorrect pricing | API | Functional | Pre-release | Focus on critical pricing rules |
| Broken checkout flow | UI | Smoke / E2E | Pre-release | Minimal but strict UI coverage |
| Order persistence issues | API | Functional | Pre-release | Validates backend integrity |
| Third-party outages | API | Contract | Pre-release + production | Detection over prevention |
| Performance degradation | Monitoring | Observability | Production | Alert-driven response |
| Cart state issues | Exploratory | Manual | Pre-release | Low-frequency, edge-focused |
| Late incident detection | Monitoring | Alerts | Production | Fast triage prioritized |

---

## Interpretation

- Not all risks rely on automation.
- Some risks are mitigated primarily through monitoring.
- UI automation is limited to high-signal journeys.
- Production signals are part of the quality strategy, not a failure of testing.

---

## Usage

This matrix is used:
- during test planning,
- to explain coverage decisions,
- as input for release readiness discussions.

It is updated when risk priorities change.
