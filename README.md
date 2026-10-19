🏥 Hospital Performance & Wait Time Analytics | لوحة مؤشرات أداء المستشفيات وزمن الانتظار

📌 Project Overview

This Power BI dashboard provides a comprehensive data analysis of operational efficiency, patient wait times, and triage distribution across 12 hospitals. By analyzing 1,000 patient visits and performance metrics of 84 doctors, this project delivers actionable insights to optimize hospital capacity and reduce patient waiting periods.

📊 Key Performance Indicators (KPIs)

Total Visits: 1,000 visits

Total Patients: 286 patients

Total Doctors: 84 doctors

Total Hospitals: 12 facilities

Average Wait Time: 62.13 minutes

% Seen Within 30 Mins Target: 23.50%

🛠️ Data Model & DAX Measures

The dataset is structured using a Star Schema model, connecting visit facts with hospital, doctor, and department dimensions.

Key DAX Formulas:

Target Line Measure (30 Mins):

خط مدة الانتظار (دقيقة) = 30


Patients Seen Within 30 Minutes %:

PercentWithin30 = 
VAR TotalVisitsCount = COUNT('جدول حركة الزيارات'[رقم الزيارة])
VAR SeenWithin30 = CALCULATE(
    COUNT('جدول حركة الزيارات'[رقم الزيارة]),
    'جدول حركة الزيارات'[مدة الانتظار (دقيقة)] <= 30
)
RETURN
DIVIDE(SeenWithin30, TotalVisitsCount, 0)


💡 Key Findings & Recommendations

Conclusions:

High Average Wait Time: The overall average wait time across all facilities is 62.13 minutes, exceeding standard benchmarks.

KPI Shortfall: Only 23.50% of patients are attended to within the target threshold of 30 minutes.

Departmental Disparities: Significant variation in wait times exists across different departments (e.g., OB/GYN vs. Emergency/General).

Recommendations:

Implement Fast-Track Triage: Establish dedicated quick-turnaround protocols for critical and urgent cases.

Dynamic Doctor Reallocation: Adjust doctor shifts according to peak visit hours to balance patient load.

KPI Alignment: Tie department operational metrics to the target of seeing >50% of patients within 30 minutes.


📌 نبذة عن المشروع

تقدم لوحة المؤشرات هذه (Power BI Dashboard) تحليلاً شاملاً للكفاءة التشغيلية، وأزمنة انتظار المرضى، وجودة الفرز الطبي عبر 12 مستشفى. من خلال تحليل 1,000 زيارة مريض ومتابعة أداء 84 طبيباً، يهدف المشروع إلى تقديم مرئيات تساعد متخذي القرار في تحسين الطاقة الاستيعابية وتقليل فترات الانتظار.

📊 مؤشرات الأداء الرئيسية (KPIs)

إجمالي الزيارات: 1,000 زيارة

إجمالي المرضى: 286 مريضاً

إجمالي الأطباء: 84 طبيباً

إجمالي المستشفيات: 12 مستشفى

متوسط زمن الانتظار: 62.13 دقيقة

نسبة الاستقبال خلال 30 دقيقة: 23.50%

🛠️ نموذج البيانات ومعادلات DAX

تم بناء البيانات اعتماداً على نموذج النجمة (Star Schema) لربط جدول حركات الزيارات مع جداول أبعاد المستشفيات والأطباء والأقسام.

أهم معادلات DAX المستخدمة:

مقياس خط الهدف المرجعي (30 دقيقة):

خط مدة الانتظار (دقيقة) = 30


نسبة المرضى الذين تم استقبالهم خلال 30 دقيقة:

PercentWithin30 = 
VAR TotalVisitsCount = COUNT('جدول حركة الزيارات'[رقم الزيارة])
VAR SeenWithin30 = CALCULATE(
    COUNT('جدول حركة الزيارات'[رقم الزيارة]),
    'جدول حركة الزيارات'[مدة الانتظار (دقيقة)] <= 30
)
RETURN
DIVIDE(SeenWithin30, TotalVisitsCount, 0)


💡 الاستنتاجات والتوصيات الرئيسية

الاستنتاجات:

ارتفاع متوسط الانتظار: بلغ متوسط زمن الانتظار الإجمالي 62.13 دقيقة، وهو ما يتجاوز المعيار المستهدف (30 دقيقة).

انخفاض نسبة الاستقبال السريع: 23.50% فقط من المرضى يتم استقبالهم وخدمتهم خلال أول 30 دقيقة.

تباين الأداء: يوجد تباين واضح في أزمنة الانتظار بين المستشفيات والأقسام المختلفة (مثل قسم النساء والولادة مقارنة ببقية الأقسام).

التوصيات:

تطبيق نظام الفرز السريع (Fast-Track): تخصيص مسارات عاجلة للحالات الحرة لتسريع عملية الكشف والتوزيع.

إعادة توزيع الكوادر الطبية: تعديل جدول المناوبات للكوادر الطبية بناءً على ساعات الذروة وكثافة الزيارات.

ربط الأداء بالمؤشر الرئيسي: تحديد هدف تشغيلي برفع نسبة الاستقبال خلال 30 دقيقة لتتجاوز 50% مستقبلاً.
