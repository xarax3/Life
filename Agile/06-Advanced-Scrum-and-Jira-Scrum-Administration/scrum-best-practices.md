# Scrum Best Practices

# Day 6 - Part 4
# Scrum Anti Patterns, Enterprise Best Practices & Jira Governance

> بررسی مشکلات رایج Scrum، استانداردهای Enterprise Jira، Governance و سناریوهای واقعی مدیریت Scrum در سازمان‌های بزرگ.

---

# 51. Scrum Anti Patterns

## Anti Pattern چیست؟

رفتاری که ظاهراً شبیه Agile است اما باعث کاهش ارزش و کیفیت فرآیند می‌شود.

---

# 52. Velocity as Performance Metric

## مشکل:

استفاده از Velocity برای ارزیابی افراد یا تیم‌ها.

مثال اشتباه:

```

Team A = 80 Story Point

Team B = 40 Story Point

پس Team A بهتر است

```

---

## چرا اشتباه است؟

Velocity:

- نسبی است.
- بین تیم‌ها قابل مقایسه نیست.
- به Context تیم وابسته است.

---

## استفاده صحیح:

Velocity فقط برای:

```

Forecast

*

Planning

```

استفاده می‌شود.

---

# 53. Too Much Work In Progress

مشکل:

تیم چندین کار را همزمان شروع می‌کند.

نتیجه:

```

Context Switching ↑

Cycle Time ↑

Delivery Delay ↑

```

---

راه‌حل:

```

Limit WIP

Finish Before Start

```

---

# 54. Large Stories

مشکل:

Story بزرگ:

- Estimate سخت
- Feedback دیر
- Risk بالا

---

راه‌حل:

Split کردن:

```

Epic

↓

Feature

↓

Story

↓

Task

````

---

# 55. No Definition of Done

مشکل:

هر فرد تعریف متفاوتی از Done دارد.

---

نتیجه:

- کیفیت پایین
- Rework
- Bug زیاد

---

راه‌حل:

DoD مشخص:

```text
Code Complete

+

Review Done

+

Test Passed

+

Documentation Updated

+

Deploy Ready
````

---

# 56. Sprint Without Goal

مشکل:

Sprint فقط لیستی از Taskها می‌شود.

---

Sprint خوب:

دارای هدف است.

مثال:

ضعیف:

```
Complete 20 Issues
```

---

قوی:

```
Enable Customer Registration Capability
```

---

# 57. Daily Scrum تبدیل به Status Meeting

مشکل:

مدیر از افراد گزارش می‌گیرد.

---

هدف Daily Scrum:

تیم برای هماهنگی خودش برنامه‌ریزی کند.

---

تمرکز:

```
Progress

+

Plan

+

Impediments
```

---

# 58. Product Owner بدون Decision Power

مشکل:

PO فقط منتقل‌کننده درخواست‌هاست.

---

PO واقعی:

* اولویت تعیین می‌کند.
* Value را مشخص می‌کند.
* تصمیم محصول می‌گیرد.

---

# 59. Backlog بدون Refinement

مشکل:

Storyها آماده Sprint نیستند.

---

نتیجه:

* Planning طولانی
* Estimate ضعیف
* Sprint Failure

---

# 60. Jira Configuration Anti Patterns

## Custom Field زیاد

مشکل:

* Performance پایین
* گزارش سخت
* Maintenance زیاد

---

Best Practice:

قبل از ساخت Field:

بپرسید:

```
آیا واقعاً نیاز است؟
```

---

# 61. Workflow Explosion

مشکل:

ساخت Workflow جدا برای هر تیم.

---

نتیجه:

* Governance سخت
* Migration سخت
* گزارش‌گیری پیچیده

---

Best Practice:

Workflow استاندارد:

```
To Do

↓

In Progress

↓

Review

↓

Testing

↓

Done
```

---

# 62. Permission Complexity

مشکل:

Permissionهای بسیار پیچیده.

---

