# Sprint Health Dashboard

هدف این Dashboard تصمیم‌گیری روزانه است؛ نه سنجش عملکرد افراد. یک Dashboard را به یک تیم و یک نوع مخاطب محدود کنید.

| ردیف | Gadget / گزارش | سؤال مدیریتی | پیکربندی پیشنهادی |
|---|---|---|---|
| بالا | Sprint Burndown | آیا تا پایان Sprint قابل‌تحویل هستیم؟ | Sprint فعال، Remaining estimate یا Story Point مطابق قرارداد تیم |
| بالا | Sprint Health / Filter Results | چه کارهایی خطر فوری دارند؟ | فیلتر «باز، اولویت بالا، عقب‌افتاده»؛ ستون‌های Key، Assignee، Status، Priority |
| بالا | Velocity Chart | ظرفیت برنامه‌ریزی آینده چیست؟ | 5 تا 8 Sprint اخیر، فقط یک تیم |
| میانی | Pie Chart | کارهای باز در کدام وضعیت گیر کرده‌اند؟ | فیلتر Sprint باز، Statistic type = Status |
| میانی | Created vs Resolved | آیا ورود کار از خروجی بیشتر است؟ | بازهٔ Sprint یا 30 روز؛ روند را ببینید نه یک روز را |
| میانی | Bug filter | ریسک کیفیت چیست؟ | Bugهای Sprint باز با Priority بالا |
| پایین | Activity Stream | چه تغییری نیاز به پیگیری دارد؟ | فقط پروژه و Sprint تیم؛ نویز عمومی را حذف کنید |

## ترتیب خواندن در Daily Scrum

1. Burndown را برای روند کلی ببینید، نه برای توضیح هر نفر.
2. Filter Results را باز کنید و مانع هر Issue پرریسک را مشخص کنید.
3. Pie Chart را برای WIP یا صف‌های غیرعادی بررسی کنید.
4. اگر Scope تغییر کرده، آن را جدا از عملکرد تیم گزارش کنید.

## نمونهٔ فیلترهای ذخیره‌شده

- `APP | Sprint | Open work`
- `APP | Sprint | High-priority bugs`
- `APP | Sprint | Unestimated work`
- `APP | Sprint | Blocked work` (فقط اگر وضعیت یا Label استاندارد Blocked دارید)

## ضدالگوها

- نمایش بیش از 6 تا 8 Gadget؛ Dashboard به دیوار اعلان تبدیل می‌شود.
- استفاده از Velocity برای مقایسهٔ تیم‌ها یا افراد.
- نمایش نموداری که اقدام مشخصی به دنبال ندارد.
- ترکیب چند پروژه با Workflow و واحد برآورد متفاوت در یک نمودار.
