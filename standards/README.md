# Registry استانداردهای Diaco

این پوشه شامل Standardهای قابل‌استفاده مجدد در پروژه‌های Diaco است.

## مدل وضعیت

هر Standard یکی از وضعیت‌های زیر را دارد:

- **ACTIVE** — Baseline تأییدشده؛ در صورت مرتبط بودن به‌صورت پیش‌فرض استفاده شود.
- **DRAFT** — ساختار اولیه وجود دارد، اما جزئیات آن هنوز به‌عنوان استاندارد عمومی Diaco تأیید نشده است.
- **PROJECT-REFERENCE** — یک پروژه می‌تواند تا زمان ارتقای قاعده به ACTIVE به‌عنوان مرجع Implementation استفاده شود.
- **DEPRECATED** — فقط برای Migration یا History نگه داشته می‌شود.

## قاعده

Standard گمشده را اختراع نکن.

اگر یک Standard در وضعیت DRAFT است:
1. Implementation یا Reference واقعی را بررسی کن،
2. Pattern تکرارشونده را استخراج کن،
3. اگر قرار است عمومی شود، تأیید بگیر،
4. سپس فقط قاعده تأییدشده را به ACTIVE ارتقا بده.

## Standardهای فعلی

| Standard | وضعیت | کاربرد |
|---|---|---|
| [Project Standard](project-standard.md) | ACTIVE | حداقل ساختار پروژه و تداوم کار |
| [Structured Data Presentation Standard](structured-data-presentation-standard.md) | ACTIVE | RTL فارسی، ترتیب جدول، شماره‌گذاری و تفکیک Structure از Theme |
| [UI Standard](ui-standard.md) | DRAFT | زبان مشترک بصری و تعاملی |
| [Print Standard](print-standard.md) | DRAFT | قواعد قابل‌استفاده مجدد Print / Preview |
| [Backup & Restore Standard](backup-restore-standard.md) | DRAFT | رفتار Backup و Restore |
| [User Management Standard](user-management-standard.md) | DRAFT | الگوهای Users / Roles / Permissions |
| [Windows App Standard](windows-app-standard.md) | ACTIVE | Baseline برنامه‌های Windows Desktop |
| [Testing Standard](testing-standard.md) | ACTIVE | حداقل انضباط Verification |
| [Engineering Toolchain Standard](engineering-toolchain-standard.md) | ACTIVE | سیاست انتخاب Context7، Playwright CLI، Supabase MCP، ابزارهای UI، Business Data و Marketing |
| [Pull Request Review Standard](pull-request-review-standard.md) | ACTIVE | کنترل کیفیت Diff پیش از Merge |
| [Security Review Standard](security-review-standard.md) | ACTIVE | Security Review در محیط مجاز |
| [Release Standard](release-standard.md) | ACTIVE | Versioning، Release، Rollback و Handoff |

## قاعده ارتقا

یک Pattern زمانی کاندید Standard شدن در Diaco است که:
- در بیش از یک پروژه تکرار شده باشد، یا
- کاربر صراحتاً بگوید باید Standard شود، یا
- یک قاعده بنیادی بین‌پروژه‌ای مانند Handoff، Security، Testing، Data Presentation یا Git Discipline باشد.

استثناهای هر پروژه همچنان مجازند و باید در `AGENTS.md` همان پروژه ثبت شوند.
