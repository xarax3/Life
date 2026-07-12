````markdown id="d7p6lb"
# File: Life/Agile/Jira/07-Jira-Data-Center-Architecture-and-Administration/load-balancer-and-network.md

# Day 7 - Part 6
# Load Balancer, Reverse Proxy, SSL/TLS & Network Architecture

> طراحی لایه Network برای Jira Data Center، ارتباط Load Balancer، Reverse Proxy، SSL و معماری Production.

---

# 97. Jira Data Center Network Architecture

معماری استاندارد Production:

```text
                    Users

                      |

                Internet / LAN

                      |

              Reverse Proxy / WAF

                      |

              Load Balancer

          /        |        \

     Jira Node1 Jira Node2 Jira Node3

          \        |        /

              Database Layer

                      |

              Shared Storage
````

---

# 98. نقش Load Balancer

Load Balancer وظیفه:

* توزیع درخواست‌ها
* Health Check
* Failover
* مدیریت Session

را دارد.

---

# 99. Load Balancing Algorithm

روش‌های رایج:

## Round Robin

درخواست‌ها چرخشی تقسیم می‌شوند.

```text
Request 1 → Node1

Request 2 → Node2

Request 3 → Node3
```

---

## Least Connections

ارسال درخواست به Node با کمترین Connection.

---

## IP Hash

بر اساس IP کاربر انتخاب Node.

---

# 100. Session Management

در Jira Data Center:

Session باید بین Nodeها هماهنگ باشد.

---

دو روش:

## Sticky Session

کاربر به همان Node برگردانده می‌شود.

```text
User A

↓

Node 1

↓

Always Node 1
```

---

## Non-Sticky Session

Session بین Nodeها مدیریت می‌شود.

---

# 101. Sticky Session در Jira

معمولاً پیشنهاد می‌شود:

```text
Enable Session Affinity
```

در Load Balancer.

---

مزایا:

* کاهش Session Replication
* کاهش Traffic داخلی

---

# 102. Health Check Design

Load Balancer باید بررسی کند:

```text
Node Available?

↓

HTTP Response OK?

↓

Application Ready?
```

---

Health Check نباید فقط Ping باشد.

مثال:

ضعیف:

```text
ICMP Ping
```

---

بهتر:

```text
HTTP Health Endpoint
```

---

# 103. Reverse Proxy چیست؟

Reverse Proxy بین کاربر و Jira قرار می‌گیرد.

وظایف:

* SSL Termination
* Security Headers
* Compression
* Routing
* Protection

---

معماری:

```text
Client

↓

Nginx

↓

Jira
```

---

# 104. Nginx در Jira Architecture

Nginx می‌تواند برای:

* SSL
* Reverse Proxy
* Static Content
* Rate Limiting

استفاده شود.

---

نمونه Flow:

```text
HTTPS

↓

Nginx :443

↓

HTTP/HTTPS

↓

Jira :8080
```

---

# 105. HAProxy در Jira Architecture

HAProxy مناسب:

* Load Balancing
* Health Check
* TCP/HTTP Routing

است.

---

نمونه:

```text
Frontend

↓

Backend Pool

↓

Jira Nodes
```

---

# 106. SSL/TLS Architecture

سه مدل رایج:

---

## SSL Termination

SSL در Proxy تمام می‌شود.

```text
User HTTPS

↓

Nginx HTTP

↓

Jira
```

---

## End-to-End SSL

تمام مسیر SSL است.

```text
User HTTPS

↓

Proxy HTTPS

↓

Jira HTTPS
```

---

## Re-encryption

SSL دوباره در Proxy ایجاد می‌شود.

---

# 107. SSL Certificate Management

موارد مهم:

* Certificate Expiration
* Private Key Security
* Chain Validation
* Renewal Process

---

بررسی:

```bash id="ssl01"
openssl x509 -in certificate.crt -text -noout
```

---

# 108. HTTP Headers مهم

Reverse Proxy باید Headerهای درست ارسال کند.

مهم:

```text id="head01"
X-Forwarded-For

X-Forwarded-Host

X-Forwarded-Proto

Host
```

---

# 109. Jira Proxy Configuration

Jira باید Proxy را بشناسد.

در:

```text
server.xml
```

تنظیمات:

```xml id="xml01"
proxyName

proxyPort

scheme

secure
```

---

# 110. Example Configuration Concept

```xml
<Connector

port="8080"

proxyPort="443"

scheme="https"

secure="true"

/>
```

---

# 111. Network Segmentation

معماری امن:

```text
Users Network

↓

DMZ

↓

Application Network

↓

Database Network

↓

Storage Network
```

---

# 112. Firewall Rules

حداقل دسترسی:

## Users → Load Balancer

```text
443/tcp
```

---

## Load Balancer → Jira Nodes

```text
8080/tcp
```

---

## Jira Nodes → Database

```text
5432/tcp
```

---

## Jira Nodes → Shared Storage

```text
2049/tcp (NFS)
```

---

# 113. DNS Design

پیشنهاد:

نام منطقی:

```text
jira.company.com
```

نه:

```text
jira-node1.company.com
```

---

کاربر فقط Load Balancer را می‌بیند.

---

# 114. Network Troubleshooting

مشکلات رایج:

## 502 Bad Gateway

دلایل:

* Jira Down
* Port اشتباه
* Firewall
* Timeout

---

## Slow Response

بررسی:

* Network Latency
* Database
* JVM
* Storage

---

## Connection Reset

بررسی:

* Proxy Timeout
* Load Balancer Settings
* Firewall

---

# 115. Production Reference Architecture

```text
                 Users

                   |

              Firewall/WAF

                   |

              Nginx/HAProxy

                   |

        +----------+----------+

        |          |          |

     Jira-1     Jira-2     Jira-3

        |          |          |

        +----------+----------+

                   |

             PostgreSQL HA

                   |

              Shared NFS
```

---

# 116. Senior Jira Admin Checklist

Network:

```text
✓ SSL Valid

✓ Proxy Headers Correct

✓ Health Checks Working

✓ Firewall Rules Reviewed

✓ DNS Correct

✓ Timeout Configured
```

---

# Day 7 Part 6 Summary

موضوعات:

✓ Load Balancer
✓ Reverse Proxy
✓ Nginx/HAProxy
✓ SSL/TLS
✓ Session Management
✓ Health Check
✓ Firewall Design
✓ Network Segmentation
✓ Production Architecture

---

# Next Part

Day 7 - Part 7:

* Final Jira Data Center Reference Architecture
* Capacity Planning
* Scaling Strategy
* Monitoring Stack
* Backup Strategy
* Day 7 Complete Summary

```
```
