# Scatter Plot (Cycle Time Scatter Plot)

> یکی از مهم‌ترین Flow Analysis Chartها در Kanban که توزیع Cycle Time یا Lead Time را در طول زمان به‌صورت نقاط مستقل نمایش می‌دهد.

---

# Definition

Scatter Plot در Jira نشان می‌دهد:

> هر آیتم چقدر طول کشیده تا Done شود و این زمان در چه تاریخی اتفاق افتاده است.

---

# ساختار نمودار

- محور X → زمان (Completion Date)
- محور Y → Cycle Time یا Lead Time
- هر نقطه → یک Issue

---

# هدف Scatter Plot

Scatter Plot به این سؤال‌ها پاسخ می‌دهد:

- آیا Cycle Time پایدار است؟
- آیا Outlier داریم؟
- آیا روند بهبود یا بدتر شدن داریم؟
- آیا Forecast قابل اعتماد است؟

---

# مثال ساده

```
Issue A → 3 days
Issue B → 4 days
Issue C → 5 days
Issue D → 15 days
Issue E → 2 days
```

---

# تحلیل Scatter Plot

## 1. خوشه‌ها (Clusters)

اگر نقاط نزدیک هم باشند:

```
Flow پایدار
```

---

## 2. پراکندگی زیاد

اگر نقاط پخش باشند:

```
Flow ناپایدار
```

---

## 3. Outlierها

نقاط بسیار بالا:

```
Blocker / Rework / Scope Change
```

---

# Scatter Plot vs Control Chart

| Scatter Plot | Control Chart |
|--------------|---------------|
| دید کلی | تحلیل دقیق‌تر |
| بدون خطوط آماری | دارای Percentile |
| ساده‌تر | پیشرفته‌تر |

---

# کاربرد در Forecast

Scatter Plot به شما کمک می‌کند:

- 50th percentile
- 85th percentile
- 95th percentile

را استخراج کنید.

---

# مثال Percentile

```
50% → 4 days
85% → 8 days
95% → 15 days
```

---

# Scatter Plot در Jira

مسیر:

```
Board → Reports → Control Chart
```

(Scatter Plot و Control Chart معمولاً در یک بخش ارائه می‌شوند)

---

# کاربردها

- تحلیل Cycle Time
- بررسی نوسان Flow
- شناسایی Outlier
- Forecasting
- SLE Definition

---

# Scatter Plot و Predictability

اگر نقاط:

- نزدیک هم باشند → Predictable
- پراکنده باشند → Unpredictable

---

# Scatter Plot و WIP

WIP بالا معمولاً باعث:

- افزایش پراکندگی
- افزایش Outlier
- افزایش Cycle Time

---

# الگوهای رایج

## 1. Stable Flow

```
نقاط نزدیک + بدون Outlier
```

---

## 2. Risky Flow

```
چند نقطه بسیار بالا
```

---

## 3. Unstable Flow

```
پراکندگی شدید
```

---

# Scatter Plot و Little’s Law

اگر:

```
WIP ↑
Throughput ثابت
```

نتیجه:

```
Cycle Time ↑
پراکندگی ↑
```

---

# اشتباهات رایج

❌ استفاده بدون تحلیل Percentile

❌ نادیده گرفتن Outlierها

❌ تحلیل فقط میانگین

❌ عدم تفکیک Issue Type

---

# Interview Questions

### Scatter Plot چیست؟

نموداری برای نمایش توزیع Cycle Time یا Lead Time در طول زمان.

---

### Scatter Plot چه چیزی را نشان می‌دهد؟

پایداری یا ناپایداری Flow و وجود Outlierها.

---

### تفاوت Scatter Plot و Control Chart چیست؟

Scatter Plot ساده‌تر است و Control Chart شامل خطوط آماری و Percentile است.

---

### چرا Scatter Plot مهم است؟

برای تحلیل توزیع زمان تحویل و پیش‌بینی دقیق‌تر.

---

# Summary

| ویژگی | Scatter Plot |
|--------|--------------|
| نوع | Distribution Chart |
| داده | Cycle/Lead Time |
| هدف | تحلیل پراکندگی |
| ابزار Jira | Control Chart Report |

---

# Enterprise Tips

## 1. به Outlierها حساس باشید

حتی یک نقطه بزرگ می‌تواند Forecast را خراب کند.

---

## 2. به جای Average از Percentile استفاده کنید

به‌خصوص 85% برای SLE.

---

## 3. Scatter Plot را در بازه زمانی تحلیل کنید

هفته‌ای یا ماهانه.

---

## 4. Trend مهم‌تر از نقطه است

به تغییرات زمان توجه کنید.

---

## 5. Scatter Plot را با CFD ترکیب کنید

برای تحلیل کامل Flow System.
