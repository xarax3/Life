# Jira Reporting - Interview Notes

> سوالاتی که معمولاً در مصاحبه‌های Jira Administrator، Scrum Master، Product Owner و Project Manager درباره Reporting پرسیده می‌شوند.

---

# Beginner Level

## سوال 1

Dashboard چیست؟

### پاسخ

Dashboard صفحه‌ای شامل چندین Gadget است که وضعیت لحظه‌ای پروژه را نمایش می‌دهد.

Dashboard برای مانیتورینگ استفاده می‌شود و معمولاً از چندین Gadget تشکیل شده است.

---

## سوال 2

Report چیست؟

### پاسخ

Report یک تحلیل از داده‌های Jira است.

مثال:

- Sprint Report
- Velocity Report
- Burndown Report

Report معمولاً برای تحلیل گذشته (Historical Analysis) استفاده می‌شود.

---

## سوال 3

Gadget چیست؟

### پاسخ

Gadget یک Widget داخل Dashboard است.

هر Gadget یک بخش از اطلاعات پروژه را نمایش می‌دهد.

مثال:

- Velocity
- Burndown
- Pie Chart

---

## سوال 4

JQL چیست؟

### پاسخ

JQL مخفف Jira Query Language است.

برای جستجو و فیلتر کردن Issueها استفاده می‌شود.

مثال

```sql
project = CRM
AND status != Done
```

---

## سوال 5

Filter چیست؟

### پاسخ

Filter نسخه ذخیره‌شده یک JQL است.

از Filter می‌توان در:

- Dashboard
- Subscription
- Gadget
- گزارش‌های سفارشی

استفاده کرد.

---

# Intermediate Level

## سوال 6

تفاوت Dashboard و Report چیست؟

### پاسخ

Dashboard

- نمایش وضعیت فعلی
- چندین Gadget
- مناسب مانیتورینگ

Report

- تحلیل داده
- معمولاً یک موضوع مشخص
- مناسب بررسی عملکرد

---

## سوال 7

تفاوت JQL و Filter چیست؟

### پاسخ

JQL یک Query است.

Filter همان Query ذخیره‌شده است.

Filter قابل اشتراک‌گذاری و استفاده مجدد است.

---

## سوال 8

تفاوت Burndown و Burnup چیست؟

### پاسخ

Burndown

↓

کار باقی‌مانده را نشان می‌دهد.

Burnup

↓

کار انجام‌شده را نشان می‌دهد.

اگر Scope تغییر کند، Burnup تصویر دقیق‌تری ارائه می‌دهد.

---

## سوال 9

Velocity چیست؟

### پاسخ

Velocity مجموع Story Pointهای Done در یک Sprint است.

از آن برای پیش‌بینی Sprintهای آینده استفاده می‌شود.

Velocity نباید برای مقایسه افراد یا تیم‌های مختلف استفاده شود.

---

## سوال 10

CFD چیست؟

### پاسخ

Cumulative Flow Diagram

گزارشی برای تحلیل جریان کار است.

این گزارش:

- WIP
- Bottleneck
- Throughput
- Queue

را نمایش می‌دهد.

---

# Advanced Level

## سوال 11

چرا Velocity دو تیم را نباید مقایسه کرد؟

### پاسخ

زیرا Story Point یک معیار نسبی است.

هر تیم ممکن است روش برآورد متفاوتی داشته باشد.

---

## سوال 12

چرا Dashboard کند می‌شود؟

### پاسخ

دلایل رایج:

- Gadget زیاد
- JQLهای پیچیده
- Filterهای غیربهینه
- تعداد زیاد Issueها
- Gadgetهای افزونه‌ای سنگین

---

## سوال 13

اگر Burndown صاف باشد، چه نتیجه‌ای می‌گیرید؟

### پاسخ

احتمالاً:

- کارها Update نشده‌اند.
- اعضا Issueها را به‌روز نمی‌کنند.
- Storyها فقط در پایان Sprint بسته می‌شوند.
- تخمین‌ها یا Workflow مشکل دارند.

---

## سوال 14

اگر Velocity به‌شدت نوسان داشته باشد؟

### پاسخ

احتمال دارد:

- تخمین‌ها نادرست باشند.
- Scope مرتب تغییر کند.
- Capacity تیم متغیر باشد.
- تیم هنوز به ثبات نرسیده باشد.

