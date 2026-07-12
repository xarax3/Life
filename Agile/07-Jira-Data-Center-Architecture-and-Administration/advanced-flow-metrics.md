تا اینجا مسیر آموزشی را این‌گونه جلو رفته‌ایم:

* Day 1 ✅
* Day 2 ✅
* Day 3 ✅
* Day 4 ✅
* **Day 5** (Flow Metrics & Kanban)
* Day 6 ✅
* Day 7 (در حال انجام)

با توجه به اینکه درخواست کردی **«ادامه روز پنجم»**، ادامه همان Day 5 را می‌دهم.

```markdown
# File: Life/Agile/Jira/05-Flow-Metrics-and-Kanban/advanced-flow-metrics.md

# Day 5 - Part 11
# Advanced Flow Metrics & Kanban Optimization

> معیارهای پیشرفته Flow، تحلیل گلوگاه‌ها و بهینه‌سازی فرآیند تحویل نرم‌افزار.

---

# 101. Flow Efficiency

Flow Efficiency نشان می‌دهد چه مقدار از زمان یک Issue واقعاً صرف کار شده است.

فرمول:

```

Flow Efficiency

=

Active Time

/

Lead Time

```

---

مثال:

```

Lead Time = 10 Days

Active Work = 4 Days

```

نتیجه:

```

40%

```

---

# تفسیر

```

80-100%

Excellent

```
```

50-80%

Good

```
```

30-50%

Needs Improvement

```
```

Below 30%

Poor Flow

```

---

# 102. Queue Time

Queue Time زمانی است که Issue منتظر انجام کار است.

مثال:

```

Ready for Development

↓

Waiting

↓

Developer Starts

```

---

هدف:

کاهش Queue Time.

---

# 103. Wait States

نمونه وضعیت‌های انتظار:

```

Waiting for Review

Waiting for QA

Waiting for Approval

Waiting for Customer

```

---

هر Wait State باعث افزایش Lead Time می‌شود.

---

# 104. Active States

نمونه وضعیت‌های فعال:

```

Development

Testing

Review

Deployment

```

---

# 105. Flow Efficiency Example

```

Development = 6 Hours

Testing = 2 Hours

Review = 2 Hours

Waiting = 30 Hours

```

---

```

Active Time = 10 Hours

Lead Time = 40 Hours

```

---

```

Flow Efficiency

=

25%

```

---

# نتیجه

بیشتر زمان صرف انتظار شده است.

---

# 106. Flow Distribution

بررسی توزیع کارها:

```

Feature

Bug

Support

Technical Debt

```

---

مثال:

```

Features

60%

Bugs

20%

Support

15%

Technical Debt

5%

```

---

# تحلیل

اگر Bugها بیش از حد افزایش پیدا کنند:

```

Development Capacity

↓

Feature Delivery

↓

Customer Value

```

---

# 107. Work Item Age

سن هر Issue که هنوز بسته نشده است.

فرمول:

```

Today

*

Created Date

```

---

مثال:

```

Created

1 June

Today

20 June

```

---

```

Age = 19 Days

```

---

# هدف

Issueهای قدیمی سریع شناسایی شوند.

---

# 108. Aging WIP Chart

نمودار:

```

Issue Age

↑

|

|

|

+-------------------->

Time

```

---

اگر نمودار ناگهان رشد کند:

احتمالاً Bottleneck ایجاد شده است.

---

# 109. Flow Debt

Flow Debt یعنی:

کارهایی که مدت زیادی در سیستم باقی مانده‌اند.

نمونه:

```

Old Stories

Old Bugs

Old Technical Debt

```

---

راهکار:

```

Regular Cleanup

*

Backlog Refinement

```

---

# 110. Bottleneck Detection

نمونه:

```

Development

↓

Review

↓

Testing

```

---

اگر:

```

Testing Queue ↑

```

یعنی:

QA گلوگاه است.

---

# 111. Little's Law

قانون معروف کانبان:

```

WIP

=

Throughput

×

Cycle Time

```

---

مثال:

```

Throughput

10 Issues/Week

Cycle Time

3 Weeks

```

---

```

WIP

=

30 Issues

```

---

# نتیجه

با کاهش WIP:

```

Cycle Time ↓

```

---

# 112. Flow-Based Forecasting

به‌جای تخمین Story Point می‌توان از داده‌های واقعی استفاده کرد.

ورودی:

- Historical Throughput
- Cycle Time
- Work Item Count

---

خروجی:

```

Forecast Completion Date

```

---

# 113. Monte Carlo Simulation

در تیم‌های بالغ:

از Monte Carlo برای پیش‌بینی تحویل استفاده می‌شود.

ورودی:

```

Historical Throughput

```

---

خروجی:

```

Probability

90%

Completion Before

15 July

```

---

# 114. Kanban Health Checklist

```

✓ WIP محدود

✓ Queue کوچک

✓ Flow Stable

✓ Blockers Visible

✓ Metrics Reviewed

✓ Policies Explicit

✓ Continuous Improvement

```

---

# Day 5 Part 11 Summary

موضوعات:

✓ Flow Efficiency

✓ Queue Time

✓ Wait States

✓ Active States

✓ Work Item Age

✓ Aging WIP

✓ Flow Debt

✓ Bottleneck Detection

✓ Little's Law

✓ Monte Carlo Forecasting

---

# Next Part

Day 5 - Part 12:

- Advanced Kanban Scaling
- Enterprise Flow Management
- Service Delivery Review
- Operations Review
- Kanban Maturity Model
- Real-world Enterprise Scenarios
```
