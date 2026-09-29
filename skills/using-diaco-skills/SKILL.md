---
name: using-diaco-skills
description: Task را به Standard، Workflow، Platform Profile و Tool / Reference مناسب در Diaco هدایت می‌کند.
---

# Using Diaco Skills

## مسیریابی Skill

- ادامه کار بین Sessionها یا Agentها → `project-context-handoff`
- GitHub Durable Memory → `github-project-memory`
- یکدستی Shared UI → `shared-ui-system`
- خروجی فارسی Excel / List / Table → `structured-data-output`
- UI Creation / Polish / Animation / Prototyping / UI Review → `ui-design-engineering`
- Local Business / Supplier / Lead Discovery → `local-business-data`
- Marketing Workflow تکرارشونده یا خودکار → `automated-marketing-growth`
- تغییر امن در Codebase موجود → `safe-existing-project-change`
- Supabase Web App → `supabase-webapp-guardrails`
- Windows Desktop App → `windows-desktop-standard`
- PR Review → `pull-request-review`
- Security Review مجاز → `security-review`
- Word / Document Automation → `document-r-automation`

## مسیریابی Standard

- Persian Structured Table / Lead List / Spreadsheet Layout → `standards/structured-data-presentation-standard.md`
- General UI → `standards/ui-standard.md`
- Tool Selection → `standards/engineering-toolchain-standard.md`
- Testing → `standards/testing-standard.md`
- Security → `standards/security-review-standard.md`
- Release → `standards/release-standard.md`

## مسیریابی Tool / Reference

- Documentation فعلی Library / API → Context7
- Web Browser Verification → Playwright CLI
- Supabase Operation → official Supabase MCP
- Rapid UI Screen / Flow Prototype قبل از کدنویسی → `lnkiai/m3e-canvas`
- UI Design Engineering / Polish / Motion → Emil Kowalski Skills
- UI Reference تکمیلی → UI Skills
- Local Business Data → `Mahanaicoach/google-maps-scraper-kit`
- Marketing / Growth Execution → `coreyhaines31/marketingskills`
- Authorized Security Automation → Strix

## مسیر UI Prototype

وقتی کاربر قبل از Coding می‌خواهد فرم/صفحه را ببیند یا چند مدل مقایسه کند:

1. Structure تأییدشده Project و Diaco را بخوان.
2. RTL، Right Sidebar، Field Order و Table/Form Hierarchy تأییدشده را حفظ کن.
3. در صورت مناسب بودن، با M3E Canvas Prototype / Screen Flow بساز.
4. کاربر Variant یا Flow را انتخاب/تأیید کند.
5. Prototype را به Prompt / Implementation Brief تبدیل کن.
6. در Stack واقعی پروژه پیاده‌سازی کن.
7. خروجی Production را جداگانه Verify کن.

M3E Canvas مرجع Theme نهایی Diaco نیست.

## ترکیب Marketing

وقتی کاربر Marketing Automation می‌خواهد:
1. `automated-marketing-growth` را Load کن.
2. Product Marketing Context را مشخص کن.
3. در صورت نیاز به Local Business Data از Google Maps Scraper Kit استفاده کن.
4. برای Qualification / Strategy / Content / Outreach Preparation از Marketing Skills استفاده کن.
5. برای خروجی فارسی List / Spreadsheet از `structured-data-output` استفاده کن.
6. ابتدا Pilot کوچک اجرا کن.
7. فقط بعد از Validation قابل‌اندازه‌گیری Automation را Scale کن.

## قواعد مشترک

1. وضعیت فعلی Repository / Data را بررسی کن.
2. فقط Standard، Skill و Tool مرتبط را Load کن.
3. Ruleهای Project-specific بر Default عمومی Diaco اولویت دارند.
4. وقتی ترجیحات قابل‌استفاده مجدد کاربر مهم است، `00-AI-HUB/WORKING-PREFERENCES.md` را بخوان.
5. Missing State را نساز.
6. تغییرات را Scoped و برگشت‌پذیر نگه دار.
7. پیش از اعلام اتمام، Verify کن.
8. State مهم را Persist کن.
9. با تغییر Theme، Structure تأییدشده را حفظ کن.
10. Marketing Automation پیش از قبولی Pilot Scale نشود.
