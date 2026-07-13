# Sprint Metrics

> در این بخش تمام شاخص‌هایی (Metrics) که برای مدیریت Sprint استفاده می‌شوند را بررسی می‌کنیم؛ از متریک‌های داخلی Jira تا شاخص‌هایی که با افزونه‌هایی مانند eazyBI، Tempo و Advanced Roadmaps قابل محاسبه هستند.

---

# اهداف یادگیری

پس از پایان این بخش، می‌توانید:

- عملکرد Sprint را تحلیل کنید.
- ظرفیت تیم را محاسبه کنید.
- پیش‌بینی Sprintهای آینده را انجام دهید.
- کیفیت برنامه‌ریزی Sprint را ارزیابی کنید.
- Dashboardهای مدیریتی طراحی کنید.
- KPIهای مناسب برای Scrum و Kanban را انتخاب کنید.

---

# Sprint Metrics چیست؟

Sprint Metric شاخصی است که عملکرد تیم را در طول یا پایان یک Sprint اندازه‌گیری می‌کند.

این شاخص‌ها به تصمیم‌گیری کمک می‌کنند و نباید به‌عنوان ابزار ارزیابی عملکرد فردی استفاده شوند.

---

# دسته‌بندی Sprint Metrics

```
Sprint Metrics

├── Planning Metrics
│   ├── Initial Commitment
│   ├── Final Commitment
│   ├── Capacity
│   ├── Team Availability
│   └── Scope Change
│
├── Delivery Metrics
│   ├── Velocity
│   ├── Burndown
│   ├── Burnup
│   ├── Throughput
│   └── Completion Rate
│
├── Flow Metrics
│   ├── Cycle Time
│   ├── Lead Time
│   ├── WIP
│   ├── Flow Efficiency
│   └── Queue Time
│
├── Quality Metrics
│   ├── Bug Rate
│   ├── Escaped Bugs
│   ├── Defect Density
│   ├── Reopened Issues
│   └── Defect Leakage
│
└── Predictability Metrics
    ├── Commitment Reliability
    ├── Predictability Index
    ├── Release Forecast
    └── Monte Carlo Forecast
```

---

# متریک‌های موجود در Jira

این متریک‌ها به‌صورت پیش‌فرض یا از طریق گزارش‌های داخلی Jira قابل مشاهده هستند:

| Metric | Built-in Jira |
|---------|---------------|
| Velocity | ✅ |
| Burndown | ✅ |
| Burnup | ✅ |
| Sprint Report | ✅ |
| Version Report | ✅ |
| Control Chart | ✅ |
| CFD | ✅ |

---

# متریک‌هایی که به افزونه نیاز دارند

| Metric | معمولاً با |
|---------|------------|
| Capacity | Tempo / Advanced Roadmaps |
| Initial Commitment | eazyBI / Rich Filters |
| Commitment Reliability | eazyBI |
| Focus Factor | eazyBI |
| Monte Carlo Forecast | ActionableAgile، eazyBI |
| Team Utilization | Tempo |
| Cost Metrics | Tempo Cost Tracker |
| Resource Allocation | BigPicture / Advanced Roadmaps |

---

# چرخه کامل یک Sprint

```mermaid
flowchart LR

A[Sprint Planning]

--> B[Initial Commitment]

--> C[Capacity Check]

--> D[Sprint Start]

--> E[Daily Scrum]

--> F[Burndown]

--> G[Velocity]

--> H[Sprint Review]

--> I[Retrospective]

--> J[Lessons Learned]
```

---

# سوالات کلیدی که متریک‌ها پاسخ می‌دهند

| سوال | Metric مناسب |
|-------|--------------|
| آیا Sprint بیش از ظرفیت برنامه‌ریزی شده است؟ | Capacity |
| آیا تیم به تعهد خود عمل کرده است؟ | Commitment Reliability |
| سرعت واقعی تیم چقدر است؟ | Velocity |
| آیا از برنامه عقب هستیم؟ | Burndown |
| چه مقدار کار انجام شده است؟ | Burnup |
| چند Issue تکمیل شده است؟ | Throughput |
| انجام هر کار چقدر طول می‌کشد؟ | Cycle Time |
| آیا کارها زیاد در انتظار می‌مانند؟ | Lead Time |
| آیا گلوگاه وجود دارد؟ | CFD |
| آیا Release به‌موقع انجام می‌شود؟ | Release Forecast |

---

# رابطه متریک‌ها

```mermaid
flowchart TD

Capacity --> InitialCommitment

InitialCommitment --> Velocity

Velocity --> Forecast

Velocity --> Burndown

Burndown --> SprintHealth

CycleTime --> Throughput

LeadTime --> FlowEfficiency

FlowEfficiency --> Predictability

Predictability --> ReleaseForecast
```

---

# نقش‌ها و متریک‌های مهم

| نقش | مهم‌ترین متریک‌ها |
|------|-------------------|
| Developer | Burndown، WIP، Cycle Time |
| Scrum Master | Velocity، Commitment، Burndown، CFD |
| Product Owner | Burnup، Forecast، Release Progress |
| QA Lead | Bug Rate، Reopened Issues |
| Project Manager | Capacity، Velocity، Forecast |
| Agile Coach | Flow Metrics، Predictability |
| CTO | Predictability، Release Forecast، Delivery Trend |

---

# اشتباهات رایج

❌ استفاده از Velocity برای مقایسه افراد

❌ افزایش مصنوعی Story Point برای بالا بردن Velocity

❌ برنامه‌ریزی Sprint بدون Capacity

❌ تحلیل Sprint فقط با Burndown

❌ نادیده گرفتن Scope Change

❌ تصمیم‌گیری بر اساس یک Sprint

همیشه روند چند Sprint متوالی را بررسی کنید.

---

# مسیر مطالعه فصل

این فصل را به ترتیب زیر بخوانید:

1. [راهنمای کامل Sprint Metrics](sprint-metrics-guide.md): مفاهیم، Capacity، Commitment، Scope و Spillover
2. [فرمول‌ها و KPIها](formulas.md): تعریف دقیق صورت و مخرج هر شاخص
3. [JQLهای کاربردی](jql.md): فیلترهای قابل استفاده در Jira
4. [طراحی Dashboard](dashboard.md): چیدمان، هدف و تفسیر هر Gadget
5. [سؤالات مصاحبه](interview-notes.md): پاسخ‌های سناریومحور

برای تحلیل عمیق‌تر، فصل‌های بعدی مکمل این فصل‌اند:

- [Flow Metrics](../03-Flow-Metrics/README.md): Lead Time، Cycle Time، WIP و Throughput
- [Capacity Planning & Forecasting](../04-Capacity-Planning-and-Forecasting/README.md): پیش‌بینی و برنامه‌ریزی ظرفیت
- [Flow Metrics & Kanban](../05-Flow-Metrics-and-Kanban/README.md): CFD، SLE و DORA

## قرارداد اندازه‌گیری

- همهٔ شاخص‌های یک تیم باید با یک واحد ثابت محاسبه شوند؛ Story Point را با ساعت جمع نکنید.
- «Done» باید به یک Status Category یا وضعیت پایانیِ توافق‌شده نگاشت شود.
- Snapshot شروع Sprint را نگه دارید؛ بدون آن، Initial Commitment و Scope Change قابل اعتماد نیستند.
- شاخص‌ها برای بهبود سیستم‌اند، نه رتبه‌بندی افراد.
