# 🚀 alfimeDev — راهنمای اجرای پروفایل گیت‌هاب (فارسی)

> راهنمای کامل برای اینکه این پروفایل فوق‌فاخر را در کمتر از ۵ دقیقه **اجرا** (زنده) کنی.

---

## ✅ پیش‌نیازها
- یک حساب **GitHub**.
- Git نصب باشد (اگر می‌خواهی با ترمینال کار کنی) — [دانلود Git](https://git-scm.com/downloads).
- فایل `alfimedev-profile.zip` که دریافت کردی (یا فایل‌های تکی).

> 💡 اگر فقط می‌خواهی ببینی چه شکلی می‌شود و هنوز آماده انتشار نیستی، بخش **«پیش‌نمایش محلی»** را ببین.

---

## 🖼️ روش ۰ — پیش‌نمایش محلی (بدون انتشار)
1. فایل `README.md` را در **VS Code** باز کن.
2. کلیدهای `Ctrl` + `Shift` + `V` را بزن (یا `Cmd + Shift + V` در مک) تا پیش‌نمایش Markdown را ببینی.
3. برای دیدن دقیق‌تر (همان ظاهر گیت‌هاب):
   - افزونه **Markdown Preview Enhanced** یا **Markdown Preview Github Styling** را نصب کن.
4. نکته: تصاویر `./assets/...` فقط وقتی نمایش داده می‌شوند که فایل‌ها داخل پوشه `assets` کنار `README.md` باشند.

> ⚠️ بخش‌هایی مثل «آمار گیت‌هاب»، «مار🐍»، «نمودار ۳بعدی🧊» فقط **بعد از انتشار** و اجرای ورک‌فلوها نمایش داده می‌شوند، چون به حساب واقعی گیت‌هاب تو وابسته‌اند.

---

## 🧭 روش ۱ — انتشار با مرورگر (ساده‌ترین، بدون ترمینال)

### گام ۱: ساخت مخزن پروفایل
1. به [github.com/new](https://github.com/new) برو.
2. نام مخزن را **دقیقاً** برابر نام کاربری‌ات بگذار (مثلاً `alfimedev`).
3. نوع را **Public** انتخاب کن. (اجباری!)
4. تیک «Add a README file» را **نزن** (چون خودمان داریم).
5. **Create repository**.

> 🔴 مهم‌ترین شرط: نام مخزن باید = نام کاربری، و Public باشد. فقط این‌طور روی صفحه پروفایل ظاهر می‌شود.

### گام ۲: آپلود فایل‌ها
1. داخل مخزن، روی **Add file → Upload files** بزن.
2. محتوای پوشه `alfimedev-profile` را بکش و رها کن (باید ساختار زیر حفظ شود):

```
alfimedev/
├── README.md
├── assets/
│   ├── banner.jpg
│   ├── logo.jpg
│   └── divider.jpg
└── .github/
    └── workflows/
        ├── snake.yml
        ├── 3d-contrib.yml
        ├── metrics.yml
        └── blog-post-workflow.yml
```

3. پایین صفحه **Commit changes** را بزن.

> ⚠️ اگر پوشه `.github` را با درگ‌ودراپ نمی‌بینی: در آپلود، با تایپ مسیر ``.github/workflows/`` می‌توانی پوشه بسازی، یا از روش ترمینال (روش ۲) استفاده کن.

### گام ۳: فعال‌سازی دسترسی Actions
`Settings → Actions → General → Workflow permissions` را باز کن و انتخاب کن:

```
✅ Read and write permissions
```

سپس **Save** بزن.
> این مرحله برای اجرای انیمیشن مار، نمودار سه‌بعدی و لوحه‌ی متریک **الزامی** است.

### گام ۴: اجرای دستی ورک‌فلوها (اولین بار)
به تب **Actions** برو و هر کدام را انتخاب کن و **Run workflow** بزن:

1. `Generate Snake Animation` 🐍
2. `Generate 3D Contribution Graph` 🧊
3. `Generate GitHub Metrics` 📊

نتیجه:
| خروجی | محل | بخش مربوطه در README |
|---|---|---|
| مار | برنچ جدید `output` | «Contribution Grid, Devoured» |
| نمودار ۳بعدی | پوشه `profile-3d-contrib/` در `main` | «3D Contribution City» |
| متریک‌ها | فایل `github-metrics.svg` در `main` | بخش بازشدنی «FULL metrics dashboard» |

> ⏱️ بعد از اولین اجرا، این‌ها خودکار اجرا می‌شوند (هر ۱۲ ساعت / روزانه).

### گام ۵: تحویل نهایی
- برو به پروفایلت: `github.com/آیدی‌تو` → باید ظاهر شود. 🎉
- در پروفایل، مخزن را **Pin** کن تا در بالای صفحه بماند.

---

## ⌨️ روش ۲ — انتشار با ترمینال (Git)

```bash
# ۱) از حالت زیپ خارج کن
unzip alfimedev-profile.zip
cd alfimedev-profile

# ۲) مخزن git بساز
git init
git add .
git commit -m "feat: legendary GitHub profile by Alfime ✦"
git branch -M main

# ۳) به مخزن گیت‌هاب وصل شو (alfimedev را با آیدی خودت عوض کن)
git remote add origin https://github.com/alfimedev/alfimedev.git

# ۴) آپلود
git push -u origin main
```

سپس همان **گام‌های ۳ تا ۵** بالا را انجام بده (فعال‌سازی Actions و اجرای ورک‌فلوها).

مرتب کردن پوشه مخفی `.github` اگر در درگ‌ودراپ مشکل داشت:

```bash
mkdir -p .github/workflows
# فایل‌های yml را داخلش بگذار و سپس:
git add .github
git commit -m "chore: add GitHub Actions workflows"
git push
```

---

## 🎛️ فعال‌سازی‌های اختیاری

### 🎧 اسپاتیفای (Spotify Now Playing)
1. برو به [spotify-github-profile.kittinanx.com](https://spotify-github-profile.kittinanx.com/) و با اکانت اسپاتیفای وارد شو.
2. UID خودت را کپی کن.
3. در `README.md` جای `YOUR_SPOTIFY_UID` را با UID خودت عوض کن.
4. اگر نمی‌خواهی، کل بلوک اسپاتیفای را از بخش `Live Signals` حذف کن.

### ⏱️ WakaTime
اگر نام کاربری‌ات در WakaTime فرق دارد، در README `username=alfimedev` را در آدرس `api/wakatime` عوض کن.

### 📰 وبلاگ (اختیاری)
اگر RSS داری (مثل `https://v2rei.surf/rss.xml`):
- در `README.md` این دو نشانگر را هر جا خواستی بگذار:
```md
<!-- BLOG-POST-LIST:START -->
<!-- BLOG-POST-LIST:END -->
```
- در `.github/workflows/blog-post-workflow.yml` مقدار `feed_list` را با آدرس واقعی RSS عوض کن.

---

## 🎨 تغییر هویت (اختیاری)
برای تغییر اسم مستعار/برند، همه‌ی کلمه‌ی `alfimedev` و `Alfime` را در این فایل‌ها جایگزین کن:
`README.md` · `snake.yml` · `3d-contrib.yml` · `metrics.yml` · `blog-post-workflow.yml`

پالت رنگی فعلی:
| رنگ | کد |
|---|---|
| طلایی لوکس | `#D4AF37` |
| فیروزه‌ای نئون | `#00E5FF` |
| بنفش سلطنتی | `#8957E5` |
| مشکی اوبسیدین | `#0D1117` |

برای عوض کردن رنگ کارت‌ها، همین کدها را داخل آدرس‌های `github-readme-stats` / `streak-stats` / `capsule-render` جابه‌جا کن.

---

## 🩺 رفع اشکال سریع
| مشکل | راه‌حل |
|---|---|
| پروفایل نمایش داده نمی‌شود | نام مخزن باید = نام کاربری و **Public** باشد. |
| مار / نمودار ۳بعدی نیست | ورک‌فلو را از تب Actions دستی اجرا کن + دسترسی Read/Write را فعال کن. |
| تصاویر بانر نمایش داده نمی‌شوند | مطمئن شو پوشه `assets` و مسیر `./assets/...` درست آپلود شده. |
| کارت‌های آمار خالی‌اند | چند دقیقه صبر کن؛ سرویس‌های آماری گاهی تأخیر دارند. |
| Actions خطا می‌دهد | در `Settings → Actions → General` دوباره Read and write permissions را سیو کن. |

---

> ✦ ساخته‌شده توسط **Alfime** — `v2rei.surf` · `t.me/alfime` · `alfimedev@gmail.com`
