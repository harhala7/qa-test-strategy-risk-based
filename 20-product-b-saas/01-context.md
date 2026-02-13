# Product B – Context (IoT Device Management SaaS)

## Product type

B2B SaaS platform for managing connected IoT devices.

The system allows business customers to:

- register and manage devices,
- collect telemetry data,
- configure device parameters remotely,
- monitor device health,
- generate analytics dashboards.

Revenue model: subscription-based (monthly / annual plans).

---

## Business context

- Revenue depends on subscription retention, not single transactions.
- Platform reliability and data accuracy are critical.
- Downtime or incorrect telemetry data reduces customer trust and increases churn risk.
- SLAs may exist for uptime and data availability.

Business prioritizes stability, scalability, and long-term customer retention.

---

## Users

Primary users:
- business administrators,
- operations teams,
- technical support teams.

Users expect:
- reliable real-time or near-real-time data,
- accurate device status,
- secure access control,
- predictable system performance.

---

## Technology assumptions

Typical architecture includes:

- web frontend for dashboards,
- backend APIs for device and data management,
- device communication layer (MQTT / HTTP or similar),
- database storing telemetry data,
- authentication and role-based access control.

High availability and scalability are expected.

---

## Team and delivery model

- Cross-functional product team.
- Continuous delivery model.
- Infrastructure may be cloud-based.
- Monitoring and observability are essential parts of the system.

---

## Quality challenges implied by context

- Data integrity risks (incorrect or lost telemetry).
- Device communication failures.
- Authorization and access control errors.
- Performance and scalability under growing device fleet.
- SLA and uptime commitments.
- Multi-tenant isolation risks.

These risks differ significantly from transactional e-commerce systems.
