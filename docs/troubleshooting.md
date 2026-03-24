# Troubleshooting Guide

This document describes how to use the dashboard to investigate common issues.

---

## High Latency

### Symptoms:
- Increased P95/P99 latency
- Slow response times

### What to check:
- CPU utilization (is it high?)
- Request rate (is there a spike?)
- Error rate (are failures increasing?)

### Possible causes:
- High traffic load
- Resource saturation
- Inefficient application performance

---

## High Error Rate

### Symptoms:
- Increase in 5XX errors
- Decrease in successful (2XX) responses

### What to check:
- Target health (are instances failing?)
- CPU and memory usage
- Recent deployments (if applicable)

### Possible causes:
- Application crashes
- Misconfigurations
- Backend service failures

---

## Low Healthy Target Count

### Symptoms:
- Increase in unhealthy targets
- Reduced availability

### What to check:
- Instance health checks
- CPU/memory spikes
- Application logs

### Possible causes:
- Instance failure
- Health check misconfiguration
- Application not responding

---

## High CPU Utilization

### Symptoms:
- CPU consistently above threshold
- Latency increase

### What to check:
- Request rate
- Memory usage
- Correlation view

### Possible causes:
- Traffic spikes
- Inefficient code
- Insufficient scaling

---

## General Debugging Strategy

1. Start with top-level metrics
2. Identify anomalies in Golden Signals
3. Check infrastructure metrics
4. Use correlation view to connect events
5. Confirm findings with logs and alarms

---

## Summary

Effective troubleshooting requires correlating multiple signals rather than relying on a single metric. This dashboard provides a structured way to investigate issues systematically.