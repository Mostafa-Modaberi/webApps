# Mostafa Modaberi — My Digital Workspace

داشبورد شخصی وب‌اپلیکیشن‌های مصطفی مدبری؛ نقطهٔ ورود و فهرست مرکزی ابزارهای تحت وب.

## داشبورد زنده
https://mostafa-modaberi.github.io/webApps/

## اپلیکیشن‌ها

| برنامه | مسیر | توضیح |
|---|---|---|
| چاپ لیست کلاسی | [apps/class-roster/](apps/class-roster/) | مدیریت، تنظیم و چاپ لیست کلاسی با قالب A4 |

## افزودن اپلیکیشن جدید

1. برای برنامه یک پوشه در `apps/APP-NAME/` بسازید.
2. فایل ورودی آن را با نام `index.html` قرار دهید.
3. یک شیء جدید به آرایهٔ `window.SITE.apps` در فایل ریشهٔ `index.html` اضافه کنید:

```js
{
  id: "my-app",
  path: "apps/my-app/",
  category: "utility", // education | utility | design | code | other
  status: "active",    // active | dev
  icon: "✦",
  name: { fa: "نام فارسی", en: "English name" },
  desc: { fa: "توضیح فارسی", en: "English description" }
}
```

4. تغییرات را به شاخهٔ `main` ارسال کنید؛ GitHub Actions سایت را منتشر می‌کند.

## امکانات داشبورد
- فارسی/انگلیسی و چینش RTL/LTR
- تم روشن و تاریک با ذخیره در مرورگر
- جست‌وجو و فیلتر دسته‌بندی
- کارت مستقل برای هر وب‌اپلیکیشن
- طراحی واکنش‌گرا برای موبایل و دسکتاپ

## ساختار
```
webApps/
├── index.html
├── README.md
├── apps/
│   └── class-roster/
│       └── index.html
└── .github/
    └── workflows/
        └── deploy-pages.yml
```

تمام برنامه‌ها به‌صورت Static میزبانی می‌شوند و برای اجرا به Backend نیاز ندارند.
