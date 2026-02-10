# Release Checklist – Product A (E-commerce)

This checklist is used immediately before a production release to confirm readiness and make the release decision explicit.

It complements quality gates and exit criteria with a final operational review.

---

## Scope confirmation

- Release scope is clearly defined and agreed.
- No unintended changes are included.
- High-risk areas affected by this release are identified.

---

## Test and quality status

- Mandatory CI checks are green.
- Smoke coverage for critical user journeys is completed and passed.
- No open **High severity** defects in:
  - payment
  - checkout
  - order creation
  - pricing or promotions
- Known Medium/Low defects are reviewed and documented.

---

## Risk review

- Risk register reviewed for release scope.
- No **High priority** risks remain unmanaged.
- Any accepted risks are:
  - explicitly documented
  - approved by product and engineering
  - time-bound where applicable

---

## Monitoring and observability

- Monitoring for critical flows is confirmed active:
  - checkout success rate
  - payment success rate
  - error rates
- Alerts are configured and tested where applicable.
- Dashboards are accessible to on-call team members.

---

## Operational readiness

- Rollback plan is defined and understood.
- On-call ownership for release window is clear.
- Support and stakeholders are informed if required.
- Release timing considers business impact (campaigns, peak traffic).

---

## Final decision

- QA recommendation recorded (GO / CONDITIONAL GO / NO-GO).
- Decision rationale documented.
- Release owner confirmed.

---

## Notes

This checklist does not eliminate risk.

It ensures that:
- the team is aware of the current risk posture,
- detection and response are prepared,
- the release decision is intentional.
