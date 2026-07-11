```markdown id="d7p1arch"
# File: Life/Agile/Jira/07-Jira-Data-Center-Architecture-and-Administration/README.md

# Day 7 - Jira Data Center Architecture & Administration

> معماری، اجزا و مدیریت حرفه‌ای Jira Data Center در محیط‌های Production و Enterprise.

---

# Day 7 Overview

در روز هفتم وارد بخش Infrastructure و Architecture Jira می‌شویم.

موضوعات:

- Jira Data Center چیست؟
- تفاوت Server و Data Center
- معماری Production
- Node Architecture
- Shared Home
- Local Home
- Database Layer
- Load Balancer
- Cache Layer
- Index Architecture
- JVM Architecture
- File System Structure

---

# 1. Jira Data Center چیست؟

Jira Data Center نسخه Enterprise از Jira است که برای:

- Availability بالا
- Scalability
- Performance
- سازمان‌های بزرگ

طراحی شده است.

---

# 2. تفاوت Jira Server و Data Center

## Jira Server

معماری:

```

Single Application Instance

↓

Database

```

---

مشکلات:

- Single Point of Failure
- محدودیت Scale
- Downtime هنگام Maintenance

---

## Jira Data Center

معماری:

```

Load Balancer

```
    |
```

+---------------+
| Jira Node 1   |
+---------------+

+---------------+
| Jira Node 2   |
+---------------+

```
    |
```

Shared Database

```
    |
```

Shared Storage
