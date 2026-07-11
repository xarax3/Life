# Jira Agile Dashboard Design

> طراحی داشبورد حرفه‌ای در Jira برای نمایش وضعیت تیم، Flow Metrics، Sprint Health، DevOps Metrics و شاخص‌های مدیریتی.

---

# Definition

Jira Dashboard مجموعه‌ای از:

- Gadgetها
- Filterها
- گزارش‌ها
- KPIها

است که برای نمایش اطلاعات موردنیاز کاربران استفاده می‌شود.

---

# هدف Dashboard

یک Dashboard خوب باید پاسخ دهد:

- وضعیت فعلی چیست؟
- چه چیزی Block شده؟
- آیا تیم طبق برنامه پیش می‌رود؟
- چه ریسک‌هایی وجود دارد؟
- روند عملکرد چگونه است؟

---

# اصول طراحی Dashboard

## 1. مخاطب را مشخص کنید

هر Role داشبورد متفاوت نیاز دارد.

| Role | نیاز |
|-|-|
| Developer | Task و Blocker |
| Scrum Master | Flow و Sprint |
| Product Owner | Backlog و Release |
| Manager | KPI و Trend |
| Executive | وضعیت کلان |

---

# Dashboard Team Level

هدف:

نمایش وضعیت روزانه تیم.

---

## Gadgetهای پیشنهادی

### Sprint Burndown

مسیر:

```
Dashboard

↓

Add Gadget

↓

Sprint Burndown
```

نمایش:

- Remaining Work
- Sprint Progress

---

### Sprint Health

نمایش:

- Sprint Goal
- Issue Status
- Progress

---

### Filter Results

برای:

- Blocked Issues
- Critical Bugs
- Open Tasks

---

### Created vs Resolved Chart

نمایش:

```
Created Issues

vs

Resolved Issues
```

---

# Team Dashboard نمونه

```
--------------------------------
Sprint Burndown

--------------------------------
Blocked Issues

--------------------------------
Aging Work Items

--------------------------------
Velocity Trend

--------------------------------
```

---

# Scrum Master Dashboard

تمرکز:

Flow + Predictability

---

Gadgetها:

- Velocity Chart
- Burndown
- Control Chart
- Cumulative Flow Diagram
- Created vs Resolved

---

# Product Owner Dashboard

تمرکز:

Value Delivery

---

Gadgetها:

- Release Progress
- Burnup Chart
- Epic Progress
- Version Report
- Roadmap

---

# Management Dashboard

تمرکز:

Executive View

---

شاخص‌ها:

- Delivery Status
- Release Forecast
- Velocity Trend
- Defect Trend
- SLA Compliance

---

# Enterprise Dashboard

در سازمان‌های بزرگ:

Jira باید با ابزارهای دیگر ترکیب شود:

```
Jira

+

Confluence

+

Git

+

CI/CD

+

Monitoring
```

---

# Flow Dashboard

برای Kanban:

تمرکز روی:

- Lead Time
- Cycle Time
- Throughput
- WIP
- Aging

---

## Flow Dashboard Example

```
--------------------------------
Cycle Time Trend

--------------------------------
Control Chart

--------------------------------
WIP Status

--------------------------------
Aging Items

--------------------------------
Throughput
--------------------------------
```

---

# DevOps Dashboard

ترکیب Jira + CI/CD

نمایش:

- Deployment Frequency
- Lead Time for Changes
- Change Failure Rate
- MTTR

---

# JQL در Dashboard

Dashboard بدون Filter مناسب ارزش کمی دارد.

---

## مثال Blocked Issues

```jql
status = Blocked
```

---

## مثال Critical Bugs

```jql
issuetype = Bug
AND priority = Highest
AND status != Done
```

---

## مثال Aging Issues

```jql
statusCategory != Done
AND created <= -14d
```

---

# Dashboard Permissions

در Jira باید مدیریت شود:

- Viewers
- Editors
- Shares

---

# Best Practice

Dashboard مدیریتی:

```
Private

↓

Team Share

↓

Organization Share
```

---

# اشتباهات رایج

## 1. Dashboard شلوغ

❌ تعداد زیاد Gadget

---

## 2. نمایش Metric بدون Context

مثلاً:

```
Velocity = 50
```

بدون مقایسه معنی ندارد.

---

## 3. KPI زیاد

تمرکز روی شاخص‌های مهم.

---

## 4. استفاده برای کنترل افراد

Dashboard باید برای بهبود سیستم باشد.

---

# Dashboard و OKR

Dashboard می‌تواند برای نمایش:

- Objective
- Key Result
- Progress

استفاده شود.

---

# Dashboard و ITIL

برای Jira Service Management:

نمایش:

- Incident
- SLA
- Change
- Problem
- Request

---

# JSM Dashboard Example

```
--------------------------------
Open Incidents

--------------------------------
SLA Breaches

--------------------------------
MTTR

--------------------------------
Major Incidents

--------------------------------
Change Success Rate
```

---

# ابزارهای پیشرفته

برای Enterprise:

- eazyBI
- Atlassian Analytics
- Power BI
- Grafana
- Custom REST API Dashboard

---

# طراحی Dashboard حرفه‌ای

قانون:

```
Question

↓

Metric

↓

Gadget

↓

Action
```

مثال:

Question:

چرا Delivery کند شده؟

Metric:

Cycle Time

Action:

Reduce WIP

---

# Interview Questions

### Dashboard خوب چه ویژگی دارد؟

اطلاعات درست را به فرد درست در زمان مناسب نشان دهد.

---

### آیا همه کاربران باید یک Dashboard داشته باشند؟

خیر. Roleها نیازهای متفاوت دارند.

---

### بهترین Dashboard برای Scrum Master چیست؟

ترکیبی از:

- Burndown
- Velocity
- CFD
- Control Chart

---

### بهترین Dashboard برای مدیر چیست؟

KPIهای سطح بالا:

- Delivery
- Quality
- Risk
- Trend

---

# Summary

| Dashboard | تمرکز |
|-|-|
| Team | Sprint Execution |
| Scrum Master | Flow |
| Product Owner | Value |
| Manager | KPI |
| Executive | Strategy |

---

# Enterprise Tips

## 1. Dashboard را Role Based طراحی کنید.

---

## 2. Metric بدون Action ایجاد نکنید.

---

## 3. Trend مهم‌تر از Snapshot است.

---

## 4. Flow Metrics را در کنار Delivery Metrics قرار دهید.

---

## 5. Dashboard باید تصمیم‌سازی کند، نه فقط گزارش بدهد.
