````markdown id="d7p4jvm"
# File: Life/Agile/Jira/07-Jira-Data-Center-Architecture-and-Administration/jvm-and-performance.md

# Day 7 - Part 4
# JVM Architecture, Memory Management & Performance Engineering

> آشنایی با معماری JVM، مدیریت حافظه، Garbage Collection، Threadها و بهینه‌سازی عملکرد Jira Data Center.

---

# 51. JVM چیست؟

Jira یک برنامه Java است و روی **Java Virtual Machine (JVM)** اجرا می‌شود.

معماری:

```text
Linux

↓

JVM

↓

Tomcat

↓

Jira
````

---

# 52. JVM Memory Model

حافظه JVM به چند بخش تقسیم می‌شود:

```text
JVM Memory

├── Heap
├── Metaspace
├── Thread Stack
├── Code Cache
└── Native Memory
```

---

# 53. Heap Memory

Heap محل نگهداری Objectهای برنامه است.

نمونه:

* Issues
* Users
* Workflows
* Cache Objects

---

Heap شامل:

```text id="heap01"
Young Generation

↓

Old Generation
```

---

# 54. Young Generation

Objectهای جدید ابتدا وارد Young Gen می‌شوند.

```text id="yg01"
Create Object

↓

Young Generation
```

اگر عمر کوتاهی داشته باشند:

```text id="yg02"
Garbage Collection

↓

Removed
```

---

# 55. Old Generation

Objectهایی که مدت بیشتری زنده می‌مانند به Old Gen منتقل می‌شوند.

نمونه:

* Cache Objects
* Configuration
* Long-lived Sessions

---

# 56. Metaspace

محل ذخیره:

* Class Metadata
* Loaded Classes
* Reflection Data

---

در Java 8 به بعد، Metaspace جایگزین PermGen شده است.

---

# 57. Thread Stack

هر Thread یک Stack اختصاصی دارد.

```text id="stack01"
Thread

↓

Method Call

↓

Local Variables

↓

Return
```

---

# 58. Code Cache

محل ذخیره کدهای JIT Compiler.

هدف:

افزایش سرعت اجرای برنامه.

---

# 59. Garbage Collection (GC)

GC حافظه بلااستفاده را آزاد می‌کند.

```text id="gc01"
Object Created

↓

Used

↓

No Reference

↓

Garbage Collection

↓

Memory Released
```

---

# 60. انواع Garbage Collection

در JVMهای جدید معمولاً:

* G1GC (پیشنهادی)
* ZGC (در برخی سناریوها)
* Shenandoah (در برخی توزیع‌های Java)

---

برای Jira Data Center معمولاً G1GC انتخاب پیش‌فرض مناسبی است.

---

# 61. Minor GC

روی Young Generation اجرا می‌شود.

مزایا:

* سریع
* تأخیر کم

---

# 62. Major / Full GC

روی Old Generation اجرا می‌شود.

اگر زیاد اتفاق بیفتد:

* افزایش Response Time
* کاهش Performance
* توقف‌های طولانی

---

# 63. Heap Sizing

Heap خیلی کوچک:

```
Frequent GC
```

Heap خیلی بزرگ:

```
Long Full GC
```

---

هدف:

Heap متناسب با:

* RAM
* تعداد کاربران
* اندازه Instance

---

# 64. Thread Model

هر درخواست HTTP معمولاً توسط یک Thread پردازش می‌شود.

```text id="thr01"
HTTP Request

↓

Tomcat Thread

↓

Jira Service

↓

Database

↓

Response
```

---

# 65. Thread Pool

Tomcat از Thread Pool استفاده می‌کند.

مزایا:

* استفاده مجدد از Threadها
* کاهش هزینه ایجاد Thread جدید
* افزایش Throughput

---

# 66. Thread Contention

اگر تعداد Threadها زیاد باشد:

* CPU افزایش می‌یابد.
* Context Switching زیاد می‌شود.
* Performance کاهش پیدا می‌کند.

---

# 67. CPU Utilization

CPU بالا همیشه نشانه مشکل نیست.

بررسی شود:

* GC
* Indexing
* Pluginها
* Database Wait
* Background Jobs

---

# 68. Memory Leak

Memory Leak زمانی رخ می‌دهد که Objectها دیگر موردنیاز نیستند اما همچنان Reference دارند.

علائم:

* Heap رشد مداوم
* Full GC زیاد
* OutOfMemoryError

---

# 69. OutOfMemoryError

نمونه:

```text id="oom01"
java.lang.OutOfMemoryError
```

دلایل:

* Heap کوچک
* Memory Leak
* Plugin معیوب
* Queryهای سنگین

---

# 70. Thread Dump

برای تحلیل Threadها استفاده می‌شود.

بررسی:

* Deadlock
* Waiting Threads
* Blocked Threads
* High CPU Threads

---

# 71. Heap Dump

برای تحلیل حافظه استفاده می‌شود.

ابزارهای رایج:

* Eclipse MAT
* VisualVM
* JDK Tools

---

# 72. JVM Monitoring

شاخص‌های مهم:

```text id="mon01"
Heap Usage

GC Time

GC Count

Thread Count

CPU Usage

Metaspace Usage
```

---

# 73. Performance Best Practices

✓ استفاده از Java نسخه پشتیبانی‌شده

✓ مانیتورینگ Heap

✓ بررسی GC Logs

✓ محدود کردن Pluginهای غیرضروری

✓ تنظیم مناسب Heap

✓ استفاده از SSD/NVMe

---

# 74. Common JVM Problems

## Full GC زیاد

علت:

* Heap کوچک
* Memory Leak

---

## Thread Starvation

علت:

* Thread Pool کوچک
* Queryهای طولانی

---

## CPU بالا

علت:

* GC
* Reindex
* Plugin
* Infinite Loop

---

# 75. Senior Jira Admin Checklist

```text id="chk75"
✓ Heap Usage Normal

✓ GC Frequency Acceptable

✓ No Full GC Storm

✓ Thread Count Stable

✓ CPU Usage Healthy

✓ No OutOfMemoryError

✓ JVM Logs Clean
```

---

# Day 7 Part 4 Summary

موضوعات:

✓ JVM Architecture
✓ Heap Memory
✓ Metaspace
✓ Garbage Collection
✓ Thread Model
✓ Thread Pool
✓ Memory Leak
✓ Thread Dump
✓ Heap Dump
✓ JVM Monitoring
✓ Performance Best Practices

---

# Next Part

Day 7 - Part 5:

* Startup Sequence
* Background Services
* Scheduler
* Cluster Locks
* Health Checks
* Production Operations
* Monitoring & Troubleshooting

```
```
