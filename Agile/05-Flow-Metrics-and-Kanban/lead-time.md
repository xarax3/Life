# Lead Time

> مهم‌ترین Flow Metric در Agile و Kanban که مدت‌زمان کل از ثبت درخواست تا تحویل نهایی به مشتری را اندازه‌گیری می‌کند.

---

# Definition

Lead Time مدت زمانی است که از لحظه‌ای که یک درخواست (Issue، Story، Bug، Task و...) ایجاد می‌شود تا زمانی که به مشتری یا کاربر نهایی تحویل داده می‌شود، سپری می‌شود.

به عبارت دیگر:

```
Lead Time

=

Request Created

↓

Delivered
```

Lead Time نشان‌دهنده تجربه واقعی مشتری است.

---

# هدف

Lead Time به این سؤال پاسخ می‌دهد:

> **کاربر از زمان ثبت درخواست تا دریافت نتیجه، چقدر منتظر می‌ماند؟**

---

# Lead Time شامل چه مراحلی است؟

Lead Time تمام زمان‌های زیر را در بر می‌گیرد:

- Waiting در Backlog
- تحلیل (Analysis)
- طراحی (Design)
- توسعه (Development)
- Code Review
- تست (Testing)
- آماده‌سازی Release
- Deployment
- تحویل به مشتری

---

# مثال

فرض کنید:

```
Issue Created

1 July
```

```
Development Started

5 July
```

```
Done

10 July
```

```
Production

12 July
```

Lead Time:

```
1 July

↓

12 July

=

11 Days
```

---

# تفاوت Lead Time و Cycle Time

```
Lead Time

Created

↓

Done
```

```
Cycle Time

Started

↓

Done
```

بنابراین:

```
Lead Time

≥

Cycle Time
```

زیرا Lead Time زمان انتظار قبل از شروع کار را نیز شامل می‌شود.

---

# اهمیت Lead Time

هرچه Lead Time کمتر باشد:

- مشتری سریع‌تر ارزش دریافت می‌کند.
- زمان انتظار کاهش می‌یابد.
- رضایت مشتری افزایش پیدا می‌کند.
- جریان کار روان‌تر است.

---

# عوامل مؤثر بر Lead Time

- اندازه Backlog
- تعداد آیتم‌های WIP
- زمان انتظار برای شروع
- سرعت توسعه
- زمان تست
- زمان Review
- فرآیند Release
- Deployment

---

# مثال واقعی

```
Created

Day 1
```

```
Backlog

3 Days
```

```
Development

4 Days
```

```
Testing

2 Days
```

```
Release

1 Day
```

Lead Time:

```
10 Days
```

---

# فرمول

```
Lead Time

=

Delivery Date

-

Creation Date
```

---

# Lead Time در Jira

در Jira Software به‌صورت پیش‌فرض گزارش مستقلی برای Lead Time وجود ندارد.

معمولاً از این ابزارها استفاده می‌شود:

- ActionableAgile Analytics
- Jira Align
- Atlassian Analytics
- eazyBI

---

# محاسبه با JQL

می‌توان Issueهای تکمیل‌شده را استخراج کرد:

```
project = ERP

AND

status = Done
```

اما برای محاسبه Lead Time نیاز به تاریخ ایجاد و تاریخ پایان داریم که معمولاً با افزونه‌ها یا گزارش‌های سفارشی محاسبه می‌شود.

---

# Dashboard KPI

شاخص‌های مرتبط:

- Average Lead Time
- Median Lead Time
- 85th Percentile Lead Time
- Max Lead Time
- Min Lead Time

---

# میانگین یا Median؟

مثال:

```
2
3
3
4
5
30
```

Average:

```
7.8
```

Median:

```
3.5
```

در عمل، Median معمولاً معیار مناسب‌تری است زیرا تحت تأثیر مقادیر غیرعادی (Outlier) قرار نمی‌گیرد.

---

# Percentile

در تیم‌های Kanban معمولاً از Percentile استفاده می‌شود.

مثال:

```
85%

از آیتم‌ها

کمتر از

8 روز
```

این معیار برای پیش‌بینی و SLE بسیار کاربردی است.

---

# ارتباط با سایر KPIها

