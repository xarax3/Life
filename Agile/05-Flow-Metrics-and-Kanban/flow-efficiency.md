# Flow Efficiency

> یکی از پیشرفته‌ترین Flow Metrics که نسبت زمان کار مفید (Active Time) به کل زمان سپری‌شده (Total Time) را اندازه‌گیری می‌کند.

---

# Definition

Flow Efficiency نشان می‌دهد چه درصدی از زمان یک آیتم واقعاً صرف انجام کار شده است.

```
Flow Efficiency

=

Active Time

/

Total Lead Time

×

100
```

---

# هدف

Flow Efficiency به این سؤال پاسخ می‌دهد:

> **چقدر از زمان صرف کار واقعی شده و چقدر در انتظار (Waiting) بوده است؟**

---

# مثال ساده

```
Total Lead Time = 10 days
Active Work = 4 days
```

```
Flow Efficiency = 40%
```

یعنی:

```
60% زمان در انتظار بوده است
```

---

# اجزای زمان

## Active Time

- Development
- Testing
- Review
- Fixing

## Waiting Time

- Backlog waiting
- Review queue
- QA queue
- Approval waiting
- Release waiting

---

# فرمول

```
Flow Efficiency

=

Active Time

/

(Active Time + Waiting Time)

×

100
```

---

# مثال واقعی

```
Story A:

Waiting: 6 days
Active: 4 days
```

```
Flow Efficiency = 40%
```

---

# اهمیت Flow Efficiency

- نشان می‌دهد چقدر سیستم کند است
- کمک به شناسایی Queueها
- بهبود Flow کلی تیم
- کاهش Lead Time
- افزایش Predictability

---

# Flow Efficiency در دنیای واقعی

در بسیاری از سازمان‌ها:

```
Flow Efficiency = 10% تا 30%
```

یعنی:

بیشتر زمان صرف انتظار می‌شود نه کار واقعی.

---

# Flow Efficiency vs Cycle Time

| Flow Efficiency | Cycle Time |
|------------------|------------|
| کیفیت زمان | مدت زمان |
| Active vs Waiting | Start → Done |
| تحلیل سیستم | سرعت |

---

# Flow Efficiency vs Lead Time

| Lead Time | Flow Efficiency |
|-----------|----------------|
| کل زمان | کیفیت زمان |
| End-to-End | داخلی سیستم |

---

# مثال تحلیلی

```
Lead Time = 12 days

Active Time = 3 days

Waiting Time = 9 days
```

```
Flow Efficiency = 25%
```

---

# علت‌های کاهش Flow Efficiency

- WIP بالا
- Queue در Review
- QA bottleneck
- Approval زیاد
- Dependency بین تیم‌ها
- Batch Size بزرگ

---

# بهبود Flow Efficiency

- کاهش WIP
- اتوماسیون تست
- کاهش مراحل Approval
- کوچک‌سازی Storyها
- Cross-functional teams
- Continuous Delivery

---

# Flow Efficiency در Kanban

Kanban بر اساس این اصل است:

> Optimize Flow, not Utilization

Flow Efficiency یکی از بهترین ابزارها برای بررسی Flow است.

---

# Flow Efficiency در Jira

Jira به‌صورت پیش‌فرض نمایش مستقیم ندارد.

اما با ابزارهای زیر قابل محاسبه است:

- ActionableAgile Analytics
- eazyBI
- Jira Align
- Value Stream Mapping tools

---

# Flow Efficiency و Little’s Law

اگر:

```
WIP = Throughput × Cycle Time
```

Flow Efficiency پایین معمولاً نشان می‌دهد:

```
Cycle Time ↑

WIP ↑

Throughput ثابت یا پایین
```

---

# KPIهای مرتبط

- Cycle Time
- Lead Time
- WIP
- Throughput
- Queue Time

---

# مثال Enterprise

قبل:

```
Lead Time = 20 days
Active Time = 5 days
Flow Efficiency = 25%
```

بعد از بهبود:

```
Lead Time = 12 days
Active Time = 6 days
Flow Efficiency = 50%
```

---

# Flow Efficiency در Dashboard

نمونه:

```
Flow Efficiency: 35%
Waiting Time: 65%
Active Time: 35%
Trend: ↑ improving
```

---

# اشتباهات رایج

❌ تمرکز فقط روی سرعت (Velocity)

❌ نادیده گرفتن Waiting Time

❌ استفاده برای ارزیابی فردی

❌ عدم تحلیل Queueها

---

# Interview Questions

### Flow Efficiency چیست؟

درصد زمانی که واقعاً صرف کار فعال شده نسبت به کل زمان.

---

### چرا Flow Efficiency مهم است؟

چون نشان می‌دهد سیستم چقدر در حالت انتظار گیر کرده است.

---

### Flow Efficiency پایین چه معنایی دارد؟

یعنی بیشتر زمان صرف Waiting و Queue شده است.

---

### چگونه Flow Efficiency را افزایش می‌دهید؟

- کاهش WIP
- کاهش Queue
- بهبود Flow
- حذف Approvalهای اضافی

---

# Summary

| ویژگی | Flow Efficiency |
|--------|-----------------|
| تعریف | Active Time / Total Time |
| تمرکز | کیفیت جریان کار |
| هدف | کاهش انتظار |
| ابزار Jira | ActionableAgile / eazyBI |

---

# Enterprise Tips

## 1. Flow Efficiency واقعی معمولاً پایین است

در اکثر سازمان‌ها زیر 30% است.

---

## 2. به Waiting Time بیشتر از Active Time توجه کنید

بیشترین مشکل در Flow معمولاً انتظار است نه توسعه.

---

## 3. Flow Efficiency را در سطح System تحلیل کنید

نه فقط یک تیم.

---

## 4. با WIP ارتباط مستقیم دارد

کاهش WIP معمولاً Flow Efficiency را بهبود می‌دهد.

---

## 5. Flow Efficiency را برای Optimization استفاده کنید

نه برای Performance Evaluation افراد.
