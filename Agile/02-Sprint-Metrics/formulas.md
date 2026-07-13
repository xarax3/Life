# Sprint Metrics: فرمول‌ها و KPIها

## پیش‌نیازهای داده

`Initial` مقدار کار در لحظه شروع Sprint، `Added` و `Removed` تغییرات پس از شروع، و `Completed` مقدار کار با وضعیت Done در پایان Sprint است. واحد همهٔ متغیرها باید یکسان باشد (معمولاً Story Point).

| شاخص | فرمول | کاربرد | تفسیر محتاطانه |
|---|---|---|---|
| Final commitment | `Initial + Added - Removed` | اندازهٔ واقعی Sprint | اختلاف زیاد با Initial، ناپایداری Scope را نشان می‌دهد. |
| Commitment reliability | `Completed / Initial × 100` | تحقق تعهد آغاز Sprint | فقط همراه با Scope Change و Sprint Goal بررسی شود. |
| Completion rate | `Completed / Final × 100` | تکمیل کار نهایی Sprint | در Sprint با Scope افزوده، از Reliability گویا‌تر است. |
| Scope growth | `(Final - Initial) / Initial × 100` | تغییر خالص Scope | مقدار منفی می‌تواند حذفِ کار یا کوچک‌سازی Sprint باشد. |
| Spillover rate | `Incomplete initial work / Initial × 100` | انتقال کار تعهدشده | Issueهای اضافه‌شده را جدا گزارش کنید. |
| Focus factor | `Completed effort / Effective capacity × 100` | نسبت کار تحویلی به ظرفیت واقعی | برای روند تیم است، نه هدف عملکردی. |
| Predictability | `min(Completed, Initial) / Initial × 100` | قابلیت اتکای برنامه | Completion بالاتر از Initial می‌تواند حاصل Scope افزوده باشد. |

## مثال یک Sprint

| مقدار | Story Point |
|---|---:|
| Initial | 40 |
| Added | 8 |
| Removed | 3 |
| Completed | 36 |
| Effective capacity | 45 |

پس `Final = 45`، `Reliability = 90%`، `Completion rate = 80%`، `Scope growth = 12.5%` و `Focus factor = 80%` است. اگر 4 SP از کار اولیه ناتمام مانده باشد، `Spillover = 10%` است.

## نکات گزارش‌دهی

- مخرج صفر را `N/A` نمایش دهید، نه صفر درصد.
- میانگین را در بازهٔ حداقل 5 تا 8 Sprint گزارش کنید؛ یک Sprint برای نتیجه‌گیری کافی نیست.
- برای Velocity از میانه (median) نیز استفاده کنید تا Sprintهای غیرعادی اثر کمتری بگذارند.
- درصدها را با داستان Sprint توضیح دهید: تعطیلات، Incident، تغییر اولویت یا وابستگی خارجی.
