# Diaco UI Standard

**Status:** DRAFT  
**Version:** 0.3

## هدف

ایجاد یک زبان بصری و تعاملی قابل‌استفاده مجدد برای Diaco تا هر برنامه جدید مجبور نباشد از صفر Conventionهای UI را اختراع کند.

## قواعد تأییدشده فعلی

- پیش از ساخت Pattern جدید، UI یا Reference تأییدشده موجود را بررسی کن.
- پیش از ایجاد Variant جدید، Tokenها و Componentهای مشترک را دوباره استفاده کن.
- Navigation، Form، Table، Dialog، Notification و Stateها را تا حد ممکن یکدست نگه دار.
- Branding اختصاصی پروژه می‌تواند عمداً Defaultهای مشترک را Override کند.
- Accessibility، Keyboard Behavior، Focus، Loading، Empty، Validation و Error State بخشی از کیفیت UI هستند.
- رنگ، ابعاد، Typography یا Layout تأییدنشده را حدس نزن.
- وقتی جهت بصری واقعاً مشخص نیست، Exploration در Prototype جدا انجام شود؛ نه با بازنویسی مداوم Production UI.
- Variantهای واقعی باید در Layout، Density، Interaction Model، Hierarchy یا Motion فرق داشته باشند؛ نه فقط رنگ.
- انتخاب جهت بصری با کاربر است. Agent می‌تواند Trade-offها را توضیح دهد، اما نباید یک Style عمومی Diaco را بدون تأیید انتخاب کند.
- Motion باید کاربردی باشد و Workflowهای پرتکرار را کند نکند.
- قبل از افزودن UI Library جدید، Dependencyهای موجود پروژه را بررسی کن.
- **Structure پایدارتر از Theme است:** ترتیب اطلاعات، Hierarchy، Direction و Workflow تأییدشده را حتی با تغییر رنگ، آیکون یا Branding حفظ کن.
- برای Interfaceهای فارسیِ داده‌محور، RTL حالت تأییدشده پیش‌فرض است.
- در Tableهای فارسی، مقادیر ساختاریافته به‌صورت پیش‌فرض Center هستند مگر اینکه ماهیت یک Field تراز دیگری را بهتر کند.
- در Shell برنامه‌های فارسی، Sidebar / Navigation اصلی سمت راست Baseline ترجیحی است، مگر اینکه Reference تأییدشده پروژه عمداً متفاوت باشد.
- رفتار Structured Data تأییدشده در `structured-data-presentation-standard.md` تعریف شده است.

## سلسله‌مراتب Referenceهای UI

برای کارهای UI / Design این ترتیب را رعایت کن:

1. UI / Reference تأییدشده خود پروژه
2. قواعد ACTIVE در Diaco
3. `emilkowalski/skills` — **Priority UI / Design Engineering Reference**
4. `adamtossell/ui-skills` — Reference تکمیلی Workflowهای UI
5. سایر Referenceهای بیرونی

Repositoryهای بیرونی راهنمای تخصصی هستند؛ هویت بصری Diaco را تعیین نمی‌کنند.

مرتبط:
- `references/emil-kowalski-skills.md`
- `skills/ui-design-engineering/SKILL.md`
- `standards/structured-data-presentation-standard.md`

## موارد استفاده مهم Emil Kowalski Skills

- UI polish و جزئیات Interaction
- تصمیم‌گیری و Implementation انیمیشن
- Review انیمیشن‌های موجود
- Prototype چند Variant در محیط جدا
- انتخاب UI / Component Library
- جزئیات Mobile-Web Interaction
- Motion در React Native / Expo در صورت مرتبط بودن

Constantهای دقیق Animation، رنگ، Typography، Layout یا انتخاب Library به‌صورت خودکار Default عمومی Diaco نمی‌شوند.

## مواردی که هنوز از Referenceهای واقعی باید تعریف شوند

موارد زیر عمداً هنوز ثابت نشده‌اند:
- رنگ‌های Primary / Secondary
- Font Family و Scale اندازه‌ها
- Spacing Scale
- Border Radius / Shadow
- ابعاد دقیق Sidebar / Header
- ظاهر Form Field
- سلسله‌مراتب Buttonها
- Density و Actionهای Table خارج از قواعد Structured Data تأییدشده
- ظاهر Modal / Dialog
- ظاهر Toast / Notification
- استثناهای ریز RTL و متن‌های Mixed-language
- Controlهای خاص Windows و High-DPI
- Motion Token / Duration / Easing رسمی Diaco

## Workflow استخراج Reference

وقتی کاربر یک Screen یا بخشی از پروژه را به‌عنوان Reference معرفی می‌کند:

1. Implementation / Screen واقعی را بررسی کن،
2. انتخاب‌های دقیق و قابل‌استفاده مجدد را ثبت کن،
3. Content اختصاصی محصول را از Design Rule عمومی جدا کن،
4. **Structure** را از **Theme** جدا کن،
5. از Referenceهای تخصصی برای بهتر شدن Craft استفاده کن بدون تغییر هویت تأییدشده،
6. فقط قواعد تأییدشده قابل‌استفاده مجدد را اینجا اضافه کن،
7. Visual Ruleها را فقط بعد از تأیید ACTIVE کن.

تا آن زمان، هیچ Theme مشخصی را Standard عمومی Diaco اعلام نکن.
