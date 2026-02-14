# Risk Register – Product A (E-commerce)

This risk register identifies and prioritizes the most significant risks affecting product quality, business continuity, and customer trust.

Risk priority is derived from **impact × likelihood**, not from test coverage or feature size.

---

## Risk scale

- **Impact**
  - High – direct revenue loss, legal exposure, or severe reputational damage
  - Medium – degraded user experience or operational overhead
  - Low – limited or localized impact

- **Likelihood**
  - High – expected to occur without active mitigation
  - Medium – possible under certain conditions
  - Low – unlikely but still plausible

---

## Identified risks

| ID | Risk description | Impact | Likelihood | Priority | Mitigation approach | Evidence / Signals |
|----|------------------|--------|------------|----------|---------------------|--------------------|
| R1 | Payment processing failures | High | Medium | High | E2E checkout tests, contract validation, monitoring | Payment success rate %, failed transaction spike alerts |
| R2 | Incorrect pricing or promotions | High | Medium | High | Pricing rule validation, API tests | Price mismatch logs, anomaly in order totals |
| R3 | Order persistence failure | High | Low | Medium | API validation, backend checks | Missing order records, reconciliation mismatch |
| R4 | Third-party outages | High | Medium | High | Contract tests, graceful degradation | Timeout rate, integration error spikes |
| R5 | Performance degradation | Medium | Medium | Medium | Performance monitoring | Response time thresholds, latency alerts |
| R6 | Cart state loss | Medium | Low | Low | Session validation tests | Increased cart abandonment rate |
| R7 | Broken critical user journeys | High | Medium | High | Smoke E2E suite | Failed smoke build, checkout error rate |
| R8 | Late detection of incidents | Medium | Medium | Medium | Monitoring + alerting | Time-to-detection KPI, alert coverage gaps |

---

## Notes

- Not all identified risks are addressed through automation.
- Some risks are mitigated primarily through monitoring and operational readiness.
- Risk priorities are reviewed before major releases or business events.
