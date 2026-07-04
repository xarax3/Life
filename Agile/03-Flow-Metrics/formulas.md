# Flow Metrics Formulas

> فرمول‌های اصلی مورد استفاده در Kanban، Jira، DevOps و Agile

---

# 1. Cycle Time

## Formula

```
Cycle Time = Done Date − Start Date
```

### Unit

- Hours
- Days

### Example

```
Start

5 July
```

```
Done

10 July
```

```
Cycle Time = 5 Days
```

---

# 2. Lead Time

## Formula

```
Lead Time = Done Date − Created Date
```

### Example

```
Created

1 July
```

```
Done

10 July
```

```
Lead Time = 9 Days
```

---

# 3. Waiting Time

```
Waiting Time

=

Lead Time

-

Cycle Time
```

### Example

Lead Time

```
12 Days
```

Cycle Time

```
5 Days
```

Waiting Time

```
7 Days
```

---

# 4. Flow Efficiency

```
Flow Efficiency

=

(Active Time / Lead Time)

×

100
```

### Example

```
7 / 20

=

35%
```

---

# 5. Throughput

```
Throughput

=

Completed Issues
```

### Example

```
Sprint

30 Issues
```

---

# 6. Work In Progress

```
WIP

=

Active Issues
```

---

# 7. Little's Law

```
Lead Time

=

WIP

/

Throughput
```

یا

```
WIP

=

Lead Time

×

Throughput
```

---

# 8. Average Cycle Time

```
Σ Cycle Time

/

Issue Count
```

---

# 9. Median Cycle Time

مرتب‌سازی داده‌ها

↓

عدد وسط

---

# 10. Percentile

```
50%

Median
```

```
85%

Forecast
```

```
95%

Safe Forecast
```

---

# Enterprise KPI Relationships

```
WIP ↑

↓

Lead Time ↑

↓

Flow Efficiency ↓
```

---

```
Throughput ↑

↓

Delivery ↑
```

---

```
Cycle Time ↓

↓

Predictability ↑
```

---

# Quick Formula Table

| Metric | Formula |
|---------|----------|
| Cycle Time | Done − Start |
| Lead Time | Done − Created |
| Waiting Time | Lead − Cycle |
| Flow Efficiency | Active ÷ Lead ×100 |
| Throughput | Completed Issues |
| WIP | Active Issues |
| Little's Law | Lead = WIP ÷ Throughput |

---

# نکته

در Jira بسیاری از این مقادیر مستقیماً نمایش داده نمی‌شوند و با استفاده از:

- Control Chart
- CFD
- JQL
- eazyBI
- ActionableAgile
- Rich Filters

محاسبه یا استخراج می‌شوند.
