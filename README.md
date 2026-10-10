# Shopping Mido

متجر إلكتروني عربي RTL مبني باستخدام Next.js وSupabase.

## المتطلبات
- Node.js 20 أو أحدث.
- مشروع Supabase.
- متغيرا البيئة `NEXT_PUBLIC_SUPABASE_URL` و`NEXT_PUBLIC_SUPABASE_ANON_KEY`.

## التشغيل محليًا
1. انسخ `.env.example` إلى `.env.local` وضع بيانات مشروع Supabase.
2. نفّذ `npm install`.
3. نفّذ `npm run dev`.
4. افتح `http://localhost:3000`.

## قاعدة البيانات
نفّذ ملف `supabase/schema.sql` من SQL Editor في لوحة Supabase. راجع سياسات RLS قبل إدخال بيانات حقيقية.
لإنشاء أول أدمن، أنشئ المستخدم من Supabase Auth ثم عيّن `profiles.role = 'admin'` لذلك المستخدم يدويًا من لوحة Supabase الموثوقة.

## النشر على Vercel
ارفع المشروع إلى GitHub، ثم استورده في Vercel، وأضف متغيرات البيئة. نفّذ SQL قبل اختبار المتجر.

## ملاحظات
- بوابة الدفع غير مفعلة؛ الطلبات تسجل كطلبات غير مدفوعة.
- لا تضع مفاتيح سرية في GitHub.
- يجب اختبار صلاحيات RLS وتدفق الطلبات قبل استخدام الموقع تجاريًا.
