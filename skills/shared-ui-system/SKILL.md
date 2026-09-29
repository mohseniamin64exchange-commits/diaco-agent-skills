---
name: shared-ui-system
description: زبان UI قابل‌استفاده مجدد را در برنامه‌های Diaco حفظ می‌کند. برای طراحی App جدید، اضافه کردن Screen یا Component، یا استفاده مجدد از Navigation، Form، Table، Dialog، Layout، Typography، Color و Interaction Pattern استفاده شود.
---

# Shared UI System

## هدف

برنامه جدید Diaco باید از Structure اطلاعاتی و تعاملی تأییدشده استفاده مجدد کند، نه اینکه در هر Chat یک Interface کاملاً جدید اختراع شود.

## تفکیک اصلی

**Structure و Theme دو لایه جدا هستند.**

وقتی Structure تأیید شده، این موارد حفظ شوند:
- ترتیب اطلاعات
- محل Navigation
- Hierarchy فیلدها
- سازمان Table / Form
- رفتار RTL / LTR
- Interaction Flow

Theme می‌تواند تغییر کند:
- رنگ
- آیکون
- Branding
- Decoration
- Shadow / Radius در صورت Project-specific بودن

صرف متفاوت بودن Theme دلیل تغییر Structure نیست.

## قبل از ساخت UI

1. Diaco UI Standard را بخوان.
2. برای Screenهای فارسی داده‌محور، `standards/structured-data-presentation-standard.md` را بخوان.
3. Reference یا Implementation تأییدشده پروژه را پیدا کن.
4. Screen / Component واقعی و نماینده را بررسی کن.
5. Tokenها و Structureهای قابل‌استفاده مجدد را مشخص کن.
6. اگر Task شامل Polish، Animation، Prototyping، UI-library choice یا Mobile-Web Behavior است، `ui-design-engineering` را Load کن.

## Baseline فارسی

برای Interfaceهای فارسی:
- RTL حالت پیش‌فرض است،
- Sidebar / Navigation اصلی سمت راست ترجیح دارد مگر Reference پروژه متفاوت باشد،
- Form و Tableهای تکرارشونده ترتیب اطلاعات یکسان داشته باشند،
- Structured Table Valueها به‌صورت پیش‌فرض Center باشند.

## Reference اولویت‌دار Design Engineering

`emilkowalski/skills`، **Priority UI / Design Engineering Reference** در Diaco است.

به‌ویژه برای:
- UI Polish
- تصمیم و Review انیمیشن
- Multi-variant Prototype در محیط جدا
- انتخاب Component / Library
- جزئیات Mobile-Web Interaction
- Motion در React Native / Expo

اما مرجع هویت بصری Diaco یا Structure تأییدشده نیست.

## Reference تکمیلی UI

`adamtossell/ui-skills` نیز می‌تواند برای Workflowهای طراحی و Frontend Practice استفاده شود.

## اولویت

1. UI / Reference تأییدشده پروژه
2. Ruleهای ACTIVE مربوط به Structure / UI در Diaco
3. Emil Kowalski Skills
4. UI Skills و سایر Referenceهای بیرونی

## قاعده Prototype

وقتی جهت بصری مشخص نیست:
- Exploration خارج از Production Code انجام شود،
- Variantها واقعاً متفاوت باشند،
- Structure تأییدشده حفظ شود مگر اینکه کاربر صراحتاً مقایسه Structure بخواهد،
- انتخاب نهایی با کاربر باشد،
- فقط Variant انتخاب‌شده وارد Production شود.

## Verification

- [ ] Patternهای Shared موجود بررسی شدند.
- [ ] Structure تأییدشده حفظ شد.
- [ ] قواعد RTL / Navigation / Alignment فارسی در صورت مرتبط بودن اعمال شدند.
- [ ] Value یا Component جدید فقط در صورت نیاز اضافه شد.
- [ ] Loading / Error / Empty State مدیریت شدند.
- [ ] Responsive و Keyboard Behavior در صورت نیاز بررسی شدند.
- [ ] Reference خارجی قواعد تأییدشده Diaco / Project را Override نکرد.
- [ ] تغییر Theme باعث تغییر Information Architecture نشد.
