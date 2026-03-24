# Widget Explanations

This document describes each widget included in the CloudWatch dashboard and its purpose.

---

## Single Value Widgets

### Current Request Rate
- Type: Single Value
- Metric: RequestCount
- Purpose: Displays the current volume of incoming requests to the application.

### Error Rate (%)
- Type: Single Value (Math Expression)
- Metrics: HTTPCode_Target_5XX_Count / RequestCount
- Purpose: Shows the percentage of failed requests, indicating system reliability.

### P95 Latency
- Type: Single Value
- Metric: TargetResponseTime (p95)
- Purpose: Represents user experience by showing response time at the 95th percentile.

### Healthy Targets
- Type: Single Value
- Metric: HealthyHostCount
- Purpose: Indicates how many backend instances are available and healthy.

---

## Golden Signals Widgets

### Traffic - Request Rate
- Type: Time Series
- Metric: RequestCount
- Purpose: Tracks request volume trends over time.

### Errors - HTTP Status Codes
- Type: Time Series (Stacked)
- Metrics: 2XX, 4XX, 5XX
- Purpose: Shows distribution of successful and failed requests.

### Latency - Response Time Percentiles
- Type: Time Series
- Metrics: P50, P95, P99
- Purpose: Provides insight into response time distribution.

### Saturation - Target Health
- Type: Time Series
- Metrics: HealthyHostCount, UnHealthyHostCount
- Purpose: Indicates system capacity and instance health.

---

## EC2 Resource Utilization

### CPU Utilization
- Type: Time Series
- Metric: CPUUtilization
- Purpose: Shows how much CPU is being used.

### Memory Utilization
- Type: Time Series
- Metric: mem_used_percent (CWAgent)
- Purpose: Tracks memory usage.

### Network In/Out
- Type: Time Series
- Metrics: NetworkIn, NetworkOut
- Purpose: Displays network traffic levels.

### Disk Usage
- Type: Time Series
- Metric: disk_used_percent (CWAgent)
- Purpose: Monitors disk space consumption.

---

## Correlation View

### Latency vs Request Rate vs Error Rate vs CPU
- Type: Time Series (Multiple metrics)
- Purpose: Combines key metrics to help identify relationships and root causes during incidents.

This view is particularly useful when investigating performance degradation.