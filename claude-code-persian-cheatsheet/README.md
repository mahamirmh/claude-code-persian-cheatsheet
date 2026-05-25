# چیت‌شیت فارسی Claude و Claude Code

یک راهنمای فارسی و کاربردی برای کار با **Claude Code**، دستورهای خط فرمان، اسلش‌کامندها، workflowهای روزمره و پرامپت‌های آماده برای تولید محتوا، کدنویسی، سئو، دیباگ و مدیریت پروژه.

> این ریپوزیتوری برای انتشار عمومی آماده شده است. هیچ کلید API، اطلاعات حساب، فایل شخصی یا داده خصوصی داخل آن قرار داده نشده است.

---

## مناسب برای چه کسانی است؟

- برنامه‌نویس‌هایی که می‌خواهند با Claude Code سریع‌تر کار کنند
- تولیدکننده‌های محتوا که از Claude برای سناریو، کپشن، سئو و تحلیل متن استفاده می‌کنند
- تیم‌هایی که می‌خواهند یک مرجع فارسی داخلی برای Claude داشته باشند
- کسانی که می‌خواهند commandها، workflowها و promptهای آماده را یک‌جا داشته باشند

---

## شروع سریع

### 1. اجرای Claude Code

```bash
claude
```

### 2. اجرای یک سؤال سریع بدون ورود به محیط تعاملی

```bash
claude -p "Explain this project structure"
```

### 3. ساخت حافظه پروژه

```text
/init
```

### 4. دیدن دستورهای موجود داخل Claude Code

```text
/help
```

### 5. دیدن مصرف context

```text
/context
```

### 6. خلاصه‌سازی مکالمه طولانی

```text
/compact
```

---

## ساختار ریپوزیتوری

```text
.
├── README.md
├── LICENSE
├── CHANGELOG.md
├── CONTRIBUTING.md
├── CODE_OF_CONDUCT.md
├── SECURITY.md
├── CLAUDE.md
├── docs
│   ├── commands.md
│   ├── workflows.md
│   ├── prompts.md
│   └── push-to-github.md
└── examples
    └── prompts
        ├── coding.md
        ├── content.md
        └── seo.md
```

---

## فایل‌های مهم

| فایل | توضیح |
|---|---|
| [`docs/commands.md`](docs/commands.md) | چیت‌شیت دستورهای Claude Code |
| [`docs/workflows.md`](docs/workflows.md) | مسیرهای کاری کاربردی برای پروژه واقعی |
| [`docs/prompts.md`](docs/prompts.md) | پرامپت‌های عمومی آماده |
| [`examples/prompts`](examples/prompts) | نمونه پرامپت‌های دسته‌بندی‌شده |
| [`docs/push-to-github.md`](docs/push-to-github.md) | راهنمای push کردن این ریپو به GitHub |

---

## دستورهای خیلی پرکاربرد

```text
/help
/init
/memory
/plan
/diff
/code-review
/security-review
/debug
/doctor
/compact
/context
/clear
/resume
/model
/effort
/permissions
/usage
/exit
```

---

## هشدار مهم درباره نسخه‌ها

دستورهای Claude Code ممکن است با نسخه‌های جدید تغییر کنند. برای دیدن لیست دقیق دستورهای فعال در محیط خودت، همیشه داخل Claude Code این دستور را بزن:

```text
/help
```

و برای راهنمای CLI:

```bash
claude --help
```

---

## منابع رسمی

- [Claude Code CLI reference](https://docs.anthropic.com/en/docs/claude-code/cli-reference)
- [Claude Code overview](https://docs.anthropic.com/en/docs/agents-and-tools/claude-code/overview)
- [Claude Code quickstart](https://docs.anthropic.com/en/docs/claude-code/quickstart)
- [Claude Code settings](https://docs.anthropic.com/en/docs/claude-code/settings)
- [Claude Code memory](https://docs.anthropic.com/en/docs/claude-code/memory)
- [Claude Code skills](https://docs.anthropic.com/en/docs/claude-code/skills)

---

## لایسنس

این پروژه تحت لایسنس MIT منتشر شده است. برای استفاده، fork، ویرایش و انتشار آزاد است.
