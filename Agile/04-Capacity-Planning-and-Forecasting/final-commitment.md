# Final Commitment

> معیاری برای سنجش اینکه تیم در پایان Sprint چه مقدار از تعهد اولیه خود را واقعاً انجام داده است.

---

# Definition

Final Commitment مقدار کاری است که **در پایان Sprint** از تعهد اولیه (Initial Commitment) به وضعیت **Done** رسیده است.

این متریک برای اندازه‌گیری کیفیت برنامه‌ریزی Sprint و قابلیت اعتماد (Reliability) تیم استفاده می‌شود.

---

# هدف

پاسخ به این سؤال:

> از کاری که در ابتدای Sprint متعهد شدیم، چه مقدار را واقعاً تحویل دادیم؟

---

# تفاوت Initial و Final Commitment

| Initial Commitment | Final Commitment |
|--------------------|------------------|
| ابتدای Sprint | پایان Sprint |
| برنامه‌ریزی | نتیجه واقعی |
| انتظار تیم | خروجی تیم |

---

# محل در Jira

```
Project
    ↓
Reports
    ↓
Sprint Report
```

در Sprint Report معمولاً این بخش‌ها دیده می‌شوند:

- Completed Issues
- Not Completed Issues
- Issues Added During Sprint
- Removed Issues

Final Commitment از روی **Completed Issues** محاسبه می‌شود.

---

# فرمول

بر اساس Story Point:

```
Final Commitment

=

Completed Story Points

(از تعهد اولیه)
```

بر اساس تعداد Issue:

```
Final Commitment

=

Completed Initial Issues
```

---

# مثال 1

Initial Commitment:

```
40 Story Points
```

در پایان Sprint:

```
34 Story Points
```

Final Commitment:

```
34 SP
```

---

# مثال 2

Initial Commitment:

```
20 Issues
```

Completed:

```
18 Issues
```

Final Commitment:

```
18 Issues
```

---

# Commitment Reliability

یکی از مهم‌ترین KPIهای Scrum

فرمول:

```
Commitment Reliability

=

Final Commitment

/

Initial Commitment

×

100
```

---

# مثال

```
Initial

40 SP
```

```
Final

36 SP
```

```
36

/

40

×

100

=

90%
```

---

# تفسیر

| مقدار | تحلیل |
|-------:|--------|
| 95% تا 100% | بسیار عالی |
| 85% تا 95% | مناسب |
| 70% تا 85% | نیاز به بررسی |
| کمتر از 70% | برنامه‌ریزی ضعیف یا مشکل اجرایی |

---

# مثال واقعی

میانگین Velocity:

```
42 SP
```

Capacity:

```
38 SP
```

Initial Commitment:

```
37 SP
```

Completed:

```
36 SP
```

Reliability:

```
97%
```

نتیجه:

برنامه‌ریزی بسیار دقیق بوده است.

---

# ارتباط با Capacity

اگر Capacity:

```
200 Hours
```

باشد اما تیم:

```
260 Hours
```

Commit کند،

معمولاً Final Commitment کاهش خواهد یافت.

---

# ارتباط با Velocity

Velocity واقعی Sprint:

```
36 SP
```

اگر Initial:

```
50 SP
```

باشد،

مشکل از برنامه‌ریزی است، نه الزاماً از عملکرد تیم.

---

# ارتباط با Sprint Goal

ممکن است:

- Final Commitment پایین باشد.
- اما Sprint Goal محقق شده باشد.

مثال:

هدف Sprint:

```
قابلیت ورود کاربران
```

Feature اصلی تکمیل شده است، اما چند Task فرعی باقی مانده‌اند.

در این حالت از دید کسب‌وکار Sprint می‌تواند موفق باشد.

---

# Dashboard KPI

معمولاً این شاخص‌ها کنار هم نمایش داده می‌شوند:

