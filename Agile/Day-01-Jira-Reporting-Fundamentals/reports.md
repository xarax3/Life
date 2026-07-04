# Jira Built-in Reports

> در این بخش تمام Reportهای پیش‌فرض Jira Software را بررسی می‌کنیم.
>
> **نکته:** بسته به نوع پروژه (Scrum یا Kanban) و نسخه Jira (Cloud یا Data Center)، ممکن است بعضی گزارش‌ها در دسترس نباشند.

---

# گزارش‌های پیش‌فرض Jira

گزارش‌های Jira را می‌توان به ۵ دسته تقسیم کرد:

```
Jira Reports

├── Sprint Reports
├── Flow Reports
├── Release Reports
├── Epic Reports
└── Time Reports
```

| دسته | هدف |
|------|------|
| Sprint | بررسی عملکرد Sprint |
| Flow | تحلیل جریان کار |
| Release | پیش‌بینی انتشار نسخه |
| Epic | بررسی پیشرفت Epic |
| Time | تحلیل زمان انجام کار |

---

# 1. Sprint Report

## هدف

بررسی عملکرد یک Sprint پس از پایان آن.

این گزارش مهم‌ترین گزارش برای **Scrum Master** است.

---

## مسیر در Jira

```
Project
    ↓
Reports
    ↓
Sprint Report
```

---

## اطلاعات نمایش داده شده

- Completed Issues
- Incomplete Issues
- Issues Added During Sprint
- Issues Removed During Sprint
- Scope Change
- Story Points Completed
- Story Points Remaining

---

## نمونه

```
Sprint 25

Completed
██████████████ 42 SP

Remaining
████ 8 SP

Added
██ 5 SP

Removed
█ 3 SP
```

---

## چه سؤالاتی را پاسخ می‌دهد؟

- آیا Sprint موفق بود؟
- چه کارهایی ناتمام ماند؟
- آیا وسط Sprint کار جدید اضافه شد؟
- آیا برنامه‌ریزی صحیح بود؟

---

## چه چیزی را نشان نمی‌دهد؟

❌ Capacity

❌ Focus Factor

❌ Commitment Reliability

❌ Team Utilization

برای این موارد معمولاً از eazyBI یا Tempo استفاده می‌شود.

---

## چه زمانی استفاده کنیم؟

- Sprint Review
- Sprint Retrospective
- جلسه PM

---

## خطاهای رایج

اگر Storyها Done نشده باشند یا Sprint به‌درستی بسته نشده باشد، گزارش ناقص یا نادرست خواهد بود.

---

# 2. Velocity Report

## هدف

اندازه‌گیری سرعت تیم در Sprintهای گذشته.

---

## مسیر

```
Project
    ↓
Reports
    ↓
Velocity Chart
```

---

## اطلاعات نمایش داده شده

- Committed Story Points
- Completed Story Points
- Average Velocity
- Velocity Trend

---

## نمونه

```
Sprint 21  32 SP
Sprint 22  34 SP
Sprint 23  31 SP
Sprint 24  36 SP
Sprint 25  35 SP
```

---

## کاربرد

- پیش‌بینی Sprint بعدی
- بررسی پایداری تیم
- تحلیل عملکرد تیم در بلندمدت

---

## نکته مهم

Velocity فقط برای **یک تیم** معنا دارد.

مقایسه Velocity بین دو تیم مختلف اشتباه است، زیرا روش برآورد Story Point ممکن است متفاوت باشد.

---

## خطاهای رایج

❌ استفاده از Velocity برای ارزیابی عملکرد افراد

Velocity یک شاخص تیمی است، نه فردی.

---

# 3. Burndown Chart

## هدف

نمایش میزان کار باقی‌مانده در طول Sprint.

---

## مسیر

```
Project
    ↓
Reports
    ↓
Burndown Chart
```

---

## نمودار

```
Story Points

40 |\
35 | \
30 |  \
20 |   \
10 |    \
 0 +-----\---------
     Day 10
```

---

## اجزای نمودار

- Ideal Line
- Actual Line
- Scope Change

---

## تفسیر

اگر خط واقعی بالاتر از خط ایده‌آل باشد:

→ تیم از برنامه عقب است.

اگر پایین‌تر باشد:

→ تیم جلوتر از برنامه حرکت می‌کند.

---

## استفاده

- Daily Scrum
- Scrum Master
- مشاهده روند Sprint

---

## محدودیت

Burndown فقط وضعیت Sprint جاری را نشان می‌دهد و برای تحلیل بلندمدت مناسب نیست.

---

# 4. Burnup Chart

## هدف

نمایش میزان کار انجام‌شده نسبت به کل Scope.

---

## تفاوت با Burndown

Burndown:

```
Remaining Work
```

Burnup:

```
Completed Work
```

---

## مزیت Burnup

اگر Scope تغییر کند، Burnup آن را واضح‌تر نمایش می‌دهد.

---

## مثال

```
Completed

40

35

30

20

10

0
```

در کنار خط دوم که Total Scope را نشان می‌دهد.

---

## مناسب برای

- Product Owner
- مدیر پروژه
- مدیریت Scope

---

# 5. Epic Report

## هدف

نمایش پیشرفت یک Epic.

---

## مسیر

```
Project

↓

Reports

↓

Epic Report
```

---

## اطلاعات

- Completed Stories
- Remaining Stories
- Progress
- Scope

---

## مثال

```
Epic

Authentication

Progress

████████░░

80%
```

---

## استفاده

- Product Owner
- Business Analyst

---

## محدودیت

فقط یک Epic را بررسی می‌کند و برای تحلیل چند Epic باید از Dashboard یا افزونه استفاده کرد.

---

# 6. Epic Burndown

## هدف

بررسی کاهش کارهای باقی‌مانده در یک Epic.

---

## مناسب برای

- پروژه‌های بزرگ
- Epicهای چند Sprint

---

# 7. Version Report

## هدف

پیش‌بینی زمان آماده شدن یک Version یا Release.

---

## مسیر

```
Project

↓

Reports

↓

Version Report
```

---

## اطلاعات

- Remaining Work
- Velocity
- Predicted Release Date

---

## مثال

```
Version

2.1

Progress

72%

Forecast

12 Sep
```

---

## چه کسی استفاده می‌کند؟

- Product Owner
- Release Manager
- Project Manager

---

# 8. Release Burndown

## هدف

بررسی روند تکمیل کارهای مربوط به یک Release.

---

## تفاوت با Burndown

Burndown → Sprint

Release Burndown → Version

---

# 9. Control Chart

## هدف

تحلیل مدت زمان انجام Issueها.

---

## مسیر

```
Project

↓

Reports

↓

Control Chart
```

---

## نمایش می‌دهد

- Cycle Time
- Average Cycle Time
- Distribution
- Percentiles

---

## مثال

```
Issue A

2 Days

Issue B

5 Days

Issue C

1 Day
```

---

## مناسب برای

- Kanban
- Continuous Delivery
- Flow Analysis

---

## اگر میانگین بالا باشد

یعنی Issueها مدت زیادی در Workflow باقی می‌مانند و باید گلوگاه‌ها بررسی شوند.

---

# 10. Cumulative Flow Diagram (CFD)

## هدف

تحلیل جریان کار و شناسایی گلوگاه‌ها.

---

## مسیر

```
Project

↓

Reports

↓

Cumulative Flow Diagram
```

---

## وضعیت‌های معمول

```
To Do

In Progress

Review

Testing

Done
```

هر وضعیت به‌صورت یک ناحیه رنگی در نمودار نمایش داده می‌شود.

---

## چه چیزی را نشان می‌دهد؟

- Work In Progress (WIP)
- Throughput
- Bottleneck
- Queue Size
- روند ورود و خروج کار

---

## مثال

اگر ناحیه **Testing** به مرور ضخیم‌تر شود، یعنی Issueها در مرحله تست انباشته شده‌اند و تیم QA گلوگاه ایجاد کرده است.

---

# مقایسه گزارش‌ها

| Report | مناسب برای | سوالی که پاسخ می‌دهد |
|---------|------------|----------------------|
| Sprint Report | Scrum Master | آیا Sprint موفق بود؟ |
| Velocity Report | Scrum Master | سرعت تیم چقدر است؟ |
| Burndown | تیم توسعه | چقدر کار باقی مانده؟ |
| Burnup | Product Owner | چه مقدار کار انجام شده است؟ |
| Epic Report | Product Owner | وضعیت Epic چیست؟ |
| Version Report | Release Manager | Release چه زمانی آماده می‌شود؟ |
| Control Chart | Kanban Team | انجام هر Issue چقدر طول می‌کشد؟ |
| CFD | Agile Coach | گلوگاه Workflow کجاست؟ |

---

# چه گزارشی برای چه جلسه‌ای؟

| جلسه | گزارش پیشنهادی |
|-------|----------------|
| Daily Scrum | Burndown، Dashboard |
| Sprint Review | Sprint Report، Burnup |
| Sprint Retrospective | Sprint Report، Velocity |
| Release Planning | Version Report، Release Burndown |
| Kanban Review | CFD، Control Chart |

---

# محدودیت‌های گزارش‌های پیش‌فرض Jira

گزارش‌های داخلی Jira این موارد را ارائه نمی‌کنند:

- Capacity
- Initial Commitment Trend
- Commitment Reliability
- Focus Factor
- Team Utilization
- Monte Carlo Forecast
- Cost Metrics
- Budget Metrics
- Resource Allocation
- Risk Metrics

برای این نیازها معمولاً از افزونه‌هایی مانند **eazyBI**، **Tempo**، **Structure** یا **Advanced Roadmaps** استفاده می‌شود.

---

# Best Practices

- Sprint Report را پس از پایان هر Sprint بررسی کنید.
- Velocity را حداقل در ۵ Sprint متوالی تحلیل کنید، نه یک Sprint.
- Burndown را در Daily Scrum بررسی کنید.
- Version Report را قبل از هر Release بازبینی کنید.
- در Kanban، CFD و Control Chart را به‌صورت منظم پایش کنید.

---

# خلاصه

اگر فقط بخواهید با گزارش‌های پیش‌فرض Jira کار کنید، این ۸ گزارش بیشترین ارزش را دارند:

1. Sprint Report
2. Velocity Report
3. Burndown Chart
4. Burnup Chart
5. Epic Report
6. Version Report
7. Control Chart
8. Cumulative Flow Diagram (CFD)

تسلط بر این گزارش‌ها برای اکثر نقش‌های Scrum Master، Product Owner، Project Manager و Jira Administrator ضروری است.
