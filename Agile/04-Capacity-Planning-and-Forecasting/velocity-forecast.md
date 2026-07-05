# Velocity Forecast

> روشی برای پیش‌بینی تعداد Sprintهای موردنیاز و زمان تقریبی اتمام Backlog با استفاده از Velocity گذشته تیم.

---

# Definition

Velocity Forecast فرآیندی است که با استفاده از **Velocity تاریخی تیم** تخمین می‌زند:

- چند Sprint دیگر نیاز داریم؟
- چه زمانی Feature تکمیل می‌شود؟
- چه زمانی Release آماده خواهد شد؟

این Forecast بر پایه داده‌های واقعی گذشته است، نه حدس.

---

# هدف

پاسخ به سؤالات:

- اگر Velocity فعلی ادامه پیدا کند، پروژه چه زمانی تمام می‌شود؟
- آیا Release طبق برنامه تحویل می‌شود؟
- آیا نیاز به افزایش ظرفیت وجود دارد؟

---

# پیش‌نیازها

برای Forecast دقیق نیاز داریم:

- حداقل ۵ تا ۱۰ Sprint گذشته
- Velocity پایدار
- Backlog تخمین‌خورده
- تغییرات محدود در Scope

---

# فرمول پایه

```
Required Sprints

=

Remaining Story Points

/

Average Velocity
```

---

# مثال 1

Backlog باقی‌مانده:

```
240 Story Points
```

Average Velocity:

```
40 Story Points
```

```
240

/

40

=

6 Sprint
```

---

# مثال 2

Backlog:

```
310 SP
```

Velocity:

```
31 SP
```

```
10 Sprint
```

---

# اگر Velocity ثابت نباشد؟

مثلاً:

```
38

42

41

39

40
```

میانگین:

```
40 SP
```

Forecast معتبر است.

اما اگر:

```
15

60

22

51

18
```

باشد، استفاده از میانگین به‌تنهایی مناسب نیست و بهتر است از **Monte Carlo Forecast** استفاده شود.

---

# Velocity Forecast در Jira

Jira به‌صورت پیش‌فرض Forecast کامل ارائه نمی‌دهد، اما داده‌های لازم را در اختیار شما قرار می‌دهد.

منابع اصلی:

```
Reports
    ↓
Velocity Chart
```

و

```
Backlog
```

---

# ابزارهای مناسب

- Advanced Roadmaps
- Jira Plans
- eazyBI
- Structure
- ActionableAgile

---

# مثال Enterprise

Velocity شش Sprint اخیر:

| Sprint | Velocity |
|---------|---------:|
| S1 | 41 |
| S2 | 39 |
| S3 | 40 |
| S4 | 42 |
| S5 | 38 |
| S6 | 40 |

میانگین:

```
40 SP
```

Backlog:

```
320 SP
```

Forecast:

```
8 Sprint
```

---

# Forecast بر اساس بازه

بهتر است به‌جای یک عدد ثابت، بازه ارائه شود.

مثال:

Velocity:

```
38 - 42 SP
```

Backlog:

```
320 SP
```

نتیجه:

```
بین 8 تا 9 Sprint
```

---

# ارتباط با Capacity

اگر Capacity Sprint بعد کاهش یابد:

```
Average Velocity

↓

Forecast تغییر می‌کند.
```

بنابراین Forecast باید به‌روزرسانی شود.

---

# ارتباط با Predictability

Predictability بالا

↓

Forecast قابل اعتماد

---

Predictability پایین

↓

Forecast پرریسک

---

# ارتباط با Scope Change

اگر در طول پروژه Storyهای جدید اضافه شوند:

```
Remaining Story Points

↑
```

در نتیجه:

```
Forecast طولانی‌تر می‌شود.
```

---

# Velocity Forecast و Release Planning

مثال:

Release شامل:

```
200 Story Points
```

Average Velocity:

```
40 SP
```

نتیجه:

```
5 Sprint
```

اگر هر Sprint دو هفته باشد:

```
حدود 10 هفته
```

---

# Dashboard KPI

Velocity Forecast معمولاً همراه این شاخص‌ها نمایش داده می‌شود:

