# Jira Dashboard Gadgets

> Gadgets اجزای اصلی Dashboard هستند. هر Gadget داده‌ای را از Jira (معمولاً از طریق Filter یا JQL) نمایش می‌دهد.

---

# Table of Contents

1. Gadget چیست؟
2. نحوه اضافه کردن Gadget
3. دسته‌بندی Gadgetها
4. معرفی Gadgetهای مهم
5. انتخاب Gadget مناسب
6. Best Practices

---

# Gadget چیست؟

Gadget یک ویجت (Widget) است که اطلاعات خاصی را روی Dashboard نمایش می‌دهد.

هر Gadget می‌تواند:

- نمودار باشد.
- جدول باشد.
- لیست باشد.
- آمار باشد.
- گراف باشد.
- Activity باشد.

هر Dashboard معمولاً بین **۶ تا ۱۰ Gadget** دارد.

---

# نحوه اضافه کردن Gadget

```
Dashboard

↓

Add Gadget

↓

Select Gadget

↓

Configure

↓

Save
```

بیشتر Gadgetها هنگام تنظیم از شما می‌خواهند:

- Filter
- Project
- Sprint
- تعداد آیتم
- رنگ یا نمایش

---

# دسته‌بندی Gadgetها

```
Gadgets

├── Agile
├── Issue
├── Chart
├── Statistics
├── Activity
├── Time
└── Custom
```

---

# 1. Filter Results

## کاربرد

نمایش خروجی یک Filter یا JQL.

---

### مثال

JQL

```sql
project = CRM
AND priority = Highest
```

Dashboard

```
Critical Bugs

CRM-21

CRM-33

CRM-81
```

---

### مناسب برای

- مدیر پروژه
- QA
- تیم توسعه

---

### مزایا

- ساده
- سریع
- بسیار پرکاربرد

---

# 2. Assigned to Me

## کاربرد

نمایش تمام Issueهای تخصیص داده‌شده به کاربر فعلی.

---

### مناسب برای

Developer

QA

Business Analyst

---

### مزیت

هر فرد بعد از ورود به Jira فوراً کارهای خود را می‌بیند.

---

# 3. Activity Stream

## کاربرد

نمایش فعالیت‌های اخیر.

---

نمونه

```
Ali created CRM-25

Sara closed CRM-81

Reza updated CRM-18

Mahdi commented on CRM-44
```

---

### مناسب

Daily Monitoring

---

### نکته

در پروژه‌های بزرگ ممکن است اطلاعات بسیار زیادی نمایش دهد؛ بهتر است با Filter محدود شود.

---

# 4. Pie Chart

## کاربرد

نمایش توزیع Issueها.

---

### مثال

بر اساس Priority

```
High

██████

Medium

██████████

Low

██
```

---

### می‌توان بر اساس موارد زیر نمایش داد

- Status
- Assignee
- Priority
- Component
- Label
- Version
- Issue Type

---

### مناسب

مدیر پروژه

Product Owner

---

# 5. Two Dimensional Filter Statistics

## کاربرد

تحلیل دوبعدی Issueها.

---

### مثال

Status × Priority

| Status | High | Medium | Low |
|----------|-----:|-------:|----:|
| To Do | 4 | 8 | 2 |
| In Progress | 2 | 6 | 1 |
| Done | 12 | 18 | 9 |

---

### کاربرد

پاسخ به سؤال:

"چند Bug با اولویت High هنوز Done نشده‌اند؟"

---

# 6. Created vs Resolved Chart

## کاربرد

مقایسه تعداد Issueهای ایجاد شده و حل شده.

---

### مثال

```
Week 1

Created

20

Resolved

18

Week 2

Created

12

Resolved

30
```

---

### تفسیر

اگر همیشه:

Created > Resolved

باشد،

تعداد Issueها در حال افزایش است.

---

### مناسب

QA Lead

Project Manager

---

# 7. Average Age Chart

## کاربرد

نمایش میانگین عمر Issueهای باز.

---

### مثال

```
Average Age

23 Days
```

---

### تفسیر

عدد زیاد

↓

Issueها مدت زیادی باز مانده‌اند.

---

### مناسب

Support Team

Maintenance Team

---

# 8. Resolution Time

## کاربرد

میانگین زمان لازم برای بستن Issueها.

---

### مثال

```
Average Resolution

3.8 Days
```

---

### تفاوت با Average Age

Average Age

↓

Issue هنوز باز است.

Resolution Time

↓

Issue بسته شده است.

---

# 9. Sprint Health

## کاربرد

نمایش وضعیت کلی Sprint.

---

معمولاً شامل:

- Progress
- Completed
- Remaining
- Scope Change

