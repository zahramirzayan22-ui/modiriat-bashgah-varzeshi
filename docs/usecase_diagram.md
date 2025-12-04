```maread

%% 🎭 بازیگران
Member([🏋️‍♂️ عضو باشگاه])
Trainer([🧑‍🏫 مربی])
Admin([👤 مدیر])
System([💻 سیستم پرداخت آنلاین])

%% 🧩 موارد استفاده اصلی (Use Cases)
UC1([ثبت‌نام عضویت])
UC2([رزرو جلسه تمرینی])
UC3([درخواست استفاده از امکانات])
UC4([مشاهده سوابق تمرینی])
UC5([تأیید درخواست‌ها])
UC6([مدیریت پرداخت‌ها])
UC7([مدیریت اعضا])
UC8([مدیریت مربیان و برنامه‌ها])

%% 🔹 جزئیات مربوط به عضو
UC1a([انتخاب نوع عضویت])
UC1b([تکمیل اطلاعات شخصی])
UC1c([پرداخت هزینه عضویت])
UC2a([انتخاب مربی])
UC2b([انتخاب تاریخ و ساعت])
UC3a([درخواست استفاده از سونا یا استخر])
UC3b([درخواست استفاده از تجهیزات خاص])
UC4a([مشاهده نمودار پیشرفت])
UC4b([دریافت برنامه تمرینی جدید])

%% 🔸 جزئیات مربوط به مربی
UC5a([بررسی درخواست رزرو])
UC5b([تأیید یا رد بر اساس ظرفیت])
UC5c([ارسال پیام به عضو])
UC8a([تنظیم برنامه‌های تمرینی])
UC8b([ارزیابی عملکرد اعضا])

%% ⚙️ جزئیات مربوط به مدیر
UC6a([بررسی تراکنش‌ها])
UC6b([گزارش مالی ماهانه])
UC7a([افزودن یا حذف اعضا])
UC7b([مدیریت تمدید عضویت])
UC8c([تنظیم ساعات کاری مربیان])
UC8d([مدیریت تجهیزات ورزشی])

%% 💳 ارتباط با سیستم پرداخت
UC1c --> System
UC6a --> System

%% ارتباطات بین بازیگران و موارد استفاده
Member --> UC1 --> UC1a & UC1b & UC1c
Member --> UC2 --> UC2a & UC2b
Member --> UC3 --> UC3a & UC3b
Member --> UC4 --> UC4a & UC4b
Trainer --> UC5 --> UC5a & UC5b & UC5c
Trainer --> UC8 --> UC8a & UC8b
Admin --> UC6 --> UC6a & UC6b
Admin --> UC7 --> UC7a & UC7b
Admin --> UC8 --> UC8c & UC8d

%% 🎨 ظاهر Use Case‌ها (صورتی)
style UC1 fill:#FFB6C1,stroke:#333,stroke-width:2px
style UC2 fill:#FFB6C1,stroke:#333,stroke-width:2px
style UC3 fill:#FFB6C1,stroke:#333,stroke-width:2px
style UC4 fill:#FFB6C1,stroke:#333,stroke-width:2px
style UC5 fill:#FFB6C1,stroke:#333,stroke-width:2px
style UC6 fill:#FFB6C1,stroke:#333,stroke-width:2px
style UC7 fill:#FFB6C1,stroke:#333,stroke-width:2px
style UC8 fill:#FFB6C1,stroke:#333,stroke-width:2px

%% ظاهر زیرمجموعه‌ها (صورتی روشن‌تر)
style UC1a fill:#FFD7E2,stroke:#666
style UC1b fill:#FFD7E2,stroke:#666
style UC1c fill:#FFD7E2,stroke:#666
style UC2a fill:#FFD7E2,stroke:#666
style UC2b fill:#FFD7E2,stroke:#666
style UC3a fill:#FFD7E2,stroke:#666
style UC3b fill:#FFD7E2,stroke:#666
style UC4a fill:#FFD7E2,stroke:#666
style UC4b fill:#FFD7E2,stroke:#666
style UC5a fill:#FFD7E2,stroke:#666
style UC5b fill:#FFD7E2,stroke:#666
style UC5c fill:#FFD7E2,stroke:#666
style UC6a fill:#FFD7E2,stroke:#666
style UC6b fill:#FFD7E2,stroke:#666
style UC7a fill:#FFD7E2,stroke:#666
style UC7b fill:#FFD7E2,stroke:#666
style UC8a fill:#FFD7E2,stroke:#666
style UC8b fill:#FFD7E2,stroke:#666
style UC8c fill:#FFD7E2,stroke:#666
style UC8d fill:#FFD7E2,stroke:#666

%% ظاهر سیستم پرداخت
style System fill:#D1C4E9,stroke:#333,stroke-width:2px
```
