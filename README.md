# Diaco Agent Skills

مجموعه Workflowها، Standardهای مشترک، ابزارهای مهندسی، Referenceهای Design Engineering، Business Data Tooling، Structured Data Presentation و Marketing Workflowهای قابل‌تکرار برای پروژه‌های مبتنی بر AI.

**نسخه فعلی:** 0.7.0

## قابلیت‌های مهم

- تداوم پروژه و GitHub-backed Memory
- Platform Profileهای Windows و Supabase
- UI Design Engineering
- **نمایش Structured Data فارسیِ تأییدشده**
- Local Business و Supplier Discovery
- Marketing و Growth Workflowهای قابل‌تکرار
- Testing، Security Review و PR Review

## مدل تأییدشده Presentation بین پروژه‌ها

Diaco اکنون این دو لایه را به‌صراحت جدا می‌کند:

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
7. تغییرات را با Evidence Verify کن.
8. Specialized Tool فقط در صورت مرتبط بودن استفاده شود.
9. Secret در Git ذخیره نشود.
10. Workflow قبل از Pilot موفق Scale نشود.
11. Data واقعی Business / Project / Customer از Generic Assumption مدل معتبرتر است.
