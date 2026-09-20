# 🚀 alfimeDev — دليل التركيب خطوة بخطوة

> دليل كامل لتشغيل **بروفايل GitHub الأسطوري** الخاص بـ **alfimeDev** في أقل من 5 دقائق.
> تصميم فاخر · حركة كاملة · محتوى غني · بدون أي قوالب جاهزة.

---

## 📁 محتوى الحزمة

| الملف / المجلد | الوصف |
|---|---|
| `README.md` | ملف البروفايل الرئيسي (النجم الرئيسي) ✨ |
| `assets/banner.jpg` | البانر العلوي الفاخر (Hero Banner) |
| `assets/logo.jpg` | شعار المونوجرام الذهبي (Monogram) |
| `assets/divider.jpg` | الفاصل النيوني المتحرك بين الأقسام |
| `.github/workflows/snake.yml` | أنيميشن الثعبان الذي يأكل شبكة المساهمات 🐍 |
| `.github/workflows/3d-contrib.yml` | مخطط المساهمات ثلاثي الأبعاد 🧊 |
| `.github/workflows/metrics.yml` | لوحة المقاييس الكاملة (شهادات + عادات + نشاط) 📊 |
| `.github/workflows/blog-post-workflow.yml` | (اختياري) أحدث تدويناتك من RSS 📰 |

---

## 🛠️ خطوات التركيب

### 1️⃣ أنشئ المستودع الخاص بالبروفايل
يجب أن يكون اسم المستودع **بنفس اسم حسابك بالضبط**:

```
alfimedev
```

> ⚠️ **مهم جدًا:** المستودع يجب أن يكون **Public** وأن يكون اسمه `alfimedev` (نفس اسم المستخدم) لكي يظهر كبروفايل شخصي على صفحتك.

---

### 2️⃣ ارفع الملفات
ارفع الملفات مع الحفاظ على نفس المسارات والبنية:

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

> 💡 الصور داخل `assets/` تُستخدم مباشرة عبر مسارات محلية `./assets/...` — لذلك لا تحتاج أي استضافة خارجية.

---

### 3️⃣ فعّل صلاحيات GitHub Actions
اذهب إلى:

```
Settings → Actions → General → Workflow permissions
```

ثم اختر:

```
✅ Read and write permissions
```

واضغط **Save**. هذا ضروري لعمل الأنيميشن والرسم ثلاثي الأبعاد ولوحة المقاييس.

---

### 4️⃣ شغّل سير العمل يدويًا (أول مرة)
اذهب إلى تبويب **Actions** ثم:

- اختر `Generate Snake Animation` ← اضغط **Run workflow** 🐍
- اختر `Generate 3D Contribution Graph` ← اضغط **Run workflow** 🧊
- اختر `Generate GitHub Metrics` ← اضغط **Run workflow** 📊

ماذا سيحدث بعد التشغيل؟
| الناتج | مكان الملف | يُستخدم في |
|---|---|---|
| أنيميشن الثعبان | فرع جديد اسمه `output` | قسم «Contribution Grid, Devoured» |
| المخطط ثلاثي الأبعاد | مجلد `profile-3d-contrib/` في `main` | قسم «3D Contribution City» |
| لوحة المقاييس | ملف `github-metrics.svg` في `main` | القسم القابل للفتح «FULL metrics dashboard» |

> ⏱️ بعد أول تشغيل، ستعمل هذه السير تلقائيًا (كل 12 ساعة / يوميًا) لتحديث البيانات.

---

### 5️⃣ (اختياري) تفعيل بطاقة Spotify
قسم **Live Signals** يحتوي بطاقة «Spotify Now Playing». لتفعيلها:

1. اذهب إلى [spotify-github-profile.kittinanx.com](https://spotify-github-profile.kittinanx.com/) وسجّل الدخول بحساب Spotify.
2. انسخ مُعرّف المستخدم (UID) الخاص بك.
3. في `README.md` استبدل:
   - `YOUR_SPOTIFY_UID` داخل رابط `spotify-github-profile` بمُعرّفك.
   - رابط `open.spotify.com/user/` بإضافة مُعرّفك.
4. في حال عدم الرغبة في تفعيلها، احذف بلوك الـ Spotify بالكامل من قسم `Live Signals`.

---

### 6️⃣ (اختياري) تفعيل بطاقة WakaTime
بطاقة `api/wakatime` تعمل تلقائيًا إذا كان اسمك في WakaTime هو `alfimedev`.
إن كان مختلفًا، استبدل `username=alfimedev` بـ `username=اسمك_في_wakatime`.

---

### 7️⃣ (اختياري) قسم «أحدث التدوينات»
إذا كان لديك مدونة أو خلاصة RSS على موقعك (مثل `https://v2rei.surf/rss.xml`):

- فعّل ملف `.github/workflows/blog-post-workflow.yml`.
- أضف داخل `README.md` العلامتين التاليتين في المكان الذي تريد ظهور التدوينات فيه:

```md
<!-- BLOG-POST-LIST:START -->
<!-- BLOG-POST-LIST:END -->
```

- عدّل `feed_list` في ملف السير ليشير إلى رابط RSS الحقيقي.

---

### 8️⃣ تخصيص الاسم
إذا كان اسم مستخدمك على GitHub مختلفًا عن `alfimedev`، استبدل كل ظهور لكلمة `alfimedev` في:

- `README.md`
- `.github/workflows/snake.yml`
- `.github/workflows/3d-contrib.yml`
- `.github/workflows/metrics.yml`
- `.github/workflows/blog-post-workflow.yml`

باسم المستخدم الصحيح.

---

## 🎨 لوحة الألوان المستخدمة (الفخامة)

| اللون | الكود | الاستخدام |
|---|---|---|
| ذهبي فاخر | `#D4AF37` | العنوان الأساسي · العناصر المميزة |
| سماوي كهربي | `#00E5FF` | الروابط · التوهج · اللمسات التقنية |
| بنفسجي ملكي | `#8957E5` | التدرجات · العناصر الثانوية |
| أسود أوبسيديان | `#0D1117` | الخلفية الأساسية |

لتغيير ألوان البطاقات، بدّل القيم `D4AF37` / `00E5FF` / `8957E5` / `0D1117` داخل روابط `github-readme-stats` و`streak-stats` و`capsule-render`.

---

## ⌨️ نصائح احترافية للفوز بالمسابقة
1. **ثبّت المستودع (Pin)** في أعلى صفحتك بعد رفع الملفات.
2. ارفع **صورة شخصية احترافية** (مربّعة) لتعزيز الهوية البصرية.
3. تأكد من أن ملف `README.md` هو الملف الرئيسي في الفرع `main`.
4. شغّل كل سير العمل مرة يدويًا حتى تظهر كل الأقسام بالبيانات.
5. حدّث الأصول البصرية (`banner` / `logo`) بأي هوية جديدة ترغبها.

---

> ✦ صُمّم بإتقان. حُرّك إطارًا بإطار. من الصفر بدون قوالب.
> **Alfime** — `v2rei.surf` · `t.me/alfime` · `alfimedev@gmail.com`
