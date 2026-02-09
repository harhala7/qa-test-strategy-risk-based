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

| ID | Risk description | Impact | Likelihood | Priority | Mitigation approach |
|----|------------------|--------|------------|----------|---------------------|
| R1 | Payment processing failures (incorrect charges, failed confirmations) | High | Medium | High | Focused end-to-end checkout testing, contract validation with payment provider, monitoring of payment success rates |
| R2 | Incorrect pricing or promotions applied at checkout | High | Medium | High | Risk-based functional testing of pricing rules, automation around critical pricing paths, post-release monitoring |
| R3 | Order creation succeeds but order is not persisted correctly | High | Low | Medium | Backend-level validation, API testing, reconciliation checks between systems |
| R4 | Third-party service outages (payments, delivery) cause cascading failures | High | Medium | High | Contract testing, graceful degradation scenarios, clear incident response procedures |
| R5 | Performance degradation during peak traffic (campaigns, sales) | Medium | Medium | Medium | Targeted performance checks, monitoring of key response times, production alerts |
| R6 | Cart state loss across sessions or devices | Medium | Low | Low | Session handling tests, exploratory testing around edge cases |
| R7 | Broken critical user journeys after release | High | Medium | High | Smoke test suite covering core flows, strict release quality gates |
| R8 | Delayed detection of production issues | Medium | Medium | Medium | Monitoring, logging, alerting, and fast triage process |

---

## Notes

- Not all identified risks are addressed through automation.
- Some risks are mitigated primarily through monitoring and operational readiness.
- Risk priorities are reviewed before major releases or business events.
