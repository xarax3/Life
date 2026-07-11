````markdown id="d6p6arch"
# File: Life/Agile/Jira/06-Advanced-Scrum-and-Jira-Scrum-Administration/scrum-enterprise-architecture.md

# Day 6 - Part 6
# Enterprise Scrum Architecture & Advanced Jira Practices

> معماری عملی Scrum در سازمان‌های Enterprise، ارتباط بین تیم‌ها، Jira Administration حرفه‌ای و مدل عملیاتی Agile.

---

# 89. Enterprise Scrum Architecture Overview

در سازمان‌های بزرگ Scrum فقط یک تیم نیست.

معماری معمول:

```text
Business Strategy

↓

Portfolio Management

↓

Products

↓

Teams

↓

Sprints

↓

Delivery

↓

Customer Value
````

---

# 90. Portfolio Level Management

سطح Portfolio مسئول:

* تعیین اهداف کلان
* مدیریت سرمایه‌گذاری
* اولویت‌بندی Initiativeها
* هماهنگی بین محصولات

---

ساختار:

```text
Initiative

↓

Epic

↓

Feature

↓

Story

↓

Task
```

---

# 91. Epic Management در Enterprise

Epic باید:

* Business Value داشته باشد.
* Owner مشخص داشته باشد.
* قابل اندازه‌گیری باشد.
* به چند تیم وابسته نباشد بدون مدیریت Dependency.

---

مثال:

```text
Epic:

Digital Customer Platform


Features:

- Registration
- Authentication
- Payment
- Notification
```

---

# 92. Feature Management

Feature بین Epic و Story قرار می‌گیرد.

ساختار:

```text
Epic

↓

Feature

↓

Story

↓

Task
```

---

هدف:

شکستن کارهای بزرگ به بخش‌های قابل Delivery.

---

# 93. Multi Team Scrum

در Enterprise:

چند تیم روی یک Product کار می‌کنند.

مثال:

```text
Product

├── Backend Team
│
├── Frontend Team
│
├── Mobile Team
│
└── QA Team
```

---

چالش‌ها:

* Dependency
* هماهنگی Release
* Shared Components

---

# 94. Cross Team Dependency Management

Dependency باید قابل مشاهده باشد.

روش‌ها:

* Issue Link
* Dependency Board
* Advanced Roadmaps

---

مثال:

```text
Team A

Needs API

↓

Team B

Creates API
```

---

# 95. Scrum of Scrums

برای هماهنگی چند تیم استفاده می‌شود.

تمرکز:

* Dependency
* Risk
* Integration

---

موضوعات:

نه Status Report.

بلکه:

```
What blocks teams?
What needs coordination?
```

---

# 96. Release Train Concept

در Enterprise Agile:

چند تیم با یک هدف Release کار می‌کنند.

مدل:

```text
Multiple Teams

↓

Integrated Increment

↓

Release
```

---

# 97. Jira Project Strategy

در Enterprise دو مدل رایج وجود دارد.

---

## مدل 1: Project per Team

```text
Team A Project

Team B Project

Team C Project
```

مزایا:

* استقلال تیم

معایب:

* گزارش سخت‌تر

---

## مدل 2: Project per Product

```text
Product Project

All Teams
```

مزایا:

* Visibility بهتر

معایب:

* Governance مهم‌تر

---

# 98. Jira Issue Type Strategy

پیشنهاد Enterprise:

```text
Initiative

Epic

Story

Task

Bug

Sub-task

Spike
```

---

# 99. Spike Management

Spike برای تحقیق فنی است.

مثال:

```text
Investigate Database Migration Options
```

---

هدف:

کاهش عدم قطعیت.

---

# 100. Technical Debt Management

Technical Debt باید Visible باشد.

روش:

Issue Type:

```text
Technical Debt
```

یا:

Component:

```text
Technical Debt
```

---

Metric:

```
Technical Debt Trend
```

---

# 101. Jira Dashboard Architecture

ساختار پیشنهادی:

## Executive Dashboard

نمایش:

* Portfolio Progress
* Release Status
* Risk

---

## Product Dashboard

نمایش:

* Epic Progress
* Roadmap
* Backlog Health

---

## Team Dashboard

نمایش:

* Sprint Progress
* Blockers
* Burndown

---

## Operations Dashboard

نمایش:

* Incidents
* SLA
* Support Load

---

# 102. Jira Filters Strategy

Filterهای استاندارد:

## My Open Issues

```jql
assignee = currentUser()
AND statusCategory != Done
```

---

## Blocked Issues

```jql
status = Blocked
```

---

## Aging Issues

```jql
created <= -30d
AND statusCategory != Done
```

---

# 103. Jira Automation Governance

Automation زیاد بدون کنترل مشکل ایجاد می‌کند.

---

Best Practice:

برای هر Rule:

ثبت شود:

```
Purpose

Owner

Trigger

Action

Impact
```

---

# 104. Enterprise Jira Documentation

مستندات ضروری:

```text
Project Standards

Workflow Catalog

Field Catalog

Permission Model

Automation Inventory

Dashboard Catalog
```

---

# 105. Jira Change Management

تغییرات Jira باید فرآیند داشته باشند.

مدل:

```text
Request

↓

Impact Analysis

↓

Approval

↓

Implementation

↓

Documentation
```

---

# 106. Agile Metrics Governance

هر Metric باید:

* هدف مشخص داشته باشد.
* Owner داشته باشد.
* Action مشخص ایجاد کند.

---

مثال:

Metric:

```
Cycle Time ↑
```

Action:

```
Analyze Bottleneck
```

---

# 107. Enterprise Scrum Anti Pattern

## Feature Team بدون Product Ownership

مشکل:

تیم فقط Task انجام می‌دهد.

---

## راه‌حل:

Product Vision و Prioritization مشخص شود.

---

# 108. Enterprise Scrum Anti Pattern

## بیش از حد Scaling Framework

مشکل:

فرآیند زیاد، ارزش کم.

---

راه‌حل:

ابتدا:

```
Simple Scrum

+

Good Engineering Practices
```

---

# 109. Senior Jira Admin Architecture View

یک Senior Admin باید این زنجیره را ببیند:

```text
Business Goal

↓

Agile Process

↓

Jira Design

↓

Workflow

↓

Automation

↓

Metrics

↓

Improvement
```

---

# Day 6 Part 6 Summary

موضوعات:

✓ Enterprise Scrum Architecture
✓ Portfolio Management
✓ Multi Team Scrum
✓ Dependency Management
✓ Jira Project Strategy
✓ Dashboard Architecture
✓ Automation Governance
✓ Documentation
✓ Change Management

---

# Next Part

Day 6 - Part 7:

* Final Scrum Enterprise Blueprint
* Jira Administration Checklist
* Production Jira Governance Model
* Complete Day 6 Summary

```
```
