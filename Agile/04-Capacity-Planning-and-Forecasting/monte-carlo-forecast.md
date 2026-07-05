# Monte Carlo Forecast

> دقیق‌ترین روش Forecast در Agile که با استفاده از داده‌های واقعی گذشته و شبیه‌سازی آماری، احتمال تکمیل پروژه در بازه‌های زمانی مختلف را محاسبه می‌کند.

---

# Definition

Monte Carlo Forecast یک روش آماری مبتنی بر **Probability Simulation** است.

به جای اینکه بگوید:

```
Release:

15 October
```

می‌گوید:

```
80%

احتمال دارد

بین

10 تا 18 October
```

همین موضوع آن را به یکی از معتبرترین روش‌های Forecast در Agile تبدیل کرده است.

---

# چرا به Monte Carlo نیاز داریم؟

Velocity همیشه ثابت نیست.

مثال:

```
Sprint 1

38
```

```
Sprint 2

45
```

```
Sprint 3

41
```

```
Sprint 4

36
```

```
Sprint 5

43
```

استفاده از میانگین ساده:

```
40.6
```

عدم قطعیت را نشان نمی‌دهد.

Monte Carlo این تغییرات را در محاسبات لحاظ می‌کند.

---

# ورودی‌های موردنیاز

- Velocity گذشته
- Throughput گذشته
- Cycle Time
- Lead Time
- Remaining Work
- Scope

---

# خروجی

به‌جای یک تاریخ:

```
Release

15 October
```

خروجی به شکل احتمال است.

| Probability | Release Date |
|-------------|--------------|
| 50% | 10 Oct |
| 70% | 14 Oct |
| 85% | 18 Oct |
| 95% | 25 Oct |

---

# روند کار

```
Historical Data
        │
        ▼
Random Sampling
        │
        ▼
Thousands of Simulations
        │
        ▼
Probability Distribution
        │
        ▼
Forecast
```

---

# مثال ساده

Velocity پنج Sprint گذشته:

```
35

38

42

39

45
```

Backlog:

```
400 SP
```

Monte Carlo هزاران حالت مختلف را شبیه‌سازی می‌کند.

نتیجه:

```
50%

9 Sprint
```

```
85%

10 Sprint
```

```
95%

11 Sprint
```

---

# تفاوت با Velocity Forecast

Velocity Forecast:

```
400

/

40

=

10 Sprint
```

Monte Carlo:

```
85%

بین

9

تا

11 Sprint
```

بنابراین عدم قطعیت نیز نمایش داده می‌شود.

---

# Monte Carlo با Throughput

در تیم‌های Kanban معمولاً به‌جای Velocity از Throughput استفاده می‌شود.

مثال:

```
Completed Items

12

15

14

11

16
```

Monte Carlo احتمال پایان کار را بر اساس این داده‌ها محاسبه می‌کند.

---

# Monte Carlo با Cycle Time

اگر سؤال این باشد:

```
این Story

چه زمانی Done می‌شود؟
```

از داده‌های Cycle Time برای شبیه‌سازی استفاده می‌شود.

---

# Confidence Level

رایج‌ترین سطوح اطمینان:

| Confidence | کاربرد |
|------------|--------|
| 50% | خوش‌بینانه |
| 70% | برنامه‌ریزی داخلی |
| 85% | مدیریت پروژه |
| 95% | قراردادها و تعهدات مهم |

---

# مثال Enterprise

Remaining Work:

```
850 SP
```

Velocity تاریخچه:

```
42

39

44

41

37

43

40

38
```

نتیجه شبیه‌سازی:

| احتمال | Sprint |
|---------|--------|
| 50% | 20 |
| 70% | 21 |
| 85% | 22 |
| 95% | 24 |

---

# Monte Carlo در Jira

Jira Software به‌صورت پیش‌فرض Monte Carlo ندارد.

ابزارهای رایج:

- ActionableAgile Analytics
- Jira Align
- eazyBI
- Nave
- Plandek

---

# چه زمانی استفاده کنیم؟

زمانی که:

- پروژه بزرگ است.
- Velocity نوسان دارد.
- مدیران تاریخ قابل اعتماد می‌خواهند.
- Release حیاتی است.
- چند تیم همزمان کار می‌کنند.

---

# Dashboard KPI

معمولاً همراه این شاخص‌ها نمایش داده می‌شود:

- Probability
- Forecast Range
- Remaining Work
- Throughput
- Cycle Time
- Lead Time

