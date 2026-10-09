# اجرای بیلد APK از داخل GitHub

Workflow با نام **DreamHouse Android APK** به مخزن اضافه شده است. این workflow آرشیو `DreamHouse_CloudBuild_Prep.zip` را در runner استخراج می‌کند و سپس Unity را برای Android اجرا می‌کند. این کار فایل ZIP را به‌صورت مستقیم به عنوان ریشه پروژه در نظر نمی‌گیرد.

## پیش‌نیاز اجباری: Unity License
GitHub Actions به اطلاعات مجوز Unity نیاز دارد. قبل از اجرا، در مخزن بروید به:

**Settings → Secrets and variables → Actions → New repository secret**

و secrets مورد نیاز روش احراز هویت Unity خود را تنظیم کنید:
- `UNITY_LICENSE`
- `UNITY_EMAIL`
- `UNITY_PASSWORD`

روش و مقادیر دقیق به نوع لایسنس Unity شما بستگی دارد. رمزها را در کد یا چت قرار ندهید. اگر از روش لایسنس شخصی/سریال استفاده می‌کنید، دستورالعمل جاری GameCI و Unity را برای همان نوع مجوز دنبال کنید.

## شروع بیلد با گوشی
1. باز کنید: https://github.com/Eh333an/DreamHouse-MVP/actions
2. انتخاب کنید **DreamHouse Android APK**.
3. روی **Run workflow** بزنید.
4. بعد از اتمام، نتیجه باید سبز باشد؛ در بخش Artifacts فایل `DreamHouse-Android-APK` ظاهر می‌شود.
5. اگر شکست خورد، وارد اجرای ناموفق شوید و متن خطا را بررسی کنید؛ رایج‌ترین موانع، مجوز Unity، ناسازگاری build method، یا خطاهای کامپایل/تنظیمات پروژه هستند.

## وضعیت فعلی و محدودیت
Workflow فقط به مخزن اضافه شده است؛ در این مرحله هیچ APK ساخته یا آزمایش نشده. باید اجرای واقعی با Unity license معتبر انجام شود. اگر build method در اسکریپت پروژه قابل فراخوانی نباشد، workflow خطا می‌دهد و لازم است بر اساس log اصلاح شود.
