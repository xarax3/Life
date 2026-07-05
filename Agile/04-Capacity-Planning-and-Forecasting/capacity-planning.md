# Capacity Planning

> پایه اصلی Sprint Planning و یکی از مهم‌ترین فعالیت‌های Scrum Master و Product Owner

---

# Definition

Capacity Planning فرآیندی است برای محاسبه میزان واقعی کاری که تیم می‌تواند در یک Sprint انجام دهد.

هدف آن پاسخ به این سؤال است:

> **با توجه به افراد، مرخصی‌ها، جلسات و کارهای غیرتوسعه‌ای، تیم واقعاً چقدر ظرفیت دارد؟**

---

# چرا Capacity Planning مهم است؟

بدون Capacity Planning معمولاً این مشکلات رخ می‌دهد:

- Sprint Over Commitment
- انجام نشدن Storyها
- Carry Over زیاد
- کاهش Predictability
- نارضایتی تیم
- Velocity ناپایدار

---

# تفاوت Capacity و Availability

بسیاری این دو را اشتباه می‌گیرند.

## Availability

مدت زمانی که فرد در شرکت حضور دارد.

مثال:

```
10 Working Days
```

---

## Capacity

مدت زمانی که واقعاً می‌تواند روی Sprint کار کند.

مثال:

```
10 روز

-

جلسات

-

مرخصی

-

Support

=

7.5 روز
```

---

# Capacity در چه واحدی محاسبه می‌شود؟

رایج‌ترین واحدها:

| واحد | کاربرد |
|-------|---------|
| Hours | متداول‌ترین |
| Person Days | رایج در PMO |
| Story Points | برخی تیم‌های Scrum |
| Percentage | برای Dashboard |

---

# مراحل Capacity Planning

```text
Working Days
      │
      ▼
Vacation
      │
      ▼
Public Holidays
      │
      ▼
Meetings
      │
      ▼
Support Tasks
      │
      ▼
Available Capacity
      │
      ▼
Sprint Planning
```

---

# مثال ۱ - محاسبه ظرفیت یک نفر

Sprint:

```
10 Working Days
```

روزانه:

```
8 Hours
```

کل ساعات:

```
80 Hours
```

---

مرخصی:

```
2 Days
```

```
16 Hours
```

جلسات:

```
10 Hours
```

Support:

```
6 Hours
```

ظرفیت واقعی:

```
80

-

16

-

10

-

6

=

48 Hours
```

---

# مثال ۲ - ظرفیت تیم

| عضو | Capacity |
|------|---------:|
| Ali | 48h |
| Sara | 60h |
| Reza | 72h |
| Mina | 56h |

```
Total Capacity

236 Hours
```

---

# Capacity در Scrum

در Sprint Planning ابتدا ظرفیت محاسبه می‌شود.

سپس Product Owner بر اساس این ظرفیت Storyها را انتخاب می‌کند.

ترتیب صحیح:

```
Capacity

↓

Velocity

↓

Sprint Goal

↓

Sprint Backlog
```

---

# Capacity در Kanban

در Kanban ظرفیت ثابت نیست.

به‌جای آن معمولاً از:

- WIP Limit
- Throughput
- Lead Time

برای کنترل جریان استفاده می‌شود.

---

# Capacity در Jira

Jira Software به‌صورت پیش‌فرض Capacity را محاسبه نمی‌کند.

برای این کار معمولاً از ابزارهای زیر استفاده می‌شود:

- Advanced Roadmaps
- Tempo Planner
- BigPicture
- Jira Plans
- افزونه‌های Capacity Planning

---

# محاسبه Capacity بر اساس Story Point

برخی تیم‌ها می‌گویند:

```
Velocity

=

40 SP
```

اگر ظرفیت این Sprint:

```
80%
```

باشد،

برنامه‌ریزی:

```
40

×

0.8

=

32 SP
```

---

# Capacity بر اساس ساعت

فرمول رایج:

```
Capacity

=

Working Hours

-

Non Project Hours
```

---

# Non Project Hours

شامل:

- Daily Scrum
- Sprint Planning
- Sprint Review
- Retrospective
- Support
- Incident
- Training
- Interviews
- Company Meetings

---

# Enterprise Example

تیم:

