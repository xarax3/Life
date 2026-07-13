# Data Quality for Reporting

گزارش درست از دادهٔ درست می‌آید. کیفیت داده یک مسئولیت مشترک میان تیم، Product Owner و Jira administrator است.

## قرارداد حداقلی داده

| داده | مالک | زمان تکمیل | استفاده |
|---|---|---|---|
| Issue type | درخواست‌کننده / PO | ایجاد Issue | تفکیک جریان و گزارش |
| Summary و Acceptance Criteria | PO و تیم | پیش از ورود به Sprint | آماده‌بودن کار |
| Story point یا estimate | تیم | Refinement | Forecast |
| Sprint | تیم | Sprint Planning | Sprint report |
| Component / service | مالک فنی | ایجاد یا refinement | Ownership و Incident analysis |
| Resolution | Workflow | فقط هنگام Done | کیفیت گزارش‌های بسته‌شدن |

## فیلتر کنترل کیفیت

```jql
project = APP
AND statusCategory != Done
AND (
    issuetype is EMPTY
    OR summary is EMPTY
    OR "Story Points" is EMPTY
)
ORDER BY created ASC
```

این JQL یک الگو است. فیلدهای اجباری را متناسب با Issue type انتخاب کنید؛ Bug ممکن است Story Point نخواهد، اما Severity و Component لازم داشته باشد.

## شاخص‌های کیفیت داده

- درصد Issueهای باز بدون Owner یا Component
- درصد Storyهای وارد Sprint بدون estimate یا Acceptance Criteria
- تعداد Transitionهای دستیِ برگشت‌خورده
- تعداد Ruleهای Automation با خطا در Audit log

هدف، صفرکردن کورکورانهٔ این اعداد نیست؛ هدف، کاهش داده‌ای است که تصمیم را گمراه می‌کند.
