# Predictability

> یکی از مهم‌ترین KPIهای Agile که نشان می‌دهد تیم تا چه اندازه می‌تواند خروجی Sprintها و زمان تحویل را به‌صورت قابل اعتماد پیش‌بینی کند.

---

# Definition

Predictability میزان توانایی تیم در تحویل کاری است که قبلاً متعهد شده است.

به بیان ساده:

> آیا تیم معمولاً همان چیزی را که قول داده، در همان زمانی که انتظار می‌رفت تحویل می‌دهد؟

Predictability یکی از مهم‌ترین شاخص‌های بلوغ تیم Agile است.

---

# چرا Predictability مهم است؟

اگر تیم قابل پیش‌بینی باشد:

- Product Owner بهتر Release را برنامه‌ریزی می‌کند.
- مدیر پروژه زمان تحویل را دقیق‌تر اعلام می‌کند.
- مشتری اعتماد بیشتری به تیم خواهد داشت.
- ریسک پروژه کاهش می‌یابد.

---

# Predictability چه چیزی نیست؟

Predictability به معنی:

❌ سرعت بیشتر

❌ Velocity بالاتر

❌ اضافه‌کاری

نیست.

هدف:

```
Stable Delivery
```

است.

---

# چگونه اندازه‌گیری می‌شود؟

روش‌های مختلفی وجود دارد.

رایج‌ترین روش:

```
Predictability

=

Completed Commitment

/

Initial Commitment

×

100
```

---

# مثال

Initial Commitment

```
40 SP
```

Completed

```
38 SP
```

```
Predictability

=

95%
```

---

# مثال دیگر

```
Sprint 1

96%
```

```
Sprint 2

93%
```

```
Sprint 3

94%
```

نتیجه:

تیم بسیار قابل پیش‌بینی است.

---

# تفسیر

| مقدار | وضعیت |
|-------:|--------|
| بالای 95% | عالی |
| 85 تا 95% | خوب |
| 70 تا 85% | قابل قبول |
| کمتر از 70% | نیازمند بهبود |

---

# ارتباط با Velocity

دو تیم را در نظر بگیرید.

## Team A

Velocity

```
30

60

20

55

25
```

---

## Team B

Velocity

```
39

41

40

38

40
```

میانگین Velocity ممکن است مشابه باشد، اما Team B بسیار قابل پیش‌بینی‌تر است.

---

# ارتباط با Capacity

Capacity مناسب

↓

Commitment منطقی

↓

Predictability بالا

---

اگر Capacity اشتباه محاسبه شود:

```
Over Commitment
```

↓

```
Predictability کاهش می‌یابد.
```

---

# ارتباط با Cycle Time

Cycle Time پایدار

↓

Predictability بالا

---

Cycle Time متغیر

↓

Forecast ضعیف

---

# ارتباط با Lead Time

Lead Time پایدار

↓

Release Forecast دقیق‌تر

---

# ارتباط با Flow Efficiency

Flow Efficiency بالا معمولاً باعث کاهش زمان انتظار و در نتیجه Predictability بهتر می‌شود.

---

# Predictability در Jira

Jira به‌صورت پیش‌فرض متریکی با این نام ارائه نمی‌دهد.

اما می‌توان آن را با استفاده از داده‌های:

- Sprint Report
- Velocity Report
- Dashboardهای سفارشی
- eazyBI
- ActionableAgile

محاسبه کرد.

---

# مثال Enterprise

شش Sprint اخیر:

| Sprint | Predictability |
|--------|---------------:|
| S1 | 96% |
| S2 | 95% |
| S3 | 94% |
| S4 | 96% |
| S5 | 95% |
| S6 | 97% |

میانگین:

```
95.5%
```

نتیجه:

تیم برای Forecast بسیار مناسب است.

---

# مثال نامناسب

| Sprint | Predictability |
|--------|---------------:|
| S1 | 55% |
| S2 | 92% |
| S3 | 61% |
| S4 | 97% |
| S5 | 72% |

نتیجه:

رفتار تیم قابل پیش‌بینی نیست.

---

# عوامل کاهش Predictability

