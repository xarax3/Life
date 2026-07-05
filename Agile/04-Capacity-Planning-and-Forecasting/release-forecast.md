# Release Forecast

> روشی برای پیش‌بینی تاریخ انتشار (Release Date) بر اساس داده‌های واقعی تیم، نه حدس و گمان.

---

# Definition

Release Forecast فرآیندی است که با استفاده از داده‌های تاریخی تیم، زمان تقریبی آماده شدن یک Release را پیش‌بینی می‌کند.

هدف آن پاسخ به این سؤال است:

> **اگر تیم با همین روند ادامه دهد، چه زمانی نسخه آماده انتشار خواهد بود؟**

---

# تفاوت Release Planning و Release Forecast

| Release Planning | Release Forecast |
|------------------|------------------|
| برنامه‌ریزی اولیه | پیش‌بینی مبتنی بر داده |
| قبل از توسعه | در طول توسعه |
| فرضیات | داده‌های واقعی |

---

# اطلاعات مورد نیاز

برای Forecast دقیق معمولاً به این داده‌ها نیاز داریم:

- Remaining Story Points
- Average Velocity
- Capacity
- Predictability
- Scope Changes
- تعطیلات و مرخصی‌ها

---

# فرمول پایه

```
Estimated Sprints

=

Remaining Story Points

/

Average Velocity
```

سپس:

```
Estimated Date

=

Sprint Length

×

Estimated Sprints
```

---

# مثال 1

Remaining Work:

```
240 SP
```

Velocity:

```
40 SP
```

Sprint:

```
2 Weeks
```

```
240

/

40

=

6 Sprint
```

```
6 × 2

=

12 Weeks
```

Release تقریباً:

```
12 هفته دیگر
```

---

# مثال 2

Remaining Backlog:

```
500 SP
```

Average Velocity:

```
50 SP
```

Sprint:

```
3 Weeks
```

Forecast:

```
10 Sprint
```

```
30 Weeks
```

---

# اثر Capacity

فرض کنید:

Capacity کاهش پیدا کند.

Velocity نیز معمولاً کاهش خواهد یافت.

در نتیجه:

```
Release Date

↓

عقب می‌رود.
```

---

# اثر Scope Change

اگر Product Owner Feature جدید اضافه کند:

```
Remaining Story Points

↑
```

در نتیجه:

```
Forecast طولانی‌تر می‌شود.
```

---

# اثر Predictability

تیمی با Predictability بالا:

```
Forecast قابل اعتماد
```

تیمی با Predictability پایین:

```
Forecast پرریسک
```

---

# Release Forecast در Jira

### Jira Software

به‌صورت پیش‌فرض تاریخ Release را پیش‌بینی نمی‌کند.

---

### Advanced Roadmaps

دارای قابلیت:

- Forecast
- Scenario Planning
- Capacity Planning
- Release Planning

---

### eazyBI

امکان ساخت Dashboardهای سفارشی برای Forecast را فراهم می‌کند.

---

### ActionableAgile

Forecastهای آماری مانند Monte Carlo را ارائه می‌دهد.

---

# Release Forecast در داشبورد

شاخص‌های رایج:

- Remaining Story Points
- Average Velocity
- Sprint Count
- Estimated Release Date
- Confidence Level
- Scope Trend

---

# مثال داشبورد

```
Remaining

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

```
Release

15 Sep
```

---

# Forecast با Confidence Level

به‌جای اعلام یک تاریخ قطعی:

```
Release:

10 October
```

بهتر است:

| Confidence | Date |
|------------|------|
| 50% | 5 Oct |
| 80% | 10 Oct |
| 95% | 18 Oct |

این روش واقع‌بینانه‌تر است.

---

# ارتباط با سایر متریک‌ها

```
Capacity

↓

Velocity

↓

Predictability

↓

Release Forecast
```

---

# مثال Enterprise

Backlog:

```
780 SP
```

Velocity:

```
52 SP
```

Forecast:

```
15 Sprint
```

Sprint:

```
2 Weeks
```

Release:

```
30 Weeks
```

---

# اگر Velocity کاهش یابد؟

Velocity:

```
52

↓

40
```

Forecast:

```
780

/

40

