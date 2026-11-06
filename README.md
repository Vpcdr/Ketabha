# کتاب خوان - ketabha
مجموعه ۱۱۰ عنوانی با یک موضوع واحد - فصل بازکن

**ساخت برنامه توسط VPCDR**

### لوگو
حرف «ک» به خط نستعلیق، مشکی با حاشیه زرد کمرنگ داخل دایره بی‌رنگ
`public/logo.png`

### امکانات
- ۱۱۰ عنوان قابل نامگذاری
- فصل بازکن واحد
- جستجو در عناوین + جستجو داخلی هر کتاب
- یادداشت برداری برای هر صفحه (ذخیره در localStorage)
- تهیه اسکرین‌شات PNG و عکس HQ از صفحه
- ساعت و تاریخ زنده شمسی + میلادی
- طراحی RTL پرمیوم

### ساختار پوشه کتاب‌ها
```
/books/
  /1/
    page_1.jpg
    page_2.jpg
    ...
  /2/
    page_1.jpg
  ...
  /110/
```

اسکن‌های خود را با نام `page_{n}.jpg` داخل هر پوشه بریزید.

کد داخل `index.html` این تابع را دارد:
```js
const getPageImage = (bookId, pageNumber) => `/books/${bookId}/page_${pageNumber}.jpg`
```

### اجرای محلی
فقط `index.html` را باز کنید یا با یک سرور ساده:
```bash
npx serve .
```

### پوش به گیت‌هاب - ریپازیتوری ketabha
```bash
cd ketabha
git init
git add .
git commit -m "نسخه اولیه ketabha - 110 عنوان + لوگو نستعلیق"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/ketabha.git
git push -u origin main
```

بعد از پوش، برای فعال‌سازی GitHub Pages:
Settings > Pages > Source: main / root

### نامگذاری ۱۱۰ عنوان
فایل `titles.json` را ویرایش کنید یا لیست را برای من بفرستید تا اعمال کنم.
