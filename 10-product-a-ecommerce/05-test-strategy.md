# Test Strategy – Product A (E-commerce)

This test strategy defines **how testing effort is allocated based on risk**, not based on feature count or test coverage targets.

The strategy directly reflects the risks identified in the risk register.

---

## Strategy objectives

The primary objectives of testing are to:

- protect revenue-critical user journeys,
- detect high-impact failures as early as possible,
- provide fast and reliable quality signals to support release decisions.

Lower-risk areas are tested selectively or monitored rather than exhaustively tested.

---

## Risk-driven testing focus

Testing effort is concentrated on the following high-priority risk areas:

- payment and checkout flows,
- pricing and promotion logic,
- order creation and persistence,
- availability of critical user journeys.

These areas receive deeper and more frequent testing than non-critical functionality.

---

## Test levels and responsibilities

### API and backend-level testing

Primary focus for:
- payment integration logic,
- order creation and validation,
- pricing and promotion calculations.

Rationale:
- faster feedback,
- higher stability compared to UI tests,
- better isolation of business logic failures.

---

### UI-level testing

Used selectively for:
- critical end-to-end user journeys,
- smoke coverage of checkout and order placement,
- validation of core navigation paths.

UI automation is **not** used for exhaustive functional coverage due to:
- high maintenance cost,
- lower signal-to-noise ratio,
- duplication of backend coverage.

---

### Exploratory testing

Applied primarily:
- before major releases,
- around high-risk changes,
- for edge cases not covered by automation.

Exploratory testing complements automation rather than replacing it.

---

## What is intentionally not tested deeply

The following areas are not tested exhaustively:

- non-critical UI variations,
- low-impact edge cases with limited business exposure,
- third-party system internals beyond contract expectations.

These risks are accepted or mitigated through monitoring and operational readiness.

---

## Role of monitoring and observability

Monitoring is treated as a **post-release testing layer** for:

- payment success rates,
- checkout error frequency,
- performance degradation under real traffic.

For certain risks, fast detection is prioritized over pre-release prevention.

---

## Strategy review and evolution

The test strategy is reviewed:
- before major releases,
- after significant incidents,
- when business priorities change.

The strategy evolves based on observed failures, not assumptions.
