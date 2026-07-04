# Jira Reporting Fundamentals (Part 1)

> سطح: Beginner → Advanced
>
> این بخش پایه تمام گزارش‌گیری در Jira است. قبل از یادگیری Velocity، Burndown یا eazyBI باید این مفاهیم را کاملاً درک کنید.

---

# Table of Contents

1. Jira Reporting Architecture
2. Data Flow in Jira
3. Report چیست؟
4. Dashboard چیست؟
5. Gadget چیست؟
6. Filter چیست؟
7. JQL چیست؟
8. ارتباط بین آن‌ها
9. بهترین روش طراحی داشبورد
10. نکات مهم

---

# 1. Jira Reporting Architecture

معماری گزارش‌گیری در Jira بسیار ساده اما قدرتمند است.

```

```
                     Issue
                       │
                       ▼
                  Workflow
                       │
                       ▼
                 Stored Data
                       │
         ┌─────────────┴─────────────┐
         │                           │
         ▼                           ▼
      JQL Filter                  Reports
         │                           │
         └─────────────┬─────────────┘
                       ▼
                   Gadgets
                       │
                       ▼
                  Dashboard
```

---

تمام گزارش‌های Jira در نهایت از **Issue**ها تولید می‌شوند.

اگر Issueها اطلاعات درستی نداشته باشند، هیچ گزارشی معتبر نخواهد بود.

به همین دلیل همیشه گفته می‌شود:

> **Good Reports Start with Good Data**

---

# 2. Data Flow

فرض کنید یک Story ایجاد می‌کنید.

```
Story

↓

Estimate = 8

↓

Sprint 12

↓

In Progress

↓

Done
```

Jira اطلاعات زیر را ذخیره می‌کند:

- زمان ایجاد
- زمان شروع
- زمان پایان
- شخص مسئول
- Sprint
- Story Point
- Version
- Labels
- Components
- Priority
- Status History

همین اطلاعات بعداً گزارش‌ها را می‌سازند.

---

# 3. Report چیست؟

Report یک تحلیل از اطلاعات موجود در Jira است.

مثال:

```
Velocity Report

↓

آخرین ۱۰ Sprint

↓

Velocity Team
```

یا

```
Burndown

↓

Remaining Work
```

Report معمولاً برای پاسخ به یک سؤال مشخص ساخته می‌شود.

مثلاً:

- آیا Sprint موفق بوده؟
- چه مقدار کار باقی مانده؟
- چند Bug داریم؟
- چه زمانی Release آماده می‌شود؟

---

## ویژگی‌های Report

✔ معمولاً Historical است.

✔ برای تحلیل استفاده می‌شود.

✔ قابل Export است.

✔ معمولاً نمودار دارد.

✔ اطلاعات را خلاصه می‌کند.

---

# 4. Dashboard چیست؟

Dashboard یک صفحه است که چندین Gadget را کنار هم نمایش می‌دهد.

نمونه:

```
+-------------------------------------------+
| Sprint Health | Velocity | Burndown       |
+-------------------------------------------+
| Critical Bugs | Activity Stream           |
+-------------------------------------------+
| Pie Chart     | My Open Issues            |
+-------------------------------------------+
```

Dashboard مانند داشبورد خودرو است.

شما سرعت، بنزین، دما و دور موتور را هم‌زمان می‌بینید.

در Jira نیز چندین شاخص را کنار هم مشاهده می‌کنید.

---

## کاربرد Dashboard

- مانیتورینگ لحظه‌ای
- مدیریت پروژه
- Daily Meeting
- Scrum Board
- Executive Dashboard
- نمایش روی مانیتور اتاق تیم

---

# 5. Gadget چیست؟

هر بخش داخل Dashboard را Gadget می‌گویند.

مثال:

```
Velocity Chart
```

یک Gadget است.

```
Pie Chart
```

یک Gadget دیگر است.

```
Activity Stream
```

یک Gadget دیگر.

Dashboard از چندین Gadget تشکیل می‌شود.

---

## مثال

```
Dashboard

├── Velocity Gadget

├── Burndown Gadget

├── Pie Chart Gadget

├── Assigned To Me Gadget

└── Activity Stream Gadget
```

---

# 6. Filter چیست؟

Filter مجموعه‌ای از Issueها است.

مثلاً:

```
همه Bugهای پروژه ABC
```

یا

```
تمام Issueهای Sprint فعلی
```

یا

```
تمام Issueهای High Priority
```

Filter هیچ نموداری ندارد.

فقط داده را انتخاب می‌کند.

---

## مثال

```
Project = CRM

AND

Priority = High

AND

Status != Done
```

خروجی:

```
34 Issue
```

---

# 7. JQL چیست؟

JQL

=

Jira Query Language

زبان جستجوی Jira است.

مثال

```sql
project = CRM
```

یا

```sql
assignee=currentUser()
```

یا

```sql
Sprint in openSprints()
```

تقریباً تمام Dashboardها و Reportهای سفارشی بر پایه JQL ساخته می‌شوند.

---

# رابطه JQL و Filter

```
JQL

↓

Filter

↓

Dashboard

↓

Report
```

---

# مثال واقعی

فرض کنید مدیر پروژه می‌خواهد:

```
تمام Bugهای Critical
```

ابتدا JQL می‌نویسد:

```sql
project = CRM
AND issuetype = Bug
AND priority = Highest
```

سپس آن را ذخیره می‌کند.

```
Critical Bugs
```

حالا این Filter را داخل Dashboard قرار می‌دهد.

---

# 8. ارتباط بین اجزا

```
Issue

↓

Workflow

↓

Database

↓

JQL

↓

Saved Filter

↓

Gadget

↓

Dashboard

↓

Manager
```

اگر یکی از این مراحل اشتباه باشد، گزارش نیز اشتباه خواهد بود.

---

# 9. چرا بعضی گزارش‌ها اشتباه هستند؟

دلایل رایج:

❌ Story Point وارد نشده است.

❌ Sprint انتخاب نشده است.

❌ Workflow اشتباه است.

❌ Issue به Version وصل نشده است.

❌ Statusها استاندارد نیستند.

❌ کاربران Worklog ثبت نمی‌کنند.

❌ Resolution تنظیم نشده است.

---

# 10. اصل طلایی گزارش‌گیری

بسیاری از مدیران فکر می‌کنند مشکل از Dashboard است.

در ۹۰٪ مواقع مشکل از کیفیت داده‌هاست.

اگر داده‌ها ناقص باشند:

- Velocity اشتباه می‌شود.
- Burndown اشتباه می‌شود.
- Capacity اشتباه می‌شود.
- Release Forecast اشتباه می‌شود.

به همین دلیل اولین وظیفه Jira Admin همیشه حفظ کیفیت داده‌هاست.

---

# خلاصه

```
Issue

↓

Data

↓

JQL

↓

Filter

↓

Gadget

↓

Dashboard

↓

Decision
```

هرچه داده‌ها دقیق‌تر باشند، تصمیم‌های مدیریتی بهتر خواهند بود.
