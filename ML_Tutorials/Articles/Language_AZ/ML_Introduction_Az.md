
# Maşın öyrənməsi və alqoritmlər: MÖ ilə tanışlıq

Bu “Maşın öyrənməsi və alqoritmlər” məqalələr seriyasında hal-hazırda perspektiv, sürətlə inkişaf edən amma Azərbaycanda çox da yayılmamış sahə olan maşın öyrənməsi və onun ən populyar və istifadə olunan alqoritmləri haqqında bəhs edəcəm.
Oxuduğunuz məqalə seriyada ilk olduğundan tanışlıq tiplidir və ümumiləşdirilmiş məlumat üzərində qurulub.

Maşın öyrənməsini 3 tipə bölünür:
* Müəllim ilə öyrənmə
* Müəllimsiz öyrənmə
* Möhkəmlətmə ilə öyrənmə

## Müəllimli öyrənmə

![ML_1_1.png](https://github.com/limpapud/data_science_tutorials_projects/blob/master/ML_Tutorials/Articles/Language_AZ/assets/ML_1_1.png)


**Müəllimli öyrənmə**nin əsas məqsədi artıq malik olduğumuz tarixi  *“yarlığlı”* (yəni adı və mənası məlum) verilənlər vasitəsi ilə gələcəkdə rast gəlinən verilənlər üzərində reqressiya və ya klassifikasiya apararaq prognozlar verməkdir.
Bu halda “müəllim” halında **giriş**də verilmiş məlumat və onun **çıxış**da olan nəticəsi çıxış edir,və artıq məlum məlumat əsasında problemə uyğun maşın öyrənməsi alqoritmi vasitəsi ilə funksiya yaradaraq  gələcək məlumat üçün proqnoz yaradır. ***Bir sözlə bu öyrmənmənin məqsədi "prognozlaşdırma"-dır.***

2 üsula bölünür:

***Klassifikasiya üsulu***

Axtardığımız cavab bir neçə cavab arasında yerləşirsə (məsəl üçün:*"Bəli"/"Yox"; "Kredit vermək"/"İmtina etmək"/"Zamin tələb etmək"*) o zaman klassifikasya tipli alqoritmlərdən istifadə etməyimiz məqsədəuyğundur. 
Ən məhşur və etalon klassifikasiyası məsəllərindən biri İris gülü məsələsidir: Bu problemdə 150 İris gülünün artıq ölçülmuş ləcək və sap əndazələrindən aslı olaraq yeni gördüyümüz İris gülü tipinin hansına aid olmasının tapılmasına imkan verir (ya hər halda tipinin proqnozlaşdırmasına). Bunun üçün adın bilmək istədiyimiz gülün ləçəkləri və sapı ölçülür və klassifikasiya alqoritmi vasitəsi ilə işləndikdən sonra nəticə olaraq alqoritm tip üzrə proqnozu verir

Alqoritmlər:

* Logistik reqressiya
* Klassifikasiya ağacı
* Təsadüfi meşə
* "SVM"
* Naive Bayes


***Reqressiya üsulu***

Reqressiya üsulu davamlı və rəqəm tipi ədədləri tapmaq üçün istiqamətlənib (*Məsəl üçün: "4"; "3426567.23", "121.5" və sair*). 
Məsəl olaraq mənzil qiyməti araşdırması çıxış edə bilər: əgər əlinizdə deyək 100 000 ev satışı elanı varsa və siz onun əsasında şəhərin müxtəlif hissələrində yerləşən 1000 evi qiymətləndirmək istəyirsinizdə o zaman reqressiya tipli alqoritmlərdən istifadə edə bilərsiniz. Bunun üçün əldə olan verilənlərin hər birin rəqəmləşdirmək,kategoriyalaşdırmaq və modelə daxil etmək lazımdır. Yaranacaq funksiya əsasında siz sadəcə mənzil haqqında məlumatı qeyd etməklə bazar qiymətini öyrənə bilərsiniz.

Alqoritmlər:

* Xətti reqressiya
* "Lasso" regressiyası
* AdaBoost
* Gradient gücləndirmə

## Müəllimsiz öyrənmə
![ML_1_2.png](https://github.com/limpapud/data_science_tutorials_projects/blob/master/ML_Tutorials/Articles/Language_AZ/assets/ML_1_2.png)

Müəllimli öyrənmədən fərqli olaraq Müəllimsiz öyrənmədə verilənlərin başlıqları və axtardığımız nəticə olmur. Bu yolun əsəs məqsədi malik olduğumuz məlumatı maksimal olaraq strukturlaşdırıb, gruplaşdırıb əsasında verilənlərin bizə "nə danışdığını" göz önünə gətirməkdir. Bu deməkdir ki əslində bu tip öyrənmədədə müəllim var amma bu rolu kompyuter yeninə yetirir. İstifadə misalı? Hansı məhsulların və xidmətlətin bir yerdə alındığını analiz edib malların mağazada yerləşməsinə və email vasitəsi ilə yalnız müşəri üçün aktual və lazımlı təklifləri vermək.
Əlavə olaraq qeyd etmək lazımdır ki müəllimsiz öyrənmə anomal halların tapılması üçün alqoritmlər də istifadə olunur.***Yəni bu öyrənmənin məqsədi *** **təsvir etməkdir və gizli bağlılığları tapmaqdır.**.

Əsas 2 üsula bölünür:

***Klasterizasiya üsulu***

Üsulun əsas məqsədi verilənlər əsasında qrafikdə noqtələri çizib qruplaşdırıb və oxşar cəhətlər ilə bölüşən,yaxınlıqda yerləşən nöqtələr ilə  *klasterlərə* yerləşdirməkdir. Beləliklə alqoritm sonrası cavab araşdırması vizual olaraq aparılır və yuxarıda yerləşən şəkildə göstərilib. Yuxarıda qeyd olunan "klasssifikasiya" üsuluna oxşasada əvvəlcədən başlıqları bilmədiyimizdən tam olaraq ayrı üsul və öyrənmə tipinə aid edilir. 

Alqorimtlər: 

* k-ortalama üzrə klasterizasiya
* Neyron şəbəkəsi
* DBSCAN


***Assosiasiya üsulu*** (a.k.a Şablon (naxış) tapılması)

Adından bəlli olduğu kimi üsul mövcud yarlıqsız məlumatda aslılıq və oxşarlıqları axtarır və nədən yarandığını aydınlaşdırmağa imkan yaradır. Məsəl üçün: Müştəri supermarketin İçki zalından şampan, Şiriniyyat zalından şokolad və Gül zalından 3 qızıl gül alsa da supermarket nəznində fəaliyyət göstərən Aptekdən lazimi məhsul almağa xəsislik etdisə o zaman bu seçim bundan 9 ay sonra pampers və uşağ geyimi alması tam olaraq anlaşılandır.

Alqorimtlər: 

* Assosiasiya qaydaları
* Apriori

## Möhkəmlətmə ilə öyrənmə
Bu öyrənmə tipində ***agent, ətraf mühit*** ilə qarşılıqlı əlaqə nəticəsində seçimlər və hərəkətlər yerinə yetirir və bunun qarşılığında əks siqnallar alır. Alınmış siqnal əsasında *agent* yeni seçimlər edir və proses yenidən başlanır. Beləliklə bu öyrənməni də bir baxımdan "müəllim ilə öyrənmə" saymaq olsa da fərqlidir, fərqi isə burada 1 müəllim və 1 şaqird yox, 2 müəllimin bir-birini öyrətməsi və təkminləşdirməsidir. Məsəl olaraq şahmat oyunu  - hər bir şahmat addımdan sonra hər iki oyunçu (*agent*) üçün vəziyyət (*mühit*) dəyişir. Indi isə təsəvvür edin ki kompyuter sizin addımınızdan aslı olaraq hər bir mümkün cavab addım və ondan sonra mümkün nəticəni qabağcadan sayır və öz şahmat figurunu və pozisiyasın ona əsasən yerləşdirir. Bax belə "Deep Blue" 1997-ci ildə şahmat üzrə dünya çempionuna qalib gəldi.
![ML_1_3.png](https://github.com/limpapud/data_science_tutorials_projects/blob/master/ML_Tutorials/Articles/Language_AZ/assets/ML_1_3.png)

Mövcud üsullar:
1. Klassifikasiya
2. Kontrol

Bu növ öyrənmə özünuidarəedən maşın və özünü öyrədən robot misallarında özünü göstərə bilər. Maşın idarəolunan zaman maşın tıxac, saysız digər maşın və piyadalar ilə təmasda olur və  hər bir saniyədə baş verə biləcək gözlənilməz hadisələr izləyir. Bu haqqda hətta "özünü idarədən maşın" fəlsəfi etikası mövcuddur. Orada qəza zamanı yalnız 2 çıxış olduqda və hər iki çıxış insan ölümünə gətirə biləcəyi halda kimin öləcəyini maşın qərar verdiyindən nə necə verdiyindən bəhs edir.


Alqoritmlər:

* Q-Öyrənmə
* Temporal Difference
* Dərin rəqib tipli şəbəkə

Beləliklə burada MÖ ilə tanışlıq bitir. Növbəti məqalələrdə alqoritmlərin açıqlanması və nümaişi planlaşdırılır. Sual/təklif olduqda şərh yaza, səhv/"GitHub"-da repozitoriyada yerləşən bu məqaləni dəyişə bilərsiniz. Və əlbəttə ki həmişə **omarbayramov@hotmail.com** ünvanına yaza bilərsiniz.