---

### مناسب

Scrum Master

---

# 10. Sprint Burndown

نمایش Burndown روی Dashboard.

---

تفاوت

Report

↓

صفحه اختصاصی

Dashboard Gadget

↓

داخل Dashboard

---

# 11. Sprint Burnup

نمایش Burnup داخل Dashboard.

---

# 12. Sprint Velocity

نمایش Velocity بدون ورود به Reports.

---

### مناسب

Executive Dashboard

---

# 13. Roadmap

## کاربرد

نمایش Roadmap پروژه.

---

معمولاً شامل

- Epic
- Version
- Timeline

---

### مناسب

Product Owner

---

# 14. Workload Pie Chart

## کاربرد

نمایش توزیع کار بین افراد.

---

مثال

```
Ali

15

Sara

9

Reza

18

Mahdi

6
```

---

### هشدار

این Gadget برای ارزیابی عملکرد افراد مناسب نیست.

فقط توزیع کار را نشان می‌دهد.

---

# 15. Heat Map

## کاربرد

نمایش نقاط بحرانی پروژه.

---

نمونه

```
High Bugs

██████

Low Bugs

██
```

---

# 16. Calendar

## کاربرد

نمایش Issueها بر اساس تاریخ.

---

مناسب

- Release
- Due Date
- Sprint

---

# 17. Introduction Gadget

## کاربرد

قرار دادن متن توضیحی در Dashboard.

---

مثال

```
CRM Project Dashboard

Last Updated

July 2026
```

---

# 18. Text Gadget

نمایش متن، لینک، راهنما یا اطلاعیه.

---

# Gadgets افزونه‌ها

افزونه‌ها Gadgetهای بیشتری اضافه می‌کنند.

| افزونه | Gadgetهای مهم |
|---------|---------------|
| eazyBI | Pivot، KPI، Charts |
| Tempo | Capacity، Timesheet |
| Rich Filters | Smart Filters |
| Structure | Hierarchy |
| BigPicture | Resources |
| Advanced Roadmaps | Team Capacity |

---

# انتخاب Gadget مناسب

| نیاز | Gadget |
|------|---------|
| مشاهده Bugها | Filter Results |
| وضعیت Sprint | Sprint Health |
| سرعت تیم | Velocity |
| پیشرفت Sprint | Burndown |
| توزیع Priority | Pie Chart |
| فعالیت کاربران | Activity Stream |
| تحلیل دوبعدی | Two Dimensional |
| روند ایجاد و حل | Created vs Resolved |
| زمان انجام | Resolution Time |
| برنامه انتشار | Roadmap |

---

# سناریوی واقعی

فرض کنید Scrum Master هستید.

بهترین Dashboard شما می‌تواند شامل این Gadgetها باشد:

1. Sprint Health
2. Sprint Burndown
3. Velocity
4. Blocked Issues (Filter Results)
5. Critical Bugs
6. Created vs Resolved
7. Activity Stream
8. Sprint Goal (Text Gadget)

با نگاه به همین Dashboard، در کمتر از یک دقیقه می‌توانید وضعیت Sprint را ارزیابی کنید.

---

# Common Mistakes

❌ استفاده از Activity Stream بدون Filter

باعث شلوغ شدن Dashboard می‌شود.

---

❌ استفاده از Pie Chart برای داده‌های بسیار زیاد

اگر ۵۰ Assignee داشته باشید، Pie Chart خوانا نخواهد بود.

---

❌ استفاده از Filterهای سنگین

باعث کند شدن Dashboard می‌شود.

---

❌ نمایش Gadgetهای تکراری

مثلاً دو Gadget که هر دو یک KPI را نمایش می‌دهند.

---

❌ قرار دادن Gadgetهای مخصوص QA روی Dashboard مدیرعامل

هر Dashboard باید متناسب با مخاطب طراحی شود.

---

# Best Practices

- از Saved Filter استفاده کنید.
- نام Gadgetها را واضح انتخاب کنید.
- Gadgetهای مهم را در ردیف اول قرار دهید.
- Dashboard را بیش از حد شلوغ نکنید.
- Gadgetهایی را انتخاب کنید که به تصمیم‌گیری کمک می‌کنند، نه فقط نمایش داده.

---

# خلاصه

پنج Gadget که تقریباً در هر Dashboard حرفه‌ای وجود دارند:

1. Sprint Health
2. Velocity
3. Burndown
4. Filter Results
5. Created vs Resolved

اگر این پنج Gadget را به‌درستی پیکربندی کنید، بخش بزرگی از نیازهای گزارش‌گیری روزانه تیم Agile پوشش داده می‌شود.
