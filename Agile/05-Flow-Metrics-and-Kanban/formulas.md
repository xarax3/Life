# Agile & Jira Metrics Formula Reference

> مرجع فرمول‌ها و محاسبات اصلی Agile، Scrum، Kanban و DevOps Metrics که در Jira و ابزارهای تحلیلی استفاده می‌شوند.

---

# 1. Lead Time

## Definition

مدت زمان از ایجاد درخواست تا تحویل نهایی.

---

## Formula

```
Lead Time

=

Completion Date

-

Request Created Date
```

---

## Example

```
Created:

1 Jan

Done:

10 Jan
```

```
Lead Time = 9 Days
```

---

## Jira Usage

برای:

- Customer Request
- Service Delivery
- Product Flow

---

# 2. Cycle Time

## Definition

زمانی که کار واقعاً روی آن انجام می‌شود.

---

## Formula

```
Cycle Time

=

Done Date

-

Work Started Date
```

---

## Example

```
In Progress:

5 Jan

Done:

8 Jan
```

```
Cycle Time = 3 Days
```

---

## Jira Usage

منبع:

```
Control Chart
```

---

# 3. Throughput

## Definition

تعداد آیتم‌های تکمیل‌شده در یک بازه زمانی.

---

## Formula

```
Throughput

=

Completed Items

/

Time Period
```

---

## Example

```
40 Issues

در 4 هفته
```

```
Throughput = 10 Issues/week
```

---

# 4. Work In Progress (WIP)

## Definition

تعداد آیتم‌هایی که در حال انجام هستند.

---

## Formula

```
WIP

=

Items Started

-

Items Completed
```

---

## Example

```
Started = 100

Completed = 80
```

```
WIP = 20
```

---

# 5. Little's Law

یکی از مهم‌ترین قوانین Flow.

---

## Formula

```
WIP

=

Throughput

×

Cycle Time
```

---

## Example

```
Throughput:

10 Items/week

Cycle Time:

2 weeks
```

پس:

```
WIP = 20 Items
```

---

# 6. Flow Efficiency

## Definition

درصد زمانی که کار واقعاً روی آن انجام می‌شود نسبت به کل زمان انتظار.

---

## Formula

```
Flow Efficiency

=

(Value Added Time)

/

(Total Lead Time)

×

100
```

---

## Example

```
Actual Work:

5 Days

Waiting:

15 Days
```

```
Efficiency

=

5/20

=

25%
```

---

# 7. Velocity

## Definition

مقدار Story Point تکمیل‌شده در Sprint.

---

## Formula

```
Velocity

=

Completed Story Points

/

Sprint
```

---

## Example

```
Sprint 1 = 30 SP

Sprint 2 = 40 SP

Sprint 3 = 50 SP
```

Average:

```
Velocity = 40 SP
```

---

# 8. Capacity

## Definition

توان واقعی تیم برای یک Sprint.

---

## Formula

```
Capacity

=

Available Working Hours

×

Focus Factor
```

---

## Example

```
5 Developers

80 Hours each

Focus Factor = 70%
```

```
Capacity

=

400 × 0.7

=

280 Hours
```

---

# 9. Burndown

## Definition

کار باقی‌مانده در طول زمان.

---

## Formula

```
Remaining Work

=

Total Work

-

Completed Work
```

---

# 10. Burnup

## Definition

کار تکمیل‌شده نسبت به Scope.

---

## Formula

```
Completed Work

=

Previous Completed

+

New Completed
```

---

# 11. Deployment Frequency

## Formula

```
DF

=

Successful Deployments

/

Time Period
```

---

## Example

```
40 Deployments

Month
```

```
DF = 40/month
```

---

# 12. Lead Time for Changes

## Formula

```
LTC

=

Production Deploy Time

-

First Commit Time
```

---

# Example

```
Commit:

Monday 10:00

Deploy:

Tuesday 14:00
```

```
LTC

=

28 Hours
```

---

# 13. Change Failure Rate

## Formula

```
CFR

=

Failed Changes

/

Total Changes

×

100
```

---

## Example

```
Failed:

5

Total:

100
```

```
CFR = 5%
```

---

# 14. MTTR

## Formula

```
MTTR

=

Total Recovery Time

/

Number of Incidents
```

---

## Example

```
Recovery:

20 Hours

Incidents:

5
```

```
MTTR = 4 Hours
```

---

# 15. SLE

## Definition

انتظار آماری برای تکمیل Work Item.

---

## Formula

```
SLE

=

Cycle Time Percentile
```

---

## Example

```
85% of Items

≤ 10 Days
```

پس:

```
SLE = 10 Days @85%
```

---

# 16. Scope Change

## Formula

```
Scope Change %

=

(New Scope - Original Scope)

/

Original Scope

×

100
```

---

## Example

```
Original:

100 SP

New:

120 SP
```

```
Scope Change

=

20%
```

---

# 17. Predictability

## Formula

```
Predictability

=

Completed Commitment

/

Committed Work

×

100
```

---

## Example

```
Committed:

50 SP

Completed:

45 SP
```

```
Predictability

=

90%
```

---

# 18. Defect Rate

## Formula

```
Defect Rate

=

Number of Defects

/

Delivered Items
```

---

# 19. Release Success Rate

## Formula

```
Successful Releases

/

Total Releases

×

100
```

---

# 20. SLA Compliance

## Formula

```
Met SLA Tickets

/

Total SLA Tickets

×

100
```

---

# Quick Reference Table

| Metric | Formula |
|-|-|
| Lead Time | Done - Created |
| Cycle Time | Done - Started |
| Throughput | Done Items / Time |
| WIP | Started - Completed |
| Flow Efficiency | Work Time / Lead Time |
| Velocity | SP Completed / Sprint |
| Capacity | Available Time × Focus Factor |
| DF | Deploy / Time |
| LTC | Deploy - Commit |
| CFR | Failed / Total Changes |
| MTTR | Recovery / Incidents |
| SLE | Percentile Cycle Time |

---

# Jira Mapping

| Metric | Jira Source |
|-|-|
| Velocity | Sprint Report |
| Burndown | Burndown Report |
| Burnup | Burnup Report |
| Cycle Time | Control Chart |
| Lead Time | Control Chart / Apps |
| Throughput | Filters / Apps |
| WIP | Board |
| CFD | Cumulative Flow Diagram |

---

# Enterprise Usage

ترکیب Metrics:

```
Flow Metrics

+

Agile Metrics

+

DORA Metrics

+

ITSM Metrics

=

Complete Delivery Intelligence
```

---

# Final Rule

Metric خوب باید:

```
Measure

↓

Understand

↓

Improve

↓

Repeat
```

باشد.

هدف Metrics کنترل افراد نیست؛ هدف بهبود سیستم Delivery است.
