# Throughput

> یکی از اصلی‌ترین Flow Metrics در Kanban که تعداد آیتم‌های تکمیل‌شده در یک بازه زمانی مشخص را اندازه‌گیری می‌کند.

---

# Definition

Throughput یعنی:

> تعداد آیتم‌هایی که در یک بازه زمانی مشخص (روز، هفته، Sprint یا ماه) به وضعیت Done رسیده‌اند.

```
Throughput

=

Completed Items per Time Period
```

---

# هدف

Throughput به این سؤال پاسخ می‌دهد:

> **تیم در یک بازه زمانی مشخص چند آیتم واقعاً تحویل داده است؟**

---

# مثال ساده

در یک هفته:

```
Monday: 3 items
Tuesday: 5 items
Wednesday: 2 items
Thursday: 4 items
Friday: 6 items
```

Throughput هفتگی:

```
20 Items
```

---

# Throughput vs Velocity

| Throughput | Velocity |
|-------------|----------|
| تعداد آیتم | Story Points |
| Kanban | Scrum |
| بدون تخمین | تخمین‌دار |
| واقعی | نسبی |

---

# چرا Throughput مهم است؟

- اندازه‌گیری خروجی واقعی تیم
- پایه اصلی Forecast آماری
- مناسب برای Kanban
- قابل استفاده در Monte Carlo
- مستقل از Story Point

---

# فرمول

```
Throughput

=

Sum(Completed Items in Time Window)
```

---

# Throughput روزانه / هفتگی / ماهانه

## Daily

```
5 items / day
```

## Weekly

```
25 items / week
```

## Monthly

```
100 items / month
```

---

# توزیع Throughput

Throughput نیز مانند Cycle Time:

- نوسانی است
- همیشه ثابت نیست
- وابسته به WIP و Bottleneckها است

---

# مثال واقعی

| Week | Completed Items |
|------|-----------------|
| Week 1 | 18 |
| Week 2 | 22 |
| Week 3 | 15 |
| Week 4 | 25 |

Average Throughput:

```
20 items/week
```

---

# Throughput و Forecast

اگر Backlog:

```
100 items
```

Throughput:

```
20 items/week
```

Forecast:

```
5 weeks
```

---

# Throughput در Kanban

Throughput یکی از مهم‌ترین KPIها در Kanban است چون:

- بدون نیاز به Story Point کار می‌کند
- کاملاً واقعی است
- بر اساس خروجی واقعی تیم است

---

# Throughput در Jira

Jira به‌صورت پیش‌فرض Throughput را مستقیم نمایش نمی‌دهد، اما می‌توان با:

- Filters
- eazyBI
- ActionableAgile
- Jira Align

آن را محاسبه کرد.

---

# Throughput و WIP

ارتباط مستقیم:

```
WIP ↑  → Throughput ↓
WIP ↓  → Throughput ↑
```

---

# Throughput و Cycle Time

این دو به هم وابسته هستند:

```
Little’s Law
```

```
WIP = Throughput × Cycle Time
```

---

# Little’s Law

یکی از مهم‌ترین قوانین در Flow:

```
WIP

=

Throughput × Cycle Time
```

یا:

```
Cycle Time

=

WIP / Throughput
```

---

# مثال Little’s Law

اگر:

```
WIP = 30
Throughput = 10 items/day
```

پس:

```
Cycle Time = 3 days
```

---

# Throughput و Predictability

- Throughput ثابت → Predictability بالا
- Throughput نوسانی → Forecast ضعیف

---

# Throughput و Monte Carlo

Monte Carlo از Throughput برای شبیه‌سازی استفاده می‌کند:

```
Historical Throughput

↓

Simulation

↓

Forecast Probability
```

---

# افزایش Throughput

روش‌ها:

- کاهش WIP
- حذف Bottleneck
- بهبود Flow
- کوچک‌سازی Work Itemها
- افزایش Automation
- کاهش Waiting Time

---

# کاهش Throughput (مشکل)

دلایل:

- WIP زیاد
- Blockerها
- Review کند
- QA bottleneck
- Scope بزرگ

---

# KPIهای مرتبط

- Cycle Time
- Lead Time
- WIP
- Flow Efficiency
- Predictability

---

# Throughput در Dashboard

نمونه:

```
This Week: 22 items
Last Week: 18 items
Trend: ↑ +22%
```

---

# Throughput vs Velocity vs Capacity

| Metric | معنی |
|--------|------|
| Capacity | توان تیم |
| Velocity | خروجی Story Point |
| Throughput | خروجی واقعی |

---

# اشتباهات رایج

❌ استفاده از Throughput بدون بازه زمانی

❌ مقایسه تیم‌ها بدون نرمال‌سازی

❌ استفاده از Story Point همراه Throughput (در Kanban)

❌ نادیده گرفتن Outlierها

---

# Interview Questions

### Throughput چیست؟

تعداد آیتم‌های تکمیل‌شده در یک بازه زمانی.

---

### تفاوت Throughput و Velocity چیست؟

Throughput تعداد آیتم است، Velocity امتیاز (Story Point).

---

### چرا Throughput مهم است؟

چون پایه اصلی Forecast در Kanban و Monte Carlo است.

---

### رابطه Throughput با WIP چیست؟

با قانون Little’s Law:

```
WIP = Throughput × Cycle Time
```

---

# Summary

| ویژگی | Throughput |
|--------|------------|
| تعریف | تعداد آیتم‌های Done در زمان |
| واحد | Item |
| مناسب برای | Kanban |
| وابستگی | WIP، Cycle Time |
| ابزار Jira | eazyBI / ActionableAgile |

---

# Enterprise Tips

## 1. Throughput را در بازه‌های ثابت بررسی کنید

هفتگی یا ماهانه، نه روزانه تنها.

---

## 2. به Trend توجه کنید

یک عدد مهم نیست، روند مهم است.

---

## 3. Throughput را با Cycle Time ترکیب کنید

برای Forecast دقیق‌تر.

---

## 4. Outlierها را جدا تحلیل کنید

یک هفته بد می‌تواند کل میانگین را خراب کند.

---

## 5. از Throughput برای Forecast استفاده کنید

در Kanban، Throughput پایه اصلی پیش‌بینی است.
