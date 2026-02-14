# QA Test Strategy – Risk-Based Testing Playbook

This repository demonstrates **how a QA / Quality Engineer thinks and makes decisions**, not how they build yet another automation framework.

It focuses on:
- **risk-based test strategy and prioritization**
- **quality gates and CI enforcement**
- **release readiness decisions**
- **incident response, RCA, and regression prevention**
- minimal “proofs” in concept only (automation is shown in other repos)

---

## What this repository shows

This repo is a practical playbook that demonstrates:

- translating product context into **risk register**
- deriving **test strategy** from risk (what to test, what not to test)
- using the **test pyramid** as a cost and signal decision
- defining **quality gates** for PR and release
- making **GO / NO-GO** decisions via exit criteria and release checklist
- handling incidents with **triage → RCA → postmortem → regression policy**
- running defect governance: **flaky policy, triage policy, severity vs priority**

Everything here is designed to be **defensible in a technical interview**.

---

## What this repository is NOT

- ❌ not an automation framework
- ❌ not a tutorial or course project
- ❌ not a dump of generic QA docs

Automation projects exist separately. This repo is the **strategy and decision layer**.

---

## Quick start: where to look first

If you only have 5 minutes, read in this order:

1. **Product A (E-commerce)**
   - Context: `10-product-a-ecommerce/01-context.md`
   - Risk register: `10-product-a-ecommerce/04-risk-register.md`
   - Test strategy: `10-product-a-ecommerce/05-test-strategy.md`
   - Test matrix: `10-product-a-ecommerce/09-test-matrix.md`
   - Exit criteria: `10-product-a-ecommerce/10-exit-criteria.md`
   - Release checklist: `10-product-a-ecommerce/11-release-checklist.md`

2. **Quality gates and governance**
   - Quality gates: `30-quality-gates/01-quality-gates.md`
   - CI enforcement model: `30-quality-gates/02-ci-pipeline-decision.md`
   - Flaky tests policy: `30-quality-gates/03-flaky-tests-policy.md`
   - Bug triage policy: `30-quality-gates/04-bug-triage-policy.md`
   - Severity vs priority: `30-quality-gates/05-severity-priority-guide.md`

3. **Incident response lifecycle**
   - Incident triage: `40-incident-response/01-incident-triage.md`
   - RCA template: `40-incident-response/02-rca-template.md`
   - Postmortem template: `40-incident-response/03-postmortem-template.md`
   - Regression policy: `40-incident-response/04-regression-policy.md`

---

## Core decision philosophy

- **Risk drives testing**, not coverage metrics
- **Signal over volume** (reliable feedback beats many fragile checks)
- **Not everything should be automated**
- **Monitoring is part of the quality system**
- **Quality decisions must be explicit** (including risk acceptance)

---

## Key strategic artifacts

These documents demonstrate leadership-level thinking and trade-off awareness:

- Decision log: `00-overview/05-decision-log.md`
- Product comparison (E-commerce vs IoT SaaS): `00-overview/06-product-comparison.md`

They highlight why specific quality decisions were made and how strategy adapts to different business models.

---

## Current status

Implemented:
- one full end-to-end case study (Product A) from context to release decision
- quality gates, CI enforcement, and defect governance
- incident response lifecycle with learning loop back to strategy

Planned next:
- decision log / trade-offs (why key choices were made)
- a second product context (SaaS) to show how strategy changes by product type
- minimal “mini-proofs” only if needed (this repo avoids building frameworks)

---

## Who this is for

- QA Engineers aiming for Senior / Lead roles
- Quality Leads defining governance and release safety
- Interviewers evaluating decision-making maturity
- Teams needing pragmatic, risk-driven quality systems
