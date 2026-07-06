# Cycle Time

> یکی از کلیدی‌ترین Flow Metrics در Kanban که زمان واقعی انجام کار را از لحظه شروع تا تکمیل اندازه‌گیری می‌کند.

---

# Definition

Cycle Time مدت زمانی است که یک آیتم از لحظه‌ای که وارد حالت **In Progress (شروع واقعی کار)** می‌شود تا زمانی که به وضعیت **Done** برسد طی می‌کند.

```
Cycle Time

=

Start Work

↓

Done
```

---

# هدف

Cycle Time به این سؤال پاسخ می‌دهد:

> **وقتی کار شروع شد، چقدر طول می‌کشد تا تمام شود؟**

---

# تفاوت Cycle Time و Lead Time

| Lead Time | Cycle Time |
|-----------|------------|
| از ایجاد درخواست | از شروع کار |
| شامل انتظار | بدون انتظار اولیه |
| نگاه مشتری | نگاه تیم |

---

# مثال ساده

```
Created: 1 July
Started: 5 July
Done: 10 July
```

- Lead Time = 9 روز
- Cycle Time = 5 روز

---

# اجزای Cycle Time

Cycle Time معمولاً شامل مراحل زیر است:

- Development
- Code Review
- Testing
- Rework
- Final Approval

---

# فرمول

```
Cycle Time

=

Done Date

-

Start Date
```

---

# چرا Cycle Time مهم است؟

- اندازه‌گیری سرعت واقعی تیم
- شناسایی گلوگاه‌ها در فرآیند توسعه
- بهبود پیش‌بینی (Forecast)
- تحلیل کارایی جریان کار

---

# مثال واقعی

```
In Progress: 3 Aug
Code Review: 6 Aug
Testing: 8 Aug
Done: 10 Aug
```

Cycle Time:

```
7 Days
```

---

# Cycle Time در Kanban

در Kanban، Cycle Time یکی از اصلی‌ترین KPIها است.

هدف:

> کاهش نوسان Cycle Time (Variability)

---

# Cycle Time vs Throughput

| Cycle Time | Throughput |
|-------------|------------|
| زمان انجام یک آیتم | تعداد آیتم‌ها |
| سرعت | حجم |
| کیفیت Flow | خروجی |

---

# توزیع Cycle Time

Cycle Time معمولاً توزیع نرمال ندارد، بلکه:

- Skewed Distribution
- Long Tail

یعنی:

بیشتر آیتم‌ها سریع تمام می‌شوند، اما برخی آیتم‌ها بسیار طولانی می‌شوند.

---

# Percentile در Cycle Time

مثال:

| Percentile | Cycle Time |
|------------|------------|
| 50% | 4 روز |
| 70% | 6 روز |
| 85% | 9 روز |
| 95% | 15 روز |

---

# کاربرد در Forecast

اگر بدانیم:

```
85% Cycle Time = 8 Days
```

می‌توان گفت:

> 85% از آیتم‌ها در 8 روز یا کمتر تکمیل می‌شوند.

---

# Cycle Time در Jira

Jira به‌صورت پیش‌فرض:

- Control Chart ارائه می‌دهد

اما برای تحلیل حرفه‌ای نیاز است:

- ActionableAgile
- eazyBI
- Jira Align

---

# Control Chart

Cycle Time معمولاً روی Control Chart نمایش داده می‌شود:

- X Axis → زمان
- Y Axis → Cycle Time

---

# عوامل افزایش Cycle Time

- WIP بالا
- Bottleneck در Review
- تست دستی سنگین
- وابستگی زیاد بین تیم‌ها
- Scope بزرگ Storyها

---

# کاهش Cycle Time

- کاهش WIP
- کوچک کردن Storyها
- اتوماسیون تست
- بهبود Code Review
- حذف صف انتظار (Queue)

---

# مثال Enterprise

قبل:

```
Average Cycle Time = 10 Days
```

بعد از بهینه‌سازی:

```
Average Cycle Time = 6 Days
```

---

# ارتباط با Lead Time

```
Lead Time

=

Waiting Time

+

Cycle Time
```

---

# ارتباط با Forecast

Cycle Time یکی از ورودی‌های مهم برای:

- Monte Carlo Forecast
- SLE (Service Level Expectation)
- Kanban Forecasting

---

# Best Practices

✅ Cycle Time را در سطح Issue Type تحلیل کنید.

✅ Median را به جای Average استفاده کنید.

✅ Outlierها را جدا بررسی کنید.

✅ Trend را بررسی کنید، نه فقط عدد.

---

# اشتباهات رایج

❌ استفاده از Cycle Time برای ارزیابی فردی

❌ نادیده گرفتن Queue Time

❌ تمرکز فقط روی Average

❌ عدم تفکیک Issue Typeها

---

# Interview Questions

### Cycle Time چیست؟

مدت زمان از شروع کار روی یک آیتم تا تکمیل آن.

---

### تفاوت Cycle Time و Lead Time چیست؟

Lead Time شامل انتظار قبل از شروع کار است، Cycle Time فقط زمان انجام کار را اندازه می‌گیرد.

---

### چرا Cycle Time مهم است؟

زیرا سرعت واقعی تیم در انجام کار را نشان می‌دهد.

---

### چگونه Cycle Time را کاهش می‌دهید؟

- کاهش WIP
- بهبود فرآیند Review
- اتوماسیون تست
- کوچک‌سازی Storyها

---

# Summary

| ویژگی | Cycle Time |
|--------|------------|
| شروع | Start Work |
| پایان | Done |
| شامل انتظار | ❌ |
| تمرکز | سرعت تیم |
| ابزار Jira | Control Chart |

---

# Enterprise Tips

## 1. Cycle Time را با Percentile تحلیل کنید

میانگین به‌تنهایی کافی نیست.

---

## 2. به Tail Distribution توجه کنید

آیتم‌های کند بیشترین تأثیر را روی Forecast دارند.

---

## 3. Cycle Time را برای هر نوع کار جدا کنید

Bug، Story و Epic رفتار متفاوتی دارند.

---

## 4. WIP مهم‌ترین عامل است

افزایش WIP تقریباً همیشه Cycle Time را افزایش می‌دهد.

---

## 5. از Cycle Time برای SLE استفاده کنید

Cycle Time پایه اصلی Service Level Expectation است.

---

# مثال کامل

```
Story A: 3 Days
Story B: 4 Days
Story C: 12 Days
Story D: 5 Days
Story E: 6 Days
```

Average:

```
6 Days
```

Median:

```
5 Days
```

85th Percentile:

```
10 Days
```

نتیجه عملی:

> 85% آیتم‌ها در کمتر از 10 روز تکمیل می‌شوند.
