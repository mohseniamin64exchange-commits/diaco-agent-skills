# Diaco Agent Skills

مجموعه Workflowها، Standardهای مشترک، ابزارهای مهندسی، Referenceهای Design Engineering، UI Prototyping، Business Data Tooling، Structured Data Presentation و Marketing Workflowهای قابل‌تکرار برای پروژه‌های مبتنی بر AI.

**نسخه فعلی:** 0.8.0

## قابلیت‌های مهم

- تداوم پروژه و GitHub-backed Memory
- Platform Profileهای Windows و Supabase
- UI Design Engineering
- **Rapid UI Prototyping / Screen Flow با M3E Canvas**
- **نمایش Structured Data فارسیِ تأییدشده**
- Local Business و Supplier Discovery
- Marketing و Growth Workflowهای قابل‌تکرار
- Testing، Security Review و PR Review

## UI Prototyping Workflow

Diaco اکنون `lnkiai/m3e-canvas` را به‌عنوان **Priority UI Prototyping / Screen-Flow Tool** ثبت می‌کند.

Flow ترجیحی:

```text
Approved Diaco / Project structure
→ M3E Canvas prototype
→ User review / selection
→ Prompt or implementation brief
→ Coding Agent implementation
→ Real browser/device/platform verification
```

M3E Canvas برای سریع دیدن فرم‌ها، Screenها و Navigation قبل از Coding است؛ مرجع اجباری Theme نهایی Diaco نیست.

Reference:
- `references/m3e-canvas.md`
- `skills/ui-design-engineering/SKILL.md`

## مدل تأییدشده Presentation بین پروژه‌ها

Diaco این دو لایه را به‌صراحت جدا می‌کند:

**Structure**
- ترتیب اطلاعات
- Hierarchy
- رفتار RTL / LTR
- Alignment Logic
- Row Numbering
- محل Navigation
- ساختار Table / Form

**Theme**
- رنگ‌ها
- آیکون‌ها
- Branding
- Decorative Styling

Defaultهای تأییدشده برای خروجی فارسی:
- RTL برای Structured Output فارسی
- Center بودن Structured Table Data به‌صورت پیش‌فرض
- Numbering پیوسته از 1 برای Result Listها
- Sidebar / Navigation اصلی سمت راست به‌عنوان Baseline ترجیحی برنامه فارسی، مگر اینکه Reference پروژه متفاوت باشد

فایل‌های مرجع:
- `standards/structured-data-presentation-standard.md`
- `skills/structured-data-output/SKILL.md`
- `references/babol-mechanics-excel-golden-template.md`

## خروجی Business / Lead List

Baseline تأییدشده از Workbook مورد تأیید کاربر با نام `babol_mechanics_clean_rtl.xlsx` استخراج شده است.

ترتیب ترجیحی:

`ردیف → نام کسب‌وکار → نوع کاربردی → دسته‌بندی منبع → آدرس خلاصه → شماره تلفن → وب‌سایت → امتیاز → تعداد Review`

Theme آبی فعلی Workbook فقط Theme همان Reference است و رنگ عمومی Diaco محسوب نمی‌شود.

## Marketing Workflow

Diaco ترکیب زیر را به‌عنوان یک قابلیت مهم و قابل‌استفاده مجدد در نظر می‌گیرد:

- `Mahanaicoach/google-maps-scraper-kit`
- `coreyhaines31/marketingskills`

Flow معمول:

```text
Product context
→ Local business discovery
→ Clean / deduplicate
→ Qualify / categorize
→ Structured Persian output
→ Marketing preparation
→ Human review
→ Measure
→ Repeat only after pilot success
```

Skillهای مرتبط:
- `skills/local-business-data/SKILL.md`
- `skills/structured-data-output/SKILL.md`
- `skills/automated-marketing-growth/SKILL.md`

## اصول اصلی

1. GitHub حافظه پایدار و Source of Truth است.
2. اطلاعات مهم پروژه نباید فقط در Chat History بمانند.
3. پیش از کار بین‌پروژه‌ای مهم، ترجیحات کاری تأییدشده را بخوان.
4. پیش از تغییر پروژه موجود، وضعیت واقعی آن را بررسی کن.
5. Scope و رفتار سالم موجود را حفظ کن.
6. Structure تأییدشده را حتی با تغییر Theme حفظ کن.
7. برای UI نامطمئن، Prototype قبل از Production Coding ترجیح دارد.
8. تغییرات را با Evidence Verify کن.
9. Specialized Tool فقط در صورت مرتبط بودن استفاده شود.
10. Secret در Git ذخیره نشود.
11. Workflow قبل از Pilot موفق Scale نشود.
12. Data واقعی Business / Project / Customer از Generic Assumption مدل معتبرتر است.
