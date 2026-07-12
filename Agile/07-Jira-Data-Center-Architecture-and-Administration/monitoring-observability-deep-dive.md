# File: Life/Agile/Jira/07-Jira-Data-Center-Architecture-and-Administration/monitoring-observability-deep-dive.md

# Day 7 - Part 18

# Jira Data Center Monitoring & Observability Deep Dive

> طراحی سیستم Monitoring و Observability برای Jira Data Center در سطح Enterprise و SRE، شامل Metrics، Logging، Tracing، Alerting و داشبوردهای عملیاتی.

---

# 306. Monitoring vs Observability

این دو مفهوم یکسان نیستند.

## Monitoring

پاسخ به سؤال:

```text id="obs01"
Is the system healthy?
```

نمونه:

* CPU Usage
* Memory Usage
* Disk Usage
* HTTP Status

---

## Observability

پاسخ به سؤال:

```text id="obs02"
Why is the system unhealthy?
```

هدف:

درک علت اصلی مشکل (Root Cause).

---

# 307. Three Pillars of Observability

مدل استاندارد:

```text id="obs03"
Metrics

+

Logs

+

Traces
```

---

## Metrics

اعداد قابل اندازه‌گیری:

```text id="obs04"
CPU

RAM

Requests/sec

Latency

GC Time
```

---

## Logs

ثبت رویدادها:

```text id="obs05"
INFO

WARN

ERROR

DEBUG
```

---

## Traces

نمایش مسیر یک درخواست:

```text id="obs06"
Client

↓

Load Balancer

↓

Jira

↓

Database
```

---

# 308. Golden Signals (SRE)

چهار شاخص اصلی:

```text id="obs07"
Latency

Traffic

Errors

Saturation
```

---

## Latency

زمان پاسخ:

```text id="obs08"
Average

P95

P99
```

---

## Traffic

حجم درخواست‌ها:

```text id="obs09"
Requests/sec

Active Users
```

---

## Errors

بررسی:

```text id="obs10"
HTTP 5xx

Application Exceptions

Failed Jobs
```

---

## Saturation

استفاده از منابع:

```text id="obs11"
CPU

Memory

Disk

Connection Pool
```

---

# 309. Monitoring Stack

نمونه Enterprise:

```text id="obs12"
Jira

↓

JMX Exporter

↓

Prometheus

↓

Grafana

↓

Alertmanager
```

---

# 310. Application Metrics

شاخص‌های مهم:

```text id="obs13"
Login Success Rate

Issue Creation Time

Workflow Execution

REST API Response

Background Jobs
```

---

# 311. JVM Metrics

مانیتورینگ JVM:

```text id="obs14"
Heap Used

Heap Max

GC Count

GC Pause

Thread Count

Class Loading
```

---

# 312. Database Metrics

برای PostgreSQL:

```text id="obs15"
Connections

Slow Queries

Locks

Replication Delay

Transactions/sec

Cache Hit Ratio
```

---

# 313. Storage Metrics

بررسی:

```text id="obs16"
Latency

IOPS

Disk Usage

NFS Availability
```

---

# 314. Network Metrics

```text id="obs17"
Bandwidth

Packet Loss

TCP Retransmission

Connection Count
```

---

# 315. Log Collection Architecture

مدل پیشنهادی:

```text id="obs18"
Jira Nodes

↓

Filebeat / Fluent Bit

↓

Logstash / OpenSearch

↓

Dashboard
```

---

# 316. Log Classification

سطوح:

```text id="obs19"
INFO

WARN

ERROR

FATAL
```

---

نمونه ERROR:

```text id="obs20"
Database Connection Failed
```

---

# 317. Alert Engineering

Alert خوب:

```text id="obs21"
Specific

Actionable

Measurable

Low Noise
```

---

نمونه:

```text id="obs22"
Heap Usage > 90%

For 10 Minutes
```

---

# 318. Dashboard Design

Dashboard باید شامل:

```text id="obs23"
Application

JVM

Database

Infrastructure

Security
```

---

# 319. Capacity Monitoring

پیش‌بینی رشد:

```text id="obs24"
Current Usage

↓

Growth Trend

↓

Capacity Forecast
```

---

# 320. SRE Operational Model

چرخه:

```text id="obs25"
Observe

↓

Detect

↓

Respond

↓

Recover

↓

Improve
```

---

# 321. Mean Time Metrics

شاخص‌ها:

```text id="obs26"
MTTD

MTTR

MTBF
```

---

## MTTD

Mean Time To Detect

---

## MTTR

Mean Time To Repair

---

## MTBF

Mean Time Between Failures

---

# 322. Monitoring Checklist

```text id="obs27"
✓ Application Metrics

✓ JVM Metrics

✓ Database Metrics

✓ Storage Metrics

✓ Network Metrics

✓ Alert Rules

✓ Dashboards

✓ Log Collection
```

---

# Day 7 Part 18 Summary

موضوعات:

✓ Monitoring vs Observability
✓ Three Pillars of Observability
✓ Golden Signals (SRE)
✓ Metrics Collection
✓ JVM Monitoring
✓ PostgreSQL Monitoring
✓ Log Aggregation
✓ Alert Engineering
✓ Dashboard Design
✓ Operational Metrics

---

# Next Part

# Day 7 - Part 19

* Enterprise Runbooks
* Incident Response Playbooks
* Root Cause Analysis (RCA)
* Postmortem Process
* Operational Excellence
* Final Day 7 Wrap-up
