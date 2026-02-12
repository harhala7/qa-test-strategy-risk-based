# Flaky Tests Policy

Flaky tests reduce trust in the CI pipeline and weaken quality signals.

This policy defines how unstable tests are handled.

---

## Definition

A flaky test is a test that:

- sometimes passes and sometimes fails without code changes,
- depends on timing, environment instability, or hidden state,
- produces inconsistent results across runs.

---

## Principles

- Flaky tests are treated as defects.
- Ignoring flakiness erodes pipeline credibility.
- Stable signal is more valuable than large coverage.

---

## Immediate handling

When flakiness is detected:

1. Reproduce and confirm instability.
2. Assess impact (critical path or non-critical).
3. Decide on one of the following actions:
   - Fix immediately
   - Isolate and investigate
   - Temporarily disable with documented reason

Temporary disabling must include:
- ticket reference
- owner
- review deadline

---

## Long-term handling

If flakiness persists:

- Root cause must be identified.
- Test design should be reviewed.
- Environment stability should be evaluated.
- Test may be rewritten or moved to different level (e.g., API instead of UI).

---

## Pipeline integrity rule

No test should remain flaky indefinitely.

Frequent flakiness indicates:
- poor test design,
- unclear ownership,
- unstable system architecture.

Pipeline credibility is a strategic asset.
