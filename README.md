# Laravel-MohEssa

Mvc

model
ليس له علاقة بآلية العرض أبداً او تفاعل المستخدم معها
--------
مسؤول عن تخزين البيانات  سواء كانت بيانات قاعدة البيانات او اي بيانات مؤقته

ومعالجة تلك البيانات وتنفيذ العمليات اللازمة عليها
مثل الاستعلام والحذف والإضافة والتعديل

----------
الكونترولر

نعم، بالضبط! الكونترولر في نمط MVC يعمل كوسيط بين الموديل والفيو. يقوم الكونترولر بتلقي طلبات المستخدم من الفيو، ويتفاعل مع الموديل لاسترجاع أو تحديث البيانات حسب الحاجة، ثم يقوم بإرسال البيانات المحدثة إلى الفيو لعرضها للمستخدم. بالإضافة إلى ذلك، قد تكون للكونترولر مهام أخرى مثل تنسيق البيانات قبل عرضها للمستخدم، أو إجراء العمليات اللازمة لمعالجة الطلبات المستلمة، مثل التحقق من صحة البيانات المُدخلة من قبل المستخدم ومعالجة الأخطاء.

____________

routing : تصنع الروابط

-------------------------------------
Route::get('/greeting', function () {
    return 'Hello World';

    هذه تعتبر
    callback function
    لأنني اول ما ادخل لهذا المسار
    /greeting
    اوتوماتيكياً سيتم استدعاء الفنكشن

--------------------------
لارجاع صفحة
view
---------------
    Route::view('/welcome2', 'welcome2'); استخدمنا فيو مباشرة


    Route::get('/welcome3', function(){استخدمنا غيت  وكملنا زي ديماً
return view ("welcome2");
    });

كل و
احد منهم اله استخداماته


استخدم Route::view عندما:

تريد ربط مسار URL بملف عرض بسيط.
لا تحتاج إلى معالجة أي بيانات أو تنفيذ أي منطق قبل عرض العرض.
تريد الحفاظ على كودك سهل القراءة.
استخدم Route::get عندما:

تحتاج إلى معالجة البيانات أو تنفيذ منطق قبل عرض العرض.
تريد المزيد من التحكم في سلوك المسار.
تحتاج إلى استخدام وظيفة تحكم للقيام بمهام أخرى.


-------------------------------------------------------
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
</head>
<body>
<h1> html <h1>
<h1> phpNative  <?php echo $name;?>        </h1>
<h2>{{$name}}</h2>


</body>
</html>


لاجظ ان ال
blade
.engine
يحتوى على صفحة
html5
عادية
وبداخلها كل من
phpNative
و
html
و
{{}}
------------------------------------------------
Route::get("/user/{id}",function(string $id){
return $id;
});

طريقة للسترينغات مع الراوتر

------------------------------------------------------------
Route::get('/user/{name?}', function (?string $name = 'John') {
    return $name;
});

اذا حطينا الاسم بينطبع واذا لا بينطبعjohn