```
8 Developers
```

Sprint:

```
10 Days
```

```
8 × 10 × 8

=

640 Hours
```

غیبت‌ها:

```
Vacation

40
```

جلسات:

```
48
```

Support:

```
72
```

Capacity

```
640

-

40

-

48

-

72

=

480 Hours
```

---

# Dashboard KPI

Capacity معمولاً کنار این شاخص‌ها نمایش داده می‌شود:

- Velocity
- Sprint Progress
- Burndown
- Predictability
- Resource Utilization

---

# نمودار نمونه

```
Total Hours

640
```

```
Available

480
```

```
Used

455
```

```
Remaining

25
```

---

# Best Practices

✅ ظرفیت را در ابتدای هر Sprint محاسبه کنید.

✅ مرخصی‌ها را از قبل ثبت کنید.

✅ جلسات ثابت را در نظر بگیرید.

✅ زمان پشتیبانی (Support) را فراموش نکنید.

✅ ظرفیت را برای هر عضو تیم جداگانه محاسبه کنید.

---

# Common Mistakes

❌ فرض اینکه همه افراد روزانه ۸ ساعت مفید کار می‌کنند.

❌ نادیده گرفتن جلسات.

❌ نادیده گرفتن Bug Fix و Support.

❌ استفاده از Velocity Sprint قبل بدون در نظر گرفتن تغییر ظرفیت.

---

# نقش‌ها

| نقش | مسئولیت |
|------|----------|
| Scrum Master | محاسبه ظرفیت |
| Product Owner | انتخاب Story متناسب با ظرفیت |
| Team | اعلام مرخصی و محدودیت‌ها |
| Project Manager | نظارت بر ظرفیت کل پروژه |

---

# Interview Questions

### Capacity Planning چیست؟

فرآیند محاسبه توان واقعی تیم برای انجام کار در یک Sprint.

---

### آیا Capacity همان Velocity است؟

خیر.

Capacity توان بالقوه قبل از Sprint است؛ Velocity خروجی واقعی پس از Sprint.

---

### اگر یکی از اعضای کلیدی مرخصی باشد چه می‌کنید؟

- ظرفیت تیم را دوباره محاسبه می‌کنم.
- در صورت نیاز Scope Sprint را کاهش می‌دهم.
- Product Owner را در جریان قرار می‌دهم.

---

### Jira به‌صورت پیش‌فرض Capacity را نمایش می‌دهد؟

خیر.

برای این کار معمولاً از افزونه‌ها یا Advanced Roadmaps استفاده می‌شود.

---

# Summary

| ویژگی | Capacity Planning |
|---------|------------------|
| زمان استفاده | قبل از Sprint |
| هدف | محاسبه توان واقعی تیم |
| واحد | ساعت / روز / Story Point |
| گزارش داخلی Jira | ❌ |
| ابزارهای رایج | Tempo، Advanced Roadmaps، BigPicture |
| نتیجه | برنامه‌ریزی واقع‌بینانه Sprint |

---

# Enterprise Tips

### 1. ظرفیت اسمی و ظرفیت واقعی را جدا کنید.

ظرفیت اسمی:

```
8 نفر × 8 ساعت × 10 روز = 640 ساعت
```

ظرفیت واقعی:

```
640 - مرخصی - جلسات - Support
```

---

### 2. ظرفیت افراد متخصص را جداگانه بررسی کنید.

اگر تنها یک DBA یا QA در تیم دارید، ظرفیت او ممکن است گلوگاه Sprint باشد.

---

### 3. ظرفیت را فقط بر اساس تعداد افراد محاسبه نکنید.

مهارت، تجربه و نقش افراد نیز بر ظرفیت واقعی اثرگذار است.

---

### 4. از داده‌های Sprintهای گذشته استفاده کنید.

اگر تیم در سه Sprint اخیر فقط 75٪ ظرفیت خود را مصرف کرده است، برنامه‌ریزی Sprint بعدی را بر همان اساس انجام دهید.

---

### 5. ظرفیت را در طول Sprint بازبینی کنید.

اگر اتفاقاتی مانند مرخصی اضطراری، Incident بحرانی یا تغییر اولویت رخ داد، Capacity و برنامه Sprint را مجدداً ارزیابی کنید.
