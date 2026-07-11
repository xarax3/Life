# Change Failure Rate (CFR)

> سومین شاخص DORA که درصد Deployهایی را اندازه‌گیری می‌کند که باعث ایجاد Failure، Incident، Rollback، Hotfix یا نیاز به اصلاح در Production شده‌اند.

---

# Definition

Change Failure Rate یعنی:

> چه درصدی از تغییرات منتشرشده باعث مشکل در محیط Production شده‌اند.

---

# فرمول

```
Change Failure Rate

=

(Number of Failed Changes)

/

(Total Number of Changes)

×

100
```

---

# مثال

در یک ماه:

```
Total Deployments = 100
```

از این تعداد:

```
Failed Deployments = 5
```

پس:

```
CFR = 5%
```

---

# چه چیزهایی Failure محسوب می‌شوند؟

بسته به سازمان:

- Rollback
- Hotfix
- Production Incident
- Service Degradation
- Emergency Patch
- Failed Deployment

---

# هدف CFR

CFR به این سؤال پاسخ می‌دهد:

> **چند درصد از تغییرات ما باعث آسیب به سیستم شده‌اند؟**

---

# CFR و Deployment Frequency

این دو باید با هم دیده شوند.

هدف DevOps:

```
Deploy More

+

Break Less
```

---

# مثال

## تیم A

```
Deployments = 10/month

Failures = 0
```

CFR:

```
0%
```

---

## تیم B

```
Deployments = 100/month

Failures = 20
```

CFR:

```
20%
```

اگرچه تیم B بیشتر Deploy می‌کند، کیفیت پایین‌تری دارد.

---

# CFR و Lead Time for Changes

هدف:

```
Lead Time ↓

CFR ↓
```

یعنی:

تغییرات سریع‌تر و با کیفیت‌تر منتشر شوند.

---

# CFR و CI/CD

افزایش کیفیت Pipeline باعث کاهش CFR می‌شود:

- Automated Testing
- Security Scan
- Code Quality Check
- Deployment Validation
- Monitoring

---

# CFR در Jira

Jira به‌تنهایی CFR را محاسبه نمی‌کند.

برای محاسبه نیاز به اتصال:

```
Jira Issue

+

Deployment Data

+

Incident Data
```

است.

---

# نمونه Integration

```
Jira

↓

Git Commit

↓

CI/CD Pipeline

↓

Deployment

↓

Incident Management
```

---

# ابزارهای اندازه‌گیری

- Jira Service Management
- GitLab
- GitHub Actions
- Jenkins
- Bamboo
- Datadog
- Grafana
- PagerDuty
- Opsgenie

---

# CFR در Jira Service Management

JSM می‌تواند برای ثبت:

- Incident
- Problem
- Change

استفاده شود.

مثال:

```
Change Request

↓

Deployment

↓

Incident Created
```

این ارتباط برای محاسبه CFR بسیار مهم است.

---

# عوامل افزایش CFR

## 1. تست ناکافی

```
Manual Testing Only
```

---

## 2. تغییرات بزرگ

```
Big Release

=

Higher Risk
```

---

## 3. نبود Monitoring

مشکل دیر کشف می‌شود.

---

## 4. محیط‌های متفاوت

```
Dev ≠ Test ≠ Production
```

---

## 5. نبود Rollback Strategy

بازگشت سخت‌تر می‌شود.

---

# کاهش CFR

روش‌ها:

- Automated Test
- CI/CD Quality Gates
- Blue-Green Deployment
- Canary Release
- Feature Flag
- Code Review
- Observability

---

# CFR و Change Management

در سازمان‌های Enterprise:

Change باید ثبت شود:

```
Request

↓

Approval

↓

Implementation

↓

Review
```

اما فرآیند نباید باعث کاهش سرعت شود.

---

# CFR و ITIL

CFR با فرآیندهای ITIL ارتباط دارد:

- Change Management
- Incident Management
- Problem Management

---

# Dashboard نمونه

```
Total Changes:

250

Failed Changes:

8

CFR:

3.2%

Trend:

↓ Improving
```

---

# اشتباهات رایج

❌ فقط شمردن Rollback

❌ نادیده گرفتن Incidentهای کوچک

❌ اندازه‌گیری بدون تعریف Failure

❌ مقایسه تیم‌های مختلف

---

# Interview Questions

### Change Failure Rate چیست؟

درصد تغییراتی که بعد از Deploy باعث Failure شده‌اند.

---

### آیا CFR کمتر همیشه بهتر است؟

بله، اما نباید با کاهش Deployment Frequency به دست بیاید.

---

### چگونه CFR را کاهش می‌دهید؟

- Automation
- Testing
- Monitoring
- کوچک کردن تغییرات
- Deployment Strategy بهتر

---

### ارتباط CFR با DORA چیست؟

CFR یکی از چهار شاخص اصلی DORA برای سنجش Stability است.

---

# Summary

| ویژگی | Change Failure Rate |
|--------|---------------------|
| نوع | DORA Metric |
| هدف | کیفیت Deployment |
| فرمول | Failed / Total Changes |
| داده | Deploy + Incident |
| ابزار Jira | JSM + CI/CD Integration |

---

# Enterprise Tips

## 1. Failure Definition را دقیق مشخص کنید.

همه تیم‌ها باید بدانند Failure چیست.

---

## 2. Incident کوچک را نادیده نگیرید.

Failure فقط Crash بزرگ نیست.

---

## 3. CFR را همراه Deployment Frequency بررسی کنید.

Deploy بیشتر با CFR پایین نشانه بلوغ DevOps است.

---

## 4. Monitoring قوی داشته باشید.

بدون Observability محاسبه CFR دقیق نیست.

---

## 5. هدف کاهش CFR با بهبود فرآیند است.

نه با کم کردن تعداد Deployها.
