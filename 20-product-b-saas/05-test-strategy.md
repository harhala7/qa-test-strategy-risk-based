# Test Strategy – Product B (IoT Device Management SaaS)

This strategy allocates testing effort to protect **data integrity, security, and platform reliability**.

Unlike transactional systems, the primary failure mode here is loss of trust caused by:
- incorrect or missing telemetry,
- unauthorized access,
- SLA breaches.

---

## Strategy objectives

- Prevent and detect data integrity failures early.
- Ensure strong authorization and tenant isolation.
- Maintain reliable platform performance as device fleet scales.
- Provide fast signals in CI and strong detection in production.

---

## Risk-driven focus areas

Highest priority areas:

- telemetry ingestion and storage correctness (R1, R2),
- authorization and access control (R3),
- tenant isolation boundaries (R4),
- scalability and performance under growth (R6),
- monitoring effectiveness (R7, R8).

UI correctness is treated as secondary unless it blocks critical operations.

---

## Test levels and responsibilities

### API and service-level testing (primary)

Primary coverage for:
- ingestion APIs and validation logic,
- device management operations,
- auth and permission rules,
- tenant boundary enforcement.

Rationale:
- stable and fast feedback,
- directly validates business and security rules,
- supports high coverage without UI maintenance cost.

---

### Contract and integration testing (critical)

Contract coverage for:
- device communication layer expectations,
- message formats and schema consistency,
- failure scenarios: timeouts, retries, duplicates, out-of-order messages.

Rationale:
- device ecosystem is not fully controllable,
- integration drift is a major risk,
- most incidents originate at boundaries.

---

### UI testing (selective)

UI validation focuses on:
- critical admin workflows (device registration, configuration push),
- visibility of device status and key alerts.

UI automation is kept minimal to avoid fragile coverage and duplicated logic.

---

### Exploratory testing

Exploratory testing is focused on:
- complex edge cases in device lifecycle,
- usability of operational workflows,
- incident-like scenarios (partial outages, stale data).

---

## Observability as a quality layer

Monitoring is treated as part of the test strategy:

- ingestion success rate and lag,
- telemetry anomaly rates,
- authorization failures,
- latency and throughput signals,
- SLA dashboards and alerting.

Fast detection is essential due to real-world device variability.

---

## What is intentionally not tested deeply

- UI layout and cosmetic behavior outside critical workflows.
- Device internal firmware behavior beyond interface contracts.
- Exhaustive combinations of device models, unless risk-driven.

These areas are mitigated through contracts, monitoring, and targeted exploratory testing.

---

## Strategy evolution

The strategy is updated:
- after production incidents,
- when fleet size changes significantly,
- when new device types are introduced,
- when SLA commitments change.

Observations from incidents feed back into risk register and test matrix decisions.
