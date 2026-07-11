# Agile, Scrum, Kanban & Jira Interview Notes

> مجموعه سوالات و پاسخ‌های مهم برای مصاحبه‌های Senior Jira Administrator، Agile Consultant، Scrum Master و DevOps Delivery Management.

---

# Section 1: Agile Fundamentals

---

## Q1: Agile چیست؟

Agile یک رویکرد توسعه محصول است که بر:

- تحویل تدریجی
- بازخورد سریع
- همکاری تیمی
- پذیرش تغییر

تمرکز دارد.

هدف Agile:

```
Deliver Value Faster
```

---

## Q2: تفاوت Agile و Waterfall چیست؟

| Agile | Waterfall |
|-|-|
| Iterative | Sequential |
| تغییرپذیر | ثابت |
| Feedback مداوم | Feedback دیر |
| Incremental Delivery | Final Delivery |

---

## Q3: چهار ارزش اصلی Agile چیست؟

طبق Agile Manifesto:

1. افراد و تعاملات بیشتر از فرآیندها و ابزارها
2. محصول کارا بیشتر از مستندات جامع
3. همکاری مشتری بیشتر از قرارداد
4. پاسخ به تغییر بیشتر از پیروی از برنامه

---

# Section 2: Scrum

---

## Q4: Scrum چیست؟

یک Framework برای مدیریت توسعه محصول پیچیده با استفاده از:

- Sprint
- Scrum Roles
- Events
- Artifacts

---

## Q5: نقش‌های Scrum چیست؟

سه نقش اصلی:

## Product Owner

مسئول:

- Product Backlog
- Prioritization
- Value

---

## Scrum Master

مسئول:

- Scrum Process
- Removing Impediments
- Coaching Team

---

## Developers

مسئول:

- ایجاد Increment
- Quality
- Delivery

---

# Q6: Sprint چیست؟

یک Timebox مشخص برای تولید Increment.

معمولاً:

```
1-4 Weeks
```

---

# Q7: Sprint Planning چیست؟

جلسه‌ای برای تعیین:

- Sprint Goal
- Sprint Backlog
- نحوه انجام کار

---

# Q8: Daily Scrum چیست؟

جلسه 15 دقیقه‌ای برای بررسی:

- Progress
- Plan
- Blockers

---

# Q9: Sprint Review چیست؟

جلسه بررسی Increment با Stakeholderها.

---

# Q10: Sprint Retrospective چیست؟

جلسه بهبود فرآیند تیم.

تمرکز:

```
What went well?

What can improve?
```

---

# Section 3: Jira Scrum

---

## Q11: ساختار Issue در Jira چگونه است؟

معمولاً:

```
Epic

↓

Story

↓

Task

↓

Sub-task
```

---

## Q12: Epic چیست؟

یک قابلیت بزرگ که شامل چند Story است.

---

## Q13: Story Point چیست؟

اندازه‌گیری نسبی پیچیدگی کار.

بر اساس:

- Complexity
- Effort
- Uncertainty

---

# Section 4: Estimation

---

## Q14: چرا از ساعت برای Estimate استفاده نمی‌کنیم؟

چون افراد سرعت متفاوت دارند.

Story Point:

- نسبی است.
- قابل مقایسه است.
- باعث همکاری می‌شود.

---

## Q15: Planning Poker چیست؟

روش تخمین گروهی با کارت‌های عددی.

معمولاً:

```
1
2
3
5
8
13
21
```

---

# Section 5: Flow Metrics

---

## Q16: تفاوت Lead Time و Cycle Time چیست؟

Lead Time:

```
Request → Done
```

Cycle Time:

```
Started → Done
```

---

## Q17: Throughput چیست؟

تعداد آیتم‌های تکمیل‌شده در زمان مشخص.

مثال:

```
20 Issues / Month
```

---

## Q18: WIP چیست؟

کارهایی که هنوز تکمیل نشده‌اند.

---

