# Work Item Age

> یکی از مهم‌ترین Flow Metrics که نشان می‌دهد یک آیتم باز (Open) چند روز یا چند ساعت است در جریان کار قرار دارد.

---

# Definition

Work Item Age یعنی:

> مدت زمانی که یک آیتم از لحظه ورود به وضعیت "In Progress" تا همین لحظه در حال سپری کردن زمان است (اگر هنوز Done نشده باشد).

```
Work Item Age

=

Now

-

Start Date (In Progress)
```

---

# هدف

Work Item Age به این سؤال پاسخ می‌دهد:

> **چه آیتم‌هایی در حال حاضر در خطر تأخیر هستند؟**

---

# تفاوت با Cycle Time

| Work Item Age | Cycle Time |
|---------------|------------|
| آیتم‌های هنوز باز | آیتم‌های Done |
| لحظه‌ای (Real-time) | تاریخی |
| پیش‌بینی ریسک | تحلیل گذشته |

---

# مثال ساده

```
Story A → 2 days in progress
Story B → 5 days in progress
Story C → 12 days in progress
```

---

# اهمیت Work Item Age

این Metric یکی از مهم‌ترین ابزارهای:

- پیشگیری از Delay
- شناسایی Bottleneck
- مدیریت WIP
- کنترل جریان کار

است.

---

# چرا مهم‌تر از Cycle Time است؟

Cycle Time گذشته را نشان می‌دهد.

Work Item Age آینده را هشدار می‌دهد.

---

# مثال عملی

فرض کنید:

| Item | Age |
|------|-----|
| A | 2 days |
| B | 4 days |
| C | 10 days |
| D | 1 day |

اگر SLE تیم:

```
85% = 6 days
```

آیتم C در وضعیت خطر قرار دارد.

---

# Work Item Age در Jira

Jira به‌صورت پیش‌فرض:

- Aging Chart (در برخی پروژه‌ها)
- Filter + JQL

ارائه می‌دهد.

---

# JQL نمونه

آیتم‌های باز:

```
status != Done
```

آیتم‌های قدیمی:

```
status != Done

AND

updated <= -5d
```

---

# Aging Threshold

معمولاً تیم‌ها threshold تعریف می‌کنند:

| وضعیت | سن آیتم |
|--------|----------|
| سبز | < 3 روز |
| زرد | 3–7 روز |
| قرمز | > 7 روز |

---

# Work Item Age vs Lead Time

| Lead Time | Work Item Age |
|-----------|---------------|
| گذشته | حال |
| تحویل شده | در حال انجام |
| تجربه مشتری | ریسک تیم |

---

# Work Item Age vs Cycle Time

Cycle Time:

```
Done analysis
```

Work Item Age:

```
Still in progress
```

---

# Flow Insight

اگر Work Item Age افزایش یابد:

- Cycle Time آینده افزایش خواهد یافت
- Lead Time بدتر خواهد شد
- Forecast دقت خود را از دست می‌دهد

---

# مثال واقعی

```
Story A → 1 day
Story B → 3 days
Story C → 6 days
Story D → 9 days
```

تحلیل:

- D در Risk Zone
- C نزدیک Risk Zone
- نیاز به کاهش WIP

---

# ارتباط با WIP

```
WIP ↑

→ Work Item Age ↑

→ Cycle Time ↑
```

---

# استفاده در Kanban

Work Item Age یکی از اصلی‌ترین ابزارهای کنترل Flow است.

هدف:

> جلوگیری از “کارهای گیر کرده”

---

# داشبورد Work Item Age

معمولاً شامل:

- Average Age
- Max Age
- Aging Distribution
- Blocked Items
- Items > SLA

---

# Flow Signal

Work Item Age یک Signal است نه KPI صرف.

یعنی:

> هشدار زودهنگام قبل از مشکل واقعی

---

# بهترین کاربردها

- شناسایی کارهای گیر کرده
- کنترل WIP
- جلوگیری از Delay
- بهبود Flow

---

# اشتباهات رایج

❌ استفاده برای ارزیابی افراد

❌ تمرکز فقط روی Average

❌ نادیده گرفتن Blockers

❌ عدم تعریف threshold

---

# Interview Questions

### Work Item Age چیست؟

مدت زمانی که یک آیتم در وضعیت فعال (In Progress) قرار دارد و هنوز تکمیل نشده است.

---

### تفاوت Work Item Age و Cycle Time چیست؟

Work Item Age مربوط به آیتم‌های باز است، Cycle Time مربوط به آیتم‌های تمام شده.

---

### چرا Work Item Age مهم است؟

چون به‌عنوان هشدار زودهنگام برای تأخیر استفاده می‌شود.

---

### چگونه Work Item Age را کاهش می‌دهید؟

- کاهش WIP
- رفع Blockerها
- کوچک‌سازی Storyها
- بهبود Flow

---

# Summary

| ویژگی | Work Item Age |
|--------|---------------|
| نوع | Real-time Metric |
| تمرکز | آیتم‌های باز |
| هدف | هشدار تأخیر |
| کاربرد | Kanban Flow Control |
| ابزار Jira | Aging Chart / Filter |

---

# Enterprise Tips

## 1. Work Item Age را روزانه بررسی کنید

این Metric برای مانیتورینگ روزانه طراحی شده است.

---

## 2. Threshold تعریف کنید

بدون Threshold، این Metric بی‌معنی است.

---

## 3. به Long Age Items توجه ویژه کنید

چند آیتم قدیمی معمولاً ریشه اصلی مشکل Flow هستند.

---

## 4. Work Item Age را با WIP ترکیب کنید

افزایش WIP معمولاً مستقیماً باعث افزایش Age می‌شود.

---

## 5. از آن برای پیش‌بینی استفاده کنید

Work Item Age می‌تواند اولین نشانه افزایش Lead Time آینده باشد.
