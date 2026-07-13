# Day 5 — Flow, Kanban & DevOps Metrics

---

# هدف این بخش

در این بخش با مهم‌ترین KPIها و Metricهایی آشنا می‌شوید که در تیم‌های Kanban، Scrum، Scrumban و DevOps برای اندازه‌گیری عملکرد تیم، تحلیل جریان کار (Flow) و پیش‌بینی زمان تحویل استفاده می‌شوند.

این مباحث در سازمان‌های Enterprise پایه اصلی Dashboardها، Forecastها و گزارش‌های مدیریتی هستند.

---

# پیش‌نیاز

پیشنهاد می‌شود قبل از مطالعه این بخش، مباحث زیر را کامل کرده باشید:

- Agile Fundamentals
- Scrum Framework
- Sprint Planning
- Jira Reports
- Capacity Planning
- Forecasting

---

# سرفصل‌ها

## Core Flow Metrics

- Lead Time
- Cycle Time
- Throughput
- Work Item Age
- Flow Efficiency
- Work In Progress (WIP)

---

## Kanban Charts

- Cumulative Flow Diagram (CFD)
- Control Chart
- Scatter Plot
- Aging Chart

---

## Agile Reports

- Burnup Chart
- Burnup vs Burndown

---

## DevOps Metrics

- Deployment Frequency
- Lead Time for Changes
- Change Failure Rate
- Mean Time To Recovery (MTTR)

---

## Service Management

- Service Level Expectation (SLE)

---

## Dashboards

- Kanban Dashboard
- DevOps Dashboard
- Executive Dashboard

---

# چرا Flow Metrics مهم هستند؟

Velocity تنها نشان می‌دهد تیم چه مقدار کار انجام داده است.

اما Flow Metrics نشان می‌دهند:

- کارها چقدر سریع حرکت می‌کنند.
- گلوگاه (Bottleneck) کجاست.
- مشتری چقدر منتظر می‌ماند.
- کیفیت فرآیند چگونه است.
- آیا Forecast قابل اعتماد است یا خیر.

به همین دلیل، بسیاری از سازمان‌های بزرگ علاوه بر Velocity از Flow Metrics نیز استفاده می‌کنند.

---

# ارتباط مفاهیم

```
Idea

↓

Backlog

↓

Selected

↓

In Progress

↓

Review

↓

Testing

↓

Done

↓

Production
```

در طول این مسیر، Metricهای مختلف اندازه‌گیری می‌شوند.

---

# مهم‌ترین KPIهای این بخش

| KPI | هدف |
|------|------|
| Lead Time | زمان کل از درخواست تا تحویل |
| Cycle Time | زمان از شروع کار تا پایان |
| Throughput | تعداد آیتم‌های تکمیل‌شده |
| WIP | تعداد آیتم‌های در حال انجام |
| Work Item Age | سن آیتم‌های باز |
| Flow Efficiency | درصد زمان مفید |
| Deployment Frequency | تعداد استقرارها |
| MTTR | زمان بازیابی سرویس |
| Change Failure Rate | درصد تغییرات ناموفق |

---

# این Metricها در Jira کجا هستند؟

| Metric | Jira | افزونه |
|---------|------|---------|
| Lead Time | ❌ | ActionableAgile |
| Cycle Time | Control Chart |
| Throughput | eazyBI |
| CFD | Jira Control Chart |
| Burnup | داخلی Jira |
| Burndown | داخلی Jira |
| DORA | Atlassian Analytics / CI-CD |

---

# ابزارهای رایج

- Jira Software
- Jira Align
- Atlassian Analytics
- ActionableAgile Analytics
- eazyBI
- Rich Filters
- BigPicture
- Tempo
- GitLab
- GitHub
- Azure DevOps

---

# ترتیب مطالعه

# ترتیب مطالعه

1. [Lead Time](lead-time.md) و [Cycle Time](cycle-time.md)
2. [Throughput](throughput.md)، [Work Item Age](work-item-age.md)، [WIP](work-in-progress.md) و [Flow Efficiency](flow-efficiency.md)
3. [CFD](cumulative-flow-diagram.md)، [Control Chart](control-chart.md)، [Scatter Plot](scatter-plot.md) و [Aging Chart](aging-chart.md)
4. [Burnup](burnup-chart.md) و [Burnup vs Burndown](burnup-vs-burndown.md)
5. [DORA Metrics](dora-metrics.md)، [SLE](service-level-expectation.md) و [Dashboard Design](dashboard-design.md)
6. [Formula Reference](formulas.md)، [Glossary](glossary.md)، [Interview Notes](interview-notes.md) و [References](references.md)

---

## پایان روز

- Formulas
- Glossary
- Interview Notes
- References

---

# آنچه در پایان Day 5 خواهید آموخت

✅ تحلیل Flow تیم

✅ شناسایی Bottleneckها

✅ اندازه‌گیری عملکرد Kanban

✅ Forecast دقیق‌تر

✅ تحلیل کیفیت DevOps

✅ طراحی Dashboardهای مدیریتی

✅ ساخت KPIهای Enterprise

---

# ارتباط با Day 6

پس از پایان این بخش وارد مباحث پیشرفته Jira Administration خواهیم شد، از جمله:

- Advanced JQL
- Automation
- Workflow Design
- Permission Scheme
- Notification Scheme
- Screen Scheme
- Issue Security
- Custom Fields
- REST API
- ScriptRunner
- Enterprise Administration

این بخش‌ها برای Jira Administrator و Solution Architect ضروری هستند.
