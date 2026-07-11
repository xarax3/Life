# Aging Chart

> یکی از مهم‌ترین Kanban Charts که نشان می‌دهد آیتم‌های باز (In Progress / WIP) چند روز است در جریان کار باقی مانده‌اند و کدام آیتم‌ها در خطر تأخیر هستند.

---

# Definition

Aging Chart نشان می‌دهد:

> هر آیتمی که هنوز Done نشده، چند روز از شروع کار یا ورود به workflow گذشته است.

---

# هدف

Aging Chart به این سؤال پاسخ می‌دهد:

> **کدام آیتم‌ها در حال حاضر در خطر تأخیر یا گیر کردن هستند؟**

---

# تفاوت با Work Item Age

| Aging Chart | Work Item Age |
|-------------|---------------|
| Visual chart | Metric |
| روی Board | عددی |
| تمرکز روی WIP | تمرکز روی هر آیتم |

---

# ساختار Aging Chart

- هر آیتم یک خط یا bar دارد
- طول bar = مدت زمان در WIP
- رنگ‌ها = وضعیت ریسک

---

# مثال ساده

```
Story A → 2 days (Green)
Story B → 5 days (Yellow)
Story C → 10 days (Red)
Story D → 1 day (Green)
```

---

# هدف اصلی

Aging Chart برای:

- پیش‌بینی Delay قبل از وقوع
- مدیریت WIP
- جلوگیری از Aging بیش از حد
- کنترل Flow

---

# Thresholdها

| وضعیت | سن آیتم |
|--------|----------|
| Green | < 3 days |
| Yellow | 3–7 days |
| Red | > 7 days |

---

# Aging Chart در Jira

در Jira:

- به‌صورت مستقیم Aging Chart استاندارد ندارد
- معمولاً با:
  - Jira Dashboard Gadgets
  - Filters + JQL
  - Plugins (ActionableAgile, eazyBI)

پیاده‌سازی می‌شود

---

# JQL نمونه

```
statusCategory != Done
```

یا:

```
status != Done
AND created <= -5d
```

---

# کاربرد Aging Chart

- شناسایی bottleneck
- مدیریت WIP
- کنترل SLA
- جلوگیری از stuck items

---

# Aging Chart vs Control Chart

| Aging Chart | Control Chart |
|-------------|---------------|
| Real-time WIP | Historical data |
| Current risk | Past performance |
| Per item | Distribution |

---

# Aging Chart vs CFD

| Aging Chart | CFD |
|-------------|-----|
| Focus on items | Focus on system |
| Real-time | Historical |
| Risk detection | Flow analysis |

---

# مثال واقعی

```
WIP:
- Story A → 1 day
- Story B → 3 days
- Story C → 8 days
- Story D → 12 days
```

تحلیل:

- C و D در خطر
- احتمال افزایش Cycle Time آینده

---

# اثر Aging بر Flow

اگر Aging افزایش یابد:

- Cycle Time افزایش می‌یابد
- Throughput کاهش می‌یابد
- Predictability کاهش می‌یابد

---

# رابطه با WIP

```
WIP ↑ → Aging ↑ → Lead Time ↑
```

---

# استفاده در Kanban

Aging Chart یکی از مهم‌ترین ابزارهای:

- Flow Management
- WIP Control
- Risk Detection

---

# بهترین Practiceها

## 1. Daily Review

Aging Chart باید روزانه بررسی شود.

---

## 2. Define SLA

برای هر نوع کار threshold مشخص کنید.

---

## 3. Focus on Red Items

قرمزها بیشترین ریسک را دارند.

---

## 4. Combine with WIP

Aging بدون WIP معنی ندارد.

---

## 5. Don’t use for Performance

برای افراد استفاده نشود.

---

# اشتباهات رایج

❌ نگاه فقط به میانگین Aging

❌ نادیده گرفتن Red items

❌ استفاده بدون WIP limit

❌ عدم تعریف SLA

---

# Interview Questions

### Aging Chart چیست؟

نموداری که نشان می‌دهد آیتم‌های باز چند روز در جریان کار هستند.

---

### تفاوت Aging Chart و Work Item Age چیست؟

Aging Chart بصری است، Work Item Age عددی.

---

### چرا Aging مهم است؟

چون قبل از تأخیر واقعی هشدار می‌دهد.

---

### چگونه Aging را کاهش می‌دهید؟

- کاهش WIP
- رفع Blockerها
- کوچک‌سازی Storyها

---

# Summary

| ویژگی | Aging Chart |
|--------|-------------|
| نوع | Visual Flow Chart |
| هدف | Risk Detection |
| تمرکز | Items in progress |
| ابزار Jira | Plugins / Filters |

---

# Enterprise Tips

## 1. Red items = immediate action

---

## 2. Aging growth = future delay

---

## 3. Use alongside CFD and Control Chart

---

## 4. Keep WIP low for better Aging control

---

## 5. Aging is early warning system

نه گزارش عملکرد.
