# Deployment Frequency (DF)

> اولین شاخص DORA که نشان می‌دهد تیم در یک بازه زمانی مشخص، چند بار تغییرات را با موفقیت در محیط Production (یا محیط هدف) Deploy کرده است.

---

# Definition

Deployment Frequency یعنی:

> تعداد دفعات استقرار (Deployment) موفق در یک بازه زمانی مشخص.

این شاخص نشان‌دهنده سرعت تحویل نرم‌افزار است، نه سرعت توسعه کد.

---

# فرمول

```
Deployment Frequency

=

Number of Successful Deployments

/

Time Period
```

---

# مثال

در یک هفته:

```
Monday     → 2 Deployments
Tuesday    → 1 Deployment
Wednesday  → 0
Thursday   → 3 Deployments
Friday     → 2 Deployments
```

```
Deployment Frequency = 8 Deployments / Week
```

---

# هدف

Deployment Frequency به این سؤال پاسخ می‌دهد:

> **تیم با چه سرعتی تغییرات را به محیط عملیاتی تحویل می‌دهد؟**

---

# چه چیزی Deployment محسوب می‌شود؟

معمولاً فقط Deploy موفق به محیط Production محاسبه می‌شود.

در برخی سازمان‌ها ممکن است Deploy به Staging نیز برای گزارش‌های داخلی محاسبه شود، اما در DORA معمولاً Production معیار اصلی است.

---

# Deployment Frequency و Release Frequency

این دو یکسان نیستند.

| Deployment Frequency | Release Frequency |
|----------------------|------------------|
| تعداد Deploy | تعداد Release |
| معیار DevOps | معیار محصول |
| ممکن است چند Deploy در یک Release باشد | ممکن است یک Release شامل چند Deploy باشد |

---

# Deployment Frequency و CI/CD

هرچه Pipeline بالغ‌تر باشد:

- Build سریع‌تر
- Test خودکار
- Deploy خودکار
- Deployment Frequency بیشتر

---

# Deployment Frequency و Jira

Jira به‌تنهایی تعداد Deployها را ثبت نمی‌کند.

برای محاسبه DF معمولاً Jira به ابزارهای زیر متصل می‌شود:

- GitLab
- GitHub
- Bitbucket
- Jenkins
- Bamboo
- Azure DevOps
- ArgoCD
- Kubernetes

---

# Jira Deployments

اگر Jira با ابزار CI/CD یکپارچه شود، در Issue View معمولاً اطلاعاتی مانند:

```
Development

↓

Build

↓

Deployment

↓

Environment
```

نمایش داده می‌شود.

---

# ارتباط با Issue

یک Issue ممکن است:

```
Story

↓

Commit

↓

Pull Request

↓

Build

↓

Deploy
```

را طی کند.

این ارتباط امکان تحلیل دقیق‌تر Deployment را فراهم می‌کند.

---

# Deployment Frequency و Velocity

این دو شاخص مستقل هستند.

ممکن است:

- Velocity بالا باشد اما Deploy کم انجام شود.
- Velocity پایین باشد اما Deployهای کوچک و مکرر انجام شوند.

---

# Deployment Frequency و Lead Time

معمولاً:

```
Deployment Frequency ↑

Lead Time ↓
```

البته تنها در صورتی که فرآیند توسعه و استقرار نیز بهینه باشد.

---

# Deployment Frequency و Change Failure Rate

افزایش DF نباید باعث افزایش Failure Rate شود.

هدف DevOps:

```
Deploy More

+

Fail Less
```

---

# Deployment Frequency و MTTR

تیمی که سریع Deploy می‌کند معمولاً می‌تواند اصلاحات (Hotfix) را نیز سریع‌تر منتشر کند و MTTR را کاهش دهد.

---

# نمونه Dashboard

```
Deployments Today : 3

Deployments This Week : 18

Deployments This Month : 74

Trend : ↑
```

---

# ابزارهای اندازه‌گیری

- Jira + GitLab
- Jira + GitHub
- Jira + Bitbucket
- Jenkins
- Bamboo
- Azure DevOps
- ArgoCD
- Grafana
- eazyBI

---

# عوامل افزایش Deployment Frequency

- Continuous Integration
- Continuous Delivery
- Automated Testing
- Feature Flags
- Trunk-Based Development
- کوچک‌تر کردن Pull Requestها

---

# عوامل کاهش Deployment Frequency

- تست دستی
- فرآیندهای Approval طولانی
- Releaseهای بزرگ
- Buildهای کند
- نبود Automation
- محیط Production ناپایدار

---

# اشتباهات رایج

❌ شمردن Deployهای ناموفق

❌ شمردن Build به‌جای Deploy

❌ مقایسه تیم‌هایی با فرآیندهای متفاوت

❌ تمرکز بر تعداد بدون توجه به کیفیت

---

# Interview Questions

### Deployment Frequency چیست؟

تعداد Deployهای موفق در یک بازه زمانی مشخص.

---

### آیا هر Build یک Deployment است؟

خیر. Build فقط فرآیند ساخت نرم‌افزار است؛ Deployment انتقال نسخه به محیط اجرا است.

---

### آیا Release با Deployment یکسان است؟

خیر. ممکن است یک Release شامل چند Deployment باشد یا یک Deployment بدون Release قابل مشاهده برای کاربر انجام شود.

---

### چگونه Deployment Frequency را افزایش می‌دهید؟

- CI/CD
- تست خودکار
- حذف Approvalهای غیرضروری
- کاهش اندازه تغییرات
- استفاده از Feature Flag

---

# Summary

| ویژگی | Deployment Frequency |
|--------|----------------------|
| نوع | DORA Metric |
| هدف | سنجش سرعت استقرار |
| واحد | Deploy / Time |
| داده موردنیاز | Successful Deployments |
| ابزار Jira | Integration با CI/CD |

---

# Enterprise Tips

## 1. فقط Deployهای موفق به Production را معیار اصلی قرار دهید.

---

## 2. Deployment Frequency را همراه CFR تحلیل کنید.

Deploy بیشتر زمانی ارزشمند است که نرخ شکست افزایش پیدا نکند.

---

## 3. Releaseهای کوچک و مکرر داشته باشید.

این کار ریسک هر Deploy را کاهش می‌دهد.

---

## 4. از Feature Flags استفاده کنید.

با Feature Flag می‌توان کد را Deploy کرد بدون اینکه قابلیت فوراً برای همه کاربران فعال شود.

---

## 5. داشبورد مشترک DevOps بسازید.

Deployment Frequency را در کنار Lead Time for Changes، Change Failure Rate و MTTR نمایش دهید تا تصویر کاملی از عملکرد تیم به دست آید.
