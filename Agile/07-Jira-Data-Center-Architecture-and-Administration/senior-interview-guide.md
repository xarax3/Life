# File: Life/Agile/Jira/07-Jira-Data-Center-Architecture-and-Administration/senior-interview-guide.md

# Day 7 - Part 15

# Jira Data Center Senior Architect Interview & Evaluation Guide

> مجموعه پرسش‌ها و سناریوهای سطح Senior Jira Administrator / Jira Architect برای ارزیابی دانش معماری، Performance، Security و Operations.

---

# 254. Architecture Questions

## Q1. تفاوت Jira Server و Jira Data Center چیست؟

پاسخ مفهومی:

```text id="dcz1a8"
Server

Single Node

↓

Data Center

Multiple Nodes

+

Cluster

+

High Availability
```

---

ویژگی‌های Data Center:

```text id="3af8n2"
Cluster Management

Load Balancing

Shared Home

Node Scaling

High Availability
```

---

# Q2. چرا Jira Data Center به Database مشترک نیاز دارد؟

زیرا Database منبع اصلی اطلاعات است.

شامل:

```text id="h5u0pq"
Issues

Projects

Users

Configuration

Workflow Data
```

---

اما:

```text id="5x2y4m"
Search Data

↓

Lucene Index
```

به صورت جداگانه مدیریت می‌شود.

---

# Q3. نقش Shared Home چیست؟

Shared Home برای داده‌هایی است که تمام Nodeها باید ببینند.

مثال:

```text id="v5e7pw"
Attachments

Avatars

Plugin Data

Exports
```

---

# Q4. آیا می‌توان Jira Data Center را بدون Load Balancer اجرا کرد؟

از نظر فنی ممکن است، اما معماری استاندارد نیست.

مشکلات:

```text id="5v1r5m"
No Failover

No Traffic Distribution

Poor Availability
```

---

# 255. Database Questions

## Q5. چرا Database Performance برای Jira مهم است؟

چون عملیات Transactional در Database انجام می‌شود:

```text id="q8z7i0"
Create Issue

Update Issue

Workflow Transition

Permission Check
```

---

# Q6. افزایش Connection Pool همیشه خوب است؟

خیر.

زیاد کردن بیش از حد:

```text id="d2p8x6"
More Connections

↓

Database Pressure

↓

Performance Drop
```

---

# Q7. Slow Jira را چگونه بررسی می‌کنید؟

روش:

```text id="0f4k8v"
Check User Impact

↓

Check Application

↓

Check JVM

↓

Check Database

↓

Check Storage

↓

Check Network
```

---

# 256. JVM Questions

## Q8. Heap زیاد بهتر است؟

خیر.

Heap باید متناسب باشد.

مشکل Heap زیاد:

```text id="q3v1x8"
Long GC Pause

↓

Slow Application
```

---

# Q9. Full GC زیاد چه معنی دارد؟

معمولاً:

```text id="3zq0s1"
Memory Pressure

+

Object Retention

+

Heap Issue
```

---

# Q10. Thread Dump چه زمانی گرفته می‌شود؟

زمان:

```text id="u7m9p4"
High CPU

Slow Requests

Deadlock

Application Hang
```

---

# 257. Cluster Questions

## Q11. اگر یک Node خراب شود چه اتفاقی می‌افتد؟

```text id="j4r6a2"
Health Check Failed

↓

Load Balancer Removes Node

↓

Users Continue On Other Nodes
```

---

# Q12. Cluster Lock چیست؟

برای جلوگیری از اجرای همزمان یک عملیات:

```text id="9j6x2q"
Node A Executes Job

Node B Waits
```

---

# 258. Security Questions

## Q13. Authentication و Authorization چه تفاوتی دارند؟

Authentication:

```text id="b6k3j9"
Who Are You?
```

Authorization:

```text id="c1s7m8"
What Can You Do?
```

---

# Q14. بهترین مدل Permission چیست؟

مدل:

```text id="w8z4k1"
Group Based

+

Least Privilege
```

---

# 259. Backup Questions

## Q15. فقط Database Backup کافی است؟

خیر.

باید:

```text id="h7q2v9"
Database

+

Shared Home

+

Configuration
```

Backup شود.

---

# Q16. Backup چگونه تست می‌شود؟

با Restore واقعی:

```text id="p3n5x0"
Backup

↓

Restore Environment

↓

Validation
```

---

# 260. Upgrade Questions

## Q17. قبل از Upgrade چه کارهایی انجام می‌دهید؟

```text id="m8z6r2"
Check Compatibility

Backup

Test Upgrade

Plugin Validation

Rollback Plan
```

---

# Q18. Rolling Upgrade چیست؟

ارتقای Nodeها به صورت مرحله‌ای:

```text id="e4y9p3"
Remove Node

↓

Upgrade

↓

Validate

↓

Return

↓

Next Node
```

---

# 261. Troubleshooting Scenario

## Scenario

کاربران می‌گویند Jira کند شده است.

پاسخ Senior:

```text id="r8v5m0"
1. Determine Scope

2. Check Metrics

3. Analyze JVM

4. Check Database

5. Check Storage

6. Review Recent Changes

7. Apply Fix

8. Document Root Cause
```

---

# 262. Architect Evaluation Checklist

## Architecture

```text id="a9p6x3"
✓ Understand Cluster

✓ Understand Database

✓ Understand Storage

✓ Understand Network
```

---

## Performance

```text id="c7m2v8"
✓ JVM Analysis

✓ Database Optimization

✓ Thread Analysis

✓ Capacity Planning
```

---

## Operations

```text id="n4q8s1"
✓ Backup

✓ DR

✓ Upgrade

✓ Monitoring
```

---

## Security

```text id="f6k3w0"
✓ Authentication

✓ Authorization

✓ Hardening

✓ Audit
```

---

# 263. Day 7 Final Competency Map

```text id="x9d4p7"
Jira Architect

|

├── Architecture

├── Database

├── JVM

├── Cluster

├── Network

├── Security

├── Backup

├── Upgrade

├── Automation

└── Operations
```

---

# Day 7 Part 15 Summary

موضوعات:

✓ Senior Interview Questions
✓ Architecture Decisions
✓ Database Knowledge
✓ JVM Knowledge
✓ Cluster Understanding
✓ Security Concepts
✓ Backup Strategy
✓ Upgrade Strategy
✓ Troubleshooting Methodology

---

# Next Part

# Day 7 - Part 16

* Jira Data Center Advanced Performance Tuning
* Database Optimization
* JVM Advanced Tuning
* Index Optimization
* Large Instance Management
* Enterprise Scale Patterns
