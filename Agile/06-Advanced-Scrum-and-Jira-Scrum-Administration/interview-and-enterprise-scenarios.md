# Interview & Enterprise Scenarios

# Day 6 - Part 5
# Advanced Scrum Interview Scenarios & Enterprise Cases

> سناریوهای واقعی مدیریت Scrum در Jira Enterprise برای نقش‌های Senior Jira Administrator، Agile Consultant و Scrum Master.

---

# 73. Scenario: Sprint همیشه کارهای زیادی Carry Over دارد

## Problem

تیم در پایان هر Sprint:

- چندین Issue باز دارد.
- هدف Sprint کامل نمی‌شود.
- اعتماد Stakeholder کاهش پیدا می‌کند.

---

## تحلیل

بررسی:

```

Committed Work

vs

Completed Work

```

Metrics:

- Sprint Completion Rate
- Velocity Trend
- Carry Over Rate

---

## دلایل احتمالی

- Over Commitment
- Storyهای بزرگ
- Dependency زیاد
- Capacity اشتباه
- Interrupt Work

---

## راه‌حل

```

Improve Refinement

*

Better Capacity Planning

*

Smaller Stories

*

Protect Sprint Goal

```

---

# 74. Scenario: تیم Story Point بیشتری می‌خواهد ثبت کند

## Problem

تیم برای افزایش Velocity:

- Storyها را بزرگ‌تر Estimate می‌کند.
- Point Inflation ایجاد می‌شود.

---

## پاسخ صحیح

Velocity معیار Output است، نه Performance.

بررسی شود:

- آیا Cycle Time بهتر شده؟
- آیا Value بیشتر تحویل شده؟
- آیا Quality بهتر شده؟

---

# 75. Scenario: Product Owner وسط Sprint کار جدید اضافه می‌کند

## Problem

Scope ثابت نیست.

---

## بررسی

آیا تغییر:

- Critical Bug است؟
- Production Issue است؟
- Business Emergency است؟

---

## راه‌حل

اگر ضروری نیست:

انتقال به:

```

Product Backlog

```

اگر ضروری است:

با تیم:

```

Swap Scope

```

انجام شود.

---

# 76. Scenario: Developers همیشه منتظر QA هستند

## مشکل

Workflow:

```

Development

↓

QA Queue

↓

Done

```

---

## تحلیل

احتمال Bottleneck:

QA

---

## Metrics:

- CFD
- Cycle Time
- Aging Chart

---

## راه‌حل:

- Shift Left Testing
- Automation Testing
- Pair Testing
- افزایش همکاری Dev و QA

---

# 77. Scenario: Jira تعداد زیادی Workflow دارد

## Problem

سازمان:

```

200 Projects

150 Workflows

```

---

## مشکلات

- Maintenance سخت
- گزارش‌گیری سخت
- Migration مشکل

---

## راه‌حل Enterprise

Workflow استاندارد:

```

Simple

Reusable

Governed

```

---

# 78. Scenario: تیم‌ها Jira را متفاوت استفاده می‌کنند

## Problem

هر تیم:

- Field متفاوت
- Status متفاوت
- Workflow متفاوت

---

## راه‌حل

ایجاد:

## Jira Governance Model

شامل:

- Templates
- Standards
- Documentation
- Approval Process

---

# 79. Scenario: مدیر فقط Dashboard می‌خواهد

## اشتباه

ساخت صدها Gadget.

---

## روش درست

ابتدا سؤال:

```

What Decision Should This Dashboard Support?

```

---

سپس:

```

Business Question

↓

Metric

↓

Dashboard

↓

Action

```

---

# 80. Scenario: Sprint Velocity کاهش یافته است

## بررسی اولیه

Velocity به تنهایی کافی نیست.

بررسی:

```

Velocity

*

Cycle Time

*

Throughput

*

Capacity

```

---

# دلایل احتمالی

- تغییر اعضای تیم
- تعطیلات
- Technical Debt
- افزایش Complexity
- کاهش Capacity

---

# 81. Scenario: تیم Bug زیادی تولید می‌کند

## Metrics

بررسی:

- Defect Rate
- Escaped Defects
- Change Failure Rate

---

## راه‌حل

- Definition of Done قوی‌تر
- Automated Testing
- Code Review
- Quality Gate

---

# 82. Scenario: تیم نمی‌تواند Release را پیش‌بینی کند

## مشکل

Forecast غیرواقعی است.

---

## راه‌حل

استفاده از:

- Historical Velocity
- Throughput
- Cycle Time
- Monte Carlo Forecast

---

# 83. Enterprise Scrum Operating Model

مدل پیشنهادی:

```

Strategy

↓

Portfolio Management

↓

Product Management

↓

Scrum Teams

↓

Delivery

↓

Metrics

↓

Continuous Improvement

```

---

# 84. Scrum Governance Framework

## استانداردها

### Issue Types

```

Epic

Story

Task

Bug

Sub-task

```

---

### Workflow

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

### Required Fields

مثال:

- Summary
- Description
- Acceptance Criteria
- Priority
- Estimate

---

# 85. Jira Administration Checklist قبل از ایجاد پروژه جدید

بررسی:

```

Project Type

↓

Issue Types

↓

Workflow

↓

Permissions

↓

Screens

↓

Fields

↓

Automation

↓

Reports

```

---

# 86. Agile Health Assessment

برای ارزیابی تیم:

## Process

- آیا Sprint Goal وجود دارد؟
- آیا Refinement انجام می‌شود؟
- آیا Retrospective مؤثر است؟

---

## Delivery

- Cycle Time
- Lead Time
- Throughput

---

## Quality

- Defect Rate
- Test Coverage
- Production Issues

---

# 87. Scrum Maturity Model

## Level 1

Jira فقط برای ثبت Task استفاده می‌شود.

---

## Level 2

Sprint و Backlog استفاده می‌شود.

---

## Level 3

Metrics و Reporting فعال است.

---

## Level 4

Flow Optimization انجام می‌شود.

---

## Level 5

Continuous Improvement و Data Driven تصمیم‌گیری می‌شود.

---

# 88. Senior Jira Admin Mindset

یک Senior Jira Admin فقط Configuration انجام نمی‌دهد.

باید بتواند:

```

Business Requirement

↓

Process Design

↓

Jira Configuration

↓

Automation

↓

Reporting

↓

Optimization

```

را طراحی کند.

---

# Day 6 Extended Summary

موضوعات تکمیلی:

✓ Scrum Real World Scenarios  
✓ Sprint Failure Analysis  
✓ Jira Governance  
✓ Enterprise Standards  
✓ Dashboard Strategy  
✓ Agile Maturity Assessment  
✓ Senior Jira Admin Responsibilities  

---

# End of Day 6

روز ششم به صورت کامل پوشش داده شد.

موضوعات اصلی:

- Advanced Scrum
- Jira Scrum Administration
- Backlog Management
- Sprint Management
- Release Planning
- Governance
- Enterprise Best Practices
