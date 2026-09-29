---
name: structured-data-output
description: خروجی‌های ساختاریافته فارسی و RTL مانند Excel Lead List، Business Directory، Data Table و Report Table را با Structure تأییدشده کاربر می‌سازد، در حالی که رنگ و آیکون می‌توانند بر اساس پروژه تغییر کنند.
---

# Structured Data Output

## چه زمانی استفاده شود

- ساخت Workbook فارسی در Excel
- خروجی گرفتن Lead / Business List
- ساخت Directory Table
- طراحی Admin Table داده‌محور
- تبدیل خروجی Scraper / API به Data قابل‌ارائه به کاربر
- وقتی کاربر می‌گوید «خروجی استاندارد من» یا عبارت مشابه

## Standard اجباری

بخوان:

`standards/structured-data-presentation-standard.md`

برای Taskهای Excel / Business List همچنین بخوان:

`references/babol-mechanics-excel-golden-template.md`

## Workflow

1. Data Source واقعی و Fieldها را مشخص کن.
2. Raw Fieldهای نامرتبط را حذف کن مگر اینکه کاربر به آن‌ها نیاز داشته باشد.
3. در صورت نیاز Deduplicate کن.
4. در صورت مفید بودن، Human-friendly Category را جدا از Source Category بساز.
5. ترتیب اطلاعات فارسی تأییدشده را اعمال کن.
6. شماره ردیف را از 1 به‌صورت پیوسته بساز.
7. Direction را RTL کن.
8. Structured Table Data را به‌صورت پیش‌فرض Center کن.
9. برای Tableهای بلند، در Formatهایی که پشتیبانی می‌کنند Filter / Freeze اضافه کن.
10. Theme پروژه فعلی را اعمال کن بدون تغییر Structure تأییدشده.
11. بررسی کن که Missing Value ساخته نشده باشد.

## Baseline فهرست کسب‌وکار

ترجیحاً:

`ردیف → نام کسب‌وکار → نوع کاربردی → دسته‌بندی منبع → آدرس خلاصه → شماره تلفن → وب‌سایت → امتیاز → تعداد Review`

Field اختصاصی فقط زمانی اضافه شود که خروجی را بهتر کند.

## Structure در برابر Theme

حفظ شود:
- RTL
- ترتیب
- Hierarchy
- Alignment Logic
- Numbering
- Usability جدول

قابل‌تغییر بر اساس پروژه:
- رنگ
- آیکون
- Font در صورت نیاز پروژه
- Decoration
- Brand Identity

## Verification

- [ ] RTL فارسی فعال است.
- [ ] شماره ردیف پیوسته است.
- [ ] Core Columnها ترتیب هدفمند دارند.
- [ ] Structured Data Cellها Center هستند مگر استثنای موجه.
- [ ] Categoryها برای کاربر قابل‌فهم هستند.
- [ ] Duplicate / Record نامرتبط در صورت نیاز مدیریت شده‌اند.
- [ ] Missing Data ساخته نشده است.
- [ ] تغییر Theme باعث تغییر Information Architecture نشده است.
