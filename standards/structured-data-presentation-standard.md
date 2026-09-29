# Diaco Structured Data Presentation Standard

**Status:** ACTIVE  
**Version:** 1.0

## هدف

یکدست کردن خروجی‌های Structured Data در Spreadsheet، Report، Business List، Admin Table و Screenهای داده‌محور، در حالی که هر پروژه بتواند Theme بصری خودش را داشته باشد.

## اصل اصلی

**Structure قابل‌استفاده مجدد است؛ Theme قابل‌تعویض است.**

این دو را با هم اشتباه نکن:

**Structure**
- Information Architecture
- ترتیب
- Alignment
- Direction
- Behavior

**Theme**
- رنگ
- آیکون
- Branding
- Shadow
- Decoration

یک پروژه می‌تواند ظاهرش را تغییر دهد بدون اینکه Structure تأییدشده اطلاعات تغییر کند.

## نمایش داده فارسی

برای خروجی‌های فارسی:

- Direction برابر RTL باشد،
- سلول‌های Structured Table به‌صورت پیش‌فرض Center باشند،
- Header از Data واضح جدا باشد،
- ترتیب Fieldها قابل‌پیش‌بینی باشد،
- در Result Setهای شماره‌دار، شماره‌گذاری از 1 شروع و پیوسته ادامه پیدا کند،
- Identifier و Contact Fieldها سریع قابل‌اسکن باشند،
- خروجی مختصر و خوانا باشد و Raw Field غیرضروری نمایش داده نشود.

اگر ماهیت یک Field به‌وضوح Alignment دیگری می‌طلبد یا Reference پروژه چیز دیگری را تأیید کرده، استثنا مجاز است.

## Schema اصلی Business / Lead List

ترتیب ترجیحی:

1. `ردیف`
2. `نام کسب‌وکار`
3. نوع یا Classification قابل‌فهم برای کاربر، مثل `نوع تعمیرگاه`
4. Category منبع، مثل `دسته‌بندی`
5. `آدرس خلاصه`
6. `شماره تلفن`
7. `وب‌سایت`
8. Rating، مثل `امتیاز Google`
9. Review Count، مثل `تعداد Review`

Fieldهای اختصاصی Task می‌توانند اضافه شوند، اما تا حد امکان ترتیب اصلی حفظ شود.

## رفتار Spreadsheet

برای Workbookهای فارسی و مرتب:

- Worksheet به‌صورت RTL باشد،
- وقتی Table Formatting استفاده می‌شود Gridline مخفی شود،
- Title و Subtitle اختیاری می‌توانند عرض Table را پوشش دهند،
- بین Title / Subtitle و Header جدول فاصله بصری وجود داشته باشد،
- برای Listهای بلند Header ناحیه Data Freeze شود،
- Filter روی Table واقعی فعال باشد،
- به‌جای Autofit کنترل‌نشده، Width خوانا و هدفمند استفاده شود،
- Header و Structured Data به‌صورت پیش‌فرض Center باشند،
- Border و Row Banding محدود و خوانا باشند،
- Phone Number در صورت نیاز به‌صورت Text نگه داشته شود،
- Rating با Format یکدست نمایش داده شود،
- Missing Value هرگز ساخته نشود.

## رفتار Application / Website

برای Applicationهای فارسیِ داده‌محور:

- RTL جهت خواندن پیش‌فرض است،
- Sidebar / Navigation اصلی سمت راست Baseline ترجیحی است مگر Reference تأییدشده پروژه متفاوت باشد،
- Tableها و Formها در Screenهای مشابه ترتیب Field یکدست داشته باشند،
- Structured Table Valueها به‌صورت پیش‌فرض Center باشند،
- رنگ و آیکون می‌توانند بر اساس پروژه تغییر کنند بدون اینکه Information Hierarchy تغییر کند.

## انعطاف Theme

موارد زیر توسط این Standard ثابت نمی‌شوند:

- رنگ دقیق
- Icon Family
- Font Family
- Border Radius
- Shadow
- Decorative Background
- Brand-specific Visual Identity

این موارد متعلق به Theme پروژه یا UI Standard عمومی هستند.

## Verification

پیش از تحویل Structured Data:

- [ ] RTL خروجی فارسی درست است.
- [ ] Fieldهای اصلی ترتیب هدفمند دارند.
- [ ] شماره‌گذاری در صورت استفاده پیوسته است.
- [ ] Alignment داده‌ها یکدست است.
- [ ] Duplicate و Recordهای واضحاً نامرتبط در صورت نیاز مدیریت شده‌اند.
- [ ] Missing Data ساخته نشده است.
- [ ] Tableهای بلند با Freeze / Filter یا رفتار معادل قابل‌استفاده مانده‌اند.
- [ ] تغییر Theme باعث شکستن Structure تأییدشده نشده است.

## Reference Implementation

ببین:

`references/babol-mechanics-excel-golden-template.md`
