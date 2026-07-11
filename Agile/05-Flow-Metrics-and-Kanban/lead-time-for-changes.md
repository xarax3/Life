# Lead Time for Changes (LTC)

> دومین شاخص DORA که مدت‌زمان لازم از **اولین Commit کد** تا **Deploy موفق آن تغییر در محیط Production** را اندازه‌گیری می‌کند.

---

# Definition

Lead Time for Changes یعنی:

> مدت زمانی که طول می‌کشد تا یک تغییر نرم‌افزاری از مرحله Commit به محیط Production برسد.

این شاخص نشان‌دهنده سرعت واقعی تحویل تغییرات است.

---

# فرمول

```
Lead Time for Changes

=

Production Deployment Time

-

First Commit Time
```

---

# Timeline

```
Developer

↓

Commit

↓

Pull Request

↓

Code Review

↓

Build

↓

Test

↓

Deploy

↓

Production
```

تمام این مراحل در محاسبه LTC لحاظ می‌شوند.

---

# مثال

```
Commit

Monday 09:00
```

```
Deploy

Thursday 15:00
```

```
Lead Time for Changes

=

3 Days + 6 Hours
```

---

# هدف

Lead Time for Changes به این سؤال پاسخ می‌دهد:

> **چقدر طول می‌کشد تا یک تغییر پس از نوشته شدن، به دست کاربر برسد؟**

---

# تفاوت با Lead Time (Kanban)

| Lead Time | Lead Time for Changes |
|-----------|-----------------------|
| ایجاد Issue تا Done | Commit تا Production |
| Agile Metric | DORA Metric |
| تمرکز روی فرآیند کاری | تمرکز روی Software Delivery |

---

# تفاوت با Cycle Time

| Cycle Time | Lead Time for Changes |
|------------|----------------------|
| شروع کار تا Done | Commit تا Production |
| Jira Workflow | CI/CD Pipeline |

---

# ارتباط با CI/CD

Pipeline سریع‌تر باعث کاهش LTC می‌شود.

```
Commit

↓

Automatic Build

↓

Automatic Test

↓

Automatic Deploy

↓

Production
```

---

# ارتباط با Jira

Jira به‌تنهایی این شاخص را محاسبه نمی‌کند.

برای محاسبه باید اطلاعات زیر یکپارچه شوند:

- Jira Issue
- Git Commit
- Pull Request
- Build
- Deployment

---

# نمونه ارتباط

```
JIRA-125

↓

Commit

↓

Merge Request

↓

Build

↓

Deploy
```

---

# داده‌های موردنیاز

- Commit Time
- Deploy Time
- Deployment Status
- Environment
- Issue Key

---

# Lead Time for Changes و Deployment Frequency

معمولاً:

```
Deployment Frequency ↑

↓

Lead Time ↓
```

اگر CI/CD بالغ باشد.

---

# Lead Time for Changes و CFR

هدف این است که:

```
Lead Time ↓

Change Failure Rate ↓
```

همزمان اتفاق بیفتد.

---

# Lead Time for Changes و MTTR

اگر تیم Pipeline سریع داشته باشد:

- اصلاح باگ‌ها سریع‌تر Deploy می‌شود.
- MTTR نیز کاهش پیدا می‌کند.

---

# عوامل افزایش Lead Time

- Code Review طولانی
- Approvalهای متعدد
- Build کند
- Test دستی
- Releaseهای بزرگ
- انتظار برای Release Window

---

# عوامل کاهش Lead Time

- CI/CD
- Test Automation
- Feature Flags
- Trunk-Based Development
- کوچک کردن Pull Requestها
- Continuous Deployment

---

# Dashboard نمونه

```
Average Lead Time

2.5 Days

Median

1.8 Days

95th Percentile

6 Days

Trend

↓

Improving
```

---

# ابزارهای اندازه‌گیری

- Jira
- GitLab
- GitHub
- Bitbucket
- Jenkins
- Bamboo
- Azure DevOps
- Grafana
- eazyBI

---

# مثال Enterprise

```
Commit

08:30
```

```
Merge

09:10
```

```
Build

09:18
```

```
Deploy Production

10:05
```

Lead Time:

```
1 Hour 35 Minutes
```

---

# اشتباهات رایج

❌ استفاده از زمان ایجاد Issue

❌ استفاده از زمان Merge به‌جای Commit

❌ نادیده گرفتن Deploy ناموفق

❌ محاسبه تا Staging به‌جای Production (در گزارش DORA)

---

# Interview Questions

### Lead Time for Changes چیست؟

مدت‌زمان لازم از اولین Commit تا Deploy موفق در Production.

---

### تفاوت آن با Lead Time چیست؟

Lead Time مربوط به فرآیند Agile است، اما Lead Time for Changes مربوط به Software Delivery و DevOps است.

---

### چگونه Lead Time for Changes را کاهش می‌دهید؟

- اتوماسیون Build و Test
- حذف Approvalهای غیرضروری
- کاهش اندازه Pull Requestها
- استفاده از CI/CD
- Continuous Deployment

---

### آیا Jira به‌تنهایی این شاخص را محاسبه می‌کند؟

خیر. نیاز به اتصال Jira با Git و ابزارهای CI/CD دارد.

---

# Summary

| ویژگی | Lead Time for Changes |
|--------|-----------------------|
| نوع | DORA Metric |
| شروع | First Commit |
| پایان | Successful Production Deploy |
| هدف | سرعت تحویل تغییرات |
| ابزار | Jira + Git + CI/CD |

---

# Enterprise Tips

## 1. Commitهای کوچک و مکرر داشته باشید.

Commitهای کوچک معمولاً سریع‌تر Review و Deploy می‌شوند.

---

## 2. Pipeline را کاملاً خودکار کنید.

هر مرحله دستی باعث افزایش Lead Time می‌شود.

---

## 3. Reviewها را کوتاه نگه دارید.

Pull Requestهای کوچک باعث کاهش زمان بررسی می‌شوند.

---

## 4. Lead Time را به‌صورت Percentile تحلیل کنید.

میانگین ممکن است تحت تأثیر چند مورد استثنایی قرار گیرد؛ 85th یا 95th Percentile تصویر دقیق‌تری از عملکرد سیستم ارائه می‌دهد.

---

## 5. Lead Time را همراه سایر شاخص‌های DORA بررسی کنید.

کاهش Lead Time زمانی ارزشمند است که Deployment Frequency، Change Failure Rate و MTTR نیز در وضعیت مناسبی باشند.