---

# نمودار نمونه

```
50%

██████████
```

```
70%

██████████████
```

```
85%

██████████████████
```

```
95%

██████████████████████
```

---

# مزایا

✅ واقع‌بینانه

✅ مبتنی بر داده

✅ در نظر گرفتن عدم قطعیت

✅ مناسب پروژه‌های Enterprise

✅ کاهش ریسک تصمیم‌گیری

---

# محدودیت‌ها

- نیاز به داده تاریخی کافی
- وابسته به کیفیت داده
- فرض می‌کند رفتار آینده تا حدی مشابه گذشته است
- در صورت تغییرات شدید Scope یا تیم باید دوباره اجرا شود

---

# Best Practices

✅ حداقل ۱۰ Sprint داده تاریخی داشته باشید.

✅ داده‌های غیرعادی (Outlier) را بررسی کنید.

✅ Forecast را در پایان هر Sprint به‌روزرسانی کنید.

✅ از Confidence Level مناسب برای مخاطب استفاده کنید.

---

# اشتباهات رایج

❌ استفاده از داده‌های بسیار کم.

❌ حذف نکردن داده‌های اشتباه.

❌ اعلام فقط یک تاریخ.

❌ نادیده گرفتن تغییرات Scope.

---

# Interview Questions

### Monte Carlo Forecast چیست؟

روشی برای پیش‌بینی زمان تکمیل پروژه با استفاده از شبیه‌سازی آماری و داده‌های تاریخی.

---

### چرا بهتر از Velocity Forecast است؟

زیرا عدم قطعیت را مدل می‌کند و به‌جای یک تاریخ قطعی، احتمال‌های مختلف ارائه می‌دهد.

---

### به چه داده‌هایی نیاز دارد؟

- Velocity یا Throughput
- Cycle Time
- Lead Time
- Remaining Work
- داده‌های تاریخی کافی

---

### آیا Jira این قابلیت را دارد؟

خیر.

برای این منظور معمولاً از ابزارهایی مانند ActionableAgile Analytics یا Jira Align استفاده می‌شود.

---

# Summary

| ویژگی | Monte Carlo Forecast |
|---------|----------------------|
| هدف | پیش‌بینی آماری زمان تکمیل |
| خروجی | بازه زمانی با احتمال |
| داده‌های موردنیاز | Velocity، Throughput، Cycle Time |
| گزارش داخلی Jira | ❌ |
| ابزارهای رایج | ActionableAgile، Jira Align، eazyBI |

---

# Enterprise Tips

## 1. از Throughput در Kanban استفاده کنید.

برای تیم‌های Kanban، Monte Carlo معمولاً بر پایه Throughput نتایج دقیق‌تری نسبت به Velocity ارائه می‌دهد.

---

## 2. برای مدیران، احتمال را گزارش کنید.

به‌جای گفتن:

```
Release در 15 مهر
```

بهتر است بگویید:

```
85٪ احتمال دارد Release بین 13 تا 18 مهر انجام شود.
```

---

## 3. داده‌های Outlier را تحلیل کنید.

Sprintهایی که به دلیل قطعی زیرساخت، تعطیلات یا Incidentهای بزرگ عملکرد غیرعادی داشته‌اند، باید قبل از شبیه‌سازی بررسی شوند.

---

## 4. Monte Carlo جایگزین مدیریت Scope نیست.

اگر Scope پروژه مرتب تغییر کند، حتی بهترین مدل آماری نیز Forecast دقیقی نخواهد داشت.

---

## 5. این متریک را با سایر شاخص‌ها ترکیب کنید.

برای بیشترین دقت، Monte Carlo را همراه این شاخص‌ها تحلیل کنید:

- Predictability
- Capacity
- Velocity
- Cycle Time
- Lead Time
- Scope Trend
- Team Stability

---

# مقایسه سه روش Forecast

| ویژگی | Velocity Forecast | Release Forecast | Monte Carlo Forecast |
|--------|------------------|------------------|-----------------------|
| خروجی | تعداد Sprint | تاریخ تقریبی Release | بازه زمانی با احتمال |
| دقت | متوسط | خوب | بسیار بالا |
| در نظر گرفتن عدم قطعیت | ❌ | محدود | ✅ |
| مناسب برای پروژه‌های Enterprise | ⚠️ | ✅ | ✅✅ |
| ابزارهای Jira | محدود | Advanced Roadmaps | ActionableAgile، Jira Align |
