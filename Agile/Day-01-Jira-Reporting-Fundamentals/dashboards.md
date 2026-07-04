# Jira Dashboards

> Dashboard اولین صفحه‌ای است که مدیران، Scrum Masterها، Product Ownerها و تیم توسعه برای مشاهده وضعیت پروژه باز می‌کنند.

---

# Table of Contents

1. Dashboard چیست؟
2. Dashboard Architecture
3. Dashboard Components
4. انواع Dashboard
5. Dashboard Permissions
6. Favorite Dashboards
7. Dashboard Layout
8. Dashboard Best Practices
9. Dashboard Design Patterns
10. Common Mistakes

---

# 1. Dashboard چیست؟

Dashboard مجموعه‌ای از Gadgetهاست که اطلاعات پروژه را به‌صورت زنده (Live) نمایش می‌دهد.

هدف Dashboard این نیست که داده‌ها را تحلیل کند؛ هدف آن نمایش سریع وضعیت فعلی پروژه است.

به عبارت دیگر:

> Dashboard = نمای کلی پروژه

---

# معماری Dashboard

```
Issues
    │
    ▼
Workflow
    │
    ▼
Database
    │
    ▼
JQL Filter
    │
    ▼
Gadget
    │
    ▼
Dashboard
```

---

# Dashboard از چه چیزهایی تشکیل شده است؟

هر Dashboard معمولاً شامل این اجزا است:

- Gadget
- Filter
- JQL
- Layout
- Permission
- Refresh Interval

---

# Dashboard Layout

Jira اجازه می‌دهد Dashboard را در چند ستون طراحی کنید.

نمونه:

```
+-------------+-------------+
| Gadget      | Gadget      |
+-------------+-------------+
| Gadget      | Gadget      |
+-------------+-------------+
| Gadget      | Gadget      |
+-------------+-------------+
```

یا

```
+---------------------------+
|        Gadget             |
+-------------+-------------+
| Gadget      | Gadget      |
+-------------+-------------+
```

---

# Dashboard Refresh

Dashboard به‌صورت خودکار Refresh می‌شود.

بازه Refresh قابل تنظیم است.

مثلاً:

- 1 دقیقه
- 5 دقیقه
- 15 دقیقه
- 30 دقیقه
- دستی (Manual)

اگر Dashboard روی مانیتور تیم نمایش داده می‌شود، معمولاً Refresh روی ۱ تا ۵ دقیقه تنظیم می‌شود.

---

# انواع Dashboard

## 1. Personal Dashboard

فقط برای یک کاربر.

نمونه:

```
My Open Issues

My Sprint

My Worklog
```

---

## 2. Team Dashboard

برای کل تیم.

معمولاً شامل:

- Sprint Health
- Burndown
- Velocity
- Active Sprint
- Blocked Issues

---

## 3. Project Dashboard

برای یک پروژه خاص.

نمونه:

```
CRM Dashboard

Velocity

Burndown

Open Bugs

Release Progress
```

---

## 4. Executive Dashboard

برای مدیران ارشد.

هدف:

مشاهده وضعیت کلی پروژه‌ها بدون ورود به جزئیات.

معمولاً شامل:

- Release Health
- Critical Bugs
- Velocity Trend
- Delivery Status
- Risk Summary

---

## 5. Portfolio Dashboard

برای چندین پروژه.

نمونه:

```
Project A

Project B

Project C

Project D
```

مدیر PMO معمولاً از این Dashboard استفاده می‌کند.

---

# Dashboard Permission

هر Dashboard می‌تواند یکی از این حالت‌ها را داشته باشد:

## Private

فقط خودتان می‌بینید.

---

## Shared

با یک Team

یا Group

یا Project

به اشتراک گذاشته می‌شود.

---

## Public

همه کاربران Jira می‌توانند آن را مشاهده کنند.

در محیط‌های Enterprise معمولاً این گزینه محدود می‌شود.

---

# Favorite Dashboard

اگر Dashboard خاصی را زیاد استفاده می‌کنید، آن را Favorite کنید.

مزایا:

- دسترسی سریع
- نمایش در Home
- جستجوی راحت‌تر

---

# Dashboard Ownership

هر Dashboard یک Owner دارد.

Owner می‌تواند:

- Dashboard را ویرایش کند.
- Gadget اضافه کند.
- Permission تغییر دهد.
- Dashboard را حذف کند.

اگر Owner از شرکت خارج شود، بهتر است مالکیت Dashboard به مدیر تیم منتقل شود.

---

# Dashboard Naming Convention

بهتر است از نام‌های استاندارد استفاده کنید.

خوب:

```
CRM Sprint Dashboard

CRM Executive Dashboard

QA Dashboard

DevOps Dashboard
```

