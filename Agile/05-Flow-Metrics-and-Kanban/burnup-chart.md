# Burnup Chart

> یکی از مهم‌ترین گزارش‌های Agile که میزان پیشرفت واقعی پروژه را در مقایسه با کل Scope نمایش می‌دهد.

---

# Definition

Burnup Chart نموداری است که نشان می‌دهد:

- چه مقدار کار تکمیل شده است.
- چه مقدار Scope کل پروژه است.
- Scope در طول زمان چگونه تغییر کرده است.

برخلاف Burndown، در Burnup تغییرات Scope به وضوح دیده می‌شود.

---

# هدف

Burnup به این سؤال‌ها پاسخ می‌دهد:

- تیم چقدر پیشرفت کرده است؟
- آیا Scope پروژه تغییر کرده است؟
- آیا Release در زمان مقرر انجام می‌شود؟
- آیا Velocity برای تکمیل Scope کافی است؟

---

# ساختار نمودار

Burnup معمولاً دو خط دارد:

### Scope Line

کل حجم کار پروژه

---

### Completed Work Line

کار انجام‌شده

---

نمایش ساده:

```
Story Points

100 |---------------- Scope
 90 |
 80 |
 70 |
 60 |            /
 50 |          /
 40 |        /
 30 |      /
 20 |    /
 10 |  /
  0 +----------------------
       Time
```

---

# تفاوت خطوط

## Scope Line

این خط نشان‌دهنده:

```
Total Story Points
```

اگر Scope افزایش پیدا کند، این خط نیز بالا می‌رود.

---

## Completed Line

این خط نشان‌دهنده:

```
Completed Story Points
```

هر Sprint این خط افزایش پیدا می‌کند.

---

# مثال

Sprint 1

```
Scope = 100

Done = 20
```

Sprint 2

```
Scope = 110

Done = 45
```

Sprint 3

```
Scope = 120

Done = 70
```

به راحتی مشاهده می‌شود که علاوه بر پیشرفت تیم، Scope نیز افزایش یافته است.

---

# مزیت اصلی Burnup

نمایش همزمان:

- پیشرفت
- تغییر Scope

به همین دلیل برای پروژه‌هایی که Scope ثابت نیست بسیار مناسب است.

---

# Burnup در Jira

در Jira Software:

```
Reports

↓

Burnup Chart
```

این گزارش برای پروژه‌های Scrum در دسترس است.

---

# داده‌های موردنیاز

Burnup بر اساس:

- Story Points
- Issue Count
- Sprint Completion

محاسبه می‌شود.

---

# تفسیر نمودار

### حالت مطلوب

Completed Line به‌صورت یکنواخت به Scope نزدیک می‌شود.

---

### Scope Creep

اگر Scope Line مدام بالا برود:

```
Scope ↑

Done ثابت
```

یعنی پروژه در حال افزایش دامنه است.

---

### Velocity پایین

اگر:

Completed Line تقریباً افقی شود:

```
Velocity ↓
```

---

### اتمام پروژه

وقتی:

```
Completed Line

=

Scope Line
```

پروژه تکمیل شده است.

---

# Burnup و Forecast

اگر:

Average Velocity

```
20 SP / Sprint
```

Remaining

```
40 SP
```

Forecast

```
2 Sprint
```

---

# Burnup و Velocity

Burnup مستقیماً تحت تأثیر Velocity قرار دارد.

Velocity بیشتر:

```
شیب بیشتر Completed Line
```

---

# Burnup و Capacity

اگر Capacity کاهش یابد:

- Velocity کاهش می‌یابد.
- شیب Burnup کمتر می‌شود.

---

# Burnup و Release

Burnup بهترین ابزار برای:

```
Release Forecast
```

است.

---

# Burnup و Scope Creep

یکی از مهم‌ترین کاربردهای Burnup:

تشخیص Scope Creep

مثال:

```
Sprint 1

100 SP
```

```
Sprint 2

125 SP
```

```
Sprint 3

140 SP
```

بدون Burnup ممکن است علت تأخیر به اشتباه عملکرد تیم تصور شود، در حالی که مشکل افزایش Scope است.

---

# Burnup vs Velocity Chart

| Burnup | Velocity |
|---------|----------|
| پیشرفت پروژه | خروجی Sprint |
| روند کلی | هر Sprint |
| مناسب برای مدیریت | مناسب برای تیم |

---

# KPIهای مرتبط

- Velocity
- Capacity
- Release Forecast
- Scope Change
- Sprint Progress

---

# اشتباهات رایج

❌ نادیده گرفتن تغییرات Scope

❌ استفاده بدون Velocity

❌ تحلیل بدون Capacity

❌ استفاده برای ارزیابی عملکرد فردی

---

# Interview Questions

### Burnup Chart چیست؟

نموداری که پیشرفت واقعی پروژه را در برابر Scope کل نمایش می‌دهد.

---

### مزیت Burnup نسبت به Burndown چیست؟

تغییرات Scope را نیز نمایش می‌دهد.

---

### چه زمانی Burnup بهتر است؟

وقتی Scope پروژه در طول زمان تغییر می‌کند.

---

### Burnup در Jira کجاست؟

```
Board

↓

Reports

↓

Burnup Chart
```

---

# Summary

| ویژگی | Burnup |
|--------|---------|
| نوع | Progress Report |
| نمایش Scope | ✅ |
| نمایش Completed Work | ✅ |
| Forecast | عالی |
| ابزار Jira | Scrum Reports |

---

# Enterprise Tips

## 1. همیشه Burnup را همراه Velocity تحلیل کنید.

---

## 2. افزایش Scope را از کاهش Velocity تفکیک کنید.

---

## 3. Burnup بهترین گزارش برای مدیران پروژه و Product Owner است.

---

## 4. برای Release Planning از Burnup استفاده کنید.

---

## 5. Burnup را در Sprint Review بررسی کنید.

---

# مثال کامل

فرض کنید:

| Sprint | Scope | Done |
|--------|------:|-----:|
| 1 | 100 | 20 |
| 2 | 110 | 45 |
| 3 | 120 | 70 |
| 4 | 120 | 95 |
| 5 | 120 | 120 |

تحلیل:

- Sprint 2: Scope افزایش یافته است.
- Sprint 3 و 4: تیم با Velocity مناسب در حال جبران افزایش Scope است.
- Sprint 5: پروژه با تکمیل تمام Scope به پایان رسیده است.

این نمودار به مدیر پروژه کمک می‌کند بین **کندی تیم** و **افزایش دامنه پروژه** تمایز قائل شود؛ موضوعی که در Burndown Chart به این وضوح قابل مشاهده نیست.
