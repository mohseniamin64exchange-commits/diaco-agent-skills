---
name: automated-marketing-growth
description: Workflowهای تکرارشونده Marketing را با ترکیب Local Business Discovery، Product Marketing Context، Prospect Qualification، Messaging، Structured Output و Measurement می‌سازد و اعتبارسنجی می‌کند.
---

# Automated Marketing & Growth

## هدف

ابزارهای Marketing در Diaco باید به یک Workflow قابل‌اندازه‌گیری تبدیل شوند، نه صرفاً Content Generator.

## اجزای اصلی

1. `Mahanaicoach/google-maps-scraper-kit` — Business Discovery
2. `coreyhaines31/marketingskills` — Marketing Strategy و Execution Guidance
3. Data واقعی Project / Customer / Product — Source of Truth
4. `structured-data-output` — Presentation تأییدشده برای List / Spreadsheet فارسی
5. CRM / Spreadsheet / Database — State و Deduplication
6. Scheduler / Jarvis / Agent در صورت نیاز — Orchestration
7. Human Approval برای Outbound Action مگر اینکه Automation Policy از قبل تأیید شده باشد

## Workflow پیش‌فرض

### Phase 1 — Product Context

Product Marketing Context را بساز یا به‌روزرسانی کن:
- چه چیزی می‌فروشیم
- Target Customer
- Geography
- Value Proposition
- Ideal Customer Profile
- Disqualifier
- Proof / Constraint

### Phase 2 — Discovery

وقتی Local Business Discovery لازم است، Google Maps Scraper تأییدشده را با Batch کوچک و هدفمند اجرا کن.

### Phase 3 — Clean + Qualify

- Deduplicate
- حذف Mismatch واضح
- Verify کردن Fieldهای مهم
- ساخت Category قابل‌فهم برای کاربر
- Score / Segment Lead بر اساس Criteria صریح
- نگه‌داشتن Reason برای Include / Exclude

### Phase 4 — Structured Delivery

برای List / Spreadsheet فارسی:
- `structured-data-output` را استفاده کن
- Field Order تأییدشده را حفظ کن
- RTL استفاده کن
- Row Number را پیوسته بساز
- Structured Data را به‌صورت پیش‌فرض Center کن
- Theme را بر اساس پروژه قابل‌تغییر نگه دار

### Phase 5 — Marketing Output

Marketing Skill مناسب را انتخاب کن:
- prospecting
- competitor profiling
- content
- cold email
- sales enablement
- pricing
- SEO
- ads
- Skill مرتبط دیگر

### Phase 6 — Human Checkpoint

قبل از Contact واقعی، Bulk Messaging، Ad Spend یا Publication:
- Audience / Output پیشنهادی را نشان بده
- مگر اینکه Policy از قبل تأیید شده باشد، Approval بگیر

### Phase 7 — Measure

Track کن:
- تعداد Result اولیه
- Duplicate Rate
- Valid Contact Rate
- Qualified Lead Rate
- Manual Review Acceptance Rate
- Response / Conversion Metric در صورت وجود
- Cost / Time به ازای Result مفید

## Validation Protocol

ابتدا یک **Pilot کوچک** اجرا کن، نه Full Automation.

تست اولیه پیشنهادی:
- یک شهر / محدوده
- یک Business Category
- 20 تا 50 Record
- بدون Automated Outreach

Sample معناداری را دستی Review کن و Pipeline را با واقعیت مقایسه کن.

## Pass Criteria

Automation فقط وقتی Scale شود که این موارد را نشان دهد:
- Stable Data Collection
- Cleaning / Deduplication قابل‌تکرار
- Classification / Qualification قابل‌قبول
- Structured Output مفید
- Marketing Output مفید
- Logging و Recovery روشن

## مرزهای Quality / Safety

- در Pilot اولیه Outreach خودکار ارسال نکن.
- Personalization ساختگی نساز.
- Scraped Contact Data را Consent برای Marketing در نظر نگیر.
- در صورت فعال شدن Outreach، Opt-out و Compliance Requirementها حفظ شوند.
- Workflow خراب را Scale نکن؛ اول Pilot را اصلاح کن.
