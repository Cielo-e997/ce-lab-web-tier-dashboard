# Lab M6.03 - Web Tier Dashboard

## Overview

This project implements a CloudWatch dashboard to monitor the health of a web tier using the four Golden Signals: latency, traffic, errors, and saturation.

The dashboard provides a centralized view that allows quick identification of issues and supports efficient troubleshooting.

---

## Dashboard Design Rationale

The dashboard is structured to prioritize fast incident response:

- Top section: Single-value widgets showing current system state
- Middle section (Golden Signals): Trends over time for core service health indicators
- Resource section: EC2 metrics to identify infrastructure bottlenecks
- Bottom section (Correlation view): Combined metrics to support root cause analysis

This layout allows engineers to quickly move from detection → investigation → diagnosis.

---

## Widget Explanations

| Widget | Type | Purpose |
|------|------|--------|
| Current Request Rate | Single Value | Shows current traffic level |
| Error Rate (%) | Single Value | Indicates percentage of failed requests |
| P95 Latency | Single Value | Measures user experience performance |
| Healthy Targets | Single Value | Shows availability of backend instances |
| Traffic - Request Rate | Time Series | Displays traffic trends over time |
| Errors - HTTP Codes | Time Series | Breaks down error and success responses |
| Latency Percentiles | Time Series | Shows performance distribution (P50, P95, P99) |
| Target Health | Time Series | Tracks healthy vs unhealthy instances |
| CPU Utilization | Time Series | Measures compute usage |
| Memory Utilization | Time Series | Tracks memory consumption |
| Network In/Out | Time Series | Shows network throughput |
| Disk Usage | Time Series | Monitors disk utilization |
| Correlation View | Time Series | Combines metrics to identify root causes |

---

## How to Use This Dashboard

1. Start with the top row to assess current system status
2. Review Golden Signals for performance and reliability trends
3. Check EC2 resource metrics for infrastructure issues
4. Use the correlation graph to identify relationships between metrics

---

## Screenshots

- screenshots/01-full-dashboard.png  
- screenshots/02-golden-signals.png  
- screenshots/03-resource-utilization.png  
- screenshots/04-correlation-view.png