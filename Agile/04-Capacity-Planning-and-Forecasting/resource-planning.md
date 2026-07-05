# Resource Planning

> برنامه‌ریزی و مدیریت منابع انسانی برای استفاده بهینه از ظرفیت تیم‌ها و تحویل به‌موقع پروژه‌ها.

---

# Definition

Resource Planning فرآیند تخصیص صحیح افراد، مهارت‌ها و زمان به پروژه‌ها و Sprintها است.

هدف اصلی:

> **قرار دادن فرد مناسب، با مهارت مناسب، در زمان مناسب روی کار مناسب**

---

# تفاوت Resource Planning و Capacity Planning

| Capacity Planning | Resource Planning |
|-------------------|-------------------|
| چقدر ظرفیت داریم؟ | چه کسی این کار را انجام می‌دهد؟ |
| تمرکز بر زمان | تمرکز بر افراد و نقش‌ها |
| سطح Sprint | سطح تیم، پروژه و سازمان |

---

# اهداف

- جلوگیری از Over Allocation
- جلوگیری از Under Utilization
- استفاده بهینه از مهارت‌ها
- مدیریت چند پروژه همزمان
- پیش‌بینی نیاز به استخدام
- برنامه‌ریزی Release

---

# مفاهیم کلیدی

## Allocation

درصد زمانی که یک فرد به پروژه اختصاص داده شده است.

مثال:

| پروژه | Allocation |
|--------|-----------:|
| Project A | 60% |
| Project B | 40% |

---

## Utilization

درصد ظرفیتی که واقعاً استفاده شده است.

فرمول:

```
Utilization

=

Used Capacity

/

Available Capacity

×

100
```

---

## Over Allocation

زمانی که مجموع Allocation از 100٪ بیشتر باشد.

مثال:

| پروژه | Allocation |
|--------|-----------:|
| A | 60% |
| B | 50% |

```
110%
```

نتیجه:

ریسک تأخیر، افت کیفیت و فرسودگی (Burnout).

---

## Under Utilization

زمانی که بخشی از ظرفیت بدون استفاده بماند.

مثال:

```
60%
```

استفاده از ظرفیت.

---

# Shared Resources

در بسیاری از سازمان‌ها، افراد بین چند تیم مشترک هستند.

مثال:

| نقش | Team A | Team B |
|------|-------:|-------:|
| DBA | 30% | 70% |
| DevOps | 40% | 60% |
| Security | 20% | 80% |

---

# Skill Matrix

نمونه ماتریس مهارت:

| Member | Java | React | QA | Kubernetes |
|--------|:----:|:-----:|:--:|:----------:|
| Ali | ✅ | ❌ | ❌ | ✅ |
| Sara | ❌ | ✅ | ❌ | ❌ |
| Reza | ✅ | ❌ | ✅ | ❌ |
| Mina | ❌ | ❌ | ✅ | ❌ |

این ماتریس برای تصمیم‌گیری درباره تخصیص افراد بسیار مهم است.

---

# Resource Calendar

تقویم منابع شامل موارد زیر است:

- مرخصی
- تعطیلات
- مأموریت
- آموزش
- On-call
- شیفت‌ها

این اطلاعات قبل از Sprint Planning باید بررسی شوند.

---

# Multi-project Planning

فرض کنید:

```
Developer A
```

روی سه پروژه کار می‌کند.

| Project | Allocation |
|----------|-----------:|
| ERP | 50% |
| Mobile | 30% |
| Website | 20% |

جمع:

```
100%
```

در این حالت برنامه‌ریزی منطقی است.

---

# Bottleneck Resource

گاهی یک تخصص کمیاب گلوگاه پروژه است.

مثال:

فقط یک نفر:

```
Database Administrator
```

وجود دارد.

تمام پروژه‌ها به او وابسته هستند.

در این شرایط Resource Planning اهمیت زیادی پیدا می‌کند.

---

# Capacity vs Resource

```
Capacity

=

400 Hours
```

اما:

```
Backend

350 Hours
```

```
QA

50 Hours
```

اگر Storyها به 120 ساعت QA نیاز داشته باشند، با وجود ظرفیت کافی، پروژه با مشکل مواجه خواهد شد.

---

# Resource Planning در Jira

Jira Software به‌صورت پیش‌فرض امکانات محدودی دارد.

برای برنامه‌ریزی حرفه‌ای منابع معمولاً از ابزارهای زیر استفاده می‌شود:

- Advanced Roadmaps
- Tempo Planner
- BigPicture
- ActivityTimeline
- Structure.Gantt
- Portfolio Planning

---

# Dashboard KPI

شاخص‌های متداول:

- Allocation %
- Utilization %
- Available Capacity
- Remaining Capacity
- Resource Load
- Team Load
- Skill Coverage

---

# مثال Dashboard

```
Ali

80%
```

```
Sara

95%
```

```
Reza

110%
```

```
Mina

65%
```

در این مثال، Reza بیش از ظرفیت خود تخصیص یافته است و نیاز به بازتوزیع کار وجود دارد.

---

# Resource Leveling

Resource Leveling یعنی متعادل‌سازی بار کاری افراد.

مثال:

قبل:

| Member | Allocation |
|--------|-----------:|
| Ali | 40% |
| Sara | 120% |
| Reza | 70% |

بعد از تنظیم:

| Member | Allocation |
|--------|-----------:|
| Ali | 70% |
| Sara | 90% |
| Reza | 70% |

---

# Resource Smoothing

در این روش، بدون تغییر تاریخ نهایی پروژه، کارها بین افراد جابه‌جا می‌شوند تا فشار کاری متعادل‌تر شود.

---

# ارتباط با Capacity

```
Resource Planning

↓

Capacity Planning

↓

Sprint Planning

↓

Execution

↓

Forecast
```

---

# Best Practices

✅ قبل از Sprint، Allocation همه اعضا را بررسی کنید.

✅ برای افراد کلیدی برنامه جایگزین (Backup) داشته باشید.

✅ Skill Matrix را همیشه به‌روز نگه دارید.

✅ منابع مشترک را به‌صورت شفاف مدیریت کنید.

✅ از داده‌های واقعی برای برنامه‌ریزی استفاده کنید.

---

# اشتباهات رایج

❌ تخصیص بیش از 100٪ به یک نفر.

❌ نادیده گرفتن مرخصی‌ها.

❌ وابستگی کامل به یک فرد متخصص.

❌ تخصیص کار بدون توجه به مهارت.

---

# Interview Questions

### Resource Planning چیست؟

فرآیند تخصیص افراد و مهارت‌ها به کارها برای استفاده بهینه از منابع.

---

### تفاوت Capacity و Resource Planning چیست؟

Capacity میزان توان تیم را اندازه می‌گیرد، اما Resource Planning مشخص می‌کند چه کسی و با چه درصدی آن کار را انجام می‌دهد.

---

### Over Allocation چیست؟

زمانی که مجموع کارهای اختصاص‌یافته به یک فرد از ظرفیت واقعی او بیشتر باشد.

---

### Jira چه امکاناتی برای Resource Planning دارد؟

در نسخه پایه محدود است؛ معمولاً از Advanced Roadmaps، Tempo Planner یا BigPicture استفاده می‌شود.

---

# Summary

| ویژگی | Resource Planning |
|---------|-------------------|
| هدف | مدیریت و تخصیص منابع |
| سطح | تیم، پروژه، سازمان |
| شاخص‌های کلیدی | Allocation، Utilization |
| گزارش داخلی Jira | محدود |
| ابزارهای رایج | Tempo، BigPicture، Advanced Roadmaps |

---

# Enterprise Tips

## 1. روی افراد کلیدی وابستگی ایجاد نکنید.

اگر تنها یک نفر مهارت حیاتی داشته باشد، پروژه در برابر مرخصی یا خروج او آسیب‌پذیر خواهد بود.

---

## 2. از Skill Matrix برای برنامه‌ریزی استفاده کنید.

تصمیم‌گیری بر اساس مهارت واقعی افراد معمولاً نتایج بهتری نسبت به تصمیم‌گیری صرفاً بر اساس ظرفیت ایجاد می‌کند.

---

## 3. Utilization را به 100٪ نرسانید.

برای یادگیری، بهبود، جلسات و رخدادهای پیش‌بینی‌نشده، مقداری ظرفیت آزاد در نظر بگیرید.

---

## 4. Allocation را به‌صورت هفتگی بازبینی کنید.

در پروژه‌های چندتیمی، تغییر اولویت‌ها ممکن است باعث Over Allocation یا Under Utilization شود.

---

## 5. Resource Planning را با سایر KPIها ترکیب کنید.

بهترین تصمیم‌ها زمانی گرفته می‌شوند که اطلاعات Resource Planning همراه با این شاخص‌ها تحلیل شوند:

- Capacity
- Velocity
- Predictability
- Focus Factor
- WIP
- Throughput
- Sprint Goal Achievement

---

# مثال کامل

فرض کنید یک تیم ۸ نفره دارید:

| نقش | تعداد | Allocation |
|------|-------:|-----------:|
| Backend | 3 | 100% |
| Frontend | 2 | 90% |
| QA | 2 | 85% |
| DevOps | 1 | 120% |

نتیجه تحلیل:

- Backend: وضعیت مناسب
- Frontend: ظرفیت قابل قبول
- QA: ظرفیت مناسب
- DevOps: **Over Allocation** و گلوگاه تیم

اقدام پیشنهادی:

- کاهش وابستگی به DevOps
- خودکارسازی برخی فعالیت‌ها (Automation)
- آموزش اعضای دیگر برای انجام بخشی از وظایف DevOps
- در صورت تداوم فشار، افزایش ظرفیت یا جذب نیروی جدید
