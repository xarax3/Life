# MTTR (Mean Time To Recovery)

> چهارمین شاخص اصلی DORA که مدت‌زمان لازم برای بازیابی سرویس بعد از یک Incident یا Failure را اندازه‌گیری می‌کند.

---

# Definition

MTTR یعنی:

> میانگین زمانی که طول می‌کشد یک سرویس پس از ایجاد اختلال دوباره به وضعیت عادی برگردد.

---

# فرمول

```
MTTR

=

Total Recovery Time

/

Number of Incidents
```

---

# مثال

در یک ماه:

Incident 1:

```
Recovery Time = 2 hours
```

Incident 2:

```
Recovery Time = 4 hours
```

Incident 3:

```
Recovery Time = 6 hours
```

محاسبه:

```
MTTR = (2+4+6) / 3

= 4 hours
```

---

# هدف

MTTR به این سؤال پاسخ می‌دهد:

> **اگر سیستم خراب شد، چقدر سریع می‌توانیم آن را برگردانیم؟**

---

# MTTR در DevOps

یک تیم DevOps بالغ فقط تلاش نمی‌کند:

```
Never Fail
```

بلکه تلاش می‌کند:

```
Fail Fast

+

Recover Fast
```

---

# MTTR و Reliability

دو حالت:

## تیم A

```
Failures = کم
Recovery = 2 روز
```

## تیم B

```
Failures = بیشتر
Recovery = 10 دقیقه
```

در سیستم‌های مدرن، تیم B ممکن است بالغ‌تر باشد.

---

# MTTR و DORA

چهار شاخص DORA:

| Metric | دسته |
|--------|------|
| Deployment Frequency | Speed |
| Lead Time for Changes | Speed |
| Change Failure Rate | Stability |
| MTTR | Stability |

---

# تفاوت MTTR با MTBF

## MTTR

Mean Time To Recovery

زمان بازیابی

---

## MTBF

Mean Time Between Failures

زمان بین خرابی‌ها

---

| MTTR | MTBF |
|-|-|
| بعد از خرابی | قبل از خرابی |
| Recovery | Reliability |

---

# انواع MTTR

در سازمان‌ها ممکن است MTTR معانی مختلف داشته باشد:

## Mean Time To Repair

زمان تعمیر

---

## Mean Time To Restore

زمان بازگرداندن سرویس

---

## Mean Time To Resolve

زمان حل کامل مشکل

---

در DORA معمولاً منظور:

```
Restore Service
```

است.

---

# MTTR در Jira Service Management

JSM یکی از اصلی‌ترین منابع داده MTTR است.

Flow:

```
Incident Created

↓

Detection Time

↓

Assignment

↓

Investigation

↓

Resolution

↓

Service Restored
```

---

# فیلدهای مهم Jira برای MTTR

- Created Date
- Incident Start Time
- Resolution Date
- Status History
- Priority
- Severity

---

# مثال JSM

Incident:

```
Created:
10:00
```

Resolved:

```
13:30
```

Recovery:

```
3.5 Hours
```

---

# MTTR Dashboard در Jira

نمونه:

```
Total Incidents:
50

Average MTTR:
2h 15m

Critical Incident MTTR:
35m

Trend:
↓ Improving
```

---

# عوامل افزایش MTTR

## 1. Monitoring ضعیف

مشکل دیر کشف می‌شود.

---

## 2. نبود Runbook

تیم نمی‌داند چه کاری انجام دهد.

---

## 3. پیچیدگی سیستم

Dependency زیاد.

---

## 4. نبود Ownership

مشخص نیست چه کسی مسئول است.

---

## 5. Rollback سخت

بازگشت طولانی می‌شود.

---

# کاهش MTTR

روش‌ها:

- Monitoring و Alerting بهتر
- Incident Runbook
- Automation
- Rollback سریع
- Canary Deployment
- Observability
- On-call Process

---

# MTTR و SRE

در SRE:

MTTR یکی از شاخص‌های اصلی Reliability Engineering است.

ارتباط با:

- SLO
- SLA
- Error Budget
- Incident Management

---

# MTTR و Jira Automation

می‌توان Automation ساخت برای:

مثال:

```
When Incident Created

↓

Set Priority

↓

Assign Team

↓

Notify On-call
```

که باعث کاهش زمان واکنش می‌شود.

---

# MTTR و Change Failure Rate

ارتباط مستقیم:

```
CFR بالا

↓

Incident بیشتر

↓

MTTR اهمیت بیشتر
```

---

# MTTR و Deployment Frequency

تیم‌هایی با Deploy سریع معمولاً:

- Fix سریع‌تر
- Rollback سریع‌تر
- MTTR کمتر

دارند.

---

# اشتباهات رایج

❌ محاسبه از زمان گزارش کاربر به جای زمان شروع Incident

❌ حذف Incidentهای کوچک

❌ تمرکز فقط روی میانگین

❌ عدم تفکیک Severity

---

# Interview Questions

### MTTR چیست؟

میانگین زمان لازم برای بازیابی سرویس بعد از Incident.

---

### MTTR پایین چه چیزی نشان می‌دهد؟

توانایی بالای تیم در Recovery و Incident Response.

---

### تفاوت MTTR و MTBF چیست؟

MTTR زمان بازیابی بعد از خرابی است، MTBF زمان بین خرابی‌ها.

---

### چگونه MTTR را کاهش می‌دهید؟

- Automation
- Monitoring
- Runbook
- Rollback Strategy
- Incident Process

---

# Summary

| ویژگی | MTTR |
|--------|------|
| نوع | DORA Metric |
| هدف | Recovery Speed |
| داده | Incident + Resolution |
| ابزار Jira | JSM |
| حوزه | DevOps / SRE |

---

# Enterprise Tips

## 1. MTTR را بر اساس Severity جدا کنید.

مثلاً:

```
Critical

Major

Minor
```

---

## 2. فقط Average را نگاه نکنید.

Percentileها مهم هستند.

---

## 3. Post Incident Review انجام دهید.

هدف کاهش تکرار مشکل است.

---

## 4. Automation بیشترین تأثیر را دارد.

هر مرحله دستی می‌تواند MTTR را افزایش دهد.

---

## 5. MTTR را با CFR ترکیب کنید.

هدف:

```
کمتر شدن Failure

+

سریع‌تر شدن Recovery
```

است.
