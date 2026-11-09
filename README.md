# skyV

**نظام ذكي لتحميل وتحويل الوسائط الرقمية (فيديو / صوت) — واجهة Tkinter + yt-dlp.**

**Smart media downloader & converter for Windows — Tkinter + yt-dlp.**

| | |
|---|---|
| 🌍 اللغة / Language | العربية · English |
| 🖥️ النظام / Platform | Windows 10 / 11 |
| 🐍 Python | 3.11+ |

---

## ✨ المميزات · Features

### 🇪🇬 عربي

**التحميل**
- تحميل فيديو من يوتيوب وأكثر من 1000 موقع يدعمه yt-dlp.
- اكتشاف كل الجودات المتاحة تلقائيًا بمجرد لصق الرابط — بدون زر إضافي.
- خيار «أعلى جودة متاحة» بدون سقف (حتى 4K).
- تفضيل `h264 + m4a` والدمج على `mp4` لأعلى توافق.
- تحميل صوت **MP3 192kbps** مع دمج صورة الغلاف تلقائيًا.
- اختيار مجلد الحفظ في كل عملية.

**التحويل المحلي**
- تحويل أي فيديو على جهازك (mp4/mkv/avi/mov/webm) إلى MP3 بالمدة الكاملة + غلاف واحد.
- فحص الملف أولًا بـ ffmpeg (صوت؟ فيديو؟ مدة؟) ورسالة خطأ واضحة بدل الفشل الصامت.

**الوسوم الذكية**
- استخراج المغني والأغنية من صيغة العنوان `مغني - أغنية` (بدون إنترنت).
- بحث في iTunes API (مجاني بدون مفتاح) لجلب الألبوم والنوع والسنة ورقم المسار.
- كتابة الوسوم بـ `mutagen` بدون إعادة ترميز — سريع ويحافظ على الغلاف.
- **حماية من البيانات الغلط:** حارس للمغني + عقوبة للنسخ (Remix/Live) + لا بحث بدون اسم مغني.

**تجربة الاستخدام**
- واجهة داكنة أنيقة + لغتان (عربي / English) بتبديل فوري.
- شريط حالة يعرض نسبة التحميل والوقت المنقضي لحظيًا.
- زر إلغاء أثناء التنزيل: يوقف yt-dlp ويقتل ffmpeg ويحذف الملفات الناقصة.
- فتح الملف تلقائيًا بعد النجاح.
- نافذة واحدة فقط (mutex) — إعادة التشغيل تركّز النافذة المفتوحة.
- لصق 📋 / تصفح 📁 / دعم Ctrl+V، ونافذة ❓ للمميزات، وزر إيميل يفتح جيميل جاهزًا.

**المتانة**
- فحص الاتصال بالإنترنت قبل البدء برسالة واضحة.
- كل عمليات الواجهة عبر queue على الـ main thread — بدون تجميد.
- منع نوافذ CMD السوداء عند تشغيل deno/ffmpeg.
- اكتشاف تلقائي لمحركات JS (deno/node/bun/quickjs) + `yt_dlp_ejs` → جودات يوتيوب الكاملة.
- ffmpeg مضمّن عبر `imageio-ffmpeg` — بدون تثبيت منفصل.
- تسجيل الأخطاء في `skyV.log` بترميز UTF-8.
- exe واحد محمول، بدون console، بأيقونة وAppUserModelID.

### 🇬🇧 English

**Downloading**
- Download video from YouTube and 1000+ sites supported by yt-dlp.
- All available qualities auto-detected the moment you paste a link (no extra button).
- "Best available" option with no cap — up to 4K.
- Prefers `h264 + m4a`, merged into `mp4` for maximum compatibility.
- Audio download as **MP3 192kbps** with embedded cover art.
- Choose the save folder for every job.

**Local conversion**
- Convert any local video (mp4/mkv/avi/mov/webm) to MP3 — full length + one cover image.
- Probes the file with ffmpeg first (audio? video? duration?) and shows a clear error instead of failing silently.

**Smart tagging**
- Parses artist & song from the `Artist - Song` title format (works offline).
- Queries the iTunes API (free, no key) for album, genre, year and track number.
- Writes tags via `mutagen` without re-encoding — fast, keeps the cover art.
- **Wrong-data protection:** artist guard + version penalty (Remix/Live) + no search without an artist name.

**User experience**
- Clean dark UI + two languages (Arabic / English) switched instantly.
- Live status bar with download percentage and elapsed time.
- Cancel button: stops yt-dlp, kills ffmpeg, removes partial files.
- Opens the finished file automatically.
- Single instance (mutex) — relaunching focuses the existing window.
- Paste 📋 / Browse 📁 / Ctrl+V support, a ❓ features dialog, and an email button that opens Gmail pre-filled.

**Robustness**
- Internet check before starting, with a clear message.
- All UI updates go through a queue on the main thread — no freezing.
- No flashing CMD windows when spawning deno/ffmpeg.
- Auto-detects JS runtimes (deno/node/bun/quickjs) + `yt_dlp_ejs` → full YouTube qualities.
- ffmpeg bundled via `imageio-ffmpeg` — nothing extra to install.
- Errors logged to `skyV.log` in UTF-8.
- Single portable exe, no console, custom icon + AppUserModelID.

---

## 📦 التثبيت · Installation
# skyV
```powershell
pip install -r requirements.txt
python main.py
