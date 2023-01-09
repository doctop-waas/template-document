# راهنمای پیاده سازی قالب

برای پیاده سازی طرح لازمه که کد های هر بخش در فایل html و css با کامنت از یکدیگر جدا شده باشند

برای مثال به شکل زیر دقت کنید

![title](images/dr-roshani.png)

دو بخش هدر سایت و بیوگرافی پزشک دا در نظر بگرید. انتظار می رود کد های این صفحه به این شکل باید

```html
<!DOCTYPE html>
<html dir="rtl" lang="en">
  <head>
    <title>title</title>
  </head>
  <body>
    <!-- start header -->
    <div>
      <!-- header code -->
    </div>
    <!-- end header -->
    <!-- start biography -->
    <div>
      <!-- biography code -->
    </div>
    <!-- end biography -->
  </body>
</html>
‍
```

برای استایل دهی به سایت می توانید از ابزار های زیر استفاده کنید

- tailwindcss

در صورتی که از هیچ کدام از ابزار های بالا استفاده نکردین
برای استایل دهی نکات زیر را رعایت کنید

همچنین برای استایل ها هم به دو فایل css نیاز است
اولی برای استایل های خوده کاموپوننت ها
و دومی رنگ ها
به مثال زیر دقت کنید

```css
/* style that common in all components */
/* start common style */

.ali {
  display: flex;
}

/*  end common */

/* header start */
.header {
  background-color: red;
}
/* header end */

/* biography start */

.bio {
  background-color: red;
}

/* biography end  */

/*  */
```

_توجه شد حتما تمام طرج به صورت کاملا ریسپانسیو پیاده شود_

فایل color.css
نیز باید به شکل زیر باشد
این فایل الزامی است و باید حتما وجود داشته باشد

```css
:root {
  --primary-color: #33b9cb;
  /*  and define all color here */
}
```

---

### _استایل دهی فقط باید کاموننت ها انجام شود و از استایل دهی به تگ های بادی یا استایل کلی به همه تگ ها خودداری کنید_

    استایل های غیر مجاز

```css
li {
}

body {
}
```

از modern normilize هم میتونید
برای نرمال کردن صفحه استفاده کنید

https://cdn.jsdelivr.net/npm/modern-normalize/modern-normalize.min.css
https://github.com/sindresorhus/modern-normalize
