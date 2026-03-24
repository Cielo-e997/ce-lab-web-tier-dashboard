# Dashboard Guide

This guide explains how to read and use the Web Tier Health Dashboard effectively.

---

## Overview

The dashboard is designed to provide a quick understanding of system health and help identify issues efficiently.

It is structured in layers, from high-level overview to detailed analysis.

---

## How to Read the Dashboard

### 1. Top Section — Current State

Start with the top row:

- Current Request Rate
- Error Rate (%)
- P95 Latency
- Healthy Targets

These widgets provide an instant snapshot of system health.

---

### 2. Golden Signals — Core Health Indicators

Focus on the four Golden Signals:

- Traffic: Request Rate
- Errors: HTTP status codes (2XX, 4XX, 5XX)
- Latency: Response time percentiles
- Saturation: Target health

These metrics help determine if the system is under stress or failing.

---

### 3. Resource Utilization — Infrastructure Health

If issues are detected in the Golden Signals, check:

- CPU usage
- Memory usage
- Network traffic
- Disk utilization

This helps identify whether the issue is caused by resource constraints.

---

### 4. Correlation View — Root Cause Analysis

Use the correlation graph to compare:

- Latency
- Request rate
- Error rate
- CPU usage

Look for patterns such as:

- High traffic → increased CPU → higher latency
- Increased errors during latency spikes

---

## Best Practices

- Always start from the top and move downward
- Use trends instead of single points for analysis
- Correlate multiple metrics before drawing conclusions
- Use this dashboard alongside logs and alarms

---

## Summary

This dashboard helps engineers move quickly from detection to diagnosis, reducing time to resolution during incidents.