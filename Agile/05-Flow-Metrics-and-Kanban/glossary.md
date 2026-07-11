# Agile, Scrum, Kanban & Jira Metrics Glossary

> واژه‌نامه مفاهیم کلیدی Agile، Scrum، Kanban، Jira Reporting، Flow Metrics و DevOps Metrics.

---

# A

## Agile

رویکرد توسعه نرم‌افزار که بر تحویل تدریجی، همکاری، بازخورد سریع و سازگاری با تغییرات تمرکز دارد.

---

## Aging Work Item

مدت زمانی که یک Work Item باز در وضعیت انجام قرار دارد.

مثال:

```
Story In Progress = 12 Days
```

---

## Automation

اجرای خودکار فعالیت‌ها بدون دخالت دستی.

در Jira:

```
Project Settings

↓

Automation
```

---

# B

## Backlog

لیست تمام کارهای آینده محصول.

شامل:

- Epic
- Story
- Task
- Bug

---

## Burnup Chart

نموداری که:

- کار انجام‌شده
- تغییرات Scope

را نمایش می‌دهد.

---

## Burndown Chart

نموداری که مقدار کار باقی‌مانده را نمایش می‌دهد.

---

## Blocker

کاری که باعث توقف پیشرفت یک Issue می‌شود.

مثال:

```
Waiting for External API
```

---

# C

## Capacity

توان واقعی تیم برای انجام کار در یک Sprint.

---

## CFD (Cumulative Flow Diagram)

نموداری که جریان کار بین Statusها را نمایش می‌دهد.

---

## Cycle Time

زمان از شروع کار واقعی تا Done شدن.

فرمول:

```
Done Date - Start Date
```

---

## Control Chart

گزارش Jira برای تحلیل Cycle Time و Lead Time.

مسیر:

```
Board

↓

Reports

↓

Control Chart
```

---

## Change Failure Rate

درصد Deployهایی که باعث Failure شده‌اند.

---

# D

## DORA Metrics

چهار شاخص استاندارد DevOps:

- Deployment Frequency
- Lead Time for Changes
- Change Failure Rate
- MTTR

---

## Deployment Frequency

تعداد Deployهای موفق در یک بازه زمانی.

---

## Definition of Done (DoD)

شرایطی که مشخص می‌کند یک کار چه زمانی کامل محسوب می‌شود.

---

# E

## Epic

یک قابلیت بزرگ که شامل چند Story است.

مثال:

```
Epic:
Payment System

Stories:
- Card Payment
- Wallet Payment
- Refund
```

---

## Estimate

تخمین میزان تلاش موردنیاز برای انجام کار.

---

# F

## Flow Efficiency

نسبت زمان ارزش‌آفرین به کل زمان انجام کار.

---

## Feature Flag

فعال یا غیرفعال کردن قابلیت بدون Deploy مجدد.

---

# I

## Issue

هر واحد کاری در Jira.

انواع:

- Story
- Task
- Bug
- Epic

---

## Incident

اختلال یا کاهش کیفیت سرویس.

در Jira Service Management مدیریت می‌شود.

---

# J

## JQL (Jira Query Language)

زبان جستجوی Jira.

مثال:

```jql
project = APP
AND status = Done
```

---

# K

## Kanban

روش مدیریت Flow با تمرکز بر:

- Visualization
- WIP Limit
- Continuous Delivery

---

## KPI

شاخص کلیدی عملکرد.

---

# L

## Lead Time

زمان از درخواست تا تحویل.

---

## Lead Time for Changes

زمان از Commit تا Production Deploy.

---

# M

## MTTR

Mean Time To Recovery

میانگین زمان بازیابی سرویس.

---

## Milestone

نقطه مهم در مسیر پروژه.

---

# P

## Percentile

روش تحلیل توزیع داده.

مثال:

```
85% Items <= 10 Days
```

---

## Planning Poker

روش تخمین گروهی با Story Point.

---

## Product Backlog

لیست اولویت‌بندی شده کارهای محصول.

---

# R

## Release

انتشار یک نسخه قابل استفاده از محصول.

---

## Release Planning

برنامه‌ریزی برای تحویل نسخه.

---

# S

## Scrum

Framework Agile با:

- Sprint
- Scrum Team
- Events
- Artifacts

---

## Sprint

بازه زمانی ثابت برای تولید Increment.

معمولاً:

```
1-4 Weeks
```

---

## Sprint Goal

هدف اصلی یک Sprint.

---

## Story Point

واحد نسبی اندازه‌گیری پیچیدگی کار.

---

## SLA

Service Level Agreement

تعهد رسمی سطح سرویس.

---

## SLE

Service Level Expectation

انتظار آماری زمان تحویل کار.

---

## SLO

Service Level Objective

هدف داخلی سطح سرویس.

---

# T

## Throughput

تعداد آیتم‌های تکمیل‌شده در واحد زمان.

---

## Timebox

بازه زمانی محدود و مشخص.

مثال:

```
Sprint = 2 Weeks
```

---

# V

## Velocity

مقدار Story Point تکمیل‌شده در Sprint.

---

## Value Stream

مسیر کامل ایجاد ارزش:

```
Idea

↓

Development

↓

Delivery

↓

Customer
```

---

# W

## WIP (Work In Progress)

تعداد آیتم‌های در حال انجام.

---

## WIP Limit

محدودیت تعداد کارهای همزمان.

مثال:

```
In Progress <= 5
```

---

# Jira Reports Glossary

| Report | کاربرد |
|-|-|
| Burndown | Remaining Work |
| Burnup | Progress + Scope |
| Velocity Chart | Sprint Output |
| Control Chart | Cycle Time |
| CFD | Flow Health |
| Sprint Report | Sprint Analysis |
| Release Report | Version Progress |

---

# DevOps Glossary

| Term | Meaning |
|-|-|
| CI | Continuous Integration |
| CD | Continuous Delivery |
| CD | Continuous Deployment |
| Pipeline | Automated Delivery Flow |
| Rollback | برگشت نسخه |
| Canary | انتشار تدریجی |
| Observability | مشاهده‌پذیری سیستم |

---

# Final Reference

چرخه کامل Delivery:

```
Backlog

↓

Refinement

↓

Planning

↓

Development

↓

Testing

↓

Deployment

↓

Monitoring

↓

Improvement
```

Metrics:

```
Flow Metrics

+

Agile Metrics

+

DORA Metrics

+

ITSM Metrics
```

باعث ایجاد دید کامل نسبت به سیستم Delivery می‌شوند.
