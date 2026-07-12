ادامه روز هفتم — بخش امنیت معماری Jira Data Center:

# File: Life/Agile/Jira/07-Jira-Data-Center-Architecture-and-Administration/security-architecture.md

# Day 7 - Part 9

# Jira Data Center Security Architecture

> طراحی مدل امنیتی Jira Data Center، Authentication، Authorization، SSO، LDAP، Audit و Hardening در محیط Enterprise.

---

# 151. Jira Security Architecture Overview

مدل امنیتی Jira شامل چند لایه است:

```text
User

↓

Identity Provider

↓

Authentication

↓

Authorization

↓

Jira Permission Model

↓

Application Data
```

---

# 152. Authentication vs Authorization

## Authentication

تشخیص هویت کاربر.

سؤال:

```text
Who are you?
```

مثال:

* Username/Password
* LDAP
* SSO
* SAML

---

## Authorization

تعیین سطح دسترسی.

سؤال:

```text
What can you access?
```

مثال:

* Project Permission
* Issue Permission
* Field Permission

---

# 153. Identity Management Architecture

معماری Enterprise:

```text
                Users

                  |

          Identity Provider

                  |

        LDAP / Active Directory

                  |

              Jira DC
```

---

# 154. LDAP Integration

LDAP برای مدیریت کاربران مرکزی استفاده می‌شود.

اطلاعات:

* Users
* Groups
* Attributes

---

Flow:

```text
User Login

↓

Jira Query LDAP

↓

Validate Credentials

↓

Create Session

↓

Access Jira
```

---

# 155. LDAP Best Practices

✓ استفاده از LDAPS

✓ محدود کردن Base DN

✓ Sync دوره‌ای کاربران

✓ مدیریت Groupها در Directory

✓ جلوگیری از Local User زیاد

---

# 156. SSO Architecture

Single Sign-On باعث می‌شود کاربر یک بار Login کند.

مدل:

```text
User

↓

Identity Provider

↓

Authentication Token

↓

Jira
```

---

روش‌های رایج:

* SAML
* OAuth
* OpenID Connect

---

# 157. SAML Authentication Flow

```text
User Opens Jira

↓

Jira Redirects To IdP

↓

User Authenticates

↓

IdP Sends Assertion

↓

Jira Creates Session
```

---

# 158. Permission Model در Jira

مدل دسترسی Jira چند لایه است:

```text
Global Permission

↓

Project Permission

↓

Issue Security

↓

Field Security

↓

Application Access
```

---

# 159. Global Permissions

سطح کل سیستم:

نمونه:

```text
Jira System Administrators

Jira Administrators

Browse Users

Create Shared Objects
```

---

# 160. Project Permissions

در سطح Project:

مثال:

```text
Browse Project

Create Issue

Edit Issue

Delete Issue

Transition Issue

Manage Sprints
```

---

# 161. Issue Security Scheme

برای محدود کردن یک Issue خاص.

مثال:

```text
Normal Issue

↓

All Project Members
```

---

یا:

```text
Confidential Issue

↓

Security Group Only
```

---

# 162. Permission Design Best Practice

اصل:

```text
Least Privilege
```

یعنی:

کمترین دسترسی لازم برای انجام کار.

---

اشتباه رایج:

```text
Grant Jira Admin To Everyone
```

---

# 163. Group-Based Access Model

مدل پیشنهادی:

```text
jira-users

jira-developers

jira-project-admins

jira-system-admins
```

---

دسترسی‌ها به Group داده شوند، نه User.

---

# 164. Admin Account Security

برای Administrator:

✓ MFA

✓ Password Policy

✓ Separate Admin Account

✓ Audit Monitoring

---

# 165. Audit Logging

هدف:

ثبت فعالیت‌های مهم.

موارد:

```text
User Login

Permission Change

Workflow Change

Configuration Change

Admin Actions
```

---

# 166. Security Monitoring

بررسی:

```text
Failed Login

Privilege Escalation

Unknown Admin Changes

Suspicious Activity
```

---

# 167. Application Security Hardening

اقدامات:

```text
Disable Unused Features

Remove Unused Apps

Update Plugins

Patch Jira

Review Permissions
```

---

# 168. Network Security

Jira باید در شبکه امن قرار گیرد:

```text
Internet

↓

Firewall

↓

Reverse Proxy

↓

Jira Application

↓

Database
```

---

# 169. HTTP Security Headers

تنظیمات مهم:

```text
X-Frame-Options

Content-Security-Policy

Strict-Transport-Security

X-Content-Type-Options
```

---

# 170. Database Security

موارد:

✓ Database User محدود

✓ عدم استفاده از Admin Database

✓ Encryption در صورت نیاز

✓ Backup امن

✓ Audit Database Access

---

# 171. File System Security

Permission مناسب:

```bash
chown -R jira:jira /var/atlassian
```

---

جلوگیری از:

* Write Access غیرضروری
* دسترسی کاربران دیگر
* تغییر فایل‌های حساس

---

# 172. Security Hardening Checklist

```text
✓ HTTPS Enabled

✓ Valid Certificate

✓ LDAP/SSO Configured

✓ MFA Enabled

✓ Permissions Reviewed

✓ Admin Access Controlled

✓ Plugins Audited

✓ Logs Monitored

✓ Backup Protected

✓ OS Patched
```

---

# Day 7 Part 9 Summary

موضوعات:

✓ Authentication
✓ Authorization
✓ LDAP
✓ SSO
✓ SAML
✓ Permission Model
✓ Issue Security
✓ Audit Logging
✓ Network Security
✓ Hardening Checklist

---

# Next Part

Day 7 - Part 10:

* Jira Data Center Backup & Disaster Recovery
* Backup Strategy
* Restore Testing
* RTO/RPO
* Disaster Scenarios
* Production Recovery Plan
