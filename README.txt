منصة بصائر - نسخة GitHub / Render

المكونات:
- index.html: الصفحة الرئيسية.
- portal.html: بوابة الدخول والفصول المباشرة ولوحة إنشاء الحسابات للمدير وطلبات التحدث للمحاضر.
- server/: خادم Express وواجهات المصادقة والصلاحيات وLiveKit وقاعدة PostgreSQL.
- server/sql/schema.sql: إنشاء الجداول والحلقات الأساسية.

التشغيل والنشر:
راجع README-DEPLOY-AR.md للتعليمات الكاملة. لا ترفع ملف .env أو أي مفاتيح سرية إلى GitHub.

قبل الاستخدام الفعلي:
1. غيّر API_BASE داخل portal.html إلى عنوان خدمة Render الحقيقي.
2. اضبط متغيرات البيئة على Render، وبالأخص DATABASE_URL وJWT_SECRET وبيانات LiveKit وCORS_ORIGINS.
3. نفّذ server/sql/schema.sql على قاعدة PostgreSQL.
4. أنشئ حساب المدير باستخدام npm run admin:create بعد ضبط BOOTSTRAP_ADMIN_NAME وBOOTSTRAP_ADMIN_EMAIL وBOOTSTRAP_ADMIN_PASSWORD.
5. اختبر المنصة بحساب محاضر وحساب طالب من جهازين مختلفين.

تم التحقق من صياغة ملفات JavaScript باستخدام Node.js. هذا الفحص لا يعادل اختبار نشر أو اتصال فعلي بخدمات Render وPostgreSQL وLiveKit.
