````markdown id="j6p3md"
# File: Life/Agile/Jira/06-Advanced-Scrum-and-Jira-Scrum-Administration/jira-scrum-configuration.md

# Day 6 - Part 3
# Jira Scrum Configuration & Sprint Management

> پیکربندی حرفه‌ای Jira برای Scrum، طراحی Board، Workflow، Sprint Management و گزارش‌گیری تیم‌های Agile.

---

# 27. Jira Scrum Project Architecture

ساختار استاندارد یک پروژه Scrum در Jira:

```text
Project

↓

Issue Types

↓

Workflows

↓

Boards

↓

Backlog

↓

Sprints

↓

Reports
````

---

# 28. Jira Scrum Board

Board در Jira نمایش Visual Workflow تیم است.

دو نوع اصلی:

* Scrum Board
* Kanban Board

---

# Scrum Board مناسب برای:

* Sprint Based Delivery
* Iteration Planning
* Velocity Tracking

---

# Kanban Board مناسب برای:

* Continuous Flow
* Support Team
* Service Delivery

---

# 29. ساخت Scrum Board در Jira

مسیر:

```text
Projects

↓

Create Board

↓

Scrum Board

↓

Select Project

↓

Configure
```

---

# 30. Board Configuration

مسیر:

```text
Board

↓

Configure
```

بخش‌ها:

* Columns
* Swimlanes
* Quick Filters
* Card Layout
* Estimation
* Working Days

---

# 31. Column Design

Workflow واقعی باید با Board هماهنگ باشد.

مثال:

```text
To Do

↓

In Progress

↓

Code Review

↓

Testing

↓

Done
```

---

# 32. Status vs Column

تفاوت مهم:

## Status

وضعیت واقعی Issue در Workflow است.

مثال:

```
Code Review
```

---

## Column

نمایش Status روی Board است.

مثال:

```
Review Column
```

ممکن است چند Status داشته باشد.

---

# 33. Workflow Design برای Scrum

Workflow پیشنهادی:

```text
Open

↓

To Do

↓

In Progress

↓

Code Review

↓

Testing

↓

Done
```

---

# 34. Workflow Anti Pattern

Workflow خیلی پیچیده:

```text
Open

↓

Analysis

↓

Approval

↓

Review

↓

Manager Approval

↓

Technical Approval

↓

QA Approval

↓

Testing

↓

Release Approval

↓

Done
```

مشکل:

* افزایش Lead Time
* کاهش Flow
* گزارش سخت

---

# 35. Definition of Done در Jira

می‌تواند با:

* Workflow Condition
* Validator
* Automation

پیاده‌سازی شود.

مثال:

قبل از Done:

بررسی:

```
Code Review Completed

+

Test Passed

+

Documentation Updated
```

---

# 36. Jira Sprint Lifecycle

چرخه Sprint:

```text
Create Sprint

↓

Backlog Selection

↓

Sprint Planning

↓

Start Sprint

↓

Daily Execution

↓

Sprint Review

↓

Sprint Retrospective

↓

Close Sprint
```

---

# 37. Start Sprint در Jira

قبل از Start:

بررسی:

✓ Sprint Goal

✓ Selected Issues

✓ Capacity

✓ Dependencies

---

# 38. During Sprint Management

در طول Sprint:

مدیریت:

* Blockers
* Scope Change
* Impediments
* Progress

---

# 39. Sprint Report

مسیر:

```text
Board

↓

Reports

↓

Sprint Report
```

---

نمایش:

* Completed Issues
* Removed Issues
* Added Issues
* Burndown

---

# 40. Velocity Chart

مسیر:

```text
Board

↓

Reports

↓

Velocity Chart
```

---

نمایش:

```
Committed Work

vs

Completed Work
```

---

# Velocity Best Practice

Velocity برای:

✓ Forecast همان تیم

است.

استفاده نمی‌شود برای:

❌ مقایسه تیم‌ها

❌ ارزیابی افراد

---

# 41. Release Planning

هدف:

پیش‌بینی زمان تحویل Version.

---

ورودی‌ها:

* Velocity
* Backlog Size
* Dependencies
* Capacity

---

# مثال:

Backlog:

```
200 Story Points
```

Velocity:

```
40 SP / Sprint
```

Forecast:

```
5 Sprint
```

---

# 42. Version Management در Jira

مسیر:

```text
Project Settings

↓

Versions
```

---

Version شامل:

* Release Date
* Issues
* Progress

---

# 43. Release Burndown

نمایش:

```
Remaining Work

vs

Release Date
```

---

# 44. Advanced Roadmaps

برای Enterprise Planning:

قابلیت‌ها:

* Multiple Teams
* Capacity Planning
* Dependencies
* Scenario Planning

---

# 45. Scrum Metrics در Jira

مهم‌ترین Metrics:

## Velocity

خروجی Sprint

---

## Commitment Reliability

نسبت:

```
Completed

/

Committed
```

---

## Sprint Completion Rate

درصد Issueهای Done شده.

---

## Carry Over Rate

کارهای منتقل شده به Sprint بعد.

---

# 46. Sprint Health Analysis

بررسی:

## Scope Change

آیا وسط Sprint کار اضافه شده؟

---

## Blocker

آیا کارها متوقف شده‌اند؟

---

## Carry Over

آیا تیم بیش از حد Commit کرده؟

---

# 47. Jira Automation در Scrum

مثال:

وقتی Issue وارد Blocked شد:

```text
Trigger:

Status Changed


Action:

Notify Scrum Master
```

---

مثال:

وقتی Sprint تمام شد:

```text
Trigger:

Sprint Completed


Action:

Create Report Task
```

---

# 48. Enterprise Scrum Governance

در سازمان بزرگ:

استانداردسازی:

* Issue Types
* Workflow
* Fields
* Naming
* Reports

ضروری است.

---

# 49. Scrum Scaling

در Enterprise:

مدل‌ها:

* SAFe
* LeSS
* Nexus

---

# 50. Jira Admin Checklist برای Scrum

```text
✓ Project Template

✓ Issue Types

✓ Workflow

✓ Board Configuration

✓ Permissions

✓ Screens

✓ Custom Fields

✓ Reports

✓ Automation

✓ Governance
```

---

# Day 6 Part 3 Summary

موضوعات:

✓ Jira Scrum Architecture
✓ Board Configuration
✓ Workflow Design
✓ Sprint Lifecycle
✓ Sprint Reports
✓ Velocity Management
✓ Release Planning
✓ Advanced Roadmaps
✓ Enterprise Governance

---

ادامه Day 6 - Part 4:

* Scrum Anti Patterns
* Enterprise Jira Best Practices
* Performance & Governance
* Jira Admin Interview Scenarios
* Final Scrum Architecture

```
```
