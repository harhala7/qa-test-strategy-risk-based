# Test Pyramid – Product A (E-commerce)

This document defines the intended balance of test types for Product A.

The pyramid is a **cost and signal optimization decision**, derived from risk and maintainability.

---

## Guiding idea

- The highest value tests are those that provide **fast, reliable feedback**.
- UI automation provides strong end-to-end confidence but is expensive and fragile.
- API and service-level tests provide better signal-to-maintenance ratio for business logic.

The goal is not maximum coverage, but **maximum actionable signal per unit of effort**.

---

## Target distribution (by intent, not exact numbers)

### Foundation: API / service-level tests (majority)

Primary coverage for:
- pricing and promotion calculations,
- cart and order workflows at API level,
- payment flow validation via contracts and controlled integration checks.

Why:
- stable and fast,
- isolates failures well,
- scales with complexity without exploding maintenance.

---

### Middle: integration and contract tests (selective but critical)

Focus on:
- third-party payment provider expectations,
- request/response shape validation,
- critical error handling and timeouts.

Why:
- third parties are outside team control,
- failures are high impact (revenue, trust),
- contract drift must be caught early.

---

### Top: UI automation (small and strict)

Used only for:
- smoke coverage of critical user journeys,
- checkout and order placement end-to-end,
- basic navigation paths that reflect real customer behavior.

Why not more:
- UI tests are slower and more brittle,
- they are costly to maintain across frequent UI changes,
- they often duplicate lower-level coverage.

UI automation exists to detect broken journeys, not to validate all rules.

---

## Exploratory testing (parallel layer)

Exploratory testing is applied:
- on risk-heavy changes,
- during release candidate validation,
- on areas where automation does not provide good signal.

It targets:
- edge cases,
- UX regressions,
- unusual user behavior patterns.

---

## Monitoring as a production layer

Certain risks are mitigated primarily through detection and fast response, for example:
- payment success rate drops,
- checkout error spikes,
- performance degradation during campaigns.

Monitoring is treated as part of the overall quality system, not separate from testing.

---

## When this pyramid changes

The pyramid is adjusted when:
- UI stability improves or degrades,
- release frequency changes significantly,
- a new incident reveals a gap in signals,
- business priorities shift (for example heavy promotions).

The pyramid is not fixed, it is recalibrated based on observed risk.
