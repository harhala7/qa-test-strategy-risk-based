# Risk Register – Product B (IoT Device Management SaaS)

This risk register identifies key risks affecting system reliability, data integrity, and customer trust.

Priority is derived from impact × likelihood.

---

## Risk scale

- Impact
  - High – SLA breach, data corruption, security exposure, churn risk
  - Medium – degraded performance or limited functionality
  - Low – minor operational inconvenience

- Likelihood
  - High – expected without active mitigation
  - Medium – possible under certain load or edge conditions
  - Low – unlikely but plausible

---

## Identified risks

| ID | Risk description | Impact | Likelihood | Priority | Mitigation approach |
|----|------------------|--------|------------|----------|---------------------|
| R1 | Telemetry data loss during device communication | High | Medium | High | Contract validation, message acknowledgment checks, monitoring of ingestion pipeline |
| R2 | Corrupted or inconsistent telemetry data | High | Low | Medium | Validation rules, backend integrity checks, anomaly detection |
| R3 | Unauthorized access to device data | High | Medium | High | Role-based access control testing, security validation, audit logging |
| R4 | Multi-tenant data leakage | High | Low | High | Isolation tests, tenant boundary validation, strict API authorization checks |
| R5 | Device configuration updates not applied correctly | Medium | Medium | Medium | API-level validation, device acknowledgment confirmation |
| R6 | Platform performance degradation with fleet growth | High | Medium | High | Load testing, monitoring of latency and throughput |
| R7 | Monitoring gaps leading to late detection of failures | Medium | Medium | Medium | Alert validation, observability review |
| R8 | SLA breach due to infrastructure instability | High | Low | Medium | Uptime monitoring, failover testing |

---

## Notes

- Data integrity and security risks are prioritized over UI concerns.
- Monitoring is a core mitigation mechanism.
- Risk profile emphasizes long-term trust over transactional correctness.
