# Lead Time

> مهم‌ترین معیار از دید مشتری (Customer Perspective)

---

# Definition

Lead Time مدت زمانی است که از لحظه ثبت درخواست (Issue Creation)
تا زمانی که آن درخواست به مشتری یا ذی‌نفع تحویل داده می‌شود.

به عبارت ساده:

> مشتری چقدر منتظر می‌ماند؟

برخلاف Cycle Time که از شروع توسعه اندازه‌گیری می‌شود،
Lead Time کل زمان انتظار مشتری را اندازه‌گیری می‌کند.

---

# Business Purpose

Lead Time به سوالات زیر پاسخ می‌دهد:

- مشتری چقدر منتظر Feature می‌ماند؟
- SLA رعایت شده است؟
- فرآیند درخواست تا تحویل چقدر طول می‌کشد؟
- آیا تیم سریع‌تر از قبل Feature تحویل می‌دهد؟
- آیا فرآیند پذیرش درخواست مشکل دارد؟

---

# Formula

```
Lead Time = Done Date - Issue Created Date
```

یا

```
Lead Time = Delivery Date - Request Date
```

---

# مثال

```
Issue Created

1 July
```

↓

```
Backlog

5 Days
```

↓

```
In Progress

3 Days
```

↓

```
Testing

2 Days
```

↓

```
Done

11 July
```

Lead Time

```
11 - 1

=

10 Days
```

---

# Lead Time شامل چه بخش‌هایی است؟

```
Lead Time

=

Waiting

+

Development

+

Review

+

Testing

+

Deployment
```

Cycle Time فقط Development تا Done را اندازه‌گیری می‌کند.

---

# تفاوت Lead Time و Cycle Time

```
Created

↓

Backlog

↓

Selected

↓

In Progress

↓

Review

↓

Testing

↓

Done
```

Cycle Time

```
In Progress

↓

Done
```

Lead Time

```
Created

↓

Done
```

---

# مثال مقایسه

Issue A

```
Created

1 July

Started

8 July

Done

10 July
```

Lead Time

```
9 Days
```

Cycle Time

```
2 Days
```

---

Issue B

```
Created

1 July

Started

2 July

Done

10 July
```

Lead Time

```
9 Days
```

Cycle Time

```
8 Days
```

نتیجه:

هر دو Lead Time یکسان دارند اما عملکرد تیم توسعه کاملاً متفاوت است.

---

# محل مشاهده در Jira

به‌صورت پیش‌فرض:

❌ گزارش مستقلی برای Lead Time وجود ندارد.

اما می‌توان آن را از طریق:

- Control Chart (با تنظیمات خاص)
- JQL
- eazyBI
- ActionableAgile
- Rich Filters
- Custom Charts

استخراج کرد.

---

# Cloud vs Data Center

| قابلیت | Cloud | Data Center |
|---------|--------|-------------|
| Lead Time Report | محدود | محدود |
| افزونه ActionableAgile | ✅ | ✅ |
| eazyBI | ✅ | ✅ |
| Automation محاسبه | ✅ | ✅ |

---

# چرا Lead Time مهم‌تر از Velocity است؟

Velocity می‌گوید:

> تیم چقدر کار انجام داده است.

Lead Time می‌گوید:

> مشتری چقدر منتظر مانده است.

از دید کسب‌وکار، معمولاً Lead Time اهمیت بیشتری دارد.

---

# عوامل افزایش Lead Time

## 1. Backlog بزرگ

Issueها مدت زیادی منتظر شروع می‌مانند.

---

## 2. Approval طولانی

مثلاً تأیید Product Owner یا مدیر.

---

## 3. وابستگی به تیم‌های دیگر

مانند:

- امنیت
- DBA
- شبکه
- DevOps

---

## 4. Deployment کند

اگر Release هر دو هفته یک بار انجام شود، Lead Time افزایش پیدا می‌کند.

---

## 5. WIP زیاد

وقتی تیم روی کارهای زیادی هم‌زمان کار می‌کند، شروع هر آیتم به تأخیر می‌افتد.

---

# Enterprise Example

یک بانک درخواست‌های مشتریان را بررسی کرده است.

| Feature | Lead Time |
|----------|----------:|
| Login | 18 روز |
| Transfer | 25 روز |
| Report | 14 روز |
| Notification | 30 روز |

تحلیل نشان داد:

