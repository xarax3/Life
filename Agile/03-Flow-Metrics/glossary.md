# Flow Metrics Glossary

> واژه‌نامه تخصصی Flow Metrics، Kanban، Scrum، DevOps و Jira

---

# A

## Active Time

مدتی که واقعاً روی یک Issue کار انجام می‌شود.

شامل:

- Development
- Review
- Testing

شامل زمان انتظار نیست.

---

# Aging Work Item

مدت زمانی که یک Issue هنوز باز است و تکمیل نشده است.

اگر یک Issue مدت زیادی در یک وضعیت باقی بماند، Aging آن افزایش پیدا می‌کند.

در بسیاری از Dashboardهای Kanban برای شناسایی آیتم‌های قدیمی استفاده می‌شود.

---

# B

## Bottleneck

مرحله‌ای از Workflow که باعث تجمع Issueها و کاهش سرعت جریان کار می‌شود.

نمونه‌ها:

- Code Review
- QA
- Security Approval
- Deployment

---

# C

## Continuous Delivery (CD)

رویکردی که در آن نرم‌افزار همیشه آماده انتشار است و انتشارها می‌توانند با حداقل تأخیر انجام شوند.

---

## Continuous Integration (CI)

فرآیندی که در آن تغییرات کد به‌صورت مداوم در شاخه اصلی ادغام و به‌صورت خودکار Build و Test می‌شوند.

---

## Control Chart

گزارش Jira برای نمایش و تحلیل **Cycle Time** هر Issue و بررسی پایداری فرآیند.

---

## Cumulative Flow Diagram (CFD)

نموداری که تعداد Issueها در هر Status را در طول زمان نمایش می‌دهد و برای شناسایی گلوگاه‌ها و تحلیل WIP استفاده می‌شود.

---

## Cycle Time

مدت زمان از شروع کار واقعی روی یک Issue تا رسیدن آن به وضعیت Done.

---

# D

## Done

وضعیتی که نشان می‌دهد کار مطابق Definition of Done تکمیل شده است.

---

## Deployment Frequency

یکی از **DORA Metrics** که تعداد دفعات استقرار (Deployment) به محیط Production را در یک بازه زمانی اندازه‌گیری می‌کند.

---

## DORA Metrics

چهار شاخص کلیدی برای ارزیابی عملکرد تیم‌های DevOps:

- Deployment Frequency
- Lead Time for Changes
- Change Failure Rate
- Mean Time to Recovery (MTTR)

---

# F

## Flow

حرکت مداوم و بدون توقف آیتم‌های کاری در فرآیند توسعه، از زمان ایجاد تا تحویل.

---

## Flow Efficiency

درصد زمانی که واقعاً روی Issue کار انجام شده است.

```
Flow Efficiency =
Active Time / Lead Time × 100
```

---

## Flow Metrics

مجموعه‌ای از شاخص‌ها برای اندازه‌گیری کیفیت و سرعت جریان کار.

مهم‌ترین آن‌ها:

- Cycle Time
- Lead Time
- Throughput
- WIP
- Flow Efficiency

---

# I

## Issue

واحد اصلی کار در Jira.

می‌تواند از نوع:

- Story
- Task
- Bug
- Epic
- Improvement
- Spike

باشد.

---

# K

## Kanban

چارچوبی برای مدیریت جریان کار که بر موارد زیر تمرکز دارد:

- محدود کردن WIP
- بهبود Flow
- تحویل مستمر
- حذف گلوگاه‌ها

---

# L

## Lead Time

مدت زمان از ایجاد Issue تا تکمیل آن.

دیدگاه این متریک، دیدگاه مشتری و کسب‌وکار است.

---

## Little's Law

قانون پایه Kanban:

```
Lead Time = WIP / Throughput
```

این قانون ارتباط بین حجم کار، سرعت خروجی و زمان تحویل را نشان می‌دهد.

---

# M

## Mean

میانگین حسابی داده‌ها.

در تحلیل Flow معمولاً به‌تنهایی کافی نیست، زیرا ممکن است تحت تأثیر Outlierها قرار گیرد.

---

## Median

عدد میانی در مجموعه داده‌های مرتب‌شده.

برای تحلیل Cycle Time معمولاً از میانگین قابل‌اعتمادتر است.

---

## MTTR (Mean Time to Recovery)

میانگین زمان لازم برای بازیابی سرویس پس از وقوع یک خرابی.

یکی از DORA Metrics.

---

# O

## Outlier

داده‌ای که به‌طور قابل‌توجهی با سایر داده‌ها متفاوت است.

مثال:

```
Cycle Time

اکثر Issueها: 4 روز

یک Issue: 27 روز
```

---

# P

## Percentile

شاخصی برای نمایش توزیع داده‌ها.

مثال:

- 50th Percentile = Median
- 85th Percentile = پیش‌بینی متداول
- 95th Percentile = پیش‌بینی محافظه‌کارانه

---

## Predictability

توانایی تیم در تحویل کارها در بازه زمانی قابل پیش‌بینی.

هرچه پراکندگی Cycle Time کمتر باشد، Predictability بیشتر است.

---

# Q

## Queue Time

مدت زمانی که یک Issue در صف انتظار قرار دارد تا پردازش شود.

مثال:

- انتظار برای Code Review
- انتظار برای QA
- انتظار برای Release

---

# R

## Rolling Average

میانگین متحرک که برای مشاهده روند تغییرات در طول زمان استفاده می‌شود.

---

# S

## SLA (Service Level Agreement)

توافق‌نامه‌ای که حداکثر زمان مجاز برای ارائه یک خدمت یا تحویل یک درخواست را مشخص می‌کند.

Lead Time معمولاً برای ارزیابی رعایت SLA استفاده می‌شود.

---

# T

## Throughput

تعداد Issueهایی که در یک بازه زمانی مشخص به وضعیت Done رسیده‌اند.

---

# V

## Value Stream

تمام مراحلی که یک درخواست از ایجاد تا تحویل طی می‌کند.

تحلیل Value Stream برای شناسایی اتلاف‌ها و گلوگاه‌ها استفاده می‌شود.

---

# W

## Waiting Time

مدت زمانی که هیچ فعالیتی روی Issue انجام نمی‌شود.

```
Waiting Time

=

Lead Time

-

Active Time
```

---

## Work In Progress (WIP)

تعداد Issueهایی که هم‌اکنون در حال انجام هستند اما هنوز تکمیل نشده‌اند.

---

## WIP Limit

حداکثر تعداد مجاز Issueها در یک مرحله از Workflow.

هدف:

- جلوگیری از چندوظیفگی
- کاهش Cycle Time
- افزایش Flow

---

# روابط مهم

```text
Created
   │
   ▼
Lead Time
   │
   ├──────────────┐
   ▼              │
Waiting Time      │
                  ▼
           In Progress
                  │
                  ▼
            Cycle Time
                  │
                  ▼
                Done
```

---

# واژه‌های پرتکرار در Jira

| اصطلاح | ارتباط با Jira |
|---------|----------------|
| Cycle Time | Control Chart |
| Lead Time | افزونه‌ها / گزارش سفارشی |
| Throughput | Dashboard |
| WIP | Kanban Board |
| CFD | Reports |
| Outlier | Control Chart |
| Bottleneck | CFD |
| Queue Time | گزارش سفارشی |
| Flow Efficiency | eazyBI / ActionableAgile |
| Percentile | ActionableAgile |

---

# نکات مصاحبه

اگر در مصاحبه از شما پرسیده شد:

> مهم‌ترین اصطلاحات Flow Metrics چیست؟

تقریباً همیشه این موارد را نام ببرید:

- Cycle Time
- Lead Time
- Throughput
- WIP
- Bottleneck
- Flow Efficiency
- CFD
- Control Chart
- Little's Law
- Predictability

این ده مفهوم، هسته اصلی تحلیل جریان کار در Jira، Kanban و DevOps هستند.
