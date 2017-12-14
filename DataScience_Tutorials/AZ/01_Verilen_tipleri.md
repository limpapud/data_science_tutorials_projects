
# Verilənlər elmi: Verilənlər tipi

Verilənlər elminə baş vurma prossesi adından bəlli olan **verilənlər**-dən, daha dəqiq onların tipindən başlanmalı. Əsas verilənlər tipləri:

1. Rəqəm əsaslı
2. Kategoriya əsaslı

## Rəqəm əsaslı

Ayrı cür "**kəmiyyət**" tipli verilən adlanılır. Rəqəm ilə, *obyektiv* ölçə biləcəyimiz məlumatları əks etdirir (məsəl üçün: mağazadan alınmış çörək sayı və şəkər tozu, aldığınız əmək haqqı, bu məqalənin baxış sayı, sosial şəbəkədə yerləşdirdiyiniz şəkilinizin "layk" sayı, gündəlik 

Özü iki alt-tipə bölünə bilər:

### Diskret

Diskret rəqəmlər ədəd-ədəd saya biləcəyimiz verilənləri əks etdirən *nöqtədən sonra rəqəm olmayan* rəqəmlərdir. Yuxarıda qeyd olunmuş nümunələrdən mağazadan alınmış çörək sayı (yarım ya 1/4 çörək satılmır) ,bu məqalənin baxış sayı (məqaləyə 1519.89 dəfə baxmaq mümkün deyil) , sosial şəbəkədə yerləşdirdiyiniz şəkilinizin "layk" sayı (hələ ki feysbukda "yarım-layk" funksiyası istifadəyə verilməyib) bu tipə aiddir.


### Davamlı

Davamlı verilənlər ölçə biləcəyimiz nöqtədən sonra sonsuz rəqəm sayı saxlaya bilən rəqəmlərdir. Yuxarıda qeyd olunmuş nümunələrdən aldığınız əmək haqqı (maaşınız vergi və DSMF əməliyyatlarından sonra adətən "qəpiklər" ilə əks olunur - 1993.55 AZN) və mağazadan aldığımız 2.39 kilo şəkər tozu bu verilənlər alt-tipinə aiddir.

Analiz zamanı rəqəm əsaslı verilənlər üzərində orta dəyər, median, standart yayınma ölçüləri istifadə olunur.

#### Nümumə vizualizasiya:
![alt text](https://github.com/limpapud/data_science_tutorials_projects/blob/master/DataScience_Tutorials/AZ/assets/digit_01.png)
![alt text](https://github.com/limpapud/data_science_tutorials_projects/blob/master/DataScience_Tutorials/AZ/assets/digit_02.png)


## Kategoriya əsaslı

Bir-biri ilə müqaisəsi mümkün olmayan və ya çətin, kənar anlamlar vasitəsi ilə ölçülə və / və ya müqaisə oluna bilən verilən tipidir.
***Subyektiv*** olçülən, ayrı sözlə "keyfiyyət" ***təsvir edən*** verilən tipi.

### Sıra tipli

Özündə rəqəm tipli və kategoriya tipli verilənləri birləşdirən verilənlər alt-tipidir. Dəyər üzrə sıralamaq mümkün olduğundan və dəyərin sırada yeri vacib olduğundan "sıra" tipli adlandırılıb. Analiz prosessinin asanlaşdırılması məqsədi ilə ilkin məlumat işləməsində dəyərlərə sıra nömrələri verilir.

***Məsəl üçün:***
* Çox xoşbəxt (+2) ( / Xoşbəxt (+1) / Adi (0) / Bədbəxt (-1) / Çox bədbəxt (-2)

Gördüyünüz kimi *Adi* hal ilə *Çox xoşbəxt* arasında 2 xal fərq var, amma bu demək deyil ki eyni 2 xal *Xoşbəxt* və *Bədbəxt* arasında fərqə də aiddir, baxmayaraq ki bu iki hal arasında eynən 2 xal fərq qeyd olunub.
* 2-ci sinif / 3-cü sinif / 4-cü sinif / 5-ci sinif / 6-cı sinif

Sıralanması vacib olsa da *6-ci sinif* 3 *2-ci sinif* ilə əvəz oluna bilməz.

Analiz zamanı sıra alt-tipli verilənlər üzərində orta dəyər, nisbət, sıxlıq ölçüləri istifadə olunur.

#### Nümumə vizualizasiya:
![alt text](https://github.com/limpapud/data_science_tutorials_projects/blob/master/DataScience_Tutorials/AZ/assets/ordinal_01.png)

### Nominal tipli

Yuxarıda qeyd olunmuş "Sıra tipli" verilənlər tipindən fərqli olaraq Nominal tipli verilənləri mənası üzrə sıralamaq mümkün deyil. Əlavə olaraq bu alt-tip  üzərində riyazi əməliyyatlar da aparmaq olmaz.

***Məsəl üçün:***
* Rənglər: sarı, qırmızı, qara, sarı.

Sarı rəngin qırmızı rəngdən daha *böyük* və ya *daha vacib* olduğunu iddia edə bilmərik.

* Kitab adları.

Cozef Heller-in "22-ci hiylə" kitabının Erika Leonard-ın "Bozun əlli çaları" kitabından daha az məna kəsb etdiyinidə iddia etmək olmaz.

* Mobil nömrəniz

088 858 23 66 nömrəsinin 091 255 55 55 nömrəsindən *böyük* olduğunu demək olmaz. 

Əlbəttə ki rəngləri və kitabları adı üzrə əlifba üzrə sıralamaq mümkündür, göy rəngin çəhrayı rəngdən *gözəyatımlı* olduğunu, *091 255 55 55* nömrəsinin *088 858 23 66* mobil nömrəsindən *gözəl*, "22-ci hiylə"-nin Erika Leonardın erotik romanı ilə müqaisədə müqaisəolunmaz şedevr olduğunu qeyd edə bilərsiniz amma bu fikirlər ya sırf olaraq **subyektiv** xarakter daşıyacaq, ya da ki mənasız olacaq.

Analiz zamanı nominal alt-tipli verilənlər üzərində nisbət, sıxlıq ölçüləri istifadə olunur.
#### Nümumə vizualizasiya:
![alt text](https://github.com/limpapud/data_science_tutorials_projects/blob/master/DataScience_Tutorials/AZ/assets/nominal_01.PNG)



### Binar tipli

Adından bəlii olduğu kimi ("bi"-"iki") özündə iki, bir-birini təqzib edən seçimdən birini əks edir.

***Məsəl üçün:***

* Hə/Yox
* Getmək/Getməmək
* Yaxşı/Pis
* Düz/Səhv

Analiz zamanı binar alt-tipli verilənlər üzərində nisbət, sıxlıq ölçüləri istifadə olunur.

#### Nümumə vizualizasiya:
![alt text](https://github.com/limpapud/data_science_tutorials_projects/blob/master/DataScience_Tutorials/AZ/assets/boolean_01.PNG)

Deyək ki biz sorğu etmək qərarına gəldik, respondentlərdən ilkin məlumat və xoşbəxtlik statusunu öyrəndikdən sonra gördüyünüz cədvəl və qrafiklər ərsəyə gəldi. Nəticə olaraq yaradılmış cədvəl və verilən tipi üzrə bölgünü əlavə edirəm.

| id   | Ad                     | Yaş (tam)          | Boy (m)            | Cins                 | Sevimli rəng            | Xoşbəxtlik statusu     |
|------|------------------------|--------------------|--------------------|----------------------|-------------------------|------------------------|
| 1    | Ömər                   | 24                 | 1.93               | Kişi                 | Göy                     | Xoşbəxt                |
| 2    | Leyla                  | 27                 | 1.79               | Qadın                | Qırmızı                 | Adi                    |
| ---- | **Kategorik: nominal** | **Rəqəm: Diskret** | **Rəqəm: Davamlı** | **Kategorik: Binar** | **Kategorik: nominal**  | **Kategorik: ordinal** |

Beləliklə qısa məqalənin nəticəsi olaraq biz verilənləri klassifikasiya etməyi öyrəndik, və burada "Verilənlər tipləri" haqqında məqalə bitdi. Sual olduqda müəllif ilə əlaqə saxlaya, əlavələrinizi qeyd etmək istədikdə isə bu məqalənin "GitHub"-da yerləşən nüsxəsinə qeydlərinizi əlavə edə bilərsiniz.

### Əlaqə

Müəllif ilə əlaqə [![](https://www.shareicon.net/data/16x16/2015/11/02/665918_email_512x512.png)](mailto:omarbayramov@hotmail.com) **omarbayramov@hotmail.com** elektron ünvan üzərindən aparıla bilər.
Əlavə olaraq sosial şəbəkə və digər saytlara linklər əlavə olunur.

[Facebook![](https://www.shareicon.net/data/32x32/2016/06/20/606800_facebook_48x48.png)](https://www.facebook.com/Omar.X.Bayramov)
[Wordpress![](https://www.shareicon.net/data/32x32/2016/07/14/606997_wordpress_64x64.png)](https://omarbayramov.wordpress.com/) [LinkedIn![](https://www.shareicon.net/data/32x32/2016/06/20/606446_linkedin_48x48.png)](https://www.linkedin.com/in/omarbayramov/)
