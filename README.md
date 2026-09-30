# Banky | محفظتك الرقمية

تطبيق محفظة مالية للهواتف مبني باستخدام Flutter، بواجهة عربية كاملة تدعم الاتجاه من اليمين إلى اليسار (RTL). يتيح التطبيق للمستخدم إدارة محافظه، متابعة معاملاته، وإجراء التحويلات والمدفوعات من خلال واجهة موحدة تتصل بخدمات `Banky.API`.

**English:** Banky is an Arabic-first Flutter mobile wallet app for managing multi-currency wallets, transfers, POS payments, and transaction history through the Banky.API backend.

## نظرة عامة

يجمع Banky أدوات المحفظة الرقمية في تطبيق واحد، مع التركيز على تجربة عربية واضحة وإدارة الحساب والتحقق من الهوية قبل إتاحة العمليات المالية. يتطلب تشغيل الوظائف المتصلة توفر خادم `Banky.API` متوافق؛ الخادم غير مضمن في هذا المستودع.

## المزايا

- إنشاء الحساب وتسجيل الدخول واستعادة كلمة المرور وتغييرها.
- عرض المحافظ والأرصدة بعملات متعددة، وإنشاء محفظة جديدة عند توفر العملة.
- التحويل إلى مستخدم عبر رقم الهاتف، مع التحقق من المستلم وعرض الرسوم قبل التأكيد.
- الدفع لنقاط البيع وإدارة نقاط البيع الخاصة بالمستخدم.
- التحويل بين محافظ المستخدم وحساب الرسوم وسعر الصرف.
- عرض سجل المعاملات والإيصالات.
- رفع وثائق الهوية ومتابعة حالة التحقق (KYC).
- إعدادات الخصوصية، وخيارات المظهر الفاتح والداكن وتلقائي.
- واجهة عربية واتجاه RTL، مع إدارة الحالة باستخدام Provider.

## التقنيات

- Flutter وDart
- Provider لإدارة الحالة
- HTTP للاتصال بواجهة API
- SharedPreferences لحفظ رمز جلسة JWT محليًا
- Intl لتنسيق القيم والتواريخ
- Image Picker لاختيار صور التحقق

## المتطلبات

- Flutter SDK يتضمن Dart SDK بإصدار متوافق مع القيد الموجود في `pubspec.yaml` (Dart 3.13.0 أو أحدث).
- خادم `Banky.API` قيد التشغيل ويمكن الوصول إليه من الجهاز أو المحاكي.
- Android Studio أو Xcode عند بناء التطبيق للمنصة المستهدفة.

## التشغيل محليًا

1. استنسخ المستودع وافتح مجلده:

   ```bash
   git clone <REPOSITORY_URL>
   cd banky_mobile_phone
   ```

2. حدّث عنوان الخادم في `lib/core/api_constants.dart` إلى عنوان `Banky.API` المتاح لبيئتك. أمثلة شائعة:

   - محاكي Android: `http://10.0.2.2:5021`
   - محاكي iOS: `http://localhost:5021`
   - جهاز فعلي: استخدم عنوان IP لجهاز الخادم على الشبكة المحلية.

   تأكد أن الخادم يسمح بالاتصال من الجهاز، ولا ترفع عنوانًا داخليًا أو بيانات اعتماد إلى مستودع عام. استخدم HTTPS وإعدادًا مناسبًا لكل بيئة قبل النشر.

3. ثبّت الحزم وشغّل التطبيق:

   ```bash
   flutter pub get
   flutter run
   ```

## بناء التطبيق

لبناء نسخة Android:

```bash
flutter build apk --release
```

لبناء نسخة iOS (على macOS مع Xcode):

```bash
flutter build ios --release
```

## بنية المشروع

```text
lib/
  core/       إعداد الثيم والمصادقة والثوابت
  models/     نماذج المستخدم والمحافظ والمعاملات ونقاط البيع
  screens/    شاشات الحساب والمحفظة والتحويل والإعدادات
  services/   الاتصال بخادم Banky.API
  widgets/    مكونات واجهة قابلة لإعادة الاستخدام
```

## إعداد GitHub المقترح

**وصف المستودع (About):**

```text
Arabic-first Flutter mobile wallet with multi-currency wallets, transfers, POS payments, and Banky.API integration.
```

**Topics:** `flutter` `dart` `digital-wallet` `mobile-banking` `fintech` `arabic` `rtl` `point-of-sale`

## ملاحظات أمنية

هذا التطبيق عميل يتصل بخادم مالي منفصل. لا تستخدمه لمعالجة أموال حقيقية قبل مراجعة أمان التطبيق والخادم، واستخدام HTTPS، وحماية الرموز والبيانات الحساسة، واختبار تدفقات المصادقة والتحويل والتحقق من الهوية. لا تضع أسرارًا أو عناوين خدمة خاصة في مستودع عام.

## English summary

Banky is an Arabic-first Flutter mobile wallet client. It includes multi-currency wallet views, phone-based transfers, POS payments and management, self-exchange, transaction history, KYC submission, account settings, and light/dark themes. It requires a separately hosted compatible `Banky.API` backend.

## الكلمات المفتاحية

Banky, Flutter wallet, mobile wallet, digital wallet, Arabic fintech, تطبيق محفظة إلكترونية, محفظة متعددة العملات, تحويل الأموال عبر الهاتف, الدفع عبر نقاط البيع, Flutter Arabic RTL, Android, iOS.