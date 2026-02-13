# Test Matrix – Product B (IoT Device Management SaaS)

This matrix maps key risks to quality signals.

In SaaS systems, data integrity and security signals are prioritized over UI validation.

---

## Risk-to-signal mapping

| Risk area | Primary test level | Test type | Signal timing | Notes |
|-----------|-------------------|-----------|---------------|-------|
| Telemetry data loss | API / Integration | Contract + functional | Pre-release + production | Monitor ingestion success and lag |
| Corrupted telemetry data | API | Validation + integrity checks | Pre-release + production | Include anomaly detection signals |
| Unauthorized access | API | Authorization tests | Pre-release | Validate role-based access control |
| Multi-tenant leakage | API | Isolation boundary tests | Pre-release | Critical security risk |
| Device config not applied | API + Integration | Functional + acknowledgment checks | Pre-release + production | Confirm end-to-end confirmation |
| Performance degradation | Monitoring | Load + observability | Production | Track latency and throughput |
| SLA breach | Monitoring | Uptime + alerting | Production | Alert-driven risk control |
| Late detection of failure | Monitoring | Alert validation | Production | Detection speed prioritized |

---

## Interpretation

- Security and data risks dominate over UI risks.
- Monitoring plays a central role in SaaS quality.
- Integration boundaries are more critical than user interface coverage.
- Production observability is treated as part of the testing model.

---

## Usage

This matrix is used to:

- justify testing scope decisions,
- guide CI enforcement,
- support release discussions,
- update risk priorities after incidents.
