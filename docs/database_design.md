جدول users

| ستون | نوع | توضیح |
|------|------|--------|
| id | int | کلید اصلی |
| name | varchar | نام کاربر |
| email | varchar | ایمیل |
| role | enum | نقش (admin / member) |

 جدول tasks
| ستون | نوع | توضیح |
|------|------|--------|
| id | int | کلید اصلی |
| title | varchar | عنوان تسک |
| description | text | توضیحات |
| status | enum | وضعیت (todo, doing, done) |
| deadline | date | مهلت |
| user_id | int | مالک تسک |