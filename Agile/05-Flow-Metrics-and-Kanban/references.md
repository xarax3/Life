# Agile, Scrum, Kanban, Jira & DevOps References

> منابع مرجع برای مطالعه عمیق‌تر Agile، Scrum، Jira Reporting، Kanban Flow Metrics و DevOps Metrics.

---

# 1. Agile Manifesto

## نام

Agile Manifesto

---

## موضوع

اصول پایه Agile.

---

## موارد اصلی

چهار ارزش اصلی:

1. Individuals and interactions
2. Working software
3. Customer collaboration
4. Responding to change

---

## کاربرد

برای درک فلسفه Agile.

---

# 2. Scrum Guide

## نام

Scrum Guide

---

## موضوع

مرجع رسمی Scrum Framework.

---

## شامل:

- Scrum Roles
- Events
- Artifacts
- Rules

---

## مفاهیم مهم:

```
Product Backlog

Sprint

Increment

Definition of Done
```

---

# 3. Kanban Guide

## موضوع

مدیریت Flow با Kanban.

---

## مفاهیم اصلی:

- Visualize Workflow
- Limit WIP
- Manage Flow
- Improve Continuously

---

# 4. Accelerate Book

## نویسندگان:

Nicole Forsgren

Jez Humble

Gene Kim

---

## موضوع:

تحقیق DORA Metrics.

---

## مفاهیم:

چهار شاخص اصلی:

```
Deployment Frequency

Lead Time for Changes

Change Failure Rate

MTTR
```

---

# 5. Team Topologies

## موضوع:

طراحی تیم‌ها برای Delivery بهتر.

---

## مفاهیم:

- Stream-aligned Team
- Platform Team
- Enabling Team

---

# 6. Jira Official Documentation

## موضوع:

مدیریت Jira Software.

---

## بخش‌های مهم:

- Boards
- Workflows
- Reports
- Dashboards
- JQL
- Automation

---

# 7. Jira Reports Reference

## Reports مهم:

| Report | کاربرد |
|-|-|
| Burndown | Sprint Progress |
| Burnup | Scope Tracking |
| Velocity | Team Output |
| Control Chart | Cycle Time |
| CFD | Flow |
| Sprint Report | Sprint Analysis |
| Release Report | Version Tracking |

---

# 8. JQL Reference

## کاربرد:

جستجوی پیشرفته Issueها.

---

## مثال:

تمام Bugهای باز:

```jql
issuetype = Bug
AND status != Done
```

---

## مثال:

کارهای قدیمی:

```jql
created <= -30d
AND statusCategory != Done
```

---

# 9. DevOps References

## مفاهیم:

- CI/CD
- Continuous Delivery
- Infrastructure as Code
- Observability
- SRE

---

# 10. SRE Resources

## مفاهیم:

- Reliability
- Error Budget
- SLO
- Incident Management

---

# 11. ITIL References

## ارتباط با Jira Service Management

مفاهیم:

- Incident Management
- Change Management
- Problem Management
- Service Request

---

# 12. Metrics Relationship Model

مدل ارتباط Metrics:

```
                 Business Value

                       ↑

              Delivery Performance

                       ↑

        Agile Metrics + DevOps Metrics

                       ↑

             Jira + CI/CD + ITSM Data
```

---

# 13. Recommended Learning Path

## Level 1 - Foundation

یادگیری:

```
Agile

Scrum

Kanban
```

---

## Level 2 - Jira

یادگیری:

```
Project Configuration

Workflow

Permission

JQL

Reports
```

---

## Level 3 - Metrics

یادگیری:

```
Flow Metrics

DORA

SLE

SLA
```

---

## Level 4 - Enterprise

یادگیری:

```
Governance

Scaling Agile

Automation

Integration

Performance
```

---

# 14. Enterprise Jira Admin Reference Areas

## Configuration

```
Issue Type Scheme

Workflow Scheme

Screen Scheme

Field Configuration

Permission Scheme
```

---

## Governance

```
Naming Convention

Workflow Standard

Custom Field Management

Project Template

Audit
```

---

## Reporting

```
Executive Dashboard

Team Dashboard

Flow Dashboard

DevOps Dashboard
```

---

# 15. Practical Implementation Checklist

## Jira Setup

```
✓ Define Issue Types

✓ Design Workflow

✓ Configure Boards

✓ Create Filters

✓ Build Dashboards
```

---

## Agile Process

```
✓ Backlog Refinement

✓ Sprint Planning

✓ Daily Scrum

✓ Review

✓ Retrospective
```

---

## Metrics

```
✓ Velocity

✓ Cycle Time

✓ Lead Time

✓ Throughput

✓ WIP

✓ DORA Metrics
```

---

# 16. Recommended Jira Apps for Advanced Reporting

## eazyBI

برای:

- Advanced Reporting
- Data Analysis
- Custom Metrics

---

## Automation for Jira

برای:

- Workflow Automation
- Notifications
- Data Updates

---

## ScriptRunner

برای:

- Advanced JQL
- Custom Automation
- Administration

---

# 17. Final Architecture View

یک سیستم Agile Enterprise:

```
              Business

                 |

            Product Management

                 |

              Jira

                 |

     Development + QA + Operations

                 |

        CI/CD + Monitoring + ITSM

                 |

              Metrics

                 |

        Continuous Improvement
```

---

# Day 5 Final Summary

در روز پنجم یاد گرفتیم:

## Flow Metrics

- Lead Time
- Cycle Time
- Throughput
- WIP
- Flow Efficiency

## Jira Reports

- Control Chart
- CFD
- Aging Chart
- Scatter Plot
- Burnup
- Burndown

## DORA

- Deployment Frequency
- Lead Time for Changes
- Change Failure Rate
- MTTR

## Kanban

- SLE
- WIP Limit
- Flow Optimization

## Jira Enterprise

- Dashboard Design
- Reporting Strategy
- Governance

---

# پایان Day 5

Next:

# Day 6 — Advanced Scrum & Jira Scrum Administration

Topics:

- Scrum Framework Deep Dive
- Product Backlog Management
- Epic Strategy
- Story Writing
- Acceptance Criteria
- Refinement Process
- Estimation Methods
- Capacity Planning
- Sprint Planning
- Release Planning
- Jira Scrum Configuration
- Enterprise Scrum Best Practices