نتیجه:

* مشکلات دسترسی
* خطای کاربر
* مدیریت سخت

---

Best Practice:

استفاده از:

* Project Roles
* Groups
* Permission Schemes استاندارد

---

# 63. Jira Governance Model

Governance یعنی:

مدیریت استاندارد تغییرات Jira.

---

شامل:

```
Request

↓

Review

↓

Approval

↓

Implementation

↓

Documentation
```

---

# 64. Jira Naming Convention

استاندارد نام‌گذاری:

## Projects

مثال:

```
APP-PAYMENT
APP-MOBILE
OPS-INFRA
```

---

## Components

مثال:

```
Backend

Frontend

Database

Infrastructure
```

---

## Versions

مثال:

```
v2.5.0

2026.Q1.Release
```

---

# 65. Custom Field Governance

قبل از ایجاد Field جدید:

بررسی:

* آیا Field مشابه وجود دارد؟
* آیا برای Reporting لازم است؟
* آیا Automation نیاز دارد؟

---

چرخه:

```
Request

↓

Analysis

↓

Approval

↓

Create

↓

Document
```

---

# 66. Jira Performance Considerations

عوامل تأثیرگذار:

## Issue History زیاد

باعث:

* Query کند
* Index بزرگ

---

## Custom Field زیاد

باعث:

* افزایش Database Load

---

## Workflow پیچیده

باعث:

* Transaction بیشتر

---

# 67. Enterprise Jira Best Practice

## Keep Jira Simple

اصل:

```
Simple Configuration

=

Better Maintainability
```

---

# 68. Scrum Metrics Dashboard

داشبورد پیشنهادی:

```
Sprint Burndown

Velocity Trend

Sprint Health

Blockers

Carry Over

Cycle Time
```

---

# 69. Senior Jira Admin Responsibilities

یک Senior Jira Admin باید:

## Technical

* Architecture
* Performance
* Database
* Integration

---

## Functional

* Scrum
* Kanban
* Workflow Design
* Reporting

---

## Governance

* Standards
* Documentation
* Change Management

---

# 70. Interview Scenarios

## Scenario 1

### تیم‌ها Workflowهای مختلف می‌خواهند.

راه‌حل:

بررسی نیاز واقعی.

اگر تفاوت واقعی وجود ندارد:

Workflow مشترک.

---

## Scenario 2

### Jira کند شده است.

بررسی:

* Custom Fields
* Database
* Index
* Apps
* Background Jobs

---

## Scenario 3

### مدیر Velocity بالا می‌خواهد.

پاسخ:

Velocity هدف نیست.

تمرکز:

* Value Delivery
* Predictability
* Quality

---

# 71. Enterprise Scrum Architecture

```text
Business Strategy

↓

Product Vision

↓

Portfolio

↓

Epic

↓

Story

↓

Sprint

↓

Increment

↓

Release

↓

Customer Value
```

---

# 72. Day 6 Final Checklist

## Scrum

✓ Roles
✓ Events
✓ Artifacts
✓ Sprint Management
✓ Refinement
✓ Estimation

---

## Jira

✓ Board Configuration
✓ Workflow
✓ Permissions
✓ Screens
✓ Reports
✓ Automation

---

## Enterprise

✓ Governance
✓ Standards
✓ Performance
✓ Metrics
✓ Scaling

---

# Day 6 Complete Summary

در روز ششم یاد گرفتیم:

* Scrum Advanced Concepts
* Product Backlog Management
* Story Engineering
* Estimation
* Sprint Planning
* Jira Scrum Configuration
* Release Management
* Governance
* Enterprise Best Practices

---

# Next Step

## Day 7 - Jira Administration Deep Dive

موضوعات:

* Jira Architecture
* Data Model
* Database Schema
* Index Management
* JVM Tuning
* Application Properties
* Jira Upgrade Strategy
* Backup & Restore
* Disaster Recovery
* Security Hardening
* Performance Optimization

```
```
