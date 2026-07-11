# Service Level Expectation (SLE)

> یکی از مفاهیم کلیدی Kanban برای پیش‌بینی زمان تحویل کار که بر اساس داده‌های واقعی گذشته (Historical Data) مشخص می‌شود.

---

# Definition

SLE یعنی:

> مدت زمانی که انتظار داریم درصد مشخصی از Work Itemها در آن بازه زمانی تکمیل شوند.

---

# تفاوت SLE با SLA

این دو مفهوم بسیار نزدیک هستند اما یکسان نیستند.

| SLE | SLA |
|-|-|
| انتظار داخلی تیم | تعهد رسمی |
| مبتنی بر Flow Data | معمولاً قرارداد |
| برای Forecast | برای Compliance |

---

# مثال SLE

فرض کنید داده ۶ ماه گذشته:

```
100 Story Completed
```

تحلیل Cycle Time:

```
85 Story در کمتر از 10 روز تمام شده‌اند
```

پس:

```
SLE = 10 Days / 85%
```

یعنی:

> 85 درصد کارها باید در کمتر از 10 روز تکمیل شوند.

---

# چرا SLE مهم است؟

SLE باعث می‌شود:

- وعده‌های واقعی داده شود.
- Forecast دقیق‌تر شود.
- فشار غیرواقعی روی تیم کم شود.
- Flow قابل اندازه‌گیری شود.

---

# SLE در Kanban

Kanban بر اساس:

```
Visualization

+

Flow Metrics

+

Historical Data
```

کار می‌کند.

SLE نتیجه تحلیل همین داده‌ها است.

---

# SLE و Cycle Time

SLE معمولاً از Cycle Time استخراج می‌شود.

مثال:

Cycle Time گذشته:

```
Day 1 → 5 items
Day 2 → 10 items
Day 3 → 15 items
Day 4 → 20 items
Day 5 → 10 items
```

تحلیل:

```
85th Percentile = 5 days
```

پس:

```
SLE = 5 days
```

---

# Percentile در SLE

معمولاً از:

- 50%
- 70%
- 85%
- 95%

استفاده می‌شود.

---

# چرا 85%؟

زیرا:

- خیلی سخت‌گیرانه نیست.
- خیلی خوش‌بینانه نیست.
- برای Forecast مناسب است.

---

# SLE و Control Chart

Control Chart یکی از ابزارهای اصلی برای تعیین SLE است.

مسیر:

```
Cycle Time Data

↓

Control Chart

↓

Percentile

↓

SLE
```

---

# SLE و Jira

Jira به‌صورت مستقیم SLE را مدیریت نمی‌کند، اما داده لازم را دارد.

منابع:

- Control Chart
- Cycle Time
- JQL
- Dashboards
- Marketplace Apps

---

# Jira Software و SLE

در Jira می‌توان:

Cycle Time را از:

```
Board

↓

Reports

↓

Control Chart
```

تحلیل کرد.

---

# SLE و JQL

مثال:

کارهای Done شده در بازه زمانی:

```jql
statusCategory = Done
AND resolved >= -30d
```

برای تحلیل تاریخی استفاده می‌شود.

---

# SLE در Jira Service Management

در JSM مفهوم نزدیک‌تر:

```
SLA
```

است.

مثلاً:

```
Critical Incident

Response < 15 min

Resolution < 4 hours
```

اما SLE بیشتر برای Flow توسعه استفاده می‌شود.

---

# SLE و Forecast

فرض:

```
Remaining Items = 50
```

Throughput:

```
10 items/week
```

Forecast:

```
5 weeks
```

با SLE می‌توان زمان تکمیل هر Item را بهتر تخمین زد.

---

# SLE و Commitment

در Kanban:

به جای گفتن:

```
این کار حتماً Friday تمام می‌شود
```

می‌گوییم:

```
85% احتمال دارد
در کمتر از 10 روز تکمیل شود.
```

---

# عوامل خراب شدن SLE

## 1. WIP زیاد

```
WIP ↑

Cycle Time ↑
```

---

## 2. کارهای خیلی بزرگ

Story بزرگ:

```
Long Cycle Time
```

---

## 3. تغییر مداوم Priority

باعث توقف Flow می‌شود.

---

## 4. Blocker زیاد

زمان انتظار افزایش می‌یابد.

---

# بهبود SLE

روش‌ها:

- کاهش WIP
- کوچک کردن Storyها
- حذف Blocker
- استانداردسازی Workflow
- Automation

---

# SLE و مدیریت محصول

Product Owner می‌تواند بر اساس SLE:

- زمان‌بندی Release
- اولویت‌بندی
- انتظار Stakeholder

را بهتر مدیریت کند.

---

# اشتباهات رایج

❌ تعیین SLE بدون داده تاریخی

❌ استفاده از SLA به جای SLE

❌ دادن Commitment قطعی بر اساس SLE

❌ تغییر مداوم SLE بدون تحلیل

---

# Interview Questions

### SLE چیست؟

انتظار آماری برای زمان تکمیل Work Item بر اساس داده تاریخی.

---

### SLE چگونه تعیین می‌شود؟

با تحلیل Cycle Time گذشته و انتخاب Percentile مناسب.

---

### تفاوت SLE و SLA چیست؟

SLE انتظار آماری داخلی است، SLA تعهد رسمی سرویس.

---

### چرا SLE بهتر از Estimate سنتی است؟

زیرا بر اساس عملکرد واقعی سیستم است.

---

# Summary

| ویژگی | SLE |
|--------|-----|
| نوع | Kanban Metric |
| هدف | Forecast |
| داده | Historical Cycle Time |
| روش | Percentile |
| ابزار Jira | Control Chart |

---

# Enterprise Tips

## 1. SLE را با داده واقعی بسازید.

حداقل چند ماه داده تاریخی بهتر است.

---

## 2. SLE را برای تیم استفاده کنید، نه افراد.

هدف بهبود Flow است.

---

## 3. SLE را دوره‌ای بازبینی کنید.

با تغییر فرآیند، SLE نیز تغییر می‌کند.

---

## 4. SLE را با Control Chart و Aging Chart ترکیب کنید.

این ترکیب تصویر کاملی از سلامت Flow می‌دهد.

---

## 5. SLE جایگزین Planning نیست.

یک ابزار Forecast است، نه قول قطعی.
