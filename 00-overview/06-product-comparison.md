# Product Comparison – E-commerce vs IoT SaaS

This document compares how quality strategy changes depending on product type.

The goal is to demonstrate adaptability of risk-based thinking.

---

## Business model impact

### E-commerce

- Revenue per transaction
- High sensitivity to checkout failures
- Campaign-driven traffic spikes
- Immediate financial impact of defects

### IoT SaaS

- Subscription-based revenue
- Long-term retention and trust
- SLA and uptime commitments
- Data accuracy more critical than UI behavior

---

## Dominant risk categories

| Category | E-commerce | IoT SaaS |
|-----------|------------|-----------|
| Revenue blocking | Payment failure | SLA breach |
| Data integrity | Order persistence | Telemetry loss or corruption |
| Security | Payment security | Authorization and tenant isolation |
| Performance | Peak campaign traffic | Fleet scalability |
| Monitoring focus | Transaction success rate | Ingestion lag, anomaly detection |

---

## Testing emphasis differences

### E-commerce

- Strong emphasis on end-to-end checkout flow
- API validation for pricing and order creation
- Smoke coverage before every release
- Monitoring of payment success rates

### IoT SaaS

- Strong emphasis on API and contract validation
- Isolation and authorization testing
- Monitoring as a core quality layer
- Observability-driven detection of ingestion issues

UI testing plays a smaller role in SaaS compared to transactional systems.

---

## Strategic quality difference

E-commerce prioritizes:
- Preventing immediate revenue loss.

IoT SaaS prioritizes:
- Protecting long-term trust and data reliability.

The quality model must adapt to business risk, not remain static.

---

## Key insight

Risk-based testing is not a template.

It is a decision framework that must be recalibrated when:

- revenue model changes,
- system architecture changes,
- customer expectations change,
- operational commitments (SLA) change.

Quality strategy is product-dependent.
