# DORA Metrics

> DORA Metrics چهار شاخص استاندارد جهانی برای ارزیابی عملکرد تیم‌های DevOps و Software Delivery هستند. این شاخص‌ها توسط تیم **DevOps Research and Assessment (DORA)** معرفی شدند و امروزه معیار اصلی سنجش عملکرد در بسیاری از سازمان‌های Enterprise محسوب می‌شوند.

---

# DORA چیست؟

DORA مخفف:

```
DevOps Research and Assessment
```

هدف DORA:

- اندازه‌گیری سرعت تحویل نرم‌افزار
- اندازه‌گیری پایداری سرویس
- اندازه‌گیری کیفیت استقرار
- مقایسه تیم‌ها بر اساس داده‌های واقعی

---

# چهار شاخص اصلی DORA

1. Deployment Frequency (DF)
2. Lead Time for Changes (LTC)
3. Change Failure Rate (CFR)
4. Mean Time To Recovery (MTTR)

---

# چرا DORA مهم است؟

DORA فقط سرعت را اندازه‌گیری نمی‌کند؛ بلکه بین **سرعت** و **پایداری** تعادل برقرار می‌کند.

دو تیم ممکن است هر دو سریع Deploy کنند، اما تیمی که خرابی کمتری ایجاد می‌کند و سریع‌تر بازیابی می‌شود، عملکرد بهتری دارد.

---

# دسته‌بندی شاخص‌ها

## Speed Metrics

- Deployment Frequency
- Lead Time for Changes

---

## Stability Metrics

- Change Failure Rate
- MTTR

---

# ارتباط DORA با Jira

خود Jira به‌صورت پیش‌فرض همه شاخص‌های DORA را تولید نمی‌کند، اما می‌تواند منبع داده باشد.

معمولاً داده‌ها از ترکیب ابزارهای زیر جمع‌آوری می‌شوند:

- Jira
- Bitbucket
- GitHub
- GitLab
- Jenkins
- Bamboo
- Azure DevOps
- ArgoCD
- Kubernetes

---

# DORA در Jira Cloud

در Jira Cloud و Atlassian Analytics می‌توان بخشی از این شاخص‌ها را با اتصال به ابزارهای CI/CD مشاهده کرد.

در Jira Data Center معمولاً از:

- eazyBI
- Atlassian Analytics
- Marketplace Apps
- Power BI
- Grafana

استفاده می‌شود.

---

# DORA و DevOps Dashboard

یک داشبورد استاندارد معمولاً شامل:

```
Deployment Frequency

Lead Time

Change Failure Rate

MTTR

Availability

Incident Count
```

است.

---

# ارتباط DORA با Agile

DORA جایگزین Velocity نیست.

بلکه مکمل آن است.

| Agile | DevOps |
|--------|---------|
| Velocity | Deployment Frequency |
| Burndown | Lead Time for Changes |
| Sprint Goal | Release Success |
| Story Points | Production Metrics |

---

# ارتباط با Kanban

در Kanban تمرکز روی Flow است.

DORA همین Flow را تا Production ادامه می‌دهد.

```
Backlog

↓

Development

↓

Testing

↓

Deploy

↓

Production

↓

Recovery
```

---

# مزایای استفاده از DORA

- سنجش واقعی عملکرد تیم
- بهبود Continuous Delivery
- کاهش ریسک Release
- افزایش قابلیت پیش‌بینی
- بهبود کیفیت سرویس

---

# محدودیت‌ها

DORA به‌تنهایی کافی نیست.

در کنار آن باید شاخص‌های دیگری نیز بررسی شوند، مانند:

- Cycle Time
- Lead Time
- WIP
- Throughput
- Flow Efficiency
- Customer Satisfaction
- SLA/SLO

---

# سطوح عملکرد (نمونه)

| شاخص | عملکرد بهتر |
|-------|-------------|
| Deployment Frequency | بیشتر |
| Lead Time for Changes | کمتر |
| Change Failure Rate | کمتر |
| MTTR | کمتر |

> مقادیر دقیق ممکن است با انتشار نسخه‌های جدید گزارش‌های DORA تغییر کنند؛ بنابراین به روند بهبود تیم بیشتر از مقایسه با یک عدد ثابت توجه کنید.

---

# بهترین سناریوهای استفاده

- تیم‌های DevOps
- تیم‌های SRE
- تیم‌های Platform
- تیم‌های Cloud
- تیم‌های Enterprise
- CI/CD Pipeline Monitoring

---

# اشتباهات رایج

❌ تمرکز فقط بر سرعت Deploy

❌ استفاده از DORA برای ارزیابی عملکرد فردی

❌ مقایسه مستقیم تیم‌هایی با مأموریت‌های متفاوت

❌ نادیده گرفتن کیفیت و رضایت مشتری

---

# Interview Questions

### DORA چیست؟

مجموعه‌ای از چهار شاخص استاندارد برای اندازه‌گیری عملکرد Software Delivery و DevOps.

---

### چهار شاخص اصلی DORA چیست؟

- Deployment Frequency
- Lead Time for Changes
- Change Failure Rate
- MTTR

---

### آیا Jira به‌تنهایی DORA را ارائه می‌دهد؟

خیر، معمولاً با اتصال Jira به ابزارهای Git و CI/CD و ابزارهای گزارش‌گیری مانند eazyBI یا Grafana محاسبه می‌شود.

---

### چرا DORA مهم است؟

زیرا هم سرعت تحویل و هم پایداری سرویس را به‌صورت هم‌زمان ارزیابی می‌کند.

---

# Summary

| شاخص | هدف |
|------|-----|
| Deployment Frequency | سرعت انتشار |
| Lead Time for Changes | سرعت رسیدن تغییرات به Production |
| Change Failure Rate | کیفیت انتشار |
| MTTR | سرعت بازیابی پس از Incident |

---

# Enterprise Tips

## 1. DORA را به‌صورت Trend تحلیل کنید.

بهبود مستمر مهم‌تر از یک عدد در یک بازه زمانی است.

---

## 2. DORA را با Jira Metrics ترکیب کنید.

ترکیب آن با Cycle Time، Throughput و WIP دید کامل‌تری از جریان توسعه می‌دهد.

---

## 3. از Pipelineهای CI/CD داده جمع‌آوری کنید.

داده‌های Git، Build و Deploy برای محاسبه دقیق ضروری هستند.

---

## 4. داشبورد مشترک بسازید.

یک داشبورد که Jira، GitLab/GitHub، Jenkins و Grafana را ترکیب کند، تصویر جامعی از عملکرد ارائه می‌دهد.

---

## 5. هدف DORA بهبود سیستم است.

این شاخص‌ها برای شناسایی گلوگاه‌ها و بهبود فرآیند طراحی شده‌اند، نه برای رتبه‌بندی یا ارزیابی افراد.
