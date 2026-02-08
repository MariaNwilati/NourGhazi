# 🚀 دليل رفع البورتفوليو على Vercel

## الطريقة الأولى: من خلال GitHub (الأفضل والأسهل)

### الخطوة 1: رفع المشروع على GitHub

1. **إنشاء مستودع جديد على GitHub:**
   - اذهب إلى: https://github.com/new
   - اسم المستودع: `portfolio` أو `nour-portfolio`
   - اختر: Public
   - **لا تضف** README أو .gitignore أو license (موجودين بالفعل)
   - اضغط "Create repository"

2. **ربط المشروع بـ GitHub:**
   ```bash
   cd /Users/maria/Nour/portfolio
   git remote add origin https://github.com/YOUR-USERNAME/portfolio.git
   git branch -M main
   git push -u origin main
   ```

   **ملاحظة:** استبدل `YOUR-USERNAME` باسم المستخدم الخاص بك على GitHub

### الخطوة 2: الرفع على Vercel

1. **إنشاء حساب على Vercel:**
   - اذهب إلى: https://vercel.com/signup
   - سجل دخول باستخدام حساب GitHub الخاص بك

2. **رفع المشروع:**
   - اضغط على "Add New..." ثم "Project"
   - اختر المستودع `portfolio` من القائمة
   - اضغط "Import"

3. **إعدادات المشروع:**
   - **Framework Preset:** Vite
   - **Build Command:** `npm run build`
   - **Output Directory:** `dist`
   - **Install Command:** `npm install`

4. **الرفع:**
   - اضغط "Deploy"
   - انتظر 1-2 دقيقة حتى يكتمل الرفع
   - ستحصل على رابط مثل: `https://your-portfolio.vercel.app`

---

## الطريقة الثانية: باستخدام Vercel CLI (للمتقدمين)

### 1. تثبيت Vercel CLI:
```bash
npm install -g vercel
```

### 2. تسجيل الدخول:
```bash
vercel login
```

### 3. الرفع:
```bash
cd /Users/maria/Nour/portfolio
vercel
```

اتبع التعليمات:
- Set up and deploy? **Y**
- Which scope? اختر حسابك
- Link to existing project? **N**
- What's your project's name? `portfolio`
- In which directory is your code located? **./`
- Auto-detected Project Settings (Vite)? **Y**

### 4. الرفع للإنتاج:
```bash
vercel --prod
```

---

## ⚙️ إعدادات إضافية (اختيارية)

### إضافة Domain مخصص:
1. في لوحة تحكم Vercel
2. اذهب إلى Settings > Domains
3. أضف Domain الخاص بك

### متغيرات البيئة:
إذا كنت تحتاج إلى API keys أو متغيرات أخرى:
1. اذهب إلى Settings > Environment Variables
2. أضف المتغيرات المطلوبة

---

## 🔄 التحديثات التلقائية

عند استخدام GitHub + Vercel:
- **كل push إلى main** = رفع تلقائي للإنتاج
- **كل pull request** = معاينة تلقائية

### لتحديث الموقع:
```bash
git add .
git commit -m "Update portfolio"
git push
```

وسيتم الرفع تلقائياً! 🎉

---

## 🐛 حل المشاكل الشائعة

### مشكلة: Build Failed
**الحل:** تأكد من أن المشروع يعمل محلياً:
```bash
npm run build
npm run preview
```

### مشكلة: الصور لا تظهر
**الحل:** تأكد من المسارات النسبية `/profile.jpeg` بدلاً من `./profile.jpeg`

### مشكلة: الصفحة فارغة
**الحل:** افتح Developer Console في المتصفح وتحقق من الأخطاء

---

## 📞 الدعم

- Vercel Docs: https://vercel.com/docs
- Vite Docs: https://vitejs.dev/guide/
- React Docs: https://react.dev/

---

## ✅ Checklist قبل الرفع

- [ ] المشروع يعمل محلياً (`npm run dev`)
- [ ] Build ينجح (`npm run build`)
- [ ] لا توجد أخطاء في Console
- [ ] الصور تظهر بشكل صحيح
- [ ] الموقع responsive على جميع الأجهزة
- [ ] روابط Social Media صحيحة
- [ ] البريد الإلكتروني صحيح

---

**ملاحظة مهمة:**
الملفات الحساسة مثل `.env` غير موجودة في هذا المشروع، لكن إذا أضفتها مستقبلاً، تأكد من إضافتها إلى `.gitignore`!

Good luck! 🚀
