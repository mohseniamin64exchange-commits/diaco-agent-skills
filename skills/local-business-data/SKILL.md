---
name: local-business-data
description: با Toolهای تأییدشده Diaco، داده Local Business را برای Research، Supplier Discovery، Lead Generation و CRM Enrichment جمع‌آوری، پاک‌سازی، Verify و Export می‌کند. در صورت مناسب بودن Google Maps Scraper Kit ثبت‌شده ترجیح دارد.
---

# Local Business Data

## Tool ترجیحی

Tool اصلی ثبت‌شده:

`Mahanaicoach/google-maps-scraper-kit`

Reference:

`references/google-maps-scraper-kit.md`

## موارد استفاده

- یافتن Business بر اساس Category و Location
- Supplier / Vendor Discovery
- Local Market Research
- ساخت Prospect / Lead List
- Enrichment رکوردهای Business
- مقایسه Competitorهای محلی

## Workflow

1. نوع Business و محدوده جغرافیایی را مشخص کن.
2. Fieldهای واقعاً موردنیاز را تعیین کن.
3. ابتدا Validation Run کوچک را ترجیح بده.
4. Scrape هدفمند اجرا کن.
5. Resultها را Clean و Deduplicate کن.
6. وقتی Source Category بیش از حد Technical است، Classification قابل‌فهم برای انسان بساز.
7. Recordهای مهم را در صورت نیاز Verify کن.
8. بر اساس Format درخواستی پروژه Export کن.
9. برای Spreadsheet / List فارسی، `structured-data-output` را Load کن.
10. اگر Result قرار است دوباره استفاده شود، Source و Date را ثبت کن.

## Fieldهای ترجیحی Business List

برای خروجی فارسی:

1. ردیف
2. نام کسب‌وکار
3. نوع / طبقه‌بندی کاربردی
4. دسته‌بندی منبع
5. آدرس خلاصه
6. شماره تلفن
7. وب‌سایت
8. امتیاز
9. تعداد Review

Email، Coordinate، Social، Query Source یا Field دیگر فقط در صورت مفید بودن اضافه شود.

## قاعده Presentation

برای Excel / List فارسی از این‌ها استفاده کن:
- `standards/structured-data-presentation-standard.md`
- `skills/structured-data-output/SKILL.md`
- `references/babol-mechanics-excel-golden-template.md`

Structure قابل‌استفاده مجدد است؛ Color و Branding می‌توانند تغییر کنند.

## Defaultهای Diaco

- استفاده سبک به‌صورت پیش‌فرض
- یک Job در هر لحظه
- پرهیز از Depth غیرضروری
- پرهیز از Mass Scraping تکراری
- نصب نکردن نسخه جداگانه Scraper داخل هر App
- اگر این Capability مشترک شد، ترجیحاً یک Local / Server Service قابل‌استفاده مجدد داشته باشد

## Data Quality / Safety

- Scraped Data ممکن است قدیمی یا ناقص باشد
- Contact / Supplier مهم پیش از استفاده عملی Verify شود
- Privacy، Marketing و Platform Ruleهای مرتبط رعایت شوند
- وجود Contact Data به معنی Consent برای Bulk Outreach نیست
- برای کامل شدن Row، Contact Information گمشده ساخته نشود
