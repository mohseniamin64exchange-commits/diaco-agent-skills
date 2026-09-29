# مرجع Golden Template اکسل مکانیکی‌های بابل

## فایل مرجع

Workbook مورد تأیید کاربر:

`babol_mechanics_clean_rtl.xlsx`

SHA-256 مشاهده‌شده:

`8d35f73dc9fc12f8f961c68c5a1a475a68041456b77a09e3c2dfe5cff46c6f3a`

این فایل Reference ساختار قابل‌استفاده مجددی را که از Workbook تأییدشده استخراج شده ثبت می‌کند. خود Workbook یک Artifact مرجعِ ارائه‌شده توسط کاربر است.

## ساختار مشاهده‌شده Workbook

Worksheet:
- `تعمیرگاه‌های بابل`

Used Range:
- `A1:I44`

Direction و View:
- RTL فعال
- Gridline مخفی
- ردیف‌های 1 تا 4 Freeze؛ Data از ردیف 5 شروع می‌شود

Presentation ادغام‌شده:
- `A1:I1` — Title
- `A2:I2` — Subtitle
- ردیف 3 — Separator بصری
- ردیف 4 — Headerهای Table

Table:
- Range برابر `A4:I44`
- Filtering فعال
- Row Striping فعال
- Table Style فعلی: `TableStyleMedium2`

## ترتیب تأییدشده ستون‌ها

1. `ردیف`
2. `نام کسب‌وکار`
3. `نوع تعمیرگاه`
4. `دسته‌بندی`
5. `آدرس خلاصه`
6. `شماره تلفن`
7. `وب‌سایت`
8. `امتیاز Google`
9. `تعداد Review`

Pattern معنایی مهم‌تر از wording اختصاصی Subject است:
- شماره ردیف
- نام اصلی Entity
- Classification کاربردی برای انسان
- Category اصلی منبع
- Location خلاصه
- Phone
- Website
- Rating
- Review Count

## Alignment و Typography مشاهده‌شده

- Title: Center، Bold، Arial 15
- Subtitle: Center، Italic، Arial 10
- Header: Center، Bold، Arial 10
- Body: Center، Arial 10
- Wrap Text برای Header فعال
- Rating Format: یک رقم اعشار
- شماره‌گذاری ردیف: پیوسته از 1

## اندازه‌های مشاهده‌شده

Column Width:
- A: 7
- B: 28
- C: 22
- D: 26
- E: 48
- F: 20
- G: 32
- H: 14
- I: 14

Row Heightهای مهم:
- ردیف 1: 30
- ردیف 2: 21.95
- ردیف 4: 27.95

## ظاهر فعلی Reference

Accent فعلی Header / Tab بر پایه آبی تیره `#1F4E78` با متن سفید است.

این رنگ **فقط متعلق به Reference فعلی است و رنگ عمومی Diaco محسوب نمی‌شود**.

کاربر به‌صراحت این موارد را تأیید کرده است:
- Structure
- رفتار RTL
- Center بودن Data
- ترتیب
- شماره‌گذاری
- نظم Table

مواردی که می‌توانند در هر پروژه تغییر کنند:
- رنگ‌ها
- آیکون‌ها
- Branding
- Decoration

## قاعده استفاده مجدد

وقتی کاربر می‌گوید:
- «خروجی استاندارد من»
- «طبق ساختار اکسل من»
- «مثل فایل قبلی مرتبش کن»
- یا عبارت معادل برای یک Persian Structured List

قواعد Structure موجود در `standards/structured-data-presentation-standard.md` را دوباره استفاده کن و Theme را با پروژه فعلی تطبیق بده.
