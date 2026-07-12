````markdown id="d7p5ops"
# File: Life/Agile/Jira/07-Jira-Data-Center-Architecture-and-Administration/production-operations.md

# Day 7 - Part 5
# Jira Startup Sequence, Services, Scheduler & Production Operations

> بررسی چرخه اجرای Jira، سرویس‌های داخلی، Scheduler، Cluster Lock، Health Check و عملیات روزانه Production.

---

# 76. Jira Startup Architecture

زمانی که Jira Start می‌شود چند مرحله اصلی انجام می‌شود:

```text
Operating System

↓

Java JVM Start

↓

Tomcat Start

↓

Jira Application Loading

↓

Database Connection

↓

Plugin Loading

↓

Cluster Join

↓

Index Validation

↓

Ready For Traffic
````

---

# 77. JVM Startup

ابتدا JVM اجرا می‌شود.

بررسی:

* Java Version
* JVM Arguments
* Heap Configuration
* System Properties

---

نمونه:

```bash
java -version
```

---

# 78. Tomcat Startup

Jira روی Apache Tomcat اجرا می‌شود.

Tomcat مسئول:

* HTTP Connector
* Servlet Container
* Request Handling

است.

---

ساختار:

```text
JVM

↓

Tomcat

↓

Jira Web Application
```

---

# 79. Jira Application Initialization

بعد از بالا آمدن Tomcat:

Jira شروع به Load کردن می‌کند:

* Configuration
* Database Connection
* Plugins
* Services
* Listeners

---

# 80. Database Connection Initialization

Jira ابتدا Database را بررسی می‌کند.

موارد:

```
Database Available?

Credentials Correct?

Schema Compatible?

Connection Pool Healthy?
```

---

اگر Database در دسترس نباشد:

Jira Startup Fail می‌شود.

---

# 81. Plugin Loading

در Startup:

Jira تمام Pluginها را Load می‌کند.

مراحل:

```text
Read Plugin Directory

↓

Resolve Dependencies

↓

Initialize Plugin

↓

Enable Plugin
```

---

مشکلات رایج:

* Plugin ناسازگار
* Dependency Missing
* Startup Delay

---

# 82. Cluster Join Process

در Data Center:

Node باید به Cluster Join شود.

فرآیند:

```text
Start Node

↓

Connect Database

↓

Discover Cluster

↓

Register Node

↓

Join Cluster
```

---

# 83. Cluster Membership

هر Node دارای:

* Node ID
* IP Address
* Status

است.

---

وضعیت‌ها:

```
ACTIVE

FAILED

OFFLINE
```

---

# 84. Cluster Communication

برای انتقال Eventها:

استفاده می‌شود از:

* Cache Replication
* Cluster Messaging

---

مثال:

```text
User Changes Issue

↓

Node 1

↓

Cluster Event

↓

Node 2

↓

Invalidate Cache
```

---

# 85. Scheduler چیست؟

Scheduler وظیفه اجرای Jobهای زمان‌بندی‌شده را دارد.

مثال:

* Email Queue
* Cleanup Tasks
* Index Jobs
* Automation Jobs

---

# 86. Jira Services

Jira دارای Serviceهای داخلی است.

نمونه:

```
Mail Service

Index Service

Notification Service

Cleanup Service

Automation Service
```

---

# 87. Background Jobs

برخی عملیات در Background اجرا می‌شوند.

مثال:

* Reindex
* Mail Sending
* Statistics Calculation
* Data Cleanup

---

مشکل:

Job سنگین می‌تواند Performance را کاهش دهد.

---

# 88. Cluster Locks

در Data Center بعضی عملیات فقط باید توسط یک Node اجرا شوند.

مثال:

```text
Scheduled Job

↓

Acquire Lock

↓

Execute

↓

Release Lock
```

---

هدف:

جلوگیری از اجرای Duplicate.

---

# 89. Health Check

برای Production ضروری است.

بررسی:

## Application

```
Jira Responding?

Login Working?

API Available?
```

---

## Infrastructure

```
CPU

Memory

Disk

Network
```

---

## Dependencies

```
Database

Shared Home

LDAP

SMTP
```

---

# 90. Load Balancer Health Check

Load Balancer باید Node سالم را تشخیص دهد.

مثال:

```text
Request

↓

Load Balancer

↓

Health Check

↓

Healthy Node
```

---

اگر Node مشکل داشته باشد:

```text
Remove From Pool
```

---

# 91. Graceful Shutdown

خاموش کردن صحیح:

```text
Stop Traffic

↓

Finish Requests

↓

Stop Services

↓

Leave Cluster

↓

Shutdown JVM
```

---

خاموشی ناگهانی باعث:

* Index Issue
* Cache Problem
* Recovery Delay

می‌شود.

---

# 92. Production Restart Procedure

قبل از Restart:

```text
Check Active Users

Check Running Jobs

Check Database

Check Disk Space

Notify Users
```

---

Restart:

```text
Drain Node

↓

Stop Jira

↓

Start Jira

↓

Validate Health

↓

Enable Traffic
```

---

# 93. Log Files مهم Jira

مسیر معمول:

```text
<JIRA_HOME>/log/
```

---

مهم‌ترین فایل:

```text
atlassian-jira.log
```

---

برای بررسی:

* Error
* Warning
* Plugin Failure
* Database Problem

---

# 94. Troubleshooting Startup Failure

ترتیب بررسی:

```text
1. Check Java

↓

2. Check Database

↓

3. Check Jira Logs

↓

4. Check Plugins

↓

5. Check File Permission

↓

6. Check Disk Space
```

---

# 95. Production Monitoring Checklist

روزانه:

```text
✓ Jira Availability

✓ CPU

✓ Memory

✓ Disk Space

✓ Database Health

✓ Shared Home

✓ Error Logs

✓ Failed Jobs

✓ Cluster Status
```

---

# 96. Senior Jira Administrator Runbook

برای هر Incident:

```text
Detect

↓

Analyze

↓

Identify Root Cause

↓

Fix

↓

Validate

↓

Document
```

---

# Day 7 Part 5 Summary

موضوعات:

✓ Jira Startup Sequence
✓ Tomcat Architecture
✓ Plugin Loading
✓ Cluster Join
✓ Scheduler
✓ Background Jobs
✓ Cluster Locks
✓ Health Checks
✓ Restart Procedure
✓ Production Operations

---

# Next Part

Day 7 - Part 6:

* Load Balancer Architecture
* Reverse Proxy
* SSL/TLS
* Nginx/HAProxy Integration
* Network Design
* Production Reference Architecture

```
```