≈20 Sprint
```

در نتیجه Release حدود ۱۰ هفته دیرتر خواهد بود.

---

# اگر Scope افزایش یابد؟

Backlog:

```
780 SP

↓

950 SP
```

Forecast:

```
950

/

52

≈19 Sprint
```

بدون تغییر در Velocity نیز Release عقب خواهد افتاد.

---

# Best Practices

✅ Forecast را پس از هر Sprint به‌روزرسانی کنید.

✅ تغییرات Scope را در محاسبات لحاظ کنید.

✅ Capacity واقعی را مبنا قرار دهید.

✅ Forecast را به‌صورت بازه زمانی ارائه کنید.

---

# اشتباهات رایج

❌ اعلام تاریخ قطعی.

❌ استفاده از Velocity یک Sprint.

❌ نادیده گرفتن تغییرات Scope.

❌ فرض ثابت بودن Capacity.

---

# Interview Questions

### Release Forecast چیست؟

پیش‌بینی زمان انتشار محصول بر اساس داده‌های واقعی تیم.

---

### چه عواملی روی آن اثر دارند؟

- Velocity
- Capacity
- Scope
- Predictability
- Sprint Length

---

### آیا Jira به‌صورت پیش‌فرض این قابلیت را دارد؟

به‌صورت محدود.

برای Forecastهای حرفه‌ای معمولاً از:

- Advanced Roadmaps
- eazyBI
- ActionableAgile

استفاده می‌شود.

---

### چرا تاریخ قطعی ارائه نمی‌کنید؟

زیرا پروژه‌های Agile ذاتاً همراه با عدم قطعیت هستند و Forecast باید احتمال و ریسک را نیز منعکس کند.

---

# Summary

| ویژگی | Release Forecast |
|---------|------------------|
| هدف | پیش‌بینی زمان انتشار |
| ورودی | Velocity، Capacity، Scope |
| خروجی | تاریخ تقریبی Release |
| گزارش داخلی Jira | محدود |
| ابزارهای رایج | Advanced Roadmaps، eazyBI، ActionableAgile |

---

# Enterprise Tips

## 1. از Forecastهای بازه‌ای استفاده کنید.

به‌جای یک تاریخ ثابت، بازه زمانی با سطح اطمینان (Confidence Level) ارائه دهید.

---

## 2. Forecast را در هر Sprint بازبینی کنید.

هر Sprint می‌تواند Velocity، Capacity یا Scope را تغییر دهد و Forecast باید بر اساس داده‌های جدید اصلاح شود.

---

## 3. Scope را کنترل کنید.

افزایش مداوم Scope یکی از اصلی‌ترین دلایل تأخیر Release است.

---

## 4. از سناریوهای مختلف استفاده کنید.

در پروژه‌های بزرگ معمولاً سه سناریو تهیه می‌شود:

- Best Case
- Expected Case
- Worst Case

این کار به مدیریت ریسک کمک می‌کند.

---

## 5. Forecast را با شاخص‌های کیفیت ترکیب کنید.

رسیدن به تاریخ Release زمانی ارزشمند است که کیفیت نیز حفظ شده باشد؛ بنابراین Forecast را در کنار این شاخص‌ها بررسی کنید:

- Defect Rate
- Predictability
- Sprint Goal Achievement
- Cycle Time
- Lead Time
- Change Failure Rate (در DevOps)

---

# مثال کامل

فرض کنید:

```
Remaining Backlog

640 SP
```

میانگین Velocity:

```
40 SP
```

طول Sprint:

```
2 هفته
```

محاسبه:

```
640 ÷ 40

=

16 Sprint
```

```
16 × 2

=

32 هفته
```

اگر Predictability تیم:

```
95%
```

باشد و تغییر قابل‌توجهی در Scope ایجاد نشود، می‌توان انتظار داشت Release حدود **۳۲ هفته دیگر** آماده شود.

---

# ارتباط با Day 5

Release Forecast یک پیش‌بینی مبتنی بر **میانگین** است.

اما اگر بخواهید احتمال وقوع سناریوهای مختلف را محاسبه کنید (مثلاً «با احتمال ۸۵٪ تا چه تاریخی Release انجام می‌شود؟»)، باید از **Monte Carlo Forecasting** استفاده کنید که موضوع بخش بعدی است.
