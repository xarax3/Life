# Throughput

> میزان خروجی واقعی تیم در یک بازه زمانی

---

# Definition

Throughput تعداد Work Itemهایی است که در یک بازه زمانی مشخص به وضعیت Done رسیده‌اند.

برخلاف Velocity که بر اساس Story Point اندازه‌گیری می‌شود، Throughput فقط تعداد آیتم‌های تکمیل‌شده را محاسبه می‌کند.

---

# Business Purpose

Throughput به این سوالات پاسخ می‌دهد:

- تیم در هر هفته یا Sprint چند آیتم تکمیل می‌کند؟
- روند خروجی تیم چگونه است؟
- آیا توان تحویل افزایش یافته است؟
- آیا می‌توان زمان تحویل Featureهای آینده را پیش‌بینی کرد؟

---

# Formula

```
Throughput = Number of Completed Work Items
```

---

# Example

| Sprint | Completed Issues |
|---------|-----------------:|
| Sprint 1 | 28 |
| Sprint 2 | 31 |
| Sprint 3 | 29 |
| Sprint 4 | 30 |

Average Throughput

```
(28+31+29+30)/4

=

29.5 Issues
```

---

# Throughput vs Velocity

| Throughput | Velocity |
|------------|----------|
| تعداد آیتم | Story Point |
| Kanban | Scrum |
| مستقل از Estimation | وابسته به Estimation |
| مناسب Continuous Flow | مناسب Sprint |

---

# محل در Jira

به‌صورت مستقیم گزارش ندارد.

قابل استخراج از:

- Dashboard Gadgets
- JQL + Filter
- eazyBI
- ActionableAgile
- Custom Charts

---

# JQL نمونه

Issueهای Done در Sprint جاری:

```sql
status = Done
AND Sprint in openSprints()
```

Issueهای Done در ۳۰ روز اخیر:

```sql
status = Done
AND resolved >= -30d
```

---

# Interpretation

### Throughput در حال افزایش

ممکن است:

- تیم بالغ‌تر شده باشد.
- فرآیندها بهینه شده باشند.
- Automation اضافه شده باشد.

---

### Throughput در حال کاهش

بررسی کنید:

- افزایش WIP
- Blocked Issueها
- کاهش Capacity
- افزایش پیچیدگی Featureها

---

# Best Practices

✅ روند چند Sprint را بررسی کنید.

✅ Throughput را همراه Cycle Time تحلیل کنید.

✅ نوع Issueها (Bug، Story، Task) را از هم تفکیک کنید.

---

# Common Mistakes

❌ مقایسه Throughput تیم‌هایی با اندازه متفاوت

❌ افزایش مصنوعی تعداد Taskهای کوچک برای بالا بردن Throughput

---

# Dashboard KPI

Throughput معمولاً کنار این شاخص‌ها نمایش داده می‌شود:

- Cycle Time
- WIP
- Lead Time
- CFD

---

# Interview Questions

### Throughput چیست؟

تعداد آیتم‌هایی که در یک بازه زمانی تکمیل شده‌اند.

---

### تفاوت Throughput و Velocity چیست؟

Velocity بر اساس Story Point است، اما Throughput بر اساس تعداد آیتم‌های تکمیل‌شده.

---

# Summary

| ویژگی | Throughput |
|--------|------------|
| واحد | تعداد Issue |
| وابسته به Story Point | ❌ |
| مناسب | Kanban، DevOps |
| هرچه بیشتر | معمولاً بهتر (در صورت حفظ کیفیت) |