- Initial Commitment
- Final Commitment
- Commitment Reliability
- Velocity
- Capacity
- Sprint Goal Success

---

# نمودار نمونه

```
Initial

████████████████

40
```

```
Final

██████████████

36
```

```
Difference

4 SP
```

---

# دلایل کاهش Final Commitment

- برآورد نادرست
- تغییر Scope
- Incidentهای بحرانی
- مرخصی پیش‌بینی‌نشده
- Bugهای مهم
- وابستگی به تیم دیگر
- Blocked Issue

---

# اگر Final Commitment بیشتر از Initial شود؟

این حالت زمانی رخ می‌دهد که در طول Sprint Issueهای جدید اضافه و تکمیل شوند.

برای تحلیل Sprint بهتر است این موارد از تعهد اولیه جدا بررسی شوند.

---

# Added Issues

مثال:

```
Initial

40 SP
```

```
Added

8 SP
```

```
Completed

44 SP
```

Velocity:

```
44 SP
```

اما:

```
Commitment Reliability

=

36

/

40

=

90%
```

زیرا فقط تعهد اولیه مبنای محاسبه است.

---

# Best Practices

✅ تغییرات Sprint را حداقل نگه دارید.

✅ Added Issueها را جداگانه گزارش کنید.

✅ Final Commitment را همراه Sprint Goal تحلیل کنید.

✅ اختلاف زیاد بین Initial و Final را در Retrospective بررسی کنید.

---

# اشتباهات رایج

❌ مقایسه Final Commitment بین تیم‌های مختلف.

❌ استفاده از این متریک برای ارزیابی عملکرد فردی.

❌ نادیده گرفتن تغییر Scope.

❌ برابر دانستن Velocity با Commitment.

---

# Interview Questions

### Final Commitment چیست؟

مقدار کاری که از تعهد اولیه در پایان Sprint تکمیل شده است.

---

### چگونه محاسبه می‌شود؟

مجموع Story Point یا Issueهای تکمیل‌شده از تعهد اولیه Sprint.

---

### Commitment Reliability چیست؟

درصد تحقق تعهد اولیه.

```
Final / Initial × 100
```

---

### اگر Reliability برابر 60٪ باشد چه نتیجه‌ای می‌گیرید؟

احتمالاً:

- Over Commitment
- برآورد ضعیف
- تغییر Scope
- مشکلات اجرایی

---

# Summary

| ویژگی | Final Commitment |
|---------|------------------|
| زمان اندازه‌گیری | پایان Sprint |
| هدف | سنجش تحقق تعهد |
| محل در Jira | Sprint Report |
| واحد | Story Point یا Issue |
| KPI اصلی | Commitment Reliability |

---

# Enterprise Tips

## 1. Reliability مهم‌تر از Completion است.

ممکن است تیم Velocity بالایی داشته باشد، اما اگر فقط 60٪ از تعهد اولیه را انجام دهد، برنامه‌ریزی Sprint قابل اعتماد نیست.

---

## 2. Added Issueها را جدا تحلیل کنید.

تکمیل Storyهای اضافه‌شده نباید باعث شود کیفیت برنامه‌ریزی اولیه بهتر از واقعیت به نظر برسد.

---

## 3. روند Reliability را بررسی کنید.

هدف، رسیدن به 100٪ نیست؛ بلکه داشتن روندی پایدار و قابل پیش‌بینی در چند Sprint متوالی است.

---

## 4. Final Commitment را در Retrospective بررسی کنید.

اگر اختلاف زیادی با Initial وجود دارد، علت را در جلسه Retrospective شناسایی و برای Sprint بعد اقدام اصلاحی تعریف کنید.

---

## 5. این متریک را با سایر KPIها ترکیب کنید.

برای تحلیل کامل Sprint، Final Commitment را همراه این شاخص‌ها بررسی کنید:

- Capacity
- Velocity
- Predictability
- Sprint Goal Achievement
- Cycle Time
- Lead Time
