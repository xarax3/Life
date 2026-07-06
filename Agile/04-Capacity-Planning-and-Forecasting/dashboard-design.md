# Dashboard Design in Jira

> طراحی داشبوردهای حرفه‌ای برای مانیتورینگ وضعیت پروژه، Sprint، تیم و سازمان با استفاده از قابلیت‌های داخلی Jira و افزونه‌های تحلیلی.

---

# Dashboard چیست؟

Dashboard صفحه‌ای است که اطلاعات مهم پروژه را به‌صورت لحظه‌ای (Real-time) نمایش می‌دهد.

هدف:

- مشاهده سریع وضعیت پروژه
- شناسایی ریسک‌ها
- پایش KPIها
- کمک به تصمیم‌گیری

---

# Dashboard برای چه کسانی؟

| نقش | هدف |
|------|-----|
| Developer | وضعیت Taskها |
| Scrum Master | سلامت Sprint |
| Product Owner | وضعیت Backlog و Release |
| Project Manager | پیشرفت پروژه |
| PMO | وضعیت چند پروژه |
| CTO | شاخص‌های کلان سازمان |

---

# ساخت Dashboard

در Jira:

```
Dashboards
    ↓
Create Dashboard
```

سپس:

```
Add Gadget
```

---

# Gadget چیست؟

Gadget ویجتی است که اطلاعات خاصی را نمایش می‌دهد.

هر Dashboard از چند Gadget تشکیل می‌شود.

---

# Gadgetهای داخلی Jira

| Gadget | کاربرد |
|----------|---------|
| Filter Results | نمایش Issueها |
| Pie Chart | توزیع داده‌ها |
| Created vs Resolved | روند ایجاد و حل Issue |
| Sprint Health | سلامت Sprint |
| Two Dimensional Filter | تحلیل دوبعدی |
| Average Age Chart | سن Issueها |
| Workload Pie Chart | توزیع بار کاری |
| Issue Statistics | آمار بر اساس فیلدها |

---

# Dashboard برای Scrum Master

پیشنهاد:

- Sprint Health
- Sprint Burndown
- Velocity Chart
- Sprint Report
- Blocked Issues
- WIP
- Bug Count

هدف:

پایش وضعیت Sprint.

---

# Dashboard برای Product Owner

پیشنهاد:

- Backlog Size
- Story Status
- Release Progress
- Feature Progress
- Scope Change
- Epic Progress

هدف:

مدیریت ارزش محصول.

---

# Dashboard برای Project Manager

پیشنهاد:

- Progress
- Capacity
- Velocity
- Resource Allocation
- Risk List
- Release Forecast
- Predictability

هدف:

مدیریت پروژه.

---

# Dashboard برای PMO

پیشنهاد:

- Portfolio Health
- Team Velocity
- Budget
- Schedule
- Risks
- Cross Project Status

---

# Dashboard برای CTO

پیشنهاد:

- Release Health
- Lead Time
- Cycle Time
- Deployment Frequency
- Change Failure Rate
- MTTR
- Team Utilization

---

# Dashboard برای مدیران ارشد

معمولاً کمتر از ۱۰ KPI نمایش داده می‌شود.

نمونه:

```
Projects

18
```

```
On Time

83%
```

```
Delayed

17%
```

```
Critical Risks

4
```

```
Capacity

82%
```

---

# Dashboard برای تیم توسعه

شاخص‌ها:

- Assigned Issues
- Blocked Issues
- Sprint Goal
- Bugs
- PR Status (در صورت اتصال به Git)
- CI/CD Status

---

# استفاده از Filter

تقریباً تمام Gadgetها از Filter استفاده می‌کنند.

مثال:

```
project = ERP

AND

Sprint in openSprints()
```

---

# استفاده از JQL

نمونه:

```
project = ERP

AND

status != Done
```

---

نمایش Bugهای بحرانی:

```
issuetype = Bug

AND

priority = Highest

AND

status != Done
```

---

نمایش Storyهای Sprint جاری:

```
Sprint in openSprints()

AND

issuetype = Story
```

---

# Dashboard با eazyBI

قابلیت‌ها:

- Pivot Table
- Burndown
- Burnup
- Forecast
- Capacity
- Velocity Trend
- Heatmap

---

# Dashboard با Rich Filters

امکانات:

- فیلترهای تعاملی
- Dynamic Dashboard
- Smart Gadget
- Quick Filter

---

# Dashboard با Advanced Roadmaps

نمایش:

- Team Capacity
- Dependencies
- Release
- Forecast
- Timeline
- Initiative Progress

---

# Dashboard با Structure

قابلیت‌ها:

- Hierarchy
- Gantt
- Rollup
- Progress

---

# Dashboard با Tempo

نمایش:

- Planned Hours
- Logged Hours
- Capacity
- Utilization
- Cost

---

