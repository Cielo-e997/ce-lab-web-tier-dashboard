# Design Decisions

This document explains the reasoning behind the dashboard layout and visualization choices.

---

## Dashboard Structure

The dashboard is organized in a top-down approach to support fast incident response:

1. Summary (Top Row)
   - Single-value widgets provide an instant view of system health.
   - Allows quick detection of anomalies without analyzing trends.

2. Golden Signals Section
   - Includes Traffic, Errors, Latency, and Saturation.
   - These are the core indicators of system health and user experience.
   - Positioned near the top for quick access during incidents.

3. Resource Utilization Section
   - Displays EC2 metrics such as CPU, memory, network, and disk.
   - Helps determine whether issues are caused by infrastructure limits.

4. Correlation View (Bottom)
   - Combines multiple metrics into a single graph.
   - Supports root cause analysis by revealing relationships between system behavior.

---

## Visualization Choices

### Single Value Widgets
- Used for real-time status indicators.
- Provide immediate visibility of current system state.

### Time Series Widgets
- Used for trend analysis.
- Help identify patterns over time such as spikes or gradual degradation.

### Stacked Graphs (Errors)
- Useful for comparing proportions of different HTTP status codes.
- Makes it easier to detect abnormal error patterns.

### Percentiles (Latency)
- P50, P95, and P99 provide a complete picture of performance.
- Helps identify tail latency issues affecting users.

### Correlation Graph
- Multiple metrics on one chart help visualize cause-and-effect relationships.
- Essential for debugging performance issues.

---

## Layout Decisions

- Left-to-right grouping: Related metrics are placed together for intuitive reading.
- Top-to-bottom flow: From detection → analysis → root cause.
- Clear section separation: Text widgets are used as headers to improve readability.

---

## Design Goals

- Fast problem detection
- Clear visualization of system health
- Efficient root cause analysis
- Minimal cognitive load for on-call engineers