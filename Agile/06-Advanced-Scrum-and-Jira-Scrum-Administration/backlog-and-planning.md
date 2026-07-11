```markdown id="m7k2q"
# File: Life/Agile/Jira/06-Advanced-Scrum-and-Jira-Scrum-Administration/backlog-and-planning.md

# Day 6 - Part 2
# Backlog Refinement, Estimation & Sprint Planning

> مدیریت حرفه‌ای Backlog، تخمین کار، آماده‌سازی Sprint و استانداردهای Planning در Jira.

---

# 15. Backlog Refinement

## Definition

Backlog Refinement جلسه‌ای است که در آن تیم:

- Issueها را بررسی می‌کند.
- نیازمندی‌ها را شفاف می‌کند.
- Acceptance Criteria را تکمیل می‌کند.
- اندازه کار را تخمین می‌زند.
- Dependencyها را مشخص می‌کند.

---

# هدف Refinement

هدف:

```

Create Sprint Ready Items

```

یعنی Itemهایی که آماده ورود به Sprint باشند.

---

# خروجی Refinement

بعد از Refinement:

```

Story

*

Acceptance Criteria

*

Estimate

*

Priority

*

Dependency

```

باید مشخص باشد.

---

# زمان‌بندی Refinement

Best Practice:

حدود:

```

5% - 10%

از ظرفیت تیم

```

---

مثال:

Sprint دو هفته‌ای:

```

2 تا 4 ساعت Refinement

```

---

# 16. Backlog Refinement در Jira

فرآیند:

```

Backlog

↓

Review Issue

↓

Update Description

↓

Add Acceptance Criteria

↓

Estimate

↓

Prioritize

```

---

# Jira Fields مهم در Refinement

## Summary

عنوان واضح.

---

## Description

شرح نیازمندی.

---

## Acceptance Criteria

شرایط پذیرش.

---

## Priority

اهمیت کسب‌وکاری.

---

## Story Point

اندازه کار.

---

## Component

بخش فنی یا محصولی.

---

## Fix Version

نسخه هدف.

---

# 17. Estimation Techniques

تخمین یعنی:

پیش‌بینی نسبی تلاش مورد نیاز.

---

# روش‌های رایج:

## 1. Story Point

رایج‌ترین روش Scrum.

---

## 2. Ideal Hours

تخمین بر اساس زمان ایده‌آل.

---

## 3. T-Shirt Size

اندازه:

```

XS

S

M

L

XL

```

---

## 4. Bucket System

تقسیم کارها در دسته‌های اندازه.

---

# 18. Story Point

Story Point زمان نیست.

معیار:

```

Complexity

*

Effort

*

Uncertainty

```

---

مثال:

Story A:

```

Complexity: Low

Effort: Low

Risk: Low

= 3 SP

```

---

Story B:

```

Complexity: High

Risk: High

= 13 SP

```

---

# 19. Fibonacci Scale

معمولاً:

```

1

2

3

5

8

13

21

```

استفاده می‌شود.

---

# چرا Fibonacci؟

زیرا هرچه کار بزرگ‌تر شود:

- عدم قطعیت بیشتر می‌شود.
- تخمین دقیق سخت‌تر می‌شود.

---

# 20. Planning Poker

روش تخمین گروهی.

مراحل:

```

Read Story

↓

Discuss

↓

Vote

↓

Reveal

↓

Discuss Difference

↓

Final Estimate

```

---

# مزایای Planning Poker

- جلوگیری از Bias
- استفاده از تجربه تیم
- ایجاد توافق

---

# 21. Large Story Problem

Story بزرگ:

```

Epic

↓

Large Story

↓

Hard Estimation

```

مشکل:

- Cycle Time بالا
- Risk بالا
- Feedback دیر

---

# راه‌حل:

Split کردن Story.

---

# Story Splitting Techniques

## Split by Workflow

مثال:

```

Order

↓

Create Order

↓

Approve Order

↓

Cancel Order

```

---

## Split by Business Rule

مثال:

```

Payment

↓

Credit Card

↓

Wallet

↓

Bank Transfer

```

---

## Split by User Type

مثال:

```

User Login

↓

Customer Login

↓

Admin Login

```

---

# 22. Capacity Planning

Capacity یعنی:

توان واقعی تیم برای Sprint.

---

فرمول:

```

Capacity

=

Available Working Time

×

Focus Factor

```

---

مثال:

5 نفر:

```

5 × 10 Days × 8 Hours

=

400 Hours

```

Focus Factor:

70%

```

400 × 0.7

=

280 Hours

```

---

# عوامل کاهش Capacity

- مرخصی
- جلسات
- Support Work
- Production Issue
- Technical Debt

---

# 23. Sprint Planning

هدف:

تعریف Sprint Goal و Sprint Backlog.

---

فرآیند:

```

Product Backlog

↓

Select Items

↓

Estimate Capacity

↓

Create Sprint Goal

↓

Start Sprint

```

---

# Sprint Goal

هدف اصلی Sprint.

مثال:

ضعیف:

```

Complete 20 Issues

```

خوب:

```

Enable Customer Registration Flow

```

---

# 24. Sprint Planning در Jira

مراحل:

```

Backlog

↓

Create Sprint

↓

Move Issues

↓

Set Sprint Goal

↓

Start Sprint

```

---

# 25. Sprint Scope Management

در طول Sprint:

تغییر Scope باید کنترل شود.

---

مشکل:

```

Continuous Scope Change

↓

Sprint Failure

```

---

راهکار:

- Negotiate Scope
- Protect Sprint Goal

---

# 26. Sprint Best Practices

✓ Sprint Goal مشخص

✓ Storyهای کوچک

✓ ظرفیت واقعی

✓ Dependency مشخص

✓ Definition of Done آماده

---

# Senior Jira Admin نکات مهم

Jira Admin باید بتواند:

```

Configure Boards

Manage Backlog

Create Filters

Manage Workflow

Support Scrum Events

Build Reports

```

---

# Day 6 Part 2 Summary

موضوعات:

✓ Backlog Refinement  
✓ Jira Backlog Management  
✓ Estimation Techniques  
✓ Story Point  
✓ Planning Poker  
✓ Story Splitting  
✓ Capacity Planning  
✓ Sprint Planning  

---

ادامه Day 6 - Part 3:

- Jira Scrum Configuration
- Board Design
- Workflow Design برای Scrum
- Sprint Reports
- Velocity Management
- Release Planning
- Enterprise Scrum Governance
```