## Q19: چرا WIP Limit مهم است؟

زیرا:

```
WIP بالا

↓

Context Switching

↓

Cycle Time بالا
```

---

# Section 6: Jira Reports

---

## Q20: Velocity Chart چیست؟

نمایش مقدار Story Point تکمیل‌شده در Sprintهای مختلف.

مسیر:

```
Board

↓

Reports

↓

Velocity Chart
```

---

## Q21: Burndown Chart چیست؟

نمایش کار باقی‌مانده در Sprint.

---

## Q22: Burnup Chart چیست؟

نمایش:

- Completed Work
- Scope Change

---

## Q23: Control Chart چیست؟

نمایش Cycle Time و Lead Time.

برای:

- Predictability
- SLE

استفاده می‌شود.

---

## Q24: CFD چیست؟

Cumulative Flow Diagram:

نمایش جریان کار بین Statusها.

---

# Section 7: DORA Metrics

---

## Q25: چهار شاخص DORA چیست؟

1. Deployment Frequency

2. Lead Time for Changes

3. Change Failure Rate

4. MTTR

---

## Q26: Deployment Frequency چیست؟

تعداد Deploy موفق در یک بازه زمانی.

---

## Q27: Lead Time for Changes چیست؟

زمان:

```
Commit

↓

Production
```

---

## Q28: Change Failure Rate چیست؟

درصد Deployهایی که Failure ایجاد کرده‌اند.

---

## Q29: MTTR چیست؟

زمان متوسط بازیابی سرویس.

---

# Section 8: Enterprise Jira

---

## Q30: چگونه Jira را در سازمان بزرگ مدیریت می‌کنید؟

با:

- استاندارد Workflow
- Permission Scheme
- Issue Type Scheme
- Screen Scheme
- Automation
- Governance

---

## Q31: مشکل Workflow زیاد چیست؟

باعث:

- پیچیدگی
- Maintenance سخت
- گزارش‌گیری ضعیف

می‌شود.

---

## Q32: Best Practice Workflow چیست؟

Workflow ساده:

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

# Section 9: Dashboard

---

## Q33: داشبورد خوب چه ویژگی دارد؟

باید:

- Role Based باشد.
- Actionable باشد.
- KPI مناسب داشته باشد.

---

## Q34: داشبورد Scrum Master شامل چیست؟

- Burndown
- Velocity
- CFD
- Control Chart
- Blockers

---

## Q35: داشبورد Manager شامل چیست؟

- Delivery Trend
- Release Status
- Quality
- Risk

---

# Section 10: Scenario Questions

---

## Q36: چرا Cycle Time تیم افزایش پیدا کرده؟

بررسی:

- WIP
- Blocker
- Story Size
- Dependency
- Review Time

---

## Q37: تیم زیاد کار شروع می‌کند ولی کم Done می‌کند، مشکل چیست؟

احتمالاً:

```
High WIP
```

راه‌حل:

- WIP Limit
- Finish Before Start

---

## Q38: Velocity تیم کاهش یافته، چه بررسی می‌کنید؟

بررسی:

- Capacity
- Team Change
- Story Size
- Technical Debt
- Dependency

---

## Q39: مدیر می‌گوید تیم کند شده، چه Metric بررسی می‌کنید؟

نباید فقط Velocity را دید.

بررسی:

- Cycle Time
- Throughput
- Lead Time
- WIP

---

# Senior Jira Admin Checklist

```
✓ Jira Architecture

✓ Workflow Design

✓ Permission Management

✓ Automation

✓ Reporting

✓ Agile Configuration

✓ Integration

✓ Governance

✓ Performance Optimization
```

---

# Final Interview Rule

یک Senior Jira Admin فقط Jira را مدیریت نمی‌کند.

باید بتواند:

```
Business Need

↓

Process

↓

Jira Configuration

↓

Automation

↓

Reporting

↓

Continuous Improvement
```

را طراحی کند.
