# Sprint Metrics

> سطح: Intermediate → Advanced
>
> ابزارها:
> - Jira Software
> - Jira Data Center
> - Jira Cloud
> - eazyBI
> - Tempo
> - Structure
> - Advanced Roadmaps

---

# Sprint Metrics چیست؟

Sprint Metrics شاخص‌هایی هستند که عملکرد یک Sprint را از جنبه‌های مختلف اندازه‌گیری می‌کنند.

این شاخص‌ها به سؤالات زیر پاسخ می‌دهند:

- آیا Sprint موفق بوده؟
- آیا تیم بیش از ظرفیت خود کار برداشته؟
- آیا تخمین‌ها درست بوده‌اند؟
- آیا Scope تغییر کرده؟
- آیا تیم قابل پیش‌بینی است؟
- آیا Velocity پایدار است؟

---

# چرخه Sprint

```text
Backlog
      │
      ▼
Sprint Planning
      │
      ▼
Initial Commitment
      │
      ▼
Development
      │
      ▼
Scope Changes
      │
      ▼
Sprint End
      │
      ▼
Completed Commitment
      │
      ▼
Velocity
```

---

# 1. Initial Commitment

## تعریف

مقدار کاری که تیم در **لحظه شروع Sprint** متعهد به انجام آن شده است.

معمولاً بر اساس:

- Story Point
- تعداد Issue
- ساعت

اندازه‌گیری می‌شود.

---

## چرا مهم است؟

این عدد مبنای تمام تحلیل‌های Sprint است.

اگر آن را ندانید:

- Velocity بی‌معنی می‌شود.
- Predictability قابل اندازه‌گیری نیست.
- Scope Change مشخص نمی‌شود.

---

## مثال

| Story | Point |
|--------|------:|
| A | 8 |
| B | 5 |
| C | 3 |
| D | 13 |

Initial Commitment = 29 SP

---

## در Jira کجاست؟

```
Project
    ↓
Reports
    ↓
Sprint Report
```

در Sprint Report این مقدار به صورت مستقیم نمایش داده نمی‌شود اما از وضعیت Sprint در زمان شروع قابل استخراج است.

---

## افزونه

اگر تاریخچه چند Sprint را بخواهید:

- eazyBI ⭐⭐⭐⭐⭐
- Structure
- Custom Charts

---

## مدیر پروژه چگونه تفسیر کند؟

کم بودن Initial Commitment

↓

ظرفیت تیم خالی مانده است.

زیاد بودن آن

↓

احتمال Carry Over زیاد است.

---

# 2. Final Commitment

## تعریف

مقدار کل کار Sprint بعد از تمام تغییرات.

فرمول

Final Commitment

=

Initial Commitment

+

Added Scope

-

Removed Scope

---

## مثال

Initial = 30 SP

Added = 10

Removed = 5

Final = 35 SP

---

## محل در Jira

Sprint Report

قسمت

Added Issues

Removed Issues

---

## چرا مهم است؟

اگر اختلاف زیادی با Initial داشته باشد یعنی:

- برنامه‌ریزی ضعیف بوده
- یا Scope کنترل نشده است.

---

# 3. Completed Commitment

## تعریف

کارهایی که تا پایان Sprint واقعاً Done شده‌اند.

مثال

Initial = 40

Done = 35

Completed Commitment = 35

---

## کاربرد

اندازه‌گیری میزان تحقق تعهد تیم.

---

## محل در Jira

Sprint Report

Velocity Report

---

# 4. Commitment Reliability

## تعریف

درصد تحقق تعهد اولیه.

فرمول

Completed

÷

Initial

×

100

---

## مثال

Initial = 40

Completed = 36

Reliability = 90%

---

## تفسیر

95~100%

⭐⭐⭐⭐⭐

عالی

90%

⭐⭐⭐⭐

خوب

70%

⭐⭐

نیازمند بررسی

کمتر از 60%

🔴

مشکل جدی

---

## Jira

به صورت پیش‌فرض ندارد.

eazyBI بهترین گزینه است.

---

# 5. Scope Change

