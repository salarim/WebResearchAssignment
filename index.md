<style type="text/css">
    @font-face {
        font-family: "custom";
        src: url("B Nazanin_p30download.com.ttf") format("truetype");
    }
    p { 
        font-family: "custom", sans-serif;
        font-size: large;
        color: #303030;
    }
</style>
<h2 dir="rtl">خلاصه:</h2>
<p dir="rtl">
    نشر محتوای بی طرف در اینترنت در زمان امروز کار سختی می باشد درننتیجه برای هر وب سایت افرادی وجود دارند که از آن متنفرند و میخواهند آنها را متوقف کنند. راحتترین راه برای این کار حمله ی DDoS می باشد. اساس این حملات ساده است. در اینترنت داده ها به صورت بسته هایی منتقل می شوند که شامل سرآیند و بدنه می باشند و در سرآیند آنها آدرس IP مبدا و مقصد آمده است. این اطلاعات را میتوان بدون محدودیت روی سیم قرار داد در نتیجه میتوان با دستکاری آدرس IP مبدا میتوان آن را جعل کرد. تنها راه توقف این کار فیلتر کردن بسته ها در نزدیکی مبدا می باشد و اینکار نیازمند سخت افزار میباشد. مطابق با پروژه spoofer.caida.org هنوز 27 درصد از ارائه دهندگان خدمات اینترنتی اجازه میدهند مشتریان جعل IP انجام دهند.
</p>
<p dir="rtl">
    به طور کلی سه دسته از ارتباطات به روتر ما وارد می شوند که هر کدام ممکن است مورد حمله قرار گیرند. دسته ی اول جفت شدن مستقیم می باشد که در آن کابل ها به طور مستقیم به یک موجودیت بزرگ اینترنت مثل گوگل یا آمازون متصل می شوند. درسته ی دوم مبادلات اینترنتی محلی می باشد که یک اجتماع محلی از ارائه دهندگان خدمات اینترنتی منطقه می باشد. و در آخر ارتباطاتی هستند که ما را به اینترنت متصل میکنند. در مورد اول دو طرف خواهان شناساتی مبدا حمله و حل مشکل هستند و ما میتوانیم مستقیما با آنها ارتباط برقرار کرده و سریعا مشکل را برطرف کنیم. در دو مورد بعدی شناسایی به سادگی نمی باشد و باید از ابزارهای دیگری استفاده کرد. برای حل مشکل جعل IP در دو حالت دیگر از netflow میتوان استفاده کرد. netflow پروتکل است که توسط بسیاری از روتر ها پشتیبانی می شود و به آنها اجازه می دهد که از ترافیک نمونه گیری کرده و آنها را به یک جای مرکزی بفرستد و در آنجا به شناسایی مبدا حمله پرداخته شود.
</p>
<h2 dir="rtl">تحلیل:</h2>
<p dir="rtl">
    اینترنتی که در حال حاضر در اختیار ماست به صورتی طراحی شده که به افراد درون شبکه اعتماد شده است درنتیجه این طراحی نمی تواند جلوی حملاتی از قبیل جعل IP را به طور کامل بگیرد. در این حملات از چند تکنیک میتوان استفاده کرد. برای مثلا میتوان درخواست هایی را با آدرس مبدا قربانی به یک سرور فرستاد که جواب آنها حجم بسیار بیشتری نسبت به حجم بسته درخواست دارند(مانند جستجوی DNS). در نتیجه پاسخی با حجمی چندین برابر درخواست اولیه به قربانی فرستاده می شود و باعث ناتوانی در ارائه خدمات شود. در روشی دیگر حمله کننده میتوان تعداد زیادی ربات در اختیار گرفته و با استفاده از آنها درخواست هایی را به قربانی بفرستد و باز قربانی دچار ناتوانی در ارائه خدماتش شود.
</p>
<p dir="rtl">
    حال برای شناسایی این نوع از حملات راه های مختلفی وجود دارد. برای مثال کابلی که از طریق آن دیتای حمله به ما ارسال می شود را بیابیم و اگر مستقیما به یک سازمانی مثل گوگل متصل است با آنها تماس گرفته و بگوییم مشکل را برطرف کنند. اما اگر داده های حمله از طریق شبکه داخلی ISP ما یا از شبکه خارجی اینترنت باشد کار به این سادگی نیست و ممکن است نتوان رد حمله کننده را گرفت. در اینجا ایده ای مطرح می شود که پروتکلی به نام netflow وجود دارد که میتوان آن را روی روتر های مختلف پیاده کرد و هزینه ی اندکی دارد. این پروتکل نمونه هایی از داده های درحال گذر از روتر را به یک جای مرکزی میفرستاد در نیتجه می توان در بخش هایی که این پروتکل پیاده شده اند داده ها را بررسی کرد و منشا حمله را مشخص نمود. درنتیجه در اینجا به جای تمرکز روی مسئله ی خاص جعل IP روی مسئله ای گسترده تر فکر کرده و پروتکی طراحی نمودیم که این نوع حمله را نیز بوسیله ی آن میتوان برطرف نمود.
</p>
