# راهنمای push کردن این ریپوزیتوری به GitHub

## روش 1: ساخت repo جدید با GitHub CLI

اگر GitHub CLI داری:

```bash
cd claude-code-persian-cheatsheet

git init
git add .
git commit -m "Initial commit: Persian Claude Code cheatsheet"

gh repo create claude-code-persian-cheatsheet --public --source=. --remote=origin --push
```

---

## روش 2: ساخت repo از سایت GitHub

1. وارد GitHub شو.
2. New repository را بزن.
3. نام repo را بگذار:

```text
claude-code-persian-cheatsheet
```

4. حالت Public را انتخاب کن.
5. README، License و `.gitignore` نساز؛ این فایل‌ها داخل پروژه آماده‌اند.
6. بعد در ترمینال:

```bash
cd claude-code-persian-cheatsheet

git init
git add .
git commit -m "Initial commit: Persian Claude Code cheatsheet"

git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/claude-code-persian-cheatsheet.git
git push -u origin main
```

`YOUR_USERNAME` را با نام کاربری GitHub خودت جایگزین کن.

---

## روش 3: آپلود مستقیم ZIP در GitHub

1. فایل ZIP را extract کن.
2. در GitHub یک repo جدید بساز.
3. گزینه Upload files را بزن.
4. همه فایل‌ها را drag & drop کن.
5. Commit changes را بزن.

---

## بررسی قبل از public کردن

قبل از push عمومی:

```bash
grep -R "API_KEY\|SECRET\|TOKEN\|PASSWORD" .
```

اگر خروجی مهمی دیدی، قبل از public کردن حذفش کن.
