# Mermaid Code for Gym Management System Use Case Diagram
```mermaid
mermaid_code = """
graph TD
    %% Actors (بازیگران)
    actor_customer[-- مشتری --]
    actor_trainer[-- مربی --]
    actor_admin[-- مدیر --]

    %% System Boundary (محدوده سیستم)
    subgraph System_Gym_Management [سیستم مدیریت باشگاه]
        %% Customer Use Cases (موارد استفاده مشتری)
        UC1(ثبت نام/تمدید عضویت)
        UC2(رزرو کلاس/سرویس)
        UC3(مشاهده برنامه تمرینی)
        UC4(پرداخت هزینه)
        
        %% Trainer Use Cases (موارد استفاده مربی)
        UC5(مدیریت برنامه تمرینی اعضا)
        UC6(ثبت حضور و غیاب)
        UC7(مشاهده گزارش کار روزانه)
        
        %% Admin Use Cases (موارد استفاده مدیر)
        UC8(مدیریت اطلاعات اعضا)
        UC9(مدیریت کلاس‌ها و زمان‌بندی)
        UC10(گزارش‌گیری مالی و آماری)
        UC11(مدیریت کاربران سیستم)
    end

    %% Relationships (روابط)
    
    %% Customer Relationships
    actor_customer --> UC1
    actor_customer --> UC2
    actor_customer --> UC3
    actor_customer --> UC4
    
    %% Trainer Relationships
    actor_trainer --> UC5
    actor_trainer --> UC6
    actor_trainer --> UC7
    
    %% Admin Relationships
    actor_admin --> UC8
    actor_admin --> UC9
    actor_admin --> UC10
    actor_admin --> UC11
    
    %% Includes/Extends (مثال برای نمایش ارتباطات پیچیده تر)
    UC2 .> UC3 : <<include>> (مشاهده برنامه پیش‌نیاز است)

"""

print(mermaid_code)