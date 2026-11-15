# KHADIJA — THE MAGICAL JOURNEY
موقع هدية عيد ميلاد تفاعلي، بحال فيلم صغير: 6 فصول، كاميرا سينمائية، حوار، دفتر رقمي، بورتريه، ومفاجأة أخيرة.
An interactive cinematic birthday story. Pure HTML / CSS / JavaScript — no backend, no paid services, no build step.

## 1) كيفاش تشغلو (Run locally)
- **أسهل طريقة:** حل `index.html` مباشرة فالمتصفح (Chrome / Edge / Firefox / Safari). كيخدم بلا سيرفر.
- **ولا بسيرفر بسيط:** فهاد المجلد دير `python -m http.server 8000` وحل `http://localhost:8000`.

## 2) كيفاش تبدل المحتوى (Customize) — ملف واحد فقط
كل شي كاين فـ **`data/config.js`**:
- الأسماء (`names`) — خديجة / أيوب
- الحوار (`dialogue`)، صفحات الدفتر (`diary`)، رسائل الرحلة (`journey`)، الرسالة الأخيرة (`final.letter`)
- عناوين الفصول (`chapters`)، النصوص ديال الواجهة (`ui`)
- مسارات الصور والموسيقى (`photos`, `music`)

كل نص يقدر يكون كلمة وحدة `"Hello"` ولا بعدة لغات `{ en:"...", ary:"...", ar:"..." }`.
`ary` = الدارجة بالحروف العربية، `ar` = العربية الفصحى. أي ترجمة ناقصة كترجع للإنجليزية.
استعمل `{khadija}` و `{ayoub}` داخل أي نص باش يتبدل الاسم أوتوماتيكيا.

> المحتوى الحالي (الذكريات، التواريخ، الرسالة) **placeholders فقط**. ما تخليهش كيف هو: كتب ذكرياتك الحقيقية.

## 3) الصور والصوت (Assets to replace)
| شنو | فين | ملاحظات |
|---|---|---|
| صورة أيوب | `assets/characters/ayoub.png` ثم `photos.ayoub` | PNG/JPG عمودية، خلفية داكنة أحسن |
| صورة خديجة | `assets/characters/khadija.png` ثم `photos.khadija` | نفس الشي |
| صورة البورتريه (الفصل 5) | `assets/images/portrait.jpg` ثم `photos.portrait` | كتظهر بتأثير cyan/emerald |
| الموسيقى (اختياري) | `assets/audio/music.mp3` ثم `music` | بلا ملف = أصوات مولّدة داخلياً |
إلا خليتي `photos` فارغة، الشخصيات رسوم أصلية خيالية (ماشي صور حقيقية).
صغّر الصور (≈ 1 MB كحد أقصى) باش يبقى الموقع خفيف على التلفون.

## 4) النشر على GitHub Pages
1. دير repository جديد فـ GitHub وطلّع فيه كل محتوى هاد المجلد (`index.html` فالجذر).
2. Settings → Pages → Source: **Deploy from a branch** → Branch: `main` / `(root)` → Save.
3. بعد دقيقة غادي يطلع الرابط: `https://USERNAME.github.io/REPO/`

## 5) ميزات
- كاميرا: تحرك أفقي وعمودي، zoom، parallax، انتقالات ضوئية بين الفصول
- حوار بكتابة تدريجية، اختيارات، سجل، دعم RTL
- دفتر بصفحات كتتقلب، بطاقات ذكريات، ملاحظات مخفية
- قائمة: الفصول، اللغة (EN / الدارجة / العربية)، تقليل الحركة
- الصوت ما كيبدا حتى تضغط عليه. الكيبورد: Enter للحوار، الأسهم فالدفتر، Esc للإغلاق

## 6) الملفات
```
index.html   css/ (main, animations, scenes, diary, responsive)
js/ (util, audio, transitions, camera, dialogue, diary, scenes, app)
data/config.js   docs/CUSTOMIZATION.md   assets/
```
