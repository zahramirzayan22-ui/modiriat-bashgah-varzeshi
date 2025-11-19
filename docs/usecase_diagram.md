```mermaid
usecaseDiagram

actor Admin as "مدیر پروژه"
actor Member as "عضو تیم"

Admin --> (ایجاد تسک)
Admin --> (تخصیص تسک)
Admin --> (مشاهده گزارش پیشرفت)

Member --> (مشاهده تسک‌ها)
Member --> (به‌روزرسانی وضعیت تسک)
Member --> (افزودن یادداشت)
```