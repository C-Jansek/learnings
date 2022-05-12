---
sidebar_position: 4
---

# Monitoring

Monitoring is a tool for teams to gain understanding about the state of their systems based on gathered data. Real-time insights on performance, system health and scalability.
This data is useful to reduce costs, improve productivity and increase reliability.

## Metrics

(Some) Key metrics that can help monitor the system health and performance are:

- Latency - Time between the start of an event and its completion
- Traffic - Amount of system usage during a time period
- Errors - High amounts can indicate deeper issues
- Saturation - Running close to system load limits can reduce performance

## SLO, SLI, SLA

A way to relate business goals and objectives to received data.

### Service Level Objective (SLO) {#slo}

A range of valid measurements for a metric. Not meeting these requirements requires action (such as speeding up load times if they are too high).

### Service Level Indicator (SLI) {#sli}

The current measurement of a metric related to an SLO.

### Service Level Agreement (SLA) {#sla}

Contract with customers to meet a metric. It binds a business to a level of expected service promised to their customers.

## Tools

Tools are used to track key metrics, create an overview of resource utilization and system health.

Different tools include:

- **Zabbix** - Offers many features such as a centralized, clear web interface. It can directly monitor Java applications with built-in graphing and visualization.
- **Prometheus** - Collects metrics values from target systems with its own PromQL query language to select real time data.
- **Sensu** - Offers high extensibility and scalability monitoring cloud infrastructure, with code defined monitoring requirements.
- **Monyog** - Database performance monitoring.

## Alerting

Alerts can be used to notify about a change of state (or problem).

To avoid alert fatigue, alert only when human intervention is required immediately. Also indicate urgency clearly and ensure that there are no duplicate alerts.

## Observability

Systems with high observability help a team track and solve issues. Low observability means that the system does not provide useful data which makes it more difficult to track and solve issues.

To improve observability:

- Align teams with [SLO's](#slo)
- Create meaningful alerts
- Optimize logging with descriptive messages
- Automate processes

## Monitoring Quality

Effective system monitoring uses:

- Actionable alerts, customized to the organization
- Available and understandable application logs
- Build and deployment process logging

Issues indicating ineffective monitoring:

- False negatives - System fails to alert about a user-affecting issue
- False positives - System alerts without an actual issue
- Unactionable alerts - Alerts that have little to do with a problem, no action required