- تغییر Scope
- Incident
- برآورد اشتباه
- Capacity اشتباه
- وابستگی به تیم‌های دیگر
- Blocked Issue
- Storyهای بزرگ

---

# چگونه Predictability را افزایش دهیم؟

✅ Storyها را کوچک‌تر کنید.

✅ WIP را کاهش دهید.

✅ Capacity واقعی را محاسبه کنید.

✅ از داده‌های Sprintهای گذشته استفاده کنید.

✅ تغییرات Sprint را به حداقل برسانید.

---

# Dashboard KPI

Predictability معمولاً کنار این شاخص‌ها قرار می‌گیرد:

- Velocity
- Capacity
- Initial Commitment
- Final Commitment
- Sprint Goal Success
- Focus Factor

---

# نمودار نمونه

```
Sprint 1

96%
```

```
Sprint 2

95%
```

```
Sprint 3

94%
```

```
Sprint 4

95%
```

روند:

```
Stable
```

---

# ارتباط با Forecast

Predictability بالا باعث می‌شود:

- Velocity Forecast دقیق‌تر شود.
- Release Forecast قابل اعتمادتر باشد.
- Monte Carlo نتایج واقعی‌تری ارائه دهد.

---

# Best Practices

✅ Predictability را در هر Sprint اندازه‌گیری کنید.

✅ به جای یک Sprint، روند چند Sprint را بررسی کنید.

✅ علت کاهش ناگهانی را در Retrospective تحلیل کنید.

✅ از آن برای بهبود فرآیند استفاده کنید، نه ارزیابی افراد.

---

# اشتباهات رایج

❌ مساوی دانستن Predictability با Velocity.

❌ انتظار Predictability برابر 100%.

❌ استفاده از این شاخص برای مقایسه تیم‌ها بدون در نظر گرفتن شرایط.

---

# Interview Questions

### Predictability چیست؟

توانایی تیم در تحویل کارهای متعهدشده در زمان پیش‌بینی‌شده.

---

### چرا Predictability مهم‌تر از Velocity است؟

زیرا قابلیت اعتماد و برنامه‌ریزی را نشان می‌دهد، نه فقط حجم خروجی را.

---

### چگونه Predictability را افزایش می‌دهید؟

- بهبود Capacity Planning
- کاهش WIP
- کوچک‌تر کردن Storyها
- کاهش تغییرات Sprint
- تحلیل Retrospective

---

### آیا Jira این متریک را دارد؟

خیر.

این متریک معمولاً با استفاده از داده‌های Sprint Report یا ابزارهای تحلیلی محاسبه می‌شود.

---

# Summary

| ویژگی | Predictability |
|---------|----------------|
| هدف | سنجش قابلیت پیش‌بینی تیم |
| واحد | درصد |
| گزارش داخلی Jira | ❌ |
| وابسته به | Capacity، Commitment، Velocity |
| کاربرد | Forecast و Release Planning |

---

# Enterprise Tips

## 1. به روند نگاه کنید، نه یک Sprint.

یک Sprint ضعیف لزوماً مشکل ساختاری نیست.

---

## 2. Predictability را با کیفیت ترکیب کنید.

تیمی که همیشه به تعهد خود می‌رسد اما با Bugهای زیاد، Predictability مطلوبی از دید کسب‌وکار ندارد.

---

## 3. از داده‌های تاریخی استفاده کنید.

Forecastهای معتبر بر اساس ۶ تا ۱۲ Sprint اخیر ساخته می‌شوند.

---

## 4. از Predictability برای مدیریت ریسک استفاده کنید.

کاهش مداوم این شاخص می‌تواند هشدار زودهنگام برای مشکلات پروژه باشد.

---

## 5. Predictability را در سطح تیم ارزیابی کنید.

این شاخص برای بهبود فرآیند تیمی طراحی شده است و نباید مبنای ارزیابی عملکرد افراد قرار گیرد.

---

# ارتباط با سایر KPIها

```text
Capacity
      │
      ▼
Initial Commitment
      │
      ▼
Final Commitment
      │
      ▼
Predictability
      │
      ▼
Velocity Forecast
      │
      ▼
Release Forecast
      │
      ▼
Monte Carlo Forecast
```
