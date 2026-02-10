# Automation Candidates – Product A (E-commerce)

This document defines which areas are suitable for automation and at which level, based on risk, stability, and maintenance cost.

Automation decisions are driven by **value and signal quality**, not by technical feasibility alone.

---

## Automation decision criteria

Automation is prioritized when a scenario is:
- high risk or revenue-impacting,
- frequently executed,
- stable enough to maintain,
- capable of providing fast feedback.

Scenarios failing these criteria are intentionally left manual or monitored.

---

## High-priority automation candidates

### API / backend-level automation

Automated at API level:

- payment request and response validation,
- pricing and promotion rule calculations,
- order creation and persistence logic,
- critical error handling and edge cases.

Why:
- strong signal with low maintenance cost,
- fast feedback in CI,
- direct coverage of revenue-impacting logic.

---

### Contract testing

Automated contract checks for:
- payment provider integrations,
- critical third-party dependencies.

Why:
- external systems change independently,
- contract drift causes high-impact failures,
- early detection is cheaper than post-release incidents.

---

## Selective UI automation candidates

Automated at UI level:

- guest checkout happy path,
- logged-in checkout happy path,
- order confirmation visibility.

Why only these:
- represent real customer journeys,
- detect broken flows end-to-end,
- provide confidence before release.

UI automation is deliberately kept minimal.

---

## Scenarios intentionally not automated

The following are **not automated by design**:

- non-critical UI layout variations,
- cosmetic changes with no functional impact,
- rarely used edge cases with low business exposure,
- third-party system internal behavior beyond contracts.

Reasons:
- low return on investment,
- high maintenance cost,
- better handled via exploratory testing or monitoring.

---

## Role of manual and exploratory testing

Manual testing is focused on:
- new or high-risk changes,
- usability and UX regressions,
- complex edge cases not suited for automation.

Exploratory testing is used as a **risk discovery tool**, not as a regression replacement.

---

## Review and adjustment

Automation candidates are reviewed:
- after incidents,
- when maintenance cost increases,
- when risk profile changes.

Automation scope is reduced or expanded based on observed value.
