# Cycle Time

> یکی از مهم‌ترین KPIهای Agile، Kanban و DevOps

---

# Definition

Cycle Time مدت زمانی است که یک Issue پس از شروع کار واقعی تا زمان پایان (Done) صرف می‌کند.

به زبان ساده:

> "وقتی تیم کار روی یک آیتم را شروع کرد، چقدر طول کشید تا آن را تحویل دهد؟"

Cycle Time یکی از مهم‌ترین شاخص‌های سرعت واقعی تیم است.

---

# Business Purpose

Cycle Time به این سوالات پاسخ می‌دهد:

- تیم چقدر سریع Feature تحویل می‌دهد؟
- آیا فرآیند توسعه کند شده است؟
- Bottleneck کجاست؟
- آیا تغییرات باعث کند شدن تیم شده‌اند؟
- آیا SLA رعایت شده است؟

---

# Formula

```
Cycle Time = Done Date - Start Date
```

یا

```
Cycle Time = Finish Time - First In Progress
```

---

# مثال

Issue

```
Created

1 July
```

↓

```
In Progress

4 July
```

↓

```
Code Review

6 July
```

↓

```
Testing

7 July
```

↓

```
Done

9 July
```

Cycle Time

```
9 - 4

=

5 Days
```

---

# Lead Time vs Cycle Time

```
Created

↓

Waiting

↓

In Progress

↓

Done
```

Lead Time

```
Created → Done
```

Cycle Time

```
In Progress → Done
```

بنابراین:

```
Lead Time ≥ Cycle Time
```

همیشه Lead Time بزرگ‌تر یا مساوی Cycle Time است.

---

# چه زمانی Clock شروع می‌شود؟

این موضوع به Workflow بستگی دارد.

در بیشتر تیم‌ها:

```
In Progress
```

به عنوان شروع Cycle Time در نظر گرفته می‌شود.

اما برخی سازمان‌ها:

```
Development
```

یا

```
Selected for Development
```

را نقطه شروع قرار می‌دهند.

بنابراین قبل از تحلیل، باید تعریف مشترکی برای Start داشته باشید.

---

# چه زمانی Clock متوقف می‌شود؟

معمولاً یکی از این Statusها:

- Done
- Closed
- Resolved

در سازمان‌های مختلف ممکن است متفاوت باشد.

---

# محل در Jira

```
Project

↓

Reports

↓

Control Chart
```

Control Chart از همین متریک استفاده می‌کند.

---

# در Jira چه داده‌هایی استفاده می‌شود؟

Jira از تاریخچه تغییر وضعیت (Status History) استفاده می‌کند.

نمونه:

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

زمان ورود و خروج از هر Status ثبت می‌شود و از این اطلاعات برای محاسبه Cycle Time استفاده می‌کند.

---

# مثال واقعی

فرض کنید تیم در یک Sprint این داده‌ها را دارد:

| Issue | Cycle Time |
|-------|-----------:|
| CRM-11 | 2 روز |
| CRM-12 | 4 روز |
| CRM-13 | 5 روز |
| CRM-14 | 3 روز |
| CRM-15 | 6 روز |

Average Cycle Time

```
(2+4+5+3+6)/5

=

4 Days
```

---

# Interpretation

## کمتر شدن Cycle Time

معمولاً نشانه خوبی است.

ممکن است نشان دهد:

- فرآیند ساده‌تر شده است.
- تیم سریع‌تر شده است.
- Blockerها کمتر شده‌اند.
- Automation اضافه شده است.

---

## بیشتر شدن Cycle Time

لزوماً بد نیست.

باید بررسی شود:

- آیا Storyها بزرگ‌تر شده‌اند؟
- آیا QA کمبود نیرو دارد؟
- آیا Review طولانی شده است؟
- آیا تعداد Blocked Issue زیاد شده است؟

---

# عوامل موثر بر Cycle Time

## 1. WIP زیاد

اگر هم‌زمان روی ۳۰ Issue کار کنید:

↓