## تعریف

تغییرات Sprint بعد از شروع.

مثال

- اضافه شدن Story
- حذف Story
- تغییر Estimate

---

## محل در Jira

Sprint Report

Added Issues

Removed Issues

---

## تفسیر

کم

↓

Planning خوب

زیاد

↓

Sprint ناپایدار

---

# 6. Scope Creep

## تعریف

افزایش کنترل‌نشده Scope.

مثال

شروع Sprint

30 Story Point

پایان Sprint

52 Story Point

یعنی Scope Creep

---

## Jira

مستقیم ندارد.

eazyBI

Rich Filters

---

# 7. Spillover

## تعریف

کارهایی که از Sprint جاری به Sprint بعد منتقل می‌شوند.

---

## مثال

Sprint

40 Story Point

Done

32

Remaining

8

Spillover = 8

---

## محل

Sprint Report

Incomplete Issues

---

## علت‌ها

- تخمین اشتباه
- باگ زیاد
- Capacity کم
- تغییر Scope

---

# 8. Carry Over

تقریباً همان Spillover است.

برخی شرکت‌ها:

Carry Over = Story

Spillover = Story Point

---

# 9. Sprint Goal Achievement

## تعریف

آیا هدف Sprint محقق شده؟

ممکن است:

80٪ Storyها Done باشند

اما هدف اصلی انجام نشده باشد.

---

## اندازه‌گیری

معمولاً توسط Product Owner

نه Jira.

---

# 10. Focus Factor

## تعریف

نشان می‌دهد تیم چه مقدار از ظرفیت واقعی خود را صرف کار مفید کرده است.

فرمول رایج

Completed Story Points

÷

Capacity

---

## مثال

Capacity

50

Completed

40

Focus Factor

80%

---

## محل

در Jira وجود ندارد.

Tempo

eazyBI

---

# 11. Capacity

## تعریف

کل توان تیم برای انجام کار.

مثال

5 نفر

هر نفر

8 ساعت

10 روز

Capacity

400 ساعت

---

## آیا Jira دارد؟

❌ خیر

---

## افزونه

Tempo Planner

Advanced Roadmaps

BigPicture

---

# 12. Effective Capacity

## تعریف

ظرفیت واقعی بعد از حذف:

- مرخصی
- جلسه
- تعطیلی
- آموزش
- پشتیبانی

---

## مثال

Capacity

400

Meeting

40

Vacation

24

Support

36

Effective Capacity

300

---

# تفاوت Capacity و Velocity

| Capacity | Velocity |
|-----------|----------|
| قبل از Sprint | بعد از Sprint |
| توان تیم | خروجی تیم |
| ساعت یا نفر-روز | Story Point |
| برای برنامه‌ریزی | برای تحلیل |

---

# تفاوت Commitment و Capacity

Capacity

↓

حداکثر توان

Commitment

↓

کاری که تیم قبول کرده

Completed

↓

کاری که واقعاً انجام شده

---

# افزونه‌های مناسب

| افزونه | کاربرد |
|----------|----------|
| eazyBI | KPIهای Sprint |
| Tempo | Capacity |
| Structure | مدیریت Sprint |
| Rich Filters | Dashboard |
| BigPicture | Planning |
| Advanced Roadmaps | Capacity Planning |

---

# اشتباهات رایج

❌ مقایسه Velocity دو تیم

❌ تغییر Story Point وسط Sprint

❌ اضافه کردن Scope زیاد

❌ استفاده از Velocity برای ارزیابی عملکرد افراد

❌ برابر دانستن Capacity با Velocity

---

# بهترین KPIهای Sprint

- Initial Commitment
- Final Commitment
- Completed Commitment
- Commitment Reliability
- Velocity
- Average Velocity
- Capacity
- Effective Capacity
- Scope Change
- Scope Creep
- Spillover
- Sprint Goal Achievement
- Focus Factor

---

# جمع‌بندی

اگر فقط این ۱۲ شاخص را همیشه بررسی کنید، حدود ۸۰٪ سلامت Sprint قابل ارزیابی است.
