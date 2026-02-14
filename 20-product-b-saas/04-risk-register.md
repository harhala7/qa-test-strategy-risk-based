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

| ID | Risk description | Impact | Likelihood | Priority | Mitigation approach | Evidence / Signals |
|----|------------------|--------|------------|----------|---------------------|--------------------|
| R1 | Telemetry data loss | High | Medium | High | Contract validation, ingestion monitoring | Ingestion success rate, lag metrics, dropped message alerts |
| R2 | Corrupted telemetry data | High | Low | Medium | Validation rules, integrity checks | Data anomaly detection, checksum mismatch |
| R3 | Unauthorized access | High | Medium | High | RBAC testing, audit logging | Failed auth spikes, unauthorized access logs |
| R4 | Multi-tenant data leakage | High | Low | High | Isolation boundary validation | Cross-tenant access attempt logs |
| R5 | Device config not applied | Medium | Medium | Medium | API + acknowledgment validation | Config failure rate, missing acknowledgments |
| R6 | Performance degradation | High | Medium | High | Load + observability | Latency thresholds, throughput drop alerts |
| R7 | Monitoring gaps | Medium | Medium | Medium | Alert validation review | Missing alert coverage, detection delay KPI |
| R8 | SLA breach | High | Low | Medium | Uptime monitoring | SLA dashboard %, uptime alerts |

---

## Notes

- Data integrity and security risks are prioritized over UI concerns.
- Monitoring is a core mitigation mechanism.
- Risk profile emphasizes long-term trust over transactional correctness.
