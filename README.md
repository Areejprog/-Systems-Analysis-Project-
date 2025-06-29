# -Systems-Analysis-Project-
📘 مشروع تحليل النظم (Systems Analysis Project)

تحليل نظام متجر إلكتروني لبيع المنتجات عبر الإنترنت

🎯 الهدف:
تصميم مشروع بسيط لتحليل نظام افتراضي، باستخدام خطوات علمية تشمل:

✔فهم المشكلة
✔تحديد متطلبات النظام
✔رسم مخططات
✔اقتراح الحل (نظام جديد أو تحسين الحالي)

📍المرحلة 1: Use Case Diagram (مخطط حالات الاستخدام)

🎭 الجهات الفاعلة (Actors):
العميل (User)
مدير النظام (Admin)
موظف الدعم الفني (Support)
💡(لو بنضيف بوابة الدفع لاحقًا، ممكن نعتبرها Actor خارجي ) . 

⚙ الوظائف الأساسية:

🔹 العميل (User):
التسجيل في الموقع
تسجيل الدخول
تصفح المنتجات
البحث عن منتج
إضافة منتج للسلة
تأكيد الطلب
الدفع أونلاين
تتبع حالة الطلب
تقييم المنتج

🔹 المدير (Admin):
إضافة/تعديل/حذف منتج
إدارة الطلبات
إدارة المستخدمين
مراجعة التقارير

🔹 الدعم الفني:
الرد على الاستفسارات
حل المشاكل
إدارة الشكاوى


📍 المرحلة 2: مخطط تدفق البيانات DFD - المستوى 0 (Level 0)

🎯 الهدف:
عرض كيف تتحرك البيانات داخل النظام بين الكيانات الرئيسية (المستخدم، المدير، النظام).

💡 مكونات DFD Level 0:

🔸 الكيانات الخارجية:
العميل (يُدخل بيانات الطلب - يستقبل إشعار)
المدير (يدخل منتجات، يراجع الطلبات)
🔸 العمليات الرئيسية (Processes):
تسجيل الدخول والتسجيل
تصفح المنتجات
تنفيذ الطلب
إدارة النظام
🔸 قواعد البيانات (Data Stores):
قاعدة بيانات المستخدمين
قاعدة بيانات المنتجات
قاعدة بيانات الطلبات

🔁 العلاقات بين الكيانات (Entities) في ERD:

1. العلاقة بين "العميل" و"الطلب"
العلاقة: العميل يقدّم طلب
النوع:
واحد إلى متعدد (1:N)
كل عميل يمكنه تقديم عدة طلبات، لكن كل طلب يعود لعميل واحد فقط.
مفتاح العلاقة:
معرف العميل في جدول الطلب هو مفتاح خارجي (Foreign Key) يشير إلى جدول العميل.

2. العلاقة بين "الطلب" و"المنتج"
العلاقة: الطلب يحتوي على منتجات
النوع:
متعدد إلى متعدد (M:N)
كل طلب يحتوي عدة منتجات، وكل منتج ممكن يكون موجود في طلبات متعددة.
الحل:
نحتاج جدول وسيط (نسميه غالبًا: تفاصيل الطلب أو Order_Details)
يحتوي على:
معرف الطلب
معرف المنتج
الكمية
السعر وقت الطلب

📝 المرحلة 3: المتطلبات الوظيفية (Functional Requirements)

هذه توضح ما يجب أن يقوم به النظام فعليًا، بناءً على ما حددناه في Use Case وERD:

📌 مثال على المتطلبات الوظيفية:
1. إدارة الحساب:

يمكن للمستخدم إنشاء حساب جديد.
يمكن للمستخدم تسجيل الدخول باستخدام البريد وكلمة المرور.
يمكن للمستخدم تعديل بياناته الشخصية.
2. تصفح المنتجات:

يمكن للمستخدم مشاهدة قائمة المنتجات.
يمكن البحث باستخدام اسم المنتج أو الفئة.
3. إدارة السلة:

يمكن للمستخدم إضافة منتج إلى السلة.
يمكن للمستخدم إزالة منتج من السلة.
النظام يحسب السعر الإجمالي تلقائيًا.
4. الطلب والدفع:

يمكن للمستخدم تأكيد الطلب.
النظام يرسل إشعار للعميل بتأكيد الطلب.
يمكن ربط النظام ببوابة دفع إلكترونية (مثل STC Pay، مدى).
5. التتبع والدعم:

يمكن للمستخدم متابعة حالة الطلب (قيد التجهيز – تم الشحن – تم التسليم).
يمكن للمستخدم إرسال بلاغ أو استفسار للدعم الفني.


📋 المرحلة 5: المتطلبات غير الوظيفية (Non-Functional Requirements)

🛡 الأمان:
يجب تشفير كلمات المرور.
صلاحيات مختلفة (العميل – المدير).
⚡ الأداء:
تحميل الصفحة لا يتجاوز 3 ثوانٍ.
استيعاب أكثر من 1000 مستخدم في نفس الوقت.
🖥 الواجهة:
الواجهة باللغة العربية وسهلة الاستخدام.
متوافقة مع الأجهزة المحمولة.


مثال بسيط يختصر لك النظام كامل تقدر تبني عليه مشروعك 

(اتمنى ان شرحي يفيد طلاب و طالبات البكالوريوس في مشاريع تخرجهم ، في يوم من الايام كنت اتمنى شخص يبسط لي الموضوع بهذي البساطة )
 بالتوفيق … شكرا 🙏