---

## سوال 15

چرا Created vs Resolved مهم است؟

### پاسخ

اگر تعداد Issueهای ایجادشده بیشتر از Issueهای حل‌شده باشد، Backlog در حال رشد است و ممکن است بدهی فنی یا حجم کار افزایش یابد.

---

# Jira Administrator Questions

## سوال

چگونه Dashboard را با تیم به اشتراک می‌گذارید؟

### پاسخ

```
Dashboard

↓

Share

↓

Project

یا

Group

یا

Role
```

---

## سوال

چگونه Dashboard را سریع‌تر می‌کنید؟

### پاسخ

- استفاده از Saved Filter
- حذف Gadgetهای غیرضروری
- ساده‌سازی JQL
- کاهش تعداد Gadgetها
- تقسیم Dashboard بر اساس نقش

---

## سوال

چرا از Saved Filter استفاده می‌کنید؟

### پاسخ

- استفاده مجدد
- مدیریت آسان
- اشتراک‌گذاری
- کاهش خطا
- یکسان بودن منبع داده در چند Dashboard

---

# Scrum Master Questions

## سوال

مهم‌ترین Report برای Scrum Master چیست؟

### پاسخ

- Sprint Report
- Burndown
- Velocity
- CFD
- Sprint Health

---

## سوال

در Retrospective از چه گزارش‌هایی استفاده می‌کنید؟

### پاسخ

- Sprint Report
- Velocity
- Burndown
- Scope Change
- CFD

---

# Product Owner Questions

## سوال

برای بررسی وضعیت Release از چه گزارشی استفاده می‌کنید؟

### پاسخ

- Version Report
- Release Burndown
- Roadmap

---

## سوال

برای بررسی Epicها؟

### پاسخ

- Epic Report
- Epic Burndown

---

# Project Manager Questions

## سوال

اگر مدیر پروژه باشید، چه Dashboardی طراحی می‌کنید؟

### پاسخ

- Sprint Health
- Velocity
- Burndown
- Critical Bugs
- Created vs Resolved
- Release Progress
- Roadmap

---

# CTO Questions

## سوال

اگر فقط ۵ KPI روی Dashboard CTO داشته باشید، چه مواردی را انتخاب می‌کنید؟

### پاسخ پیشنهادی

- Release Health
- Velocity Trend
- Critical Bugs
- Deployment Success Rate
- Delivery Predictability

---

# سوالات سناریویی

## سناریو 1

Velocity از ۴۰ به ۲۰ کاهش یافته است.

چه مواردی را بررسی می‌کنید؟

### پاسخ

- Capacity
- مرخصی اعضا
- Scope Change
- Bugهای زیاد
- Blocked Issueها
- تغییر تیم
- مشکلات زیرساخت

---

## سناریو 2

Burndown طبیعی نیست.

چه دلایلی ممکن است وجود داشته باشد؟

### پاسخ

- اعضا Issueها را به‌روز نمی‌کنند.
- Workflow اشتباه است.
- Story Pointها تغییر کرده‌اند.
- Scope زیاد تغییر کرده است.
- Sprint به‌درستی تنظیم نشده است.

---

# اشتباهات رایج در مصاحبه

❌ Velocity معیار عملکرد افراد است.

✅ خیر، معیار عملکرد تیم است.

---

❌ Burndown همان Burnup است.

✅ خیر، یکی Remaining Work و دیگری Completed Work را نمایش می‌دهد.

---

❌ Dashboard همان Report است.

✅ Dashboard برای مانیتورینگ است، Report برای تحلیل.

---

❌ JQL همان Filter است.

✅ Filter نسخه ذخیره‌شده JQL است.

---

# Cheat Sheet

| مفهوم | یک جمله برای حفظ کردن |
|--------|------------------------|
| Issue | داده اصلی Jira |
| JQL | زبان جستجو |
| Filter | JQL ذخیره‌شده |
| Gadget | ویجت نمایش داده |
| Dashboard | مجموعه Gadgetها |
| Report | تحلیل داده |
| Velocity | خروجی تیم در Sprint |
| Burndown | کار باقی‌مانده |
| Burnup | کار انجام‌شده |
| CFD | تحلیل جریان کار |
| Control Chart | تحلیل Cycle Time |
