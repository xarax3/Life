# Flow Efficiency

> یکی از مهم‌ترین KPIهای Lean، Kanban و DevOps برای اندازه‌گیری میزان ارزش‌آفرینی واقعی در فرآیند توسعه

---

# Definition

Flow Efficiency نشان می‌دهد چه درصدی از زمان یک Issue واقعاً صرف انجام کار (Active Work) شده و چه مقدار از زمان صرف انتظار (Waiting Time) شده است.

به بیان ساده:

> از کل زمانی که یک Issue در سیستم بوده، چند درصد آن واقعاً روی آن کار شده است؟

---

# Business Purpose

Flow Efficiency به این سؤالات پاسخ می‌دهد:

- آیا فرآیند توسعه کارآمد است؟
- بیشترین زمان در انتظار سپری می‌شود یا در توسعه؟
- گلوگاه اصلی کجاست؟
- آیا فرآیند نیاز به بهینه‌سازی دارد؟

---

# Formula

```
Flow Efficiency =

(Active Time / Lead Time) × 100
```

یا

```
Flow Efficiency =

(Value Added Time / Total Time) × 100
```

---

# مثال

فرض کنید یک Story:

| مرحله | زمان |
|--------|------|
| Waiting in Backlog | 6 روز |
| Development | 3 روز |
| Code Review | 2 روز |
| Waiting for QA | 4 روز |
| Testing | 2 روز |
| Waiting for Release | 3 روز |

---

## محاسبه

Active Time

```
Development

3

+

Review

2

+

Testing

2

=

7 Days
```

Lead Time

```
20 Days
```

Flow Efficiency

```
7 / 20 × 100

=

35%
```

---

# Interpretation

## بالای 70%

فرآیند بسیار بهینه است.

---

## بین 40 تا 70%

وضعیت مناسب است اما جای بهبود وجود دارد.

---

## کمتر از 40%

معمولاً زمان انتظار زیاد است.

باید Bottleneck بررسی شود.

---

# Active Time چیست؟

زمانی که واقعاً روی Issue کار انجام می‌شود.

نمونه:

- Development
- Code Review
- Testing
- Documentation

---

# Waiting Time چیست؟

زمانی که هیچ فعالیتی روی Issue انجام نمی‌شود.

نمونه:

- انتظار برای Approval
- انتظار برای QA
- انتظار برای Release
- انتظار برای Product Owner
- انتظار برای تیم امنیت

---

# رابطه با Lead Time

```
Lead Time

=

Active Time

+

Waiting Time
```

بنابراین:

```
Waiting زیاد

↓

Lead Time زیاد

↓

Flow Efficiency کم
```

---

# Enterprise Example

یک تیم بیمه داده‌های زیر را بررسی می‌کند:

| مرحله | زمان |
|--------|------|
| Waiting | 14 روز |
| Development | 5 روز |
| Review | 2 روز |
| Testing | 3 روز |

Flow Efficiency

```
10 / 24

=

41.6%
```

تحلیل:

بیش از نیمی از زمان صرف انتظار شده است.

مشکل اصلی سرعت توسعه نیست، بلکه فرآیندهای بین تیمی است.

---

# عوامل کاهش Flow Efficiency

## Approvalهای متعدد

هر Approval باعث افزایش Waiting Time می‌شود.

---

## Releaseهای بزرگ

اگر انتشار فقط ماهی یک بار انجام شود، زمان انتظار زیاد خواهد شد.

---

## WIP بالا

چندوظیفگی باعث توقف و جابه‌جایی مداوم بین کارها می‌شود.

---

## کمبود QA

Issueها مدت زیادی در صف تست می‌مانند.

---

## وابستگی به تیم‌های دیگر

مانند:

- DBA
- Network
- Security
- Infrastructure

---

# روش‌های افزایش Flow Efficiency

✅ کاهش WIP

✅ Continuous Integration

✅ Continuous Delivery

✅ خودکارسازی تست‌ها

✅ حذف Approvalهای غیرضروری

✅ کاهش اندازه Storyها

✅ Cross-functional Team

---

# محل در Jira

Jira به‌صورت پیش‌فرض گزارش مستقلی برای Flow Efficiency ندارد.

معمولاً با ابزارهای زیر محاسبه می‌شود:

- eazyBI
- ActionableAgile
- Rich Filters
- Jira API
- گزارش‌های سفارشی

---

# Dashboard KPI

Flow Efficiency معمولاً همراه این شاخص‌ها نمایش داده می‌شود:

- Cycle Time
- Lead Time
- Throughput
- WIP
- Deployment Frequency

---

# نمودار نمونه

```
Lead Time

████████████████████

20 Days
```

```
Active Work

███████

7 Days
```

```
Waiting

█████████████

13 Days
```

---

# Common Bottlenecks

| Bottleneck | اثر |
|------------|-----|
| Code Review | افزایش Waiting |
| QA | افزایش Lead Time |
| Approval | کاهش Flow Efficiency |
| Release Window | افزایش Queue |
| Security Review | افزایش Waiting |

---

# Common Mistakes

❌ تمرکز فقط روی سرعت برنامه‌نویسی

گاهی توسعه فقط ۲۰٪ زمان را تشکیل می‌دهد.

---

❌ حذف Waiting Time از تحلیل

Waiting معمولاً مهم‌ترین بخش تحلیل است.

---

❌ افزایش Throughput با افزایش WIP

در بلندمدت نتیجه معکوس خواهد داشت.

---

# KPI ارتباطی

```
WIP ↑

↓

Waiting ↑

↓

Lead Time ↑

↓

Flow Efficiency ↓
```

---

# استفاده در DevOps

در تیم‌های DevOps، Flow Efficiency یکی از شاخص‌های مهم برای کاهش Time to Market است.

بهبود این متریک معمولاً باعث:

- انتشار سریع‌تر
- کاهش هزینه
- رضایت بیشتر مشتری

می‌شود.

---

# Interview Questions

### Flow Efficiency چیست؟

درصد زمانی که واقعاً روی Issue کار انجام شده است.

---

### چرا مهم است؟

زیرا نشان می‌دهد مشکل اصلی توسعه است یا انتظار.

---

### چگونه آن را افزایش می‌دهید؟

- کاهش WIP
- حذف صف‌ها
- خودکارسازی
- Continuous Delivery
- کاهش وابستگی بین تیم‌ها

---

# Summary

| ویژگی | Flow Efficiency |
|---------|----------------|
| واحد | درصد |
| فرمول | Active Time / Lead Time |
| هرچه بیشتر | بهتر |
| وابسته به | Waiting Time |
| گزارش داخلی Jira | ❌ |
| ابزارهای رایج | eazyBI، ActionableAgile |

---

# ارتباط با سایر متریک‌ها

```text
          WIP
           │
           ▼
     Waiting Time
           │
           ▼
      Lead Time
           │
           ▼
   Flow Efficiency
           │
           ▼
 Time to Market
```

---

# Best Practice (Enterprise)

سازمان‌های بالغ فقط میانگین Flow Efficiency را بررسی نمی‌کنند، بلکه آن را به تفکیک موارد زیر تحلیل می‌کنند:

- تیم
- نوع Issue (Bug، Story، Task)
- Component
- سرویس
- تیم محصول
- بازه زمانی

این کار کمک می‌کند گلوگاه‌های واقعی سازمان شناسایی شوند و تصمیم‌های بهبود مبتنی بر داده گرفته شود.