# KPIهای پیشنهادی

## Sprint Dashboard

- Velocity
- Burndown
- Sprint Health
- WIP
- Bug Count
- Predictability

---

## Release Dashboard

- Remaining Story Points
- Forecast
- Release Date
- Scope Trend
- Epic Progress

---

## Executive Dashboard

- Portfolio Health
- Budget
- Schedule
- Risk
- Capacity
- Delivery Rate

---

# Best Practices

✅ برای هر نقش Dashboard جداگانه طراحی کنید.

✅ Dashboard را شلوغ نکنید.

✅ KPIهای کلیدی را در بالای صفحه قرار دهید.

✅ از رنگ‌ها برای هشدار استفاده کنید.

✅ Dashboard را به‌صورت دوره‌ای بازبینی کنید.

---

# اشتباهات رایج

❌ قرار دادن تعداد زیادی Gadget.

❌ نمایش داده‌های غیرضروری.

❌ استفاده از Filterهای کند.

❌ نداشتن Dashboard اختصاصی برای هر نقش.

---

# Interview Questions

### Dashboard چیست؟

صفحه‌ای برای نمایش وضعیت پروژه و KPIها به‌صورت لحظه‌ای.

---

### Gadget چیست؟

ویجتی که بخشی از اطلاعات پروژه را در Dashboard نمایش می‌دهد.

---

### تفاوت Dashboard و Report چیست؟

Dashboard وضعیت فعلی را به‌صورت لحظه‌ای نمایش می‌دهد.

Report معمولاً تحلیل یک بازه زمانی یا یک فرآیند است.

---

### چگونه Dashboard را سفارشی می‌کنید؟

با استفاده از:

- Gadget
- JQL
- Filter
- eazyBI
- Rich Filters
- Advanced Roadmaps

---

# Summary

| ویژگی | Dashboard |
|---------|-----------|
| هدف | نمایش وضعیت پروژه |
| واحد نمایش | Gadget |
| فیلتر | JQL / Saved Filter |
| گزارش لحظه‌ای | ✅ |
| گزارش تحلیلی | با افزونه‌ها |

---

# Enterprise Tips

## 1. Dashboard را بر اساس مخاطب طراحی کنید.

اطلاعات موردنیاز یک Developer با CTO کاملاً متفاوت است.

---

## 2. KPIهای عملیاتی و مدیریتی را جدا کنید.

داشبورد تیم توسعه باید روی اجرای Sprint تمرکز داشته باشد، در حالی که داشبورد مدیران باید روندها و ریسک‌ها را نمایش دهد.

---

## 3. از Drill-down استفاده کنید.

کاربر باید بتواند از KPI کلی وارد جزئیات Issueها شود.

---

## 4. Dashboardها را استاندارد کنید.

در سازمان‌های بزرگ، قالب Dashboard برای همه پروژه‌ها معمولاً یکسان است تا مقایسه آسان‌تر شود.

---

## 5. داده‌های Dashboard را بهینه نگه دارید.

از Filterهای بهینه، JQLهای ساده و Gadgetهای ضروری استفاده کنید تا Dashboard سریع بارگذاری شود.

---

# نمونه Dashboard برای Scrum Master

| KPI | ابزار |
|------|-------|
| Sprint Health | Sprint Health Gadget |
| Velocity | Velocity Report |
| Burndown | Burndown Chart |
| Predictability | eazyBI |
| Blocked Issues | Filter Results |
| WIP | Rich Filters |
| Bug Trend | Created vs Resolved |

---

# نمونه Dashboard برای Project Manager

| KPI | ابزار |
|------|-------|
| Capacity | Tempo / Advanced Roadmaps |
| Resource Allocation | Tempo Planner |
| Release Forecast | Advanced Roadmaps |
| Scope Trend | eazyBI |
| Risks | Filter Results |
| Budget (در صورت اتصال) | BigPicture یا ابزار PM |

---

# نمونه Dashboard برای CTO

| KPI | ابزار |
|------|-------|
| Lead Time | Jira + DevOps Integration |
| Cycle Time | ActionableAgile |
| Deployment Frequency | CI/CD Integration |
| Change Failure Rate | DevOps Dashboard |
| MTTR | Incident Management |
| Portfolio Health | Advanced Roadmaps |

---

# پایان Day 4

در این روز مباحث زیر به‌صورت کامل پوشش داده شد:

- Capacity Planning
- Team Capacity
- Initial Commitment
- Final Commitment
- Focus Factor
- Predictability
- Velocity Forecast
- Release Forecast
- Monte Carlo Forecast
- Resource Planning
- Dashboard Design

این مجموعه، پایه برنامه‌ریزی، پیش‌بینی، مدیریت ظرفیت و گزارش‌دهی حرفه‌ای در Jira و Agile در سطح Enterprise را تشکیل می‌دهد.
