# Quality Gates

This document defines the minimum quality conditions that must be met before a change is allowed to progress through the delivery pipeline.

Quality gates exist to **control risk**, not to maximize test coverage.

---

## Purpose of quality gates

Quality gates are designed to:
- prevent known high-impact failures from reaching production,
- provide clear stop/go signals for releases,
- protect critical business flows under time pressure.

They are directly derived from identified product risks.

---

## Gate ownership

- QA owns the definition and evaluation of quality gates.
- Final release decisions remain a shared responsibility with product and engineering.
- Overriding a quality gate requires explicit risk acceptance.

---

## Pull Request (PR) quality gates

The following conditions must be met before a PR can be merged:

- All automated checks defined as mandatory must pass.
- No unresolved **High severity** defects related to the change scope.
- Critical user flows impacted by the change have been validated.
- Known test flakiness is not ignored without justification.

Failure of any PR gate blocks the merge.

---

## Release quality gates

The following conditions must be met before a release is approved:

- Smoke tests for critical user journeys pass.
- No open **High priority** risks without documented mitigation or acceptance.
- Payment and checkout flows show acceptable success rates in pre-release validation.
- Monitoring and alerting for critical paths are confirmed active.

Release gates may be conditionally relaxed only with documented risk acceptance.

---

## Risk-based exceptions

Not all quality gates are absolute.

Examples of acceptable exceptions:
- low-impact UI defects with no revenue impact,
- known issues with clear rollback or mitigation plan,
- changes isolated from critical paths.

All exceptions must be:
- explicitly documented,
- time-bound,
- visible to stakeholders.

---

## Signals, not guarantees

Passing quality gates does not guarantee absence of defects.

It indicates that:
- the most significant risks have been actively managed,
- the team is prepared to detect and respond to failures,
- quality decisions are intentional and transparent.
