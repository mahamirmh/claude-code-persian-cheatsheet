# Workflowهای کاربردی با Claude Code

این فایل برای کار واقعی روی پروژه‌هاست؛ یعنی فقط لیست دستور نیست، مسیر استفاده است.

---

## 1. شروع بررسی یک پروژه جدید

```bash
cd path/to/project
claude
```

داخل Claude Code:

```text
/init
```

بعد بگو:

```text
Analyze this codebase and explain the project structure, main entry points, run commands, test commands, risky areas, and what I should read first. Do not edit files yet.
```

هدف: Claude اول پروژه را بفهمد و بی‌دلیل فایل‌ها را تغییر ندهد.

---

## 2. گرفتن پلن قبل از تغییر سنگین

```text
/plan
```

سپس:

```text
I want to add this feature with the smallest safe change. First create a plan. Do not edit files until the plan is clear.
Feature: ...
```

هدف: جلوگیری از تغییرات پراکنده و پرریسک.

---

## 3. دیباگ با کمترین ریسک

```text
/debug
```

پرامپت:

```text
Find the root cause of this bug. First list possible causes, then identify likely files, then propose the safest fix. Do not edit files before explaining.
Bug: ...
```

بعد از اصلاح:

```text
/diff
```

و سپس:

```text
/code-review
```

---

## 4. ریفکتور بدون تغییر رفتار

```text
/plan
```

پرامپت:

```text
Refactor this module without changing behavior. Keep the public API stable. Improve readability, naming, duplication, and error handling. Add or update tests only if needed.
Module: ...
```

بعد:

```text
/diff
/code-review
```

---

## 5. بررسی امنیتی قبل از انتشار

```text
/security-review
```

پرامپت:

```text
Review the current project for security risks: exposed secrets, unsafe input handling, auth problems, dependency risks, insecure defaults, and deployment issues. Report first. Do not edit files.
```

---

## 6. آماده‌سازی برای deploy

پرامپت:

```text
Prepare this project for deployment. Check build config, environment variables, scripts, missing docs, test commands, and common deployment mistakes. Report issues first.
```

سپس:

```text
/doctor
```

---

## 7. بررسی تغییرات قبل از commit

```text
/diff
```

سپس:

```text
Review my current git diff for correctness bugs, security issues, broken edge cases, unnecessary complexity, and missing tests. Do not edit files.
```

---

## 8. وقتی context پر شد

```text
/context
```

اگر مصرف بالا بود:

```text
/compact
```

بعد از compact، ادامه بده:

```text
Continue from the summary. Focus only on the remaining tasks.
```

---

## 9. وقتی Claude مسیر را اشتباه رفت

```text
/rewind
```

بعد دقیق‌تر دستور بده:

```text
Redo this with a smaller scope. Only change the files necessary for the bug. Do not refactor unrelated code.
```

---

## 10. ساخت README برای پروژه

```text
Create a README for this project including installation, environment variables, run commands, test commands, deployment notes, folder structure, and troubleshooting.
```