Cycle Time افزایش می‌یابد.

---

## 2. Code Review طولانی

مثلاً:

```
Development

2 Days

↓

Review

6 Days
```

در این حالت مشکل از توسعه نیست؛ گلوگاه در Review است.

---

## 3. تست دستی

Manual Testing معمولاً Cycle Time را افزایش می‌دهد.

---

## 4. وابستگی به تیم‌های دیگر

مثلاً:

- تیم شبکه
- تیم امنیت
- DBA

می‌توانند باعث انتظار طولانی شوند.

---

## 5. اندازه Story

Storyهای بزرگ معمولاً Cycle Time بیشتری دارند.

به همین دلیل یکی از Best Practiceها شکستن Storyهای بزرگ است.

---

# Enterprise Example

یک تیم مالی داده‌های زیر را ثبت کرده است:

| Sprint | Average Cycle Time |
|---------|------------------:|
| Sprint 1 | 8 روز |
| Sprint 2 | 7 روز |
| Sprint 3 | 6 روز |
| Sprint 4 | 5 روز |
| Sprint 5 | 4 روز |

نتیجه:

Automation تست و بازبینی کد باعث کاهش تدریجی زمان تحویل شده است.

---

# Dashboard KPI

Cycle Time معمولاً کنار این شاخص‌ها نمایش داده می‌شود:

- Lead Time
- Throughput
- WIP
- CFD
- Control Chart

---

# نمودار نمونه

```
Average Cycle Time

8 ┤

7 ┤ █

6 ┤ █ █

5 ┤ █ █ █

4 ┤ █ █ █ █

3 ┤ █ █ █ █ █

   S1 S2 S3 S4 S5
```

---

# Best Practices

✅ Storyهای بزرگ را خرد کنید.

✅ WIP را محدود کنید.

✅ Code Review را سریع انجام دهید.

✅ تست‌ها را خودکار کنید.

✅ Blocked Issueها را سریع رفع کنید.

✅ Cycle Time را به صورت روند (Trend) بررسی کنید، نه فقط یک عدد.

---

# Common Mistakes

❌ مقایسه Cycle Time دو تیم مختلف

هر تیم فرآیند متفاوتی دارد.

---

❌ تحلیل فقط میانگین

گاهی Median یا Percentile تصویر دقیق‌تری ارائه می‌دهد.

---

❌ حذف زمان انتظار از تحلیل

Waiting Time بخش مهمی از مشکل است.

---

❌ استفاده برای ارزیابی عملکرد فردی

Cycle Time یک KPI فرآیند است، نه KPI افراد.

---

# ارتباط با سایر KPIها

```
WIP ↑

↓

Cycle Time ↑

↓

Lead Time ↑

↓

Customer Satisfaction ↓
```

اگر WIP زیاد شود، معمولاً Cycle Time و Lead Time نیز افزایش پیدا می‌کنند.

---

# سوالات مصاحبه

### Cycle Time چیست؟

مدت زمان از شروع کار واقعی روی Issue تا تکمیل آن.

---

### تفاوت Lead Time و Cycle Time چیست؟

Lead Time از زمان ایجاد Issue محاسبه می‌شود، اما Cycle Time از زمان شروع کار.

---

### Cycle Time از کجا در Jira مشاهده می‌شود؟

```
Reports

↓

Control Chart
```

---

### اگر Cycle Time ناگهان دو برابر شود چه می‌کنید؟

موارد زیر را بررسی می‌کنم:

- Bottleneck
- WIP
- QA
- Code Review
- Blocked Issues
- Workflow Changes
- Team Capacity

---

# خلاصه

| ویژگی | Cycle Time |
|---------|------------|
| هدف | اندازه‌گیری سرعت انجام کار |
| فرمول | Done - In Progress |
| واحد | ساعت / روز |
| گزارش Jira | Control Chart |
| مناسب | Scrum، Kanban، DevOps |
| بهتر است | هرچه کمتر (با حفظ کیفیت) |
| وابسته به | WIP، Review، QA، Automation |
