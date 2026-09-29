# قواعد عملیاتی Agentهای Diaco

## Source of Truth

در صورت تعارض اطلاعات در کار پروژه، این ترتیب اولویت دارد:

1. فایل‌های فعلی Repository و وضعیت Verifyشده Git
2. Rule / Specification اختصاصی پروژه و Reference تأییدشده
3. آخرین Handoff پروژه
4. Standard و Skill تأییدشده Diaco
5. Global Ruleهای HUB و Working Preferenceهای تأییدشده
6. Conversation History

Chat قدیمی را به‌عنوان نمایش قطعی وضعیت فعلی Repository فرض نکن.

## پیش از تغییر پروژه موجود

- Repository هدف را بررسی کن
- README / AGENTS / Rule / Handoff را بخوان
- File و Test مرتبط را بررسی کن
- قبل از ساخت Pattern جدید، Pattern موجود را پیدا کن
- رفتار سالم نامرتبط را حفظ کن
- وقتی Preference بین‌پروژه‌ای مهم است، `00-AI-HUB/WORKING-PREFERENCES.md` را بخوان

## لایه Standard

پیش از Implementation یک Feature قابل‌استفاده مجدد، `standards/README.md` و Standard مرتبط را بخوان.

نمونه:
- ساختار پروژه / Onboarding → `standards/project-standard.md`
- Structured Data / Persian Table / Lead List → `standards/structured-data-presentation-standard.md`
- UI / Layout / Component → `standards/ui-standard.md`
- Printing → `standards/print-standard.md`
- Backup / Restore → `standards/backup-restore-standard.md`
- User / Role / Permission → `standards/user-management-standard.md`
- Windows Application Behavior → `standards/windows-app-standard.md`
- Testing / Verification → `standards/testing-standard.md`
- Engineering Tool → `standards/engineering-toolchain-standard.md`
- Pull Request Review → `standards/pull-request-review-standard.md`
- Security Review → `standards/security-review-standard.md`
- Release / Version / Rollback → `standards/release-standard.md`

### قاعده وضعیت Standard

- **ACTIVE** یعنی در صورت مرتبط بودن Default قابل‌استفاده است.
- **DRAFT** یعنی Missing Detail را نساز؛ از Reference واقعی استفاده کن و فقط Rule تأییدشده را Promote کن.
- Exception پروژه باید در `AGENTS.md` همان پروژه ثبت شود.

## رفتار Presentation تأییدشده

در صورت مرتبط بودن:

- Structure اطلاعاتی تأییدشده را حتی با تغییر Theme حفظ کن.
- Structured Data فارسی به‌صورت پیش‌فرض RTL است.
- Structured Persian Table Valueها به‌صورت پیش‌فرض Center هستند.
- Result Listهای شماره‌دار از 1 شروع و پیوسته ادامه می‌یابند مگر Filter Semantics عمداً چیز دیگری بخواهد.
- Shell فارسی ترجیحاً Navigation اصلی سمت راست دارد مگر Reference پروژه خلاف آن را تأیید کرده باشد.
- Color / Icon / Branding می‌توانند تغییر کنند بدون اینکه Information Hierarchy تغییر کند.

استفاده کن:
- `standards/structured-data-presentation-standard.md`
- `skills/structured-data-output/SKILL.md`

## انتخاب Engineering Tool و Reference

Specialized Tool فقط وقتی استفاده شود که Task را بهتر می‌کند؛ همه ابزارها را همه‌جا نصب نکن.

- External Library / API → Context7 در صورت موجود بودن
- Web UI / Browser Verification → Playwright CLI
- Supabase Project → official Supabase MCP با Access مجاز
- UI Polish / Animation / Prototype / UI Review / Mobile-Web / Library Choice → `ui-design-engineering` و `emilkowalski/skills`
- UI Reference تکمیلی → UI Skills
- Security Review مجاز → Diaco Security Workflow و Strix در صورت مفید بودن
- تغییر مهم قبل از Merge / Release → Diaco Pull Request Review Workflow

UI تأییدشده پروژه و Standardهای Diaco همیشه بر External Reference اولویت دارند.

## هنگام Implementation

- Scope را محدود نگه دار
- Step کوچک و برگشت‌پذیر را ترجیح بده
- Architecture را بی‌صدا جایگزین نکن
- Code را فقط به‌خاطر ظاهراً unused بودن حذف نکن
- Dependency بدون دلیل اضافه نکن
- Credential / Secret Commit نکن
- DRAFT Standard را بدون Evidence / Approval عمومی نکن
- Taste یک External UI Reference را به Rule عمومی Diaco تبدیل نکن
- صرفاً برای تغییر Theme، Structure تأییدشده را تغییر نده

## قواعد Platform-aware

Diaco یک Core مشترک و Platform Profileهای جدا دارد.

پیش از Implementation، Platform واقعی پروژه را از Repository تشخیص بده و فقط Skill مربوط را اعمال کن.

نمونه:
- Windows Desktop → `skills/windows-desktop-standard/SKILL.md`
- Supabase / Web → `skills/supabase-webapp-guardrails/SKILL.md`

## Verification

صرف نوشتن Code به معنی تکمیل Task نیست.

در صورت مرتبط بودن Verify کن:
- build
- tests
- type checking
- linting
- runtime behavior
- user flow تحت تأثیر
- browser flow با Playwright CLI
- UI interaction / polish روی Platform واقعی
- ordering / RTL / alignment در Structured Data
- print / backup / restore در صورت تغییر
- security impact در Change حساس

در صورت Failure، آن را ثبت کن و Success اعلام نکن.

## Cross-session Persistence

اگر کار احتمالاً در Session یا Agent دیگری ادامه دارد:
- Handoff پروژه را Update کن
- Branch / Commit را در صورت مفید بودن ثبت کن
- Change انجام‌شده را ثبت کن
- Verification را ثبت کن
- مشکل حل‌نشده را ثبت کن
- Next Action را ثبت کن
- Do-not-change Constraint مهم را ثبت کن

## Repositoryهای خارجی

هنگام استفاده از Third-party Work:
- Attribution و License را حفظ کن
- Upstream اصلی را ثبت کن
- Upstream و نسخه سفارشی Diaco را جدا نگه دار
- Third-party Work را به‌عنوان کار تولیدشده توسط Diaco جا نزن

## قاعده استاندارد پذیرش پروژه

هر Application که تحت Diaco مدیریت می‌شود باید حداقل شامل این دو فایل باشد:

- `AGENTS.md`
- `HANDOFF.md`

پروژه جدید باید از این Templateها شروع کند:
- `templates/PROJECT-AGENTS.md`
- `templates/PROJECT-HANDOFF.md`

پروژه موجود می‌تواند بدون Restructure کردن App این Standard را بپذیرد.

ترتیب استاندارد شروع Agent:

1. `00-AI-HUB/AGENT-START-HERE.md`
2. `00-AI-HUB/WORKING-PREFERENCES.md`
3. `diaco-agent-skills/AGENTS.md`
4. Standardهای مرتبط Diaco
5. Skillهای مرتبط و Platform Profile درست
6. `AGENTS.md` اختصاصی پروژه
7. `HANDOFF.md` پروژه
8. File / Test / Config / Git State واقعی پروژه

Rule اختصاصی پروژه در صورت تعریف عمدی بر Default عمومی Diaco اولویت دارد.
