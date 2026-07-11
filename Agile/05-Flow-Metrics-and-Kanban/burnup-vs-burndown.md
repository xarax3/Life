# Burnup vs Burndown Chart

> دو مورد از مهم‌ترین گزارش‌های Agile در Jira که برای اندازه‌گیری پیشرفت پروژه استفاده می‌شوند، اما کاربرد، نحوه نمایش داده‌ها و اهداف متفاوتی دارند.

---

# مقدمه

هر دو نمودار برای پاسخ به یک سؤال طراحی شده‌اند:

> **آیا پروژه طبق برنامه در حال پیشرفت است؟**

اما هر کدام از زاویه‌ای متفاوت به این سؤال پاسخ می‌دهند.

---

# Burndown Chart چیست؟

Burndown نشان می‌دهد:

> چه مقدار کار **باقی مانده است**.

تمرکز آن روی **کار باقی‌مانده (Remaining Work)** است.

---

# Burnup Chart چیست؟

Burnup نشان می‌دهد:

> چه مقدار کار **انجام شده است**.

تمرکز آن روی **کار تکمیل‌شده (Completed Work)** است.

---

# تفاوت اصلی

```
Burndown

Remaining Work ↓
```

```
Burnup

Completed Work ↑
```

---

# مقایسه کلی

| ویژگی | Burndown | Burnup |
|--------|----------|---------|
| نمایش کار باقی‌مانده | ✅ | ❌ |
| نمایش کار انجام‌شده | ❌ | ✅ |
| نمایش تغییر Scope | ❌ | ✅ |
| مناسب برای Sprint | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ |
| مناسب برای Release | ⭐⭐⭐ | ⭐⭐⭐⭐⭐ |
| مناسب برای پروژه‌های ثابت | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ |
| مناسب برای Scope متغیر | ⭐⭐ | ⭐⭐⭐⭐⭐ |

---

# ساختار Burndown

```
Remaining Story Points

100 |
 80 |
 60 |
 40 |
 20 |
  0 +-------------------
      Time
```

خط باید به سمت صفر حرکت کند.

---

# ساختار Burnup

```
Story Points

120 |---------------- Scope
100 |
 80 |          /
 60 |        /
 40 |      /
 20 |    /
  0 +-------------------
      Time
```

خط انجام‌شده باید به Scope برسد.

---

# تحلیل Burndown

اگر خط:

- بالاتر از Ideal باشد → تیم عقب است.
- پایین‌تر باشد → تیم جلوتر است.

---

# تحلیل Burnup

اگر:

Completed Line

به Scope نزدیک شود:

```
پروژه در حال پیشرفت است.
```

اگر:

Scope بالا برود:

```
Scope Creep
```

---

# Scope Change

## Burndown

تقریباً قابل مشاهده نیست.

---

## Burnup

کاملاً مشخص است.

مثال:

```
Sprint 1

100 SP
```

```
Sprint 2

120 SP
```

Scope Line بالا می‌رود.

---

# Forecast

| نمودار | Forecast |
|---------|----------|
| Burndown | متوسط |
| Burnup | بسیار مناسب |

---

# کاربرد در Jira

Burndown:

```
Board

↓

Reports

↓

Burndown Chart
```

---

Burnup:

```
Board

↓

Reports

↓

Burnup Chart
```

---

# ارتباط با Velocity

هر دو نمودار از Velocity تأثیر می‌گیرند.

اما:

Burnup تغییر Scope را نیز لحاظ می‌کند.

---

# ارتباط با Capacity

اگر Capacity کاهش پیدا کند:

- Burndown کندتر می‌شود.
- Burnup شیب کمتری پیدا می‌کند.

---

# ارتباط با Sprint

Burndown بهترین گزینه برای:

```
Sprint Tracking
```

است.

---

# ارتباط با Release

Burnup بهترین گزینه برای:

```
Release Planning
```

است.

---

# مزایای Burndown

- ساده
- قابل فهم
- مناسب Daily Scrum
- مناسب Sprint

---

# معایب Burndown

- عدم نمایش Scope Change
- امکان برداشت اشتباه از علت تأخیر
- مناسب نبودن برای پروژه‌های پویا

---

# مزایای Burnup

- نمایش Scope
- مناسب Forecast
- مناسب Release
- مناسب مدیریت محصول

---

# معایب Burnup

- نسبت به Burndown پیچیده‌تر است.
- برای Sprintهای کوتاه همیشه ضروری نیست.

---

# مثال واقعی

Sprint 1

```
Scope = 100

Done = 20
```

Sprint 2

```
Scope = 120

Done = 45
```

Burndown:

```
تنها افزایش Remaining Work را نشان می‌دهد.
```

Burnup:

```
هم پیشرفت تیم را نشان می‌دهد.

هم افزایش Scope را.
```

---

# کدام را انتخاب کنیم؟

| سناریو | بهترین گزارش |
|---------|--------------|
| Daily Scrum | Burndown |
| Sprint Review | Burndown + Burnup |
| Release Planning | Burnup |
| Executive Dashboard | Burnup |
| Scope ثابت | Burndown |
| Scope متغیر | Burnup |

---

# اشتباهات رایج

❌ استفاده از Burndown برای پروژه‌های دارای Scope متغیر

❌ تحلیل Burnup بدون بررسی Velocity

❌ استفاده از این نمودارها برای ارزیابی عملکرد افراد

---

# Interview Questions

### تفاوت Burnup و Burndown چیست؟

Burndown کار باقی‌مانده را نمایش می‌دهد، Burnup کار تکمیل‌شده و تغییرات Scope را.

---

### کدام برای Release مناسب‌تر است؟

Burnup Chart.

---

### کدام برای Sprint مناسب‌تر است؟

Burndown Chart.

---

### چرا Burnup برای مدیران بهتر است؟

زیرا هم پیشرفت پروژه و هم تغییرات دامنه پروژه را به‌صورت هم‌زمان نمایش می‌دهد.

---

# Summary

| ویژگی | Burndown | Burnup |
|--------|----------|---------|
| Remaining Work | ✅ | ❌ |
| Completed Work | ❌ | ✅ |
| Scope Change | ❌ | ✅ |
| Sprint | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ |
| Release | ⭐⭐⭐ | ⭐⭐⭐⭐⭐ |
| Forecast | متوسط | عالی |

---

# Enterprise Tips

## 1. برای Sprint از Burndown استفاده کنید.

---

## 2. برای Release از Burnup استفاده کنید.

---

## 3. در Executive Dashboard همیشه Burnup را قرار دهید.

---

## 4. اگر Scope پروژه مرتب تغییر می‌کند، Burnup انتخاب اول است.

---

## 5. بهترین روش در سازمان‌های Enterprise

نمایش هر دو نمودار در کنار هم است.

Burndown وضعیت اجرای Sprint را نشان می‌دهد و Burnup تصویر کامل‌تری از وضعیت پروژه و تغییرات Scope ارائه می‌کند.
