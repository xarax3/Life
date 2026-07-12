````markdown id="d7p3db"
# File: Life/Agile/Jira/07-Jira-Data-Center-Architecture-and-Administration/database-and-index-architecture.md

# Day 7 - Part 3
# Database Architecture, Connection Pool & Index Management

> معماری پایگاه داده Jira Data Center، مدیریت Connection Pool، ساختار Lucene Index، Reindex و ارتباط Cluster.

---

# 31. Database Architecture

در Jira Data Center فقط **یک Database** وجود دارد.

تمام Nodeها به همان Database متصل می‌شوند.

معماری:

```text
                Jira Node 1
                      │
                Jira Node 2
                      │
                Jira Node 3
                      │
             Connection Pool
                      │
                PostgreSQL
````

---

# 32. چرا فقط یک Database؟

Database منبع اصلی حقیقت (**Single Source of Truth**) است.

تمام اطلاعات در آن ذخیره می‌شود:

* Users
* Issues
* Projects
* Workflows
* Comments
* History
* Configuration
* Custom Fields

---

# 33. Database Requirements

Database باید:

✓ ACID Compliant

✓ Transaction Safe

✓ High Availability

✓ Backup Strategy

✓ Replication Support

را داشته باشد.

---

# 34. Supported Databases

نسخه‌های جدید Jira Data Center معمولاً از:

* PostgreSQL (پیشنهادی)
* Oracle
* Microsoft SQL Server

پشتیبانی می‌کنند.

---

# بهترین انتخاب

برای اکثر سازمان‌ها:

```text id="pgbest1"
PostgreSQL

+

Patroni

+

HAProxy

+

Keepalived
```

---

# 35. Connection Pool

هر Node دارای Connection Pool خودش است.

```text
Users

↓

Jira Node

↓

HikariCP

↓

Database
```

---

مزایا:

* کاهش زمان اتصال
* استفاده مجدد از Connection
* افزایش Performance

---

# 36. Connection Lifecycle

```text id="connl1"
Application Start

↓

Create Pool

↓

Borrow Connection

↓

Execute SQL

↓

Return Connection

↓

Reuse
```

---

# 37. Connection Pool Best Practices

✓ Pool Size متناسب با منابع Database

✓ Monitor Active Connections

✓ جلوگیری از Connection Leak

✓ تنظیم Timeout مناسب

---

# 38. Database Transactions

مثال:

```text id="txn01"
Create Issue

↓

Insert Issue

↓

Insert History

↓

Insert Change Log

↓

Commit
```

در صورت خطا:

```text id="txn02"
Rollback
```

---

# 39. Database Locking

Jira از Transaction Lock برای جلوگیری از ناسازگاری داده‌ها استفاده می‌کند.

نمونه:

```text
User A

↓

Edit Issue

↓

Lock Row

↓

Commit

↓

Unlock
```

---

# 40. Database Performance

عوامل مهم:

* Indexهای PostgreSQL
* سرعت Storage
* RAM
* CPU
* Queryهای طولانی
* Vacuum و Analyze

---

# 41. Lucene Index چیست؟

Jira برای جستجو از **Lucene Index** استفاده می‌کند.

جستجو مستقیماً روی Database انجام نمی‌شود.

```text
User Search

↓

Lucene Index

↓

Issue Results
```

---

# 42. چرا Index لازم است؟

بدون Index:

```text
Search

↓

Database Scan

↓

Very Slow
```

با Index:

```text
Search

↓

Lucene Index

↓

Fast Result
```

---

# 43. Local Index

هر Node یک Local Index دارد.

مزایا:

* جستجوی سریع
* کاهش بار Database
* استقلال Nodeها

---

# 44. Index Synchronization

پس از تغییر Issue:

```text id="idx01"
Issue Updated

↓

Database Commit

↓

Index Update

↓

Cluster Notification

↓

Other Nodes Update Index
```

---

# 45. Full Reindex

موارد استفاده:

* Upgrade
* Index Corruption
* Restore Backup
* Migration

---

فرآیند:

```text
Read Database

↓

Rebuild Lucene

↓

Replace Index
```

---

# 46. Background Reindex

در برخی سناریوها:

* کاربران می‌توانند هم‌زمان از Jira استفاده کنند.
* Index در پس‌زمینه بازسازی می‌شود.

---

# 47. Lock & Reindex

در Reindex کامل:

```text
Stop Index Update

↓

Rebuild

↓

Enable Search
```

ممکن است بخشی از سیستم موقتاً محدود شود.

---

# 48. Common Index Problems

## Index Corruption

علائم:

* Search Error
* Missing Issue
* Incorrect JQL Result

---

## Out of Sync Index

علائم:

* یک Node نتیجه متفاوتی نشان می‌دهد.
* Issue تازه ایجاد شده پیدا نمی‌شود.

---

راه‌حل:

```text id="reidx01"
Reindex
```

---

# 49. Cluster Communication

Nodeها از طریق Cluster Messaging با هم ارتباط دارند.

برای:

* Cache Invalidation
* Index Update
* Event Distribution

---

نمونه:

```text
Issue Updated

↓

Node 1

↓

Cluster Event

↓

Node 2

↓

Node 3
```

---

# 50. Senior Jira Admin Checklist

به‌صورت روزانه بررسی شود:

```text id="chk31"
✓ Database Available

✓ Connection Pool Healthy

✓ Active Sessions Normal

✓ Slow Queries

✓ Index Healthy

✓ Reindex Status

✓ Cluster Synchronization
```

---

# Day 7 Part 3 Summary

موضوعات:

✓ Database Architecture
✓ PostgreSQL Design
✓ Connection Pool
✓ Transactions
✓ Lucene Index
✓ Local Index
✓ Reindex Strategy
✓ Cluster Synchronization

---

# Next Part

Day 7 - Part 4:

* JVM Architecture
* Memory Management
* Garbage Collection
* Thread Model
* Application Startup
* JVM Tuning
* Production Performance

```
```
