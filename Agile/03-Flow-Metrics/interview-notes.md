# Interview Notes

> سوالات متداول مصاحبه برای Jira Administrator، Scrum Master، Agile Coach، Project Manager و DevOps Engineer

---

# بخش اول — مفاهیم پایه

## سؤال 1

Flow Metrics چیست؟

### پاسخ

Flow Metrics مجموعه‌ای از شاخص‌ها هستند که نحوه حرکت Work Itemها را از زمان ایجاد تا تحویل اندازه‌گیری می‌کنند.

مهم‌ترین آن‌ها:

- Cycle Time
- Lead Time
- Throughput
- WIP
- Flow Efficiency

---

## سؤال 2

چرا Flow Metrics از Velocity مهم‌تر هستند؟

### پاسخ

Velocity فقط میزان کار انجام‌شده در یک Sprint را نشان می‌دهد.

Flow Metrics نشان می‌دهند:

- مشتری چقدر منتظر مانده است.
- فرآیند چقدر پایدار است.
- گلوگاه‌ها کجا هستند.
- آیا تحویل قابل پیش‌بینی است.

---

# بخش دوم — Cycle Time

## سؤال

Cycle Time چیست؟

### پاسخ

مدت زمان از شروع کار واقعی روی یک Issue تا رسیدن آن به Done.

---

## سؤال

Cycle Time زیاد شده است. چه بررسی می‌کنید؟

### پاسخ

- WIP
- Blocked Issue
- QA
- Code Review
- وابستگی به تیم دیگر
- تغییر Workflow
- اندازه Story

---

## سؤال

Cycle Time پایین همیشه خوب است؟

### پاسخ

خیر.

ممکن است:

- کیفیت کاهش یافته باشد.
- تست حذف شده باشد.
- Storyها بیش از حد کوچک شده باشند.

همیشه باید همراه Quality بررسی شود.

---

# بخش سوم — Lead Time

## سؤال

Lead Time چیست؟

### پاسخ

مدت زمان از ایجاد درخواست تا تحویل آن.

---

## سؤال

چرا Lead Time برای Product Owner مهم است؟

### پاسخ

زیرا تجربه واقعی مشتری را اندازه‌گیری می‌کند و مستقیماً بر Time to Market و SLA اثر می‌گذارد.

---

## سؤال

چگونه Lead Time را کاهش می‌دهید؟

### پاسخ

- کاهش Approvalها
- کاهش WIP
- Continuous Delivery
- حذف انتظارهای غیرضروری
- کوچک‌تر کردن Storyها

---

# بخش چهارم — Throughput

## سؤال

Throughput چیست؟

### پاسخ

تعداد Issueهای تکمیل‌شده در یک بازه زمانی.

---

## سؤال

تفاوت Throughput و Velocity چیست؟

### پاسخ

| Throughput | Velocity |
|------------|----------|
| تعداد Issue | Story Point |
| Kanban | Scrum |
| بدون نیاز به Estimation | وابسته به Estimation |

---

# بخش پنجم — WIP

## سؤال

چرا WIP Limit مهم است؟

### پاسخ

زیرا:

- چندوظیفگی را کاهش می‌دهد.
- تمرکز تیم را افزایش می‌دهد.
- Cycle Time را کاهش می‌دهد.
- Predictability را افزایش می‌دهد.

---

## سؤال

اگر WIP دو برابر شود چه اتفاقی می‌افتد؟

### پاسخ

در اغلب موارد:

- Waiting Time افزایش می‌یابد.
- Cycle Time افزایش می‌یابد.
- Lead Time افزایش می‌یابد.
- Flow Efficiency کاهش می‌یابد.

---

# بخش ششم — CFD

## سؤال

CFD چه چیزی را نشان می‌دهد؟

### پاسخ

تعداد Issueها در هر Status در طول زمان.

---

## سؤال

اگر نوار Testing ضخیم شود؟

### پاسخ

احتمالاً گلوگاه در QA یا فرآیند تست وجود دارد.

---

## سؤال

اگر خطوط CFD تقریباً موازی باشند؟

### پاسخ

فرآیند پایدار و قابل پیش‌بینی است.

---

# بخش هفتم — Control Chart

## سؤال

Control Chart برای چه استفاده می‌شود؟

### پاسخ

برای تحلیل:

- Cycle Time
- روند عملکرد
- Outlier
- Predictability

---

## سؤال

Outlier چیست؟

### پاسخ

Issueی که Cycle Time آن به‌طور غیرعادی بیشتر یا کمتر از سایر Issueها است و نیاز به بررسی علت دارد.

