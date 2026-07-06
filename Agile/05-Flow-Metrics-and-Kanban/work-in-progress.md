# Work In Progress (WIP)

> یکی از بنیادی‌ترین اصول Kanban که تعداد آیتم‌های همزمان در حال انجام را محدود و کنترل می‌کند.

---

# Definition

WIP یعنی:

> تعداد آیتم‌هایی که در هر لحظه در وضعیت "In Progress" قرار دارند.

```
WIP = Number of Active Work Items
```

---

# هدف

WIP به این سؤال پاسخ می‌دهد:

> **چند کار همزمان در حال انجام است و آیا سیستم بیش از حد بارگذاری شده است؟**

---

# مثال ساده

```
To Do: 10
In Progress: 8
Review: 5
Done: 20
```

```
WIP = 13
```

(اگر In Progress + Review را حساب کنیم)

---

# چرا WIP مهم است؟

WIP یکی از قوی‌ترین کنترل‌کننده‌های Flow است.

زیرا:

> افزایش WIP → افزایش Lead Time و Cycle Time

---

# قانون طلایی Kanban

```
Stop starting, start finishing
```

---

# اثر WIP روی سیستم

| WIP | نتیجه |
|-----|--------|
| زیاد | Flow کند |
| زیاد | Cycle Time بالا |
| زیاد | Context Switching |
| کم | Flow سریع |
| کم | Predictability بالا |

---

# مثال واقعی

## وضعیت بد

```
WIP = 25
Cycle Time = 12 days
```

## وضعیت بهتر

```
WIP = 10
Cycle Time = 5 days
```

---

# WIP Limit چیست؟

WIP Limit یعنی:

> حداکثر تعداد آیتم مجاز در هر ستون

مثال:

```
In Progress Limit = 5
Review Limit = 3
```

---

# هدف WIP Limit

- جلوگیری از overload
- افزایش تمرکز تیم
- کاهش Cycle Time
- بهبود Flow

---

# WIP در Jira

در Jira Board:

- Column Constraints
- WIP Limits per Column
- Swimlane policies

---

# تنظیم WIP Limit در Jira

```
Board Settings
→ Columns
→ Column Constraint
→ Set limit
```

---

# ارتباط WIP با Metrics دیگر

## Little’s Law

```
WIP = Throughput × Cycle Time
```

یا:

```
Cycle Time = WIP / Throughput
```

---

# مثال Little’s Law

```
WIP = 20
Throughput = 5 items/day
```

```
Cycle Time = 4 days
```

---

# WIP و Flow Efficiency

WIP بالا معمولاً باعث:

- افزایش Waiting Time
- کاهش Flow Efficiency

---

# WIP و Bottleneck

اگر یک ستون WIP زیاد داشته باشد:

```
Review Queue
→ Bottleneck
```

---

# WIP و Context Switching

WIP بالا یعنی:

- کار همزمان زیاد
- تمرکز کمتر
- زمان از دست رفته در switching

---

# نشانه‌های WIP زیاد

- آیتم‌های زیاد در In Progress
- Delay
