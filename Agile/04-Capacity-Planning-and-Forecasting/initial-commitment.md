# Initial Commitment

> یکی از مهم‌ترین متریک‌های Sprint که نشان می‌دهد تیم در ابتدای Sprint چه مقدار کار را متعهد شده است.

---

# Definition

Initial Commitment مقدار کل کاری است که **در لحظه شروع Sprint** داخل Sprint Backlog قرار دارد.

این مقدار مبنای اندازه‌گیری موفقیت Sprint است.

در Scrum، تیم در Sprint Planning روی این مقدار توافق می‌کند.

---

# هدف

پاسخ به این سؤال:

> تیم در ابتدای Sprint متعهد شده بود چه مقدار کار انجام دهد؟

---

# محل در Jira

```
Project
    ↓
Reports
    ↓
Sprint Report
```

در بخش بالای گزارش معمولاً مشاهده می‌کنید:

```
Completed Issues

Not Completed Issues

Issues Added During Sprint
```

Initial Commitment همان Issueهایی است که **قبل از Start Sprint** داخل Sprint بوده‌اند.

---

# نحوه محاسبه

اگر تیم بر اساس Story Point کار می‌کند:

```
Initial Commitment

=

Sum(Story Points)

Before Sprint Start
```

اگر بر اساس تعداد Issue کار می‌کند:

```
Initial Commitment

=

Issue Count

Before Sprint Start
```

---

# مثال 1

قبل از شروع Sprint:

| Story | Story Point |
|--------|------------:|
| ST-101 | 8 |
| ST-102 | 5 |
| ST-103 | 3 |
| ST-104 | 2 |
| ST-105 | 5 |

```
Initial Commitment

=

23 Story Points
```

---

# مثال 2

اگر تیم از Story Point استفاده نکند:

```
Initial Commitment

=

18 Issues
```

---

# چرا مهم است؟

زیرا کیفیت برنامه‌ریزی Sprint را اندازه‌گیری می‌کند.

اگر این مقدار بیش از ظرفیت تیم باشد:

- Sprint شکست می‌خورد.
- Carry Over افزایش می‌یابد.
- Predictability کاهش می‌یابد.

---

# ارتباط با Sprint Planning

```
Capacity
      │
      ▼
Initial Commitment
      │
      ▼
Sprint Goal
      │
      ▼
Sprint Start
```

---

# ارتباط با Capacity

مثال:

```
Capacity

=

200 Hours
```

اما تیم:

```
280 Hours
```

کار Commit کرده است.

نتیجه:

```
Over Commitment
```

---

# ارتباط با Velocity

میانگین Velocity:

```
35 Story Points
```

اگر تیم:

```
55 Story Points
```

Commit کند،

ریسک بالاست.

---

# Initial Commitment در Sprint Report

نمونه:

```
Sprint

Story Points

Initial Commitment

40 SP

Completed

34 SP

Added

8 SP

Removed

5 SP
```

---

# تحلیل

اگر مقدار Initial Commitment نزدیک به Velocity میانگین باشد،

برنامه‌ریزی واقع‌بینانه است.

اگر اختلاف زیاد باشد،

احتمالاً Sprint بیش از حد خوش‌بینانه یا محافظه‌کارانه برنامه‌ریزی شده است.

---

# مثال واقعی

میانگین Velocity:

```
42 SP
```

Capacity:

```
85%
```

محاسبه:

```
42

×

0.85

=

36 SP
```

اگر تیم:

```
38 SP
```

Commit کند،

ریسک قابل‌قبول است.

اگر:

```
55 SP
```

Commit کند،

احتمال اتمام Sprint پایین است.

---

# KPI مرتبط

Initial Commitment معمولاً همراه این شاخص‌ها تحلیل می‌شود:

- Velocity
- Capacity
- Final Commitment
- Predictability
- Sprint Success Rate

---

# Dashboard

```
Capacity

220h
```

```
Initial Commitment

205h
```

```
Difference

15h
```

---

# تفاوت Initial Commitment و Sprint Goal

Initial Commitment:

```
چه مقدار کار؟
```

Sprint Goal:

```
چرا این کار انجام می‌شود؟
```

Sprint Goal یک هدف تجاری است، نه مجموع Story Pointها.

---

# ارتباط با تغییرات Sprint

در Scrum توصیه می‌شود پس از شروع Sprint، تغییرات حداقلی باشند.

هرچه Issue بیشتری بعد از شروع Sprint اضافه شود:

- تحلیل Initial Commitment دشوارتر می‌شود.
- Predictability کاهش می‌یابد.

---

# Best Practices

✅ Commit را بر اساس Capacity انجام دهید.

✅ از Velocity میانگین استفاده کنید.

✅ Storyهای بزرگ را قبل از Sprint خرد کنید.

✅ از اضافه کردن Storyهای جدید در میانه Sprint خودداری کنید.

---

# اشتباهات رایج

❌ Commit بر اساس خوش‌بینی.

❌ نادیده گرفتن مرخصی‌ها.

❌ Commit بر اساس فشار مدیر.

❌ استفاده از Velocity یک Sprint به‌جای میانگین چند Sprint.

---

# Interview Questions

### Initial Commitment چیست؟

مقدار کاری که تیم در ابتدای Sprint متعهد به انجام آن شده است.

---

### از کجا در Jira مشاهده می‌شود؟

```
Sprint Report
```

---

### اگر Initial Commitment از Capacity بیشتر باشد چه می‌شود؟

احتمال Over Commitment، Carry Over و کاهش Predictability افزایش می‌یابد.

---

### آیا باید پس از شروع Sprint مقدار Commit تغییر کند؟

در Scrum بهتر است فقط در شرایط ضروری تغییر کند.

---

# Summary

| ویژگی | Initial Commitment |
|---------|--------------------|
| زمان ثبت | ابتدای Sprint |
| واحد | Story Point یا Issue |
| محل در Jira | Sprint Report |
| هدف | اندازه‌گیری تعهد اولیه |
| وابسته به | Capacity و Velocity |

---

# Enterprise Tips

## 1. Commit را بر اساس داده انجام دهید.

از میانگین Velocity سه تا شش Sprint اخیر استفاده کنید، نه احساس یا فشار زمانی.

---

## 2. تفاوت Commit و Completion را اندازه بگیرید.

اختلاف زیاد بین Initial Commitment و کار تکمیل‌شده، نشان‌دهنده مشکل در برنامه‌ریزی یا اجرای Sprint است.

---

## 3. Commit را به KPI مدیریتی تبدیل نکنید.

هدف، بهبود برنامه‌ریزی است، نه ارزیابی عملکرد افراد.

---

## 4. Commit را با Capacity تطبیق دهید.

اگر ظرفیت واقعی تیم کاهش یافته است (مرخصی، Incident، Support)، مقدار Commit نیز باید کاهش یابد.

---

## 5. روند Commit را تحلیل کنید.

اگر تیم در Sprintهای متوالی بیش از ظرفیت Commit می‌کند، لازم است فرآیند Sprint Planning بازنگری شود.
