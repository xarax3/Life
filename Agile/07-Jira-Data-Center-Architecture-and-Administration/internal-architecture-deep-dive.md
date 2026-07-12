# File: Life/Agile/Jira/07-Jira-Data-Center-Architecture-and-Administration/internal-architecture-deep-dive.md

# Day 7 - Part 23

# Jira Data Center Internal Architecture Deep Dive

> بررسی ساختار داخلی Jira Data Center، نحوه کار Componentها، Plugin Framework، Cache، Index، Cluster Communication و جریان پردازش Request در سطح Architect.

---

# 397. Jira Internal Architecture Overview

Jira از چندین لایه اصلی تشکیل شده است:

```text id="int01"

User Request

      |

Web Layer

      |

Jira Application Layer

      |

Service Layer

      |

Database Layer

      |

Storage Layer

```

---

# 398. Request Processing Flow

زمانی که کاربر یک درخواست ارسال می‌کند:

```text id="int02"

Browser

↓

Load Balancer

↓

Jira Node

↓

Servlet Container

↓

Jira Services

↓

Database

↓

Response

```

---

# 399. Tomcat Layer

Jira روی Tomcat اجرا می‌شود.

وظایف:

```text id="int03"
HTTP Handling

Request Threads

Session Management

Application Deployment
```

---

تنظیمات مهم:

```text id="int04"
server.xml

setenv.sh

Connector Configuration
```

---

# 400. Jira Application Components

اجزای اصلی:

```text id="int05"

Issue Manager

Workflow Engine

Permission Engine

User Management

Notification Engine

Search Engine

Plugin System

```

---

# 401. Issue Processing Flow

ایجاد یک Issue:

```text id="int06"

Create Request

↓

Validate Fields

↓

Check Permission

↓

Execute Workflow

↓

Save Database

↓

Update Index

↓

Send Notification

```

---

# 402. Workflow Engine Internals

Workflow شامل:

```text id="int07"
Statuses

Transitions

Conditions

Validators

Post Functions
```

---

در Transition:

```text id="int08"

User Action

↓

Permission Check

↓

Validator

↓

Post Function

↓

Update Issue

```

---

# 403. Permission Engine

Permission بررسی می‌کند:

```text id="int09"
Who

↓

Can Do What

↓

On Which Object
```

---

سطوح:

```text id="int10"
Global Permission

Project Permission

Issue Security

Field Security
```

---

# 404. Jira Plugin Architecture

Pluginها قابلیت‌های Jira را توسعه می‌دهند.

ساختار:

```text id="int11"

Jira Core

+

Plugins

+

Modules

```

---

Plugin شامل:

```text id="int12"
Java Code

XML Descriptor

Resources

Frontend Components
```

---

# 405. OSGi Framework

Jira Plugin System بر پایه OSGi است.

هدف:

```text id="int13"
Dynamic Module Loading

Isolation

Dependency Management
```

---

مشکل‌های رایج:

```text id="int14"
Dependency Conflict

Class Loading Error

Plugin Startup Failure
```

---

# 406. Plugin Lifecycle

چرخه:

```text id="int15"

Install

↓

Enable

↓

Start

↓

Use

↓

Disable

↓

Uninstall

```

---

# 407. Plugin Impact Analysis

قبل از نصب Plugin:

بررسی:

```text id="int16"
Memory Usage

Database Usage

Permissions

Compatibility

Support Status
```

---

# 408. Jira Cache Architecture

برای Performance، Jira از Cache استفاده می‌کند.

نمونه:

```text id="int17"
User Cache

Permission Cache

Project Cache

Configuration Cache
```

---

# 409. Cache در Data Center

در Data Center:

Cache بین Nodeها هماهنگ می‌شود.

مدل:

```text id="int18"

Node 1 Cache

       |

Cluster Communication

       |

Node 2 Cache

```

---

# 410. Cache Problems

علائم:

```text id="int19"
Old Data Visible

Permission Delay

Configuration Mismatch
```

---

دلایل:

```text id="int20"
Cluster Issue

Network Problem

Node Failure
```

---

# 411. Jira Index Architecture

Jira از Apache Lucene برای Search استفاده می‌کند.

Index شامل:

```text id="int21"
Issue Data

Fields

Text Content

Permissions
```

---

# 412. Database vs Index

تفاوت مهم:

Database:

```text id="int22"
Source Of Truth
```

---

Index:

```text id="int23"
Search Optimization Layer
```

---

اگر Index خراب شود:

```text id="int24"
Database Safe

Search Broken
```

---

# 413. Index Lifecycle

مراحل:

```text id="int25"

Issue Change

↓

Index Update

↓

Lucene Commit

↓

Search Available

```

---

# 414. Cluster Communication

Nodeها نیاز دارند:

```text id="int26"
Share Events

Synchronize Cache

Coordinate Tasks
```

---

موارد مهم:

```text id="int27"
Network Latency

Firewall Rules

Time Synchronization
```

---

# 415. Background Jobs Architecture

Jira Jobها:

```text id="int28"
Email Sending

Cleanup

Reindex

Automation

Scheduled Tasks
```

---

در Cluster:

باید کنترل شود:

```text id="int29"
Which Node Executes Job
```

---

# 416. Notification System

Flow:

```text id="int30"

Issue Event

↓

Notification Scheme

↓

User Resolution

↓

Email Queue

↓

SMTP

```

---

# 417. Jira Event System

Eventها:

```text id="int31"
Issue Created

Issue Updated

Workflow Changed

User Changed
```

---

Pluginها می‌توانند Event Listener داشته باشند.

---

# 418. Jira Internal Performance Points

مهم‌ترین نقاط:

```text id="int32"
Database

Index

Cache

Plugins

Automation

JVM
```

---

# 419. Architect Understanding Checklist

یک Architect باید بداند:

```text id="int33"

✓ Request Flow

✓ Workflow Engine

✓ Permission Engine

✓ Plugin Architecture

✓ Cache Model

✓ Index Lifecycle

✓ Cluster Communication

✓ Background Jobs

```

---

# Day 7 Part 23 Summary

موضوعات:

✓ Jira Internal Architecture
✓ Request Lifecycle
✓ Tomcat Layer
✓ Plugin Framework
✓ OSGi
✓ Cache Architecture
✓ Index Architecture
✓ Cluster Communication
✓ Internal Components

---

# Next Part

# Day 7 - Part 24

* Enterprise Implementation Blueprint
* Production Design Template
* Server Sizing
* Network Architecture
* Security Zones
* Deployment Checklist
