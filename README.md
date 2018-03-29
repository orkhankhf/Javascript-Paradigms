# Javascript-Paradigms (21.11.2017)
### İzah Etməyim Tələb Olunan Mövzular.

⦁	Javascript hansi paradigmalara sahib bir dildir?

⦁	Interpreter diller ve compiler diller arasindaki ferqler nelerdir?

⦁	Javascript deyisen nedir?

⦁	Nece cur deyisen teyin etme usulu var?

⦁	Javascript data tipleri hansilardir? (izahatini verin)

⦁	Data tipleri niye var?

⦁	Funksiya nedir?

⦁	Nece cur funksiya teyin ede bilerik? Aralarindaki ferqler nelerdir?

Yuxarıda qeyd edilən suallara cavab verilməlidir.


## Mənim mövzulara ətraflı izahatım.

1. Javascript multi paradigmalı bir dildir. Javascriptin paradigmaları OOP, İmperative, Functional və event-driven'dir.

2. Interpreter (Tərcüməçi və ya yorumlayıcı) və compiler (kompilyator) dillər arasındakı ən böyük fərq, compiler dillərin yorumlayıcı dillərə nəzərən daha sürətli olmasıdır. Buna səbəb interpreter dillərin kodu yuxarıdan aşağı oxuyub tək tək hər sətiri icra etməsidir. İnterpreter dillər xətalarıda tək tək göstərir çünkü bir sətirdəki əmri oxuyub icra etməmiş alt sətirə keçmir. Compiler dillər isə bütün program kodlarını oxuyur və ən sonda ümumi xətaları çıxarır yoxdursa işləməyə davam edir.

3. Dəyişənlər müəyyən və ya bir neçə məlumat və ya dəyərləri, dilin syntax'ına zidd olmadan istədiyimiz adı verərək, bir növ məlumatı daha asan və əl çatan eyni zamanda da funksiyonal şəkildə istifadə etməyimizi təmin edən qutudur.

4. Javascriptdə dəyişənləri aşağıdakılar kimi 3 cür təyin edə bilərik.

```
	var a;
	var a = 5;
	var a = 5, b=6, c=7;
```

5. JS'da bir neçə data tipi mövcuddur. Text datalarını stringdə, hesablama aparacağımız rəqəmləri numberdə, doğru və yalnış dəyərlərini (if else üçün) alacağımız dataları boleanda, bir neçə dəyəri tək datada saxlayırıqsa (ad, soyad, yaş və s.) objectdə və ya arrayda saxlayırıq. Əlavə olaraqda null var.

6. Mən bu sual ilə bağlı sadəcə 2 data tipini misal gətirəcəm. Çox bəsit bir örnək verim fikrimi izah edə bilmək üçün. İki dəyişən təyin etmişik və dəyərinə "5" və ya 5 yazmışıq elə mi? əgər data tipləri yəni string number anlayışı olmasaydı dırnaq içində və ya dırnaqsız yazdığımız dəyərlərin hər ikisi üzərində eyni əməliyyat aparılacaqdı. Belə olan halda var a = "5"; var b=6; yazaraq dəyişənlərimizi təyin etdikdən sonra nəticəni görmək üçün  console.log(a+b) yazsaydıq ekrana 56 və ya 11 çıxardı. Haydi bunu geçtim hocam, bəs yaxşı programa harada 5 və 6 rəqəmini yanaşı gətirib ekrana 56 və harda 5 rəqəminə 6 rəqəmini toplamasını yəni ekrana 11 rəqəmini çıxarmasını necə izah edə bilərdik? Məhz buna görədə string və number olaraq ayrılır ki, harada yanına gətirərək 56 harada isə toplama əməliyyatı apararaq 11 rəqəmini yazdığını bilsin programımız.

7. Function müəyyən əmrləri sırası ilə və bir neçə yerdə təkrarlamağa, argumentlər sayəsində müxtəlif dəyərlərlə eyni əmrləri icra edib fərqli nəticələri görməyimizi təmin edir (Function overloading).

8. 5 cür function təyin etmək olar. Əlavələriniz varsa zəhmət olmasa mütləq bildirin çünkü bu mənə görə önəmli bir mövzudur və istifadəsi bir çox yerdə yalnış olduqda bəzən kodumun düzgün metodla yazılmamasına səbəb ola bilər ona görə biraz geniş araşdırmaq istəyirəm bu mövzunu.
```
     function myFunction(a, b) {
         return a * b;
     }

     var x = function (a, b) {return a * b};

     var myFunction = new Function("a", "b", "return a * b");

     (function () {
         var x = "Hello!!";      // I will invoke myself
     })();
```
