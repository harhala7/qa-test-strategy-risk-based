# Exit Criteria – Product A (E-commerce)

Exit criteria define when testing is considered sufficient to support a release decision.

They are designed to prevent shipping changes with unmanaged high-impact risk, while keeping delivery practical under time pressure.

---

## Release candidate is eligible when

### Mandatory quality signals

- Critical smoke coverage for core user journeys is green:
  - browse → add to cart → checkout → order confirmation
- No failing mandatory CI checks required for release.
- No unresolved defects classified as **High severity** affecting:
  - payment, checkout, order creation, pricing/promotions
- Risk register review completed for the release scope:
  - no unmitigated **High priority** risks without explicit acceptance

---

## Conditional release criteria (allowed with explicit risk acceptance)

A release may proceed if the following conditions are met and the risk is documented:

- Medium severity defects remain open, but:
  - do not impact payment/checkout/order creation
  - have clear user impact description and workaround (if applicable)
- Some non-critical automated checks are missing, but:
  - the change is outside critical paths
  - monitoring is confirmed active for relevant signals
- Exploratory testing is limited, but:
  - scope is low risk
  - release is reversible (rollback available)

All conditional releases require documented risk acceptance by product and engineering.

---

## Explicit blockers (hard stop)

Release is blocked if any of the following is true:

- Checkout or payment smoke fails
- Known regression in critical user journeys exists
- Any High severity defect is open in revenue-critical areas
- Production monitoring for critical flows is unavailable or disabled
- The release contains high-risk changes with no validation plan

---

## Evidence expected for release readiness

Minimum evidence set:
- smoke results (or confirmation of execution and outcome)
- list of known issues and their severity
- risk acceptance notes for any conditional criteria
- confirmation that monitoring and alerting are active

---

## Notes

Exit criteria do not guarantee absence of defects.

They ensure that:
- the highest risks are managed intentionally,
- the team has reliable signals,
- remaining risk is explicit, not accidental.
