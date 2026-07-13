# پروژهٔ نهایی: Delivery Operating System در Jira

## سناریو

یک محصول SaaS با سه تیم (Platform، Checkout و Mobile) می‌خواهد زمان فعال‌سازی مشتری را از سه روز به یک روز کاهش دهد. وابستگی میان تیم‌ها، ورود Bugهای فوری و گزارش‌های ناسازگار باعث شده Forecast قابل اعتماد نباشد.

## تحویل‌دادنی‌ها

### 1. مدل داده و Workflow

- Issue typeهای Initiative، Epic، Story، Bug و Dependency را تعریف کنید.
- Definition of Ready و Definition of Done را برای Story و Bug بنویسید.
- Component و Owner هر سرویس را مشخص کنید.

### 2. گزارش و Dashboard

- Dashboard تیمی: Sprint Burndown/Burnup، کارهای پرریسک، WIP و Bugهای با اولویت بالا.
- Dashboard جریان: Control Chart یا CFD، Work Item Age و throughput trend.
- Dashboard Portfolio: Initiative status، وابستگی‌های در خطر و Outcome metric.

### 3. Automation و Governance

- Rule بستن Parent بعد از تکمیل Sub-taskها، با Audit log.
- Rule اعلان Dependency at risk با شرط دقیق و بدون Spam.
- Data dictionary، Owner دارایی‌های Jira و روال بازبینی ماهانه.

### 4. Forecast و تصمیم

- بر اساس 5 تا 8 Sprint اخیر، یک بازهٔ Forecast برای Epic بسازید.
- Capacity و ریسک وابستگی را جداگانه توضیح دهید.
- یک تصمیم Portfolio ثبت کنید: ادامه، تغییر Scope یا تأخیر؛ دلیل را به Outcome وصل کنید.

## چک‌لیست ارزیابی

| معیار | پرسش |
|---|---|
| شفافیت | آیا هر نمودار، فیلتر و Rule مالک و هدف دارد؟ |
| کیفیت داده | آیا فیلدهای اجباری واقعاً در تصمیم یا گزارش مصرف می‌شوند؟ |
| قابلیت اقدام | آیا هر Dashboard به یک گفت‌وگو یا تصمیم منتهی می‌شود؟ |
| ایمنی | آیا Automation محدود، آزمایش‌شده و audit-able است؟ |
| Outcome | آیا Initiative به یک اثر قابل اندازه‌گیری برای مشتری وصل است؟ |

## Definition of Done دوره

دوره زمانی تمام شده است که بتوانید این سناریو را برای یک ذی‌نفع در 15 دقیقه ارائه دهید: مسئله، دادهٔ قابل‌اعتماد، جریان کار، ریسک، Forecast و تصمیم بعدی. در ارائه از Velocity فردی یا درصدهای بدون زمینه استفاده نکنید.
