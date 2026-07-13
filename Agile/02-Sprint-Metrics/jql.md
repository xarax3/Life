# JQLهای کاربردی Sprint

> JQL به‌تنهایی Snapshot شروع Sprint یا زمان افزوده‌شدن Issue را نگه نمی‌دارد. برای Scope Change تاریخی از Sprint Report، Automation، eazyBI یا افزونه‌ای مانند ScriptRunner استفاده کنید.

## فیلترهای پایه

| هدف | JQL |
|---|---|
| تمام کارهای Sprint باز | `project = APP AND Sprint in openSprints()` |
| کار Done در Sprint باز | `project = APP AND Sprint in openSprints() AND statusCategory = Done` |
| کار باقی‌مانده | `project = APP AND Sprint in openSprints() AND statusCategory != Done` |
| Bugهای Sprint | `project = APP AND Sprint in openSprints() AND issuetype = Bug` |
| کار با اولویت بالا | `project = APP AND Sprint in openSprints() AND priority in (Highest, High)` |
| کار بدون برآورد | `project = APP AND Sprint in openSprints() AND "Story Points" is EMPTY` |

`APP` را با کلید پروژه و `"Story Points"` را با نام واقعی فیلد برآورد خود جایگزین کنید. در بعضی پروژه‌ها فیلد «Story point estimate» نام دارد.

## کنترل سلامت Sprint

```jql
project = APP
AND Sprint in openSprints()
AND statusCategory != Done
AND duedate < startOfDay()
ORDER BY priority DESC, updated ASC
```

این فیلتر برای Daily Scrum مناسب است: کارهای بازِ عقب‌افتاده را به ترتیب اولویت نشان می‌دهد. اگر Due date در تیم استفاده نمی‌شود، آن شرط را حذف کنید.

```jql
project = APP
AND Sprint in openSprints()
AND created >= startOfDay(-7d)
ORDER BY created DESC
```

این فیلتر Issueهای تازه‌ساخته‌شده را نشان می‌دهد، اما الزاماً «Added to sprint» نیست؛ آن دو رویداد متفاوت‌اند.

## Scope change تاریخی

در ScriptRunner نمونه‌ای از تابع افزونه‌محور ممکن است چنین باشد:

```jql
issueFunction in addedAfterSprintStart("APP Sprint 24")
```

نام تابع و پشتیبانی آن به افزونه و نسخهٔ Jira وابسته است. پیش از ساخت Dashboard، آن را در محیط خود تست کنید و نتیجه را با بخش **Added issues** در Sprint Report تطبیق دهید.

## راهنمای استفاده

- Filter را با نام، مالک و سطح دسترسی مشخص ذخیره کنید؛ نام پیشنهادی: `APP | Sprint | Open work`.
- در Dashboard به جای یک فیلتر بسیار بزرگ، فیلترهای کوچک و هدف‌دار استفاده کنید.
- `statusCategory = Done` از نام وضعیت‌ها پایدارتر است؛ مگر تیم تعریف Done متفاوتی داشته باشد.