---

# بخش هشتم — Flow Efficiency

## سؤال

Flow Efficiency چیست؟

### پاسخ

درصد زمانی که واقعاً روی Issue کار انجام شده است.

```
Flow Efficiency

=

Active Time

/

Lead Time
```

---

## سؤال

Flow Efficiency پایین چه چیزی را نشان می‌دهد؟

### پاسخ

زمان انتظار زیاد، Approvalهای طولانی یا گلوگاه‌های فرآیند.

---

# بخش نهم — Jira

## سؤال

Cycle Time را در Jira از کجا مشاهده می‌کنید؟

### پاسخ

```
Project
    ↓
Reports
    ↓
Control Chart
```

---

## سؤال

CFD را از کجا مشاهده می‌کنید؟

### پاسخ

```
Project
    ↓
Reports
    ↓
Cumulative Flow Diagram
```

---

## سؤال

Lead Time به‌صورت پیش‌فرض در Jira وجود دارد؟

### پاسخ

خیر.

برای تحلیل کامل معمولاً از ابزارهایی مانند:

- eazyBI
- ActionableAgile
- Custom Charts

استفاده می‌شود.

---

# بخش دهم — سناریوهای واقعی

## سناریو 1

Velocity ثابت است اما Lead Time افزایش یافته است.

### تحلیل

احتمالاً:

- Approvalها بیشتر شده‌اند.
- Backlog بزرگ‌تر شده است.
- Releaseها با تأخیر انجام می‌شوند.
- Waiting Time افزایش یافته است.

---

## سناریو 2

Throughput کاهش یافته اما WIP افزایش یافته است.

### تحلیل

تیم کارهای زیادی را شروع کرده اما تعداد کمی را به پایان رسانده است.

راهکار:

- اعمال WIP Limit
- تکمیل کارهای نیمه‌تمام
- کاهش Context Switching

---

## سناریو 3

CFD نشان می‌دهد نوار Review در حال ضخیم شدن است.

### تحلیل

گلوگاه در Code Review است.

راهکار:

- افزایش Reviewer
- تعیین SLA برای Review
- Pair Review
- خودکارسازی بررسی‌های اولیه

---

## سناریو 4

Control Chart دارای Outlierهای متعدد است.

### تحلیل

فرآیند قابل پیش‌بینی نیست.

باید علت هر Outlier بررسی شود، مانند:

- Blocked Issue
- وابستگی خارجی
- تغییر Scope
- مشکل زیرساخت

---

# سؤالات سطح Senior

### چگونه پیش‌بینی می‌کنید یک Epic چه زمانی تکمیل می‌شود؟

پاسخ:

با استفاده از:

- Historical Throughput
- Cycle Time Distribution
- Monte Carlo Forecast
- Percentile Analysis

---

### اگر مدیر بخواهد Velocity را دو برابر کنید، چه پاسخی می‌دهید؟

پاسخ:

به‌جای تمرکز بر Velocity، باید فرآیند را بهبود داد:

- کاهش WIP
- حذف گلوگاه‌ها
- خودکارسازی تست و استقرار
- کوچک‌تر کردن Storyها

افزایش مصنوعی Velocity بدون بهبود فرآیند ارزش واقعی ایجاد نمی‌کند.

---

### مهم‌ترین KPI برای مدیرعامل چیست؟

بسته به نوع سازمان:

- Lead Time
- Time to Market
- Predictability
- Release Frequency
- Customer Satisfaction

---

# اشتباهات رایج در مصاحبه

❌ گفتن اینکه Velocity معیار بهره‌وری افراد است.

❌ مقایسه مستقیم Cycle Time تیم‌های مختلف.

❌ استفاده از Story Point برای مقایسه بین تیم‌ها.

❌ نادیده گرفتن Waiting Time در تحلیل Lead Time.

❌ فرض اینکه Throughput بالا همیشه نشانه عملکرد بهتر است.

---

# خلاصه طلایی

اگر فقط ۵ مفهوم را به خاطر بسپارید، این‌ها مهم‌ترین هستند:

1. **Cycle Time** → سرعت انجام کار
2. **Lead Time** → زمان انتظار مشتری
3. **Throughput** → تعداد خروجی
4. **WIP** → حجم کار هم‌زمان
5. **Flow Efficiency** → درصد زمان ارزش‌آفرین

این پنج متریک، پایه اکثر تحلیل‌های حرفه‌ای Jira، Kanban و DevOps هستند.