- Average Velocity
- Remaining Story Points
- Estimated Sprints
- Predicted Release Date
- Scope Change

---

# نمودار نمونه

```
Remaining Work

320 SP
```

```
Velocity

40 SP
```

```
Forecast

8 Sprint
```

---

# محدودیت‌ها

Velocity Forecast فرض می‌کند:

- Velocity تقریباً ثابت است.
- تیم تغییر نمی‌کند.
- Scope تغییرات شدید ندارد.
- ظرفیت مشابه Sprintهای گذشته است.

اگر این فرض‌ها برقرار نباشند، Forecast دقت کمتری خواهد داشت.

---

# Best Practices

✅ از میانگین چند Sprint استفاده کنید.

✅ پس از هر Sprint Forecast را به‌روزرسانی کنید.

✅ تغییرات Scope را لحاظ کنید.

✅ از Predictability برای اعتبارسنجی Forecast استفاده کنید.

---

# اشتباهات رایج

❌ استفاده از Velocity یک Sprint.

❌ نادیده گرفتن تغییرات تیم.

❌ فرض ثابت بودن Scope.

❌ اعلام تاریخ قطعی به‌جای بازه زمانی.

---

# Interview Questions

### Velocity Forecast چیست؟

پیش‌بینی تعداد Sprintها یا زمان تکمیل پروژه بر اساس Velocity تاریخی تیم.

---

### چرا نباید فقط از آخرین Velocity استفاده کرد؟

زیرا ممکن است آن Sprint شرایط غیرعادی داشته باشد و نماینده عملکرد واقعی تیم نباشد.

---

### اگر Velocity نوسان زیادی داشته باشد چه می‌کنید؟

از Monte Carlo Forecast یا بازه‌های اطمینان استفاده می‌کنم.

---

### آیا Jira این Forecast را دارد؟

به‌صورت محدود در Advanced Roadmaps و برخی افزونه‌ها وجود دارد، اما معمولاً نیاز به گزارش‌های تحلیلی یا ابزارهای جانبی است.

---

# Summary

| ویژگی | Velocity Forecast |
|---------|------------------|
| هدف | پیش‌بینی تعداد Sprint یا زمان تکمیل |
| ورودی | Average Velocity + Remaining Work |
| خروجی | Sprintهای موردنیاز یا تاریخ تقریبی |
| گزارش داخلی Jira | محدود |
| ابزارهای رایج | Advanced Roadmaps، eazyBI، ActionableAgile |

---

# Enterprise Tips

## 1. از میانگین متحرک (Rolling Average) استفاده کنید.

به‌جای میانگین کل تاریخچه، میانگین ۵ تا ۸ Sprint اخیر معمولاً Forecast دقیق‌تری ایجاد می‌کند.

---

## 2. Forecast را در هر Sprint به‌روزرسانی کنید.

هر Sprint جدید داده‌های تازه‌ای برای بهبود پیش‌بینی فراهم می‌کند.

---

## 3. بازه ارائه کنید، نه تاریخ قطعی.

به‌جای:

```
Release: 15 آبان
```

بهتر است بگویید:

```
Release بین 10 تا 20 آبان
```

---

## 4. Velocity را با Capacity بررسی کنید.

اگر Velocity کاهش یافته، ابتدا بررسی کنید آیا علت آن کاهش Capacity بوده است یا مشکل در فرآیند توسعه.

---

## 5. Forecast را با شاخص‌های دیگر اعتبارسنجی کنید.

پیش‌بینی معتبر زمانی به دست می‌آید که Velocity را در کنار این شاخص‌ها تحلیل کنید:

- Predictability
- Capacity
- Cycle Time
- Lead Time
- Scope Change
- Team Stability

---

# مثال کامل

فرض کنید:

```
Remaining Backlog

450 SP
```

Velocity شش Sprint اخیر:

```
42
39
41
40
38
40
```

Average Velocity:

```
40 SP
```

Forecast:

```
450 ÷ 40

≈ 11.25 Sprint
```

اگر طول هر Sprint:

```
2 هفته
```

باشد:

```
حدود 22 تا 24 هفته
```

در صورتی که Scope ثابت بماند و Velocity تغییر محسوسی نداشته باشد.