توسعه فقط ۶ روز طول می‌کشد.

۱۹ روز باقی‌مانده صرف انتظار، تأیید و انتشار می‌شود.

بنابراین مشکل اصلی تیم توسعه نیست؛ فرآیند سازمانی است.

---

# رابطه با SLA

فرض کنید SLA سازمان:

```
10 Days
```

باشد.

اگر Lead Time:

```
14 Days
```

شود،

SLA نقض شده است.

---

# Lead Time Distribution

به جای میانگین، بسیاری از تیم‌های حرفه‌ای از Percentile استفاده می‌کنند.

مثلاً:

```
50%

4 Days
```

```
85%

7 Days
```

```
95%

12 Days
```

این روش برای پیش‌بینی زمان تحویل دقیق‌تر است.

---

# ارتباط با DORA Metrics

در DevOps، یکی از مهم‌ترین شاخص‌ها:

```
Lead Time for Changes
```

است.

این شاخص مدت زمان بین Commit تا Deployment در Production را اندازه‌گیری می‌کند.

---

# Dashboard KPI

Lead Time معمولاً کنار این متریک‌ها قرار می‌گیرد:

- Cycle Time
- Throughput
- Deployment Frequency
- CFD
- WIP
- Flow Efficiency

---

# Best Practices

✅ کاهش زمان انتظار در Backlog

✅ خودکارسازی Approvalها

✅ کاهش Batch Size

✅ انتشارهای کوچک و مکرر

✅ محدود کردن WIP

✅ بررسی روند Lead Time در بازه‌های زمانی

---

# Common Mistakes

❌ تمرکز فقط روی سرعت توسعه

گاهی توسعه سریع است اما فرآیندهای سازمانی باعث افزایش Lead Time می‌شوند.

---

❌ مقایسه تیم‌ها بر اساس Lead Time بدون در نظر گرفتن پیچیدگی کار

---

❌ استفاده از میانگین به‌تنهایی

همیشه توزیع داده‌ها را نیز بررسی کنید.

---

# JQL مرتبط

Issueهای ایجاد شده در ۳۰ روز گذشته:

```sql
created >= -30d
```

Issueهای Done شده در این ماه:

```sql
status = Done
AND resolved >= startOfMonth()
```

این JQLها به‌تنهایی Lead Time را محاسبه نمی‌کنند، اما داده‌های اولیه برای گزارش‌گیری را فراهم می‌کنند.

---

# سوالات مصاحبه

## Lead Time چیست؟

مدت زمان از ایجاد درخواست تا تحویل آن.

---

## چرا Lead Time مهم است؟

زیرا تجربه واقعی مشتری را اندازه‌گیری می‌کند.

---

## تفاوت Lead Time و Cycle Time؟

Lead Time شامل زمان انتظار قبل از شروع توسعه نیز می‌شود.

---

## چگونه Lead Time را کاهش می‌دهید؟

- کاهش WIP
- حذف Approvalهای غیرضروری
- کوچک کردن Storyها
- Continuous Deployment
- خودکارسازی فرآیندها

---

# خلاصه

| ویژگی | Lead Time |
|---------|-----------|
| شروع | Created |
| پایان | Done / Delivered |
| دیدگاه | مشتری |
| واحد | ساعت / روز |
| گزارش داخلی Jira | محدود |
| افزونه‌های رایج | eazyBI، ActionableAgile |
| هرچه کمتر | بهتر (در صورت حفظ کیفیت) |

---

# Cycle Time vs Lead Time

| ویژگی | Cycle Time | Lead Time |
|---------|------------|-----------|
| شروع | In Progress | Created |
| پایان | Done | Done |
| زمان انتظار را شامل می‌شود؟ | ❌ | ✅ |
| مناسب برای | تیم توسعه | کسب‌وکار و مشتری |
| گزارش داخلی Jira | Control Chart | محدود |
| سوال اصلی | تیم چقدر سریع کار می‌کند؟ | مشتری چقدر منتظر می‌ماند؟ |

---

# نکته Enterprise

در سازمان‌های بالغ، کاهش Lead Time معمولاً ارزش بیشتری نسبت به افزایش Velocity دارد؛ زیرا Lead Time مستقیماً بر رضایت مشتری، زمان ورود محصول به بازار (Time to Market) و قابلیت رقابت کسب‌وکار تأثیر می‌گذارد.