بد:

```
Dashboard 1

Test

New Dashboard

Ali Dashboard
```

---

# Dashboard Design Pattern

## Executive

```
Release Health

Velocity Trend

Critical Bugs

Risk Summary
```

---

## Scrum

```
Sprint Health

Burndown

Velocity

Blocked Issues

Activity Stream
```

---

## Product Owner

```
Epic Progress

Roadmap

Version Report

Open Stories
```

---

## QA

```
Open Bugs

Severity

Resolution Time

Created vs Resolved
```

---

## DevOps

```
Deployment

MTTR

Failed Deployments

Lead Time
```

---

# Dashboard Size

هر Dashboard نباید بیش از حد شلوغ باشد.

پیشنهاد Atlassian:

۶ تا ۱۰ Gadget

نه بیشتر.

---

# Dashboard Loading

هر Gadget یک Query اجرا می‌کند.

اگر Dashboard شامل:

۳۰ Gadget

باشد،

سرعت Dashboard کاهش پیدا می‌کند.

---

# Dashboard Performance

برای Dashboard سریع‌تر:

✔ از Saved Filter استفاده کنید.

✔ Queryهای پیچیده ننویسید.

✔ Gadgetهای غیرضروری را حذف کنید.

✔ Dashboardهای مختلف برای نقش‌های مختلف بسازید.

---

# Dashboard Sharing Best Practice

بهتر است:

هر Team

Dashboard مخصوص خود را داشته باشد.

به جای:

یک Dashboard بزرگ برای همه.

---

# Dashboard Lifecycle

```
Create

↓

Add Gadgets

↓

Share

↓

Review

↓

Improve

↓

Archive
```

Dashboardها نیز باید مانند پروژه‌ها بازبینی و به‌روزرسانی شوند.

---

# Dashboard Review Checklist

هر چند ماه یک‌بار بررسی کنید:

- آیا Gadgetها هنوز کاربرد دارند؟
- آیا Queryها صحیح هستند؟
- آیا Dashboard کند شده است؟
- آیا کاربران از آن استفاده می‌کنند؟
- آیا Permissionها مناسب هستند؟

---

# Common Mistakes

❌ قرار دادن ۲۰ یا ۳۰ Gadget در یک Dashboard

---

❌ استفاده از Dashboard برای گزارش‌های بسیار تخصصی

برای تحلیل عمیق از Report یا eazyBI استفاده کنید.

---

❌ استفاده از Queryهای بسیار سنگین

باعث کند شدن Dashboard می‌شود.

---

❌ استفاده از Dashboard مشترک برای همه نقش‌ها

مدیرعامل، Scrum Master و QA نیازهای متفاوتی دارند.

---

❌ عدم بازبینی Dashboard

Dashboard قدیمی معمولاً اطلاعات غیرضروری نمایش می‌دهد.

---

# چه Dashboardی برای چه کسی؟

| نقش | Dashboard پیشنهادی |
|------|--------------------|
| Developer | Personal Dashboard |
| Scrum Master | Sprint Dashboard |
| Product Owner | Product Dashboard |
| QA Lead | QA Dashboard |
| DevOps | DevOps Dashboard |
| Project Manager | Project Dashboard |
| PMO | Portfolio Dashboard |
| CTO | Executive Dashboard |
| CEO | Executive Dashboard |

---

# Dashboard vs Report

| Dashboard | Report |
|------------|---------|
| Live | Historical |
| چند Gadget | یک تحلیل مشخص |
| مانیتورینگ | تحلیل |
| قابل شخصی‌سازی | معمولاً ثابت |
| مناسب جلسات روزانه | مناسب جلسات تحلیلی |

---

# Enterprise Best Practices

- برای هر نقش Dashboard جداگانه طراحی کنید.
- از Saved Filter به‌جای JQL تکراری استفاده کنید.
- Dashboardها را نام‌گذاری استاندارد کنید.
- تعداد Gadgetها را بین ۶ تا ۱۰ نگه دارید.
- Dashboardها را هر فصل بازبینی کنید.
- از Dashboard برای تصمیم‌گیری لحظه‌ای استفاده کنید، نه تحلیل‌های پیچیده.
- برای KPIهای سفارشی از eazyBI یا افزونه‌های مشابه استفاده کنید.

---

# خلاصه

یک Dashboard خوب باید:

- سریع بارگذاری شود.
- فقط اطلاعات مهم را نمایش دهد.
- متناسب با نقش کاربر طراحی شده باشد.
- از Gadgetهای مرتبط تشکیل شده باشد.
- نیاز به پیمایش زیاد نداشته باشد.
- وضعیت پروژه را در کمتر از یک دقیقه به کاربر منتقل کند.
