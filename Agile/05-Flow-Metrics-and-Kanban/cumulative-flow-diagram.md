# Cumulative Flow Diagram (CFD)

> یکی از مهم‌ترین Kanban Charts که وضعیت جریان کار (Flow) را در طول زمان و به‌صورت تجمعی نمایش می‌دهد.

---

# Definition

CFD یک نمودار است که نشان می‌دهد:

> تعداد آیتم‌ها در هر وضعیت (To Do, In Progress, Review, Done) در طول زمان چگونه تغییر کرده است.

---

# ساختار CFD

CFD شامل لایه‌های زیر است:

- Backlog / To Do
- In Progress
- Review / Testing
- Done

هر لایه به‌صورت تجمعی نمایش داده می‌شود.

---

# هدف CFD

CFD به این سؤال‌ها پاسخ می‌دهد:

- کارها کجا گیر کرده‌اند؟
- آیا WIP در حال افزایش است؟
- آیا Flow پایدار است؟
- آیا Bottleneck داریم؟
- آیا Delivery قابل پیش‌بینی است؟

---

# ظاهر CFD

```
Done        ██████████████████
Review      ████████████
In Progress ████████
To Do       █████████████████████
```

---

# تحلیل CFD

## 1. شیب (Slope)

- شیب Done = Throughput
- شیب زیاد = تحویل سریع

---

## 2. فاصله بین لایه‌ها

- فاصله زیاد = WIP بالا
- فاصله کم = Flow سالم

---

## 3. انحناها

- برآمدگی در In Progress = Bottleneck
- رشد سریع To Do = Backlog growth

---

# مثال واقعی

### وضعیت سالم

- خطوط صاف
- فاصله کم بین ستون‌ها
- رشد یکنواخت Done

---

### وضعیت ناسالم

- In Progress در حال افزایش
- Done ثابت
- To Do در حال رشد

---

# CFD و Little’s Law

CFD به‌صورت بصری نشان می‌دهد:

```
WIP = Throughput × Cycle Time
```

---

# CFD در Jira

در Jira:

- CFD در Kanban Board Reports وجود دارد
- در Scrum هم قابل مشاهده است

مسیر:

```
Board → Reports → Cumulative Flow Diagram
```

---

# کاربرد CFD

- تحلیل Flow تیم
- شناسایی Bottleneck
- بررسی WIP
- بررسی Stability سیستم
- Forecasting

---

# Bottleneck در CFD

اگر یک لایه:

```
In Progress ↑↑↑
```

و بعد:

```
Done → flat
```

یعنی:

> Bottleneck در مرحله بعدی وجود دارد

---

# CFD و WIP

اگر فاصله بین خطوط زیاد شود:

```
WIP ↑
Cycle Time ↑
Flow Efficiency ↓
```

---

# CFD و Predictability

CFD پایدار یعنی:

- Flow پایدار
- Forecast قابل اعتماد
- Variation کم

---

# CFD vs Burnup

| CFD | Burnup |
|-----|--------|
| Flow view | Progress view |
| وضعیت سیستم | پیشرفت پروژه |
| Kanban | Scrum |

---

# CFD vs Burndown

| CFD | Burndown |
|-----|----------|
| چند لایه | یک خط |
| Flow-based | Sprint-based |

---

# الگوهای CFD

## 1. Healthy Flow

- خطوط موازی
- شیب ثابت

---

## 2. Bottleneck Pattern

- یک لایه متورم

---

## 3. Unstable Flow

- خطوط موج‌دار
- نوسان زیاد

---

## 4. Backlog Explosion

- To Do در حال رشد

---

# KPIهایی که از CFD استخراج می‌شوند

- Throughput
- WIP
- Cycle Time (تقریبی)
- Bottleneck detection
- Flow stability

---

# اشتباهات رایج

❌ استفاده بدون تحلیل روند

❌ نگاه فقط به یک روز

❌ نادیده گرفتن لایه‌ها

❌ تفسیر بدون WIP context

---

# Interview Questions

### CFD چیست؟

نموداری تجمعی برای نمایش وضعیت جریان کار در طول زمان.

---

### CFD چه چیزی را نشان می‌دهد؟

توزیع آیتم‌ها در مراحل مختلف workflow.

---

### مهم‌ترین کاربرد CFD چیست؟

شناسایی Bottleneck و تحلیل Flow.

---

### CFD چگونه به Forecast کمک می‌کند؟

با نمایش Throughput و WIP در طول زمان.

---

# Summary

| ویژگی | CFD |
|--------|-----|
| نوع | Flow Chart |
| هدف | تحلیل سیستم |
| داده | تجمعی |
| ابزار Jira | Kanban Reports |
| کاربرد | Bottleneck + Forecast |

---

# Enterprise Tips

## 1. خطوط CFD باید موازی باشند

عدم موازی بودن = عدم پایداری Flow

---

## 2. رشد WIP خطرناک است

In Progress رو به رشد = هشدار جدی

---

## 3. Done باید یکنواخت رشد کند

نوسان در Done = ناپایداری Throughput

---

## 4. CFD بهترین ابزار برای Kanban Coaching است

چون کل سیستم را یکجا نشان می‌دهد.

---

## 5. CFD را روزانه نگاه نکنید

به Trend هفتگی نگاه کنید، نه لحظه‌ای.
