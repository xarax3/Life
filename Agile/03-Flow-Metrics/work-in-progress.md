# Work In Progress (WIP)

> مهم‌ترین شاخص کنترل جریان کار در Kanban

---

# Definition

Work In Progress (WIP) تعداد آیتم‌هایی است که **هم‌زمان** در حال انجام هستند اما هنوز تکمیل نشده‌اند.

نمونه وضعیت‌ها:

- In Progress
- Development
- Code Review
- Testing

این وضعیت‌ها معمولاً جزو WIP محسوب می‌شوند.

---

# Business Purpose

WIP به سوالات زیر پاسخ می‌دهد:

- آیا تیم روی کارهای زیادی هم‌زمان کار می‌کند؟
- آیا احتمال ایجاد گلوگاه وجود دارد؟
- آیا تمرکز تیم مناسب است؟
- آیا فرآیند پایدار است؟

---

# Formula

```
WIP = Number of Active Work Items
```

---

# Example

| Status | Issues |
|---------|-------:|
| In Progress | 8 |
| Code Review | 3 |
| Testing | 4 |

```
WIP = 15
```

---

# WIP Limit

در Kanban معمولاً برای هر ستون محدودیت تعریف می‌شود.

مثال:

| Column | WIP Limit |
|---------|----------:|
| Development | 5 |
| Review | 3 |
| Testing | 4 |

اگر تعداد آیتم‌ها از این مقدار بیشتر شود، تیم باید ابتدا آیتم‌های موجود را تکمیل کند و سپس کار جدید را آغاز کند.

---

# Little's Law

یکی از مهم‌ترین قوانین Flow:

```
Lead Time = WIP / Throughput
```

یا

```
WIP = Throughput × Lead Time
```

این قانون پایه بسیاری از تحلیل‌های Kanban است.

---

# محل در Jira

Jira به‌صورت پیش‌فرض WIP Limit را نمایش نمی‌دهد (مگر در برخی Boardها و تنظیمات Kanban).

برای گزارش‌های پیشرفته معمولاً از:

- Kanban Board
- Dashboard
- Rich Filters
- eazyBI
- ActionableAgile

استفاده می‌شود.

---

# Example

```
Development

████████

(8 Issues)

Limit = 5

❌ Over Limit
```

نتیجه:

اعضای تیم باید از شروع کار جدید خودداری کنند.

---

# اثر WIP بر سایر KPIها

```
WIP ↑

↓

Cycle Time ↑

↓

Lead Time ↑

↓

Customer Satisfaction ↓
```

افزایش بیش از حد WIP تقریباً همیشه باعث کند شدن جریان کار می‌شود.

---

# Interpretation

### WIP پایین

- تمرکز بیشتر
- تحویل سریع‌تر
- کاهش Context Switching

---

### WIP بالا

- چندوظیفگی زیاد
- صف‌های طولانی
- افزایش زمان انتظار
- افزایش احتمال خطا

---

# Dashboard KPI

WIP معمولاً کنار این متریک‌ها نمایش داده می‌شود:

- Cycle Time
- Lead Time
- Throughput
- CFD

---

# Best Practices

✅ برای هر ستون WIP Limit تعیین کنید.

✅ قبل از شروع کار جدید، کارهای نیمه‌تمام را تکمیل کنید.

✅ آیتم‌های Blocked را سریع شناسایی و رفع کنید.

✅ WIP را به‌صورت روزانه در Daily Scrum بررسی کنید.

---

# Common Mistakes

❌ شروع هم‌زمان تعداد زیادی Story

❌ نادیده گرفتن Code Review و Testing در محاسبه WIP

❌ افزایش WIP برای "مشغول نگه داشتن" افراد

---

# Enterprise Example

یک تیم دارای:

- 7 Developer
- 2 QA

است.

بدون WIP Limit، تعداد آیتم‌های فعال به 26 می‌رسد.

پس از اعمال محدودیت:

- Development = 7
- Review = 3
- Testing = 2

نتیجه پس از دو ماه:

- Cycle Time: 11 روز → 6 روز
- Lead Time: 18 روز → 10 روز
- Throughput: 22 → 31 آیتم در Sprint

---

# Interview Questions

### WIP چیست؟

تعداد آیتم‌هایی که هم‌اکنون در حال انجام هستند و هنوز تکمیل نشده‌اند.

---

### چرا WIP Limit مهم است؟

زیرا از چندوظیفگی بیش از حد جلوگیری می‌کند و باعث بهبود جریان کار می‌شود.

---

### ارتباط WIP با Cycle Time چیست؟

در اغلب موارد، افزایش WIP باعث افزایش Cycle Time و Lead Time می‌شود.

---

# Summary

| ویژگی | WIP |
|--------|-----|
| واحد | تعداد آیتم |
| هدف | کنترل حجم کار هم‌زمان |
| مهم برای | Kanban |
| قانون مرتبط | Little's Law |
| بهتر است | تا حد امکان پایین و متعادل |
