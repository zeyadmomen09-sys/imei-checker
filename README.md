# 📱 Xiaomi IMEI Checker – دليل التشغيل الكامل

---

## 📁 الملفات

| الملف | الوصف |
|-------|-------|
| `index.html` | صفحة تسجيل الدخول |
| `checker.html` | لوحة فحص IMEI الرئيسية |
| `README.md` | هذا الملف |

---

## 🔐 بيانات الدخول

- **اسم المستخدم:** `mohamed`
- **كلمة المرور:** `mahmah`

---

## 🌐 الرفع على استضافة مجانية

### الطريقة 1 – Netlify (الأسهل والأسرع)

1. اذهب إلى [https://netlify.com](https://netlify.com) وسجل حساب مجاني
2. من الـ Dashboard اضغط **"Add new site"** → **"Deploy manually"**
3. اسحب مجلد الموقع كاملاً (index.html + checker.html) وأفلته في الصفحة
4. ✅ الموقع يشتغل فوراً على رابط مثل: `https://random-name.netlify.app`
5. يمكنك تغيير الاسم من Site Settings

### الطريقة 2 – GitHub Pages (مجاناً)

1. سجل على [https://github.com](https://github.com)
2. أنشئ repository جديد (Public)
3. ارفع الملفين `index.html` و `checker.html`
4. اذهب Settings → Pages → Source: **main branch**
5. الرابط: `https://username.github.io/repository-name`

### الطريقة 3 – Vercel

1. اذهب إلى [https://vercel.com](https://vercel.com)
2. سجل دخول بـ GitHub
3. Import المشروع أو ارفع الملفات مباشرة
4. Deploy تلقائي مع رابط مخصص

---

## ⚙️ إعداد الـ API

عند فتح صفحة الفحص، أدخل:

1. **رابط الـ API** – مثال: `https://api.example.com/imei/check?imei=`
2. **مفتاح API** – المفتاح الخاص بك (إن وجد)
3. **طريقة الإرسال** – GET أو POST

### مثال GET:
```
https://your-api.com/check?imei=352999111234567
```
الموقع سيضيف كل رقم IMEI تلقائياً في نهاية الرابط.

### مثال POST:
يُرسل الموقع JSON بهذا الشكل:
```json
{
  "imei": "352999111234567",
  "key": "YOUR_API_KEY"
}
```

---

## ✅ مميزات الموقع

- 🔒 تسجيل دخول بيوزر وباسورد
- 📱 تصميم Xiaomi احترافي متحرك
- 🚀 فحص حتى 200 IMEI دفعة واحدة
- ⚡ يتصل بـ API الخاص بك مباشرة
- 🚫 **لا يُخزّن أي بيانات** – كل شيء في الذاكرة فقط
- 📊 إحصائيات لحظية (ناجح / فاشل)
- ⬇ تصدير النتائج CSV
- 📱 يعمل على الموبايل والكمبيوتر

---

## 🔄 تغيير الباسورد أو اليوزر

افتح `index.html` وابحث عن هذا السطر:
```javascript
if (u === 'mohamed' && p === 'mahmah') {
```
غيّر `mohamed` و `mahmah` لأي قيم تريدها.

---

## ⚠️ ملاحظة مهمة

الموقع يعمل **Client-Side** بالكامل – يعني:
- لا يوجد سيرفر خلفي
- لا قاعدة بيانات
- البيانات تختفي بمجرد إغلاق المتصفح
- الاتصال يتم مباشرة من متصفحك إلى API الخاص بك
