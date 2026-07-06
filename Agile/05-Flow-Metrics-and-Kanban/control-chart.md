# Control Chart

> یکی از مهم‌ترین Kanban Reports در Jira که توزیع Cycle Time و Lead Time را برای تحلیل پایداری فرآیند و شناسایی Outlierها نمایش می‌دهد.

---

# Definition

Control Chart نموداری است که نشان می‌دهد:

> هر آیتم چقدر زمان برده تا تکمیل شود و این زمان در طول زمان چگونه تغییر کرده است.

---

# ساختار Control Chart

- محور X → زمان (Completion Date)
- محور Y → Cycle Time یا Lead Time
- نقاط → هر Issue

---

# هدف Control Chart

Control Chart به این سؤال‌ها پاسخ می‌دهد:

- آیا فرآیند پایدار است؟
- آیا نوسان داریم؟
- آیا Outlier داریم؟
- چقدر می‌توان پیش‌بینی کرد؟

---

# مثال ساده

```
Issue A → 3 days
Issue B → 4 days
Issue C → 12 days
Issue D → 5 days
Issue E → 20 days
```

---

# تحلیل Control Chart

## 1. Cluster

اگر نقاط نزدیک هم باشند:

```
Flow پایدار
```

---

## 2. Scatter

اگر نقاط پراکنده باشند:

```
Flow ناپایدار
```

---

## 3. Outlier

نقاط بسیار دور:

```
Delay یا Blocker
```

---

# خطوط در Control Chart

## Mean Line

میانگین Cycle Time

---

## Percentile Lines

مثلاً:

- 50%
- 85%
- 
