````markdown id="d7p2nodes"
# File: Life/Agile/Jira/07-Jira-Data-Center-Architecture-and-Administration/node-architecture.md

# Day 7 - Part 2
# Node Architecture, Shared Home & Storage Design

> شناخت دقیق Nodeهای Jira Data Center، ساختار فایل‌ها، Shared Home، Local Home و طراحی Storage در محیط Production.

---

# 13. Jira Node Architecture

هر Node یک Jira Application کامل است.

هر Node شامل:

```text
Operating System

↓

JVM

↓

Tomcat

↓

Jira Application

↓

Local Cache
````

تمام Nodeها به:

* Database
* Shared Home

متصل هستند.

---

# 14. Node Responsibilities

هر Node مسئول:

* پردازش درخواست کاربران
* اجرای Workflow
* اجرای Automation
* اجرای REST API
* پردازش Background Jobها
* ارتباط با Database

---

# 15. Active-Active Architecture

تمام Nodeها همزمان فعال هستند.

```text
           Users

              |

        Load Balancer

      /       |       \

 Node-1    Node-2    Node-3

      \       |       /

      PostgreSQL Database

              |

         Shared Home
```

مزایا:

* High Availability
* Horizontal Scaling
* Failover سریع

---

# 16. Shared Home چیست؟

Shared Home پوشه‌ای است که بین تمام Nodeها مشترک است.

نمونه مسیر:

```text id="sh1x02"
/var/atlassian/application-data/jira/shared
```

---

# Shared Home شامل

* Attachments
* Avatars
* Logos
* Import/Export
* Plugins Cache
* Shared Index Snapshot

---

# مواردی که نباید در Shared Home باشند

* Logs
* JVM Files
* Temp Files
* Local Cache

---

# 17. Local Home چیست؟

هر Node یک Local Home اختصاصی دارد.

مثال:

```text id="lh2b14"
/var/atlassian/application-data/jira/local
```

---

Local Home شامل:

* Logs
* Temporary Files
* Local Index
* Local Cache
* JVM Temp

---

# 18. Shared Home Requirements

Storage باید:

✓ High Availability

✓ Low Latency

✓ High IOPS

✓ File Lock Support

✓ POSIX Compatible

باشد.

---

# Storageهای مناسب

* NFS v4
* NetApp
* Pure Storage
* Dell PowerScale
* Enterprise NAS

---

# Storageهای نامناسب

❌ FTP

❌ SMB قدیمی

❌ Object Storage به صورت مستقیم

---

# 19. File Structure

نمونه ساختار:

```text
shared/

├── data/

├── attachments/

├── avatars/

├── export/

├── import/

├── logos/

├── plugins/

├── caches/

└── indexes/
```

---

# 20. Local Directory Structure

```text
local/

├── log/

├── temp/

├── plugins/

├── caches/

├── index/

└── tmp/
```

---

# 21. Shared Home Synchronization

تمام Nodeها فایل‌ها را از Shared Home می‌خوانند.

نمونه:

```
User Uploads Attachment

↓

Stored in Shared Home

↓

Visible to All Nodes
```

---

# 22. Attachment Flow

```text
User

↓

Node-2

↓

Shared Home

↓

Node-1

↓

Another User Downloads
```

---

# 23. Plugin Deployment

در نسخه‌های جدید:

Plugin از طریق Jira نصب می‌شود.

سپس:

```
Plugin Uploaded

↓

Shared Home

↓

Node Synchronization

↓

Plugin Activated
```

---

# 24. Local Cache

هر Node Cache مخصوص خود را دارد.

هدف:

* کاهش Query به Database
* افزایش سرعت پاسخگویی

---

# Cache Example

```
Issue Requested

↓

Cache Exists?

↓

Yes → Return

No → Query Database
```

---

# 25. Cache Invalidation

اگر Issue تغییر کند:

```
Update Issue

↓

Database Commit

↓

Cluster Notification

↓

Invalidate Cache

↓

Reload Data
```

---

# 26. Temporary Files

Temp Fileها همیشه Local هستند.

دلیل:

* سرعت بیشتر
* جلوگیری از ترافیک Storage

---

# 27. Logs

هر Node Log جداگانه دارد.

نمونه:

```text id="lg4m81"
/var/atlassian/application-data/jira/local/log/
```

---

# در محیط Production

پیشنهاد:

ارسال Logها به:

* ELK Stack
* OpenSearch
* Splunk
* Grafana Loki

---

# 28. Shared Home Best Practices

✓ Backup منظم

✓ مانیتورینگ فضای دیسک

✓ مانیتورینگ Latency

✓ تست Failover

✓ عدم ذخیره فایل‌های موقت

---

# 29. Common Problems

## Shared Home کند

نتیجه:

* Login کند
* Upload کند
* Startup کند

---

## NFS Timeout

نتیجه:

* Node Freeze
* Cluster Instability

---

## Disk Full

نتیجه:

* Failure در Upload
* Index Failure
* Plugin Installation Failure

---

# 30. Senior Jira Admin Checklist

بررسی روزانه:

```text
✓ Shared Home Available

✓ Storage Latency Normal

✓ Free Disk Space

✓ Attachment Upload Test

✓ Plugin Synchronization

✓ Log Errors
```

---

# Day 7 Part 2 Summary

موضوعات:

✓ Node Architecture
✓ Shared Home
✓ Local Home
✓ Storage Design
✓ Cache
✓ Plugin Synchronization
✓ File Structure
✓ Production Best Practices

---

# Next Part

Day 7 - Part 3:

* Database Architecture
* Connection Pool
* PostgreSQL Design
* Index Architecture
* Lucene Index
* Reindex Strategy
* Cluster Communication

```
```