```
Lead Time

↓

Cycle Time

↓

Throughput

↓

Forecast
```

کاهش Lead Time معمولاً باعث بهبود Forecast و افزایش رضایت مشتری می‌شود.

---

# چگونه Lead Time را کاهش دهیم؟

- کاهش WIP
- حذف مراحل غیرضروری
- خودکارسازی تست و Deployment
- کوچک‌تر کردن User Storyها
- کاهش زمان انتظار برای Review
- حذف گلوگاه‌ها

---

# مثال Enterprise

میانگین Lead Time:

```
18 Days
```

هدف سازمان:

```
10 Days
```

اقدامات:

- کاهش WIP از 15 به 8
- خودکارسازی تست
- حذف Approvalهای غیرضروری
- افزایش ظرفیت تیم QA

پس از سه Sprint:

```
Lead Time

11 Days
```

---

# Best Practices

✅ Lead Time را به‌صورت هفتگی بررسی کنید.

✅ از Median و Percentile استفاده کنید.

✅ روند (Trend) را تحلیل کنید، نه فقط یک مقدار.

✅ Lead Time را همراه با Cycle Time بررسی کنید.

---

# اشتباهات رایج

❌ تمرکز فقط روی Velocity.

❌ نادیده گرفتن زمان انتظار.

❌ تحلیل بر اساس میانگین بدون بررسی Outlierها.

❌ استفاده از Lead Time برای ارزیابی عملکرد یک فرد.

---

# Interview Questions

### Lead Time چیست؟

مدت زمان از ثبت درخواست تا تحویل نهایی به مشتری.

---

### چرا Lead Time مهم است؟

زیرا تجربه واقعی مشتری را اندازه‌گیری می‌کند و یکی از مهم‌ترین شاخص‌های Flow است.

---

### تفاوت Lead Time و Cycle Time چیست؟

Lead Time از زمان ایجاد درخواست محاسبه می‌شود، اما Cycle Time از زمان شروع کار.

---

### آیا Jira Lead Time را به‌صورت پیش‌فرض محاسبه می‌کند؟

خیر. معمولاً از ActionableAgile، Jira Align یا eazyBI استفاده می‌شود.

---

### چگونه Lead Time را کاهش می‌دهید؟

- کاهش WIP
- حذف Bottleneckها
- بهبود فرآیند Review
- اتوماسیون تست و استقرار

---

# Summary

| ویژگی | Lead Time |
|---------|-----------|
| هدف | اندازه‌گیری زمان انتظار مشتری |
| شروع | Creation Date |
| پایان | Delivery / Done |
| شامل زمان انتظار | ✅ |
| ابزارهای Jira | ActionableAgile، eazyBI |

---

# Enterprise Tips

## 1. فقط میانگین را گزارش نکنید.

همراه Average، مقدار Median و 85th Percentile را نیز نمایش دهید.

---

## 2. Lead Time را بر اساس نوع Issue تحلیل کنید.

Lead Time یک Bug معمولاً با یک Epic یا Story یکسان نیست.

---

## 3. روند تغییرات را بررسی کنید.

اگر Lead Time در چند Sprint متوالی افزایش یابد، احتمال وجود Bottleneck در فرآیند زیاد است.

---

## 4. Lead Time را با WIP مقایسه کنید.

در بسیاری از تیم‌ها افزایش WIP مستقیماً باعث افزایش Lead Time می‌شود.

---

## 5. از Lead Time برای Forecast استفاده کنید.

در Kanban و SLE، Lead Time مهم‌ترین ورودی برای پیش‌بینی زمان تحویل است.

---

# مثال کامل

فرض کنید:

| مرحله | تاریخ |
|--------|--------|
| Created | 1 Aug |
| Selected | 4 Aug |
| In Progress | 6 Aug |
| Code Review | 10 Aug |
| Testing | 12 Aug |
| Done | 14 Aug |
| Production | 15 Aug |

Lead Time:

```
15 - 1

=

14 Days
```

اگر تحلیل نشان دهد ۶ روز از این مدت صرف انتظار در Backlog شده است، تمرکز تیم باید بر کاهش زمان انتظار باشد، نه صرفاً افزایش سرعت توسعه.
