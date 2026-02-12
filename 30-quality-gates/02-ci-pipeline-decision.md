# CI Pipeline Decision Model

This document defines how the CI pipeline supports quality decisions.

The pipeline is not a test runner.
It is a risk control mechanism.

---

## Pipeline purpose

The CI pipeline exists to:

- provide fast feedback on code changes,
- prevent high-impact defects from progressing,
- enforce minimum quality standards automatically.

It supports, but does not replace, human judgment.

---

## Mandatory pipeline stages (blocking)

The following stages must pass before a change can be merged:

- Build verification
- Mandatory automated tests (API + critical paths)
- Static checks if defined as required

Failure in any mandatory stage blocks the merge.

---

## Non-blocking stages (informational)

Some checks may be configured as non-blocking when:

- test instability is known and tracked,
- impact area is non-critical,
- signal is useful but not reliable enough to block work.

Non-blocking checks must never hide critical failures.

---

## Risk-based enforcement

Pipeline strictness is aligned with risk:

- Changes affecting payment or checkout → full mandatory validation.
- Changes outside critical flows → reduced mandatory scope allowed.

Risk classification must be explicit, not assumed.

---

## Handling flaky tests

Flaky tests are treated as a quality issue.

Rules:

- Repeated flakiness must be investigated.
- Tests with unstable behavior should be:
  - fixed,
  - isolated,
  - or temporarily removed with documented reason.
- Flaky tests must not silently block productivity long-term.

Pipeline credibility depends on signal reliability.

---

## Emergency override

In exceptional cases:

- A pipeline stage may be overridden.
- Override requires documented risk acceptance.
- Override must trigger follow-up review.

Frequent overrides indicate systemic weakness.

---

## Principle

The pipeline enforces minimum safety.

Quality responsibility remains shared across QA, engineering, and product.
