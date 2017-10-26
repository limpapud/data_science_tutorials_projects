
# Maşın öyrənməsi və alqoritmlər: Sadə(löv) Bayes alqoritmi (1 hissə)

Bu məqalədə müzakirə mövzusu sadə Bayes alqoritmi olacaq. İlkin olaraq alqoritmin rezyumesinə baxaq:

* Adı: Sadə Bayes alqoritmi
* Tipi:Ehtimalı generativ Klassifikator
* Növ: Müəllim ilə öyrənmə
* İstifadə sahəsi: Mətn və sənəd klassifikasiyası, multi-kategoriya klassifikasiyası, tibb diaqnozların qoyulması
* Iş üçün resept: böyük həcmli bir birindən aslı olmayan verilənlər, iki və ya bir neçə klass üzrə klassifikasiya problemi və qısa vaxt çərçivələri, zəif hesablama resursları olduqda,xüsusiyyət sayı çox amma verilən həcmi kiçik olanda

### Tarixçə:

Sadə Bayes klassifikatoru Bayes klassifikatorlarından birindir və sadə (və ya sadəlöv) adlandırılmasının səbəbi alqotmin girişinə verilən məlumat yığımın bir biridən müstəqil olduğu, yəni prognozlaşdırıcı ədədlər bir biri ilə koorelyasiyada olmadığını saymasıdır, amma əlbəttə ki bu həmişə belə olmur və çox bir halda verilənlər bilavasitə və ya dolayı yolla bir biri ilə əlaqədər olur. Məsəl üçün adamın boyu onun çəkisi ilə əlaqədardır, amma SBK işləmə zamanı onların bir birindən ümumiyyətlə aslı olmadığı "fikirləşəcək".

Sadəlöv Bayes klassifikatoru haqqında danışmaqdan əvvəl SBK əsasında dayanan Bayes Teoremi və üzərində praktik problemdən başlayaq. Teorem 18-ci əsrdə Tomas Bayes tərəfindən inkişaf edilmişdir, amma həyatı zamanı Thomas ixtirasınına fikir vermədiyindən (o fikirləşirdi ki teorem məntiqidir və bu cür əhəmiyyətsiz fikir nəticəsin rəsmən dərc etməyə ehtiyac yoxdur). Teorem yalnız onun ölümündən sonra dostu Prays tərəfindən geniş ictimayyətə təqdim olunmuşdur. Təqdim edəcəyim problem isə mənim ilə bu gün baş vermişdir:

Mənim Əhməd adlı tanışım var və 5 ay əvvəl onunla danışanda o mənə demişdi ki onun yaxın bir-iki ay ərzində işlədiyi xoldinqdə yeni vəzifəyə keçmə şansı 70% təşkil edir və əgər bu baş versə o 80% əmindir ki maliyyə vəziyyəti yaxşılaşdığı səbəbindən özünə yeni maşın alacaq, keçid alınmadığı təqdirdə isə 30% ehtimal ilə maşın alacağını planlaşdırır.  Dünən mən avtobusla işə gedəndə onu avtobus pəncərəsindən yeni Range Rover Sport sürən gördüm və sual ilə daldım: ~~mənim niyə belə maşınım yoxdur?~~ O yeni vəzifəyə keçdi mi?

Elə bu cür suallara cavab vermək üçün bizə Bayes formulası lazım olur. Bayes formulasının mənası ehtimalı yeni daxil olmuş məlumat üzərində yeniləməkdir. Suala cavab vermək üçün vizual ehtimal ağacından istifadə edək:

![ML_2_1.png](https://github.com/limpapud/data_science_tutorials_projects/blob/master/ML_Tutorials/Articles/Language_AZ/assets/ML_2_1.png)

Bizdə olan məlumat, artıq baş vermiş maşın alışı faktı üzərində əsaslanır, lazım olan ondan əvvəl baş vermiş vəzifə statusunun yenilənməsinin ehtimalın tapmaqdır. Bunun üçün ehtimal ağacı budağların kodlaşdıraq və faizləri rəqəmə keçirək.!
![ML_2_2.png](https://github.com/limpapud/data_science_tutorials_projects/blob/master/ML_Tutorials/Articles/Language_AZ/assets/ML_2_2.png)

Budaqlara kod hərfləri verdikdən sonra formula üzərinə keçək:

![ML_2_3.png](https://github.com/limpapud/data_science_tutorials_projects/blob/master/ML_Tutorials/Articles/Language_AZ/assets/ML_2_3.png)

Əgər formulanı Azərbaycan dilinə tərcümə etsək:

![ML_2_4.png](https://github.com/limpapud/data_science_tutorials_projects/blob/master/ML_Tutorials/Articles/Language_AZ/assets/ML_2_4.png)

Nəhayət bildiyimiz ehtimal faizlərini işə salaq:

![ML_2_5.png](https://github.com/limpapud/data_science_tutorials_projects/blob/master/ML_Tutorials/Articles/Language_AZ/assets/ML_2_5.png)

Cavabı tapdıq və o 86.1% bərabırdir amma tam anlam üçün ağaca və klasslara yenə nəzər yetirək:

![ML_2_6.png](https://github.com/limpapud/data_science_tutorials_projects/blob/master/ML_Tutorials/Articles/Language_AZ/assets/ML_2_6.png)

Beləliklə Bayes teoremi köməkliyi ilə mən 86.1% əminliklə zəng edib yeni vəzifə və yeni maşın münasibəti ilə dostumu təbrik edə bilərəm.

## SBK tipləri:
* Multinomial modeli (aşağıda qeyd olunmuş misalda istifadə olunur)

Verilənlərin hədəf klass sayı ikidən çox olanda  Binomial modeldən fərqli olaraq ədədin ehtimalının olub/olmaması ilə yox, nə qədər  təkrarlandığı haqqında xəbər verir. Formulada gördüyünüz "α" yeni verilən məlumat üzərində ehtimal hesablaması aparan zaman test verilənlər içərisində qarşılaşmadığımız ədədlər üçün ehtimal hesablayarkən klas ehtimalın sıfıra bərabər olmaması üçün "α>1"(Laplas üzrə) və ya "α<1" (Lindston üzrə) bərabər olur.

![ML_2_7.png](https://github.com/limpapud/data_science_tutorials_projects/blob/master/ML_Tutorials/Articles/Language_AZ/assets/ML_2_7.png)


* Gaus modeli

![ML_2_8.png](https://github.com/limpapud/data_science_tutorials_projects/blob/master/ML_Tutorials/Articles/Language_AZ/assets/ML_2_8.png)

Müxtəlif klas üzrə klassifikasiya üçün daha uyğundur.  Verilmiş xüsusiyyət davamlı ehtimalların mərkəzdən eyni uzaqlığda yerləşdiyini və simmetrik olduğunu fərziyyə edir. (68% məlumat mərkəzdən 1 standart paylama, 95% - 2 və 99.7%- 3 standart paylamada yerləşir).

* Binomial modeli

![ML_2_9.png](https://github.com/limpapud/data_science_tutorials_projects/blob/master/ML_Tutorials/Articles/Language_AZ/assets/ML_2_9.png)

 Adından bəlli olduğu kimi verilənlərin hədəf klass sayı ikiyə bərabər olanda ( "Hə"/"Yox", "True"/"False") yəni binar oldğuğu halda özünü daha yaxşı göstərir. Mətn klassifikasiyasında Multinomial model ilə bir istifadə olunur.

## Sadəlöv Bayes klassifikatoru ilə mətn analizi
Mənim son MÖ ilə bağlı məqaləm qısa bir zaman ərzində kifayət qədər baxış yığıb. Məqaləmdəmdən həm xoşu gələn, həm də narazı insanlar da olub. Aşağıda qeyd olunmuş cədvəldə mənə yazılan son 12 şərhi təqdim edirəm.

| Mətn                                       | Klas   |
|--------------------------------------------|--------|
| Məqalənizə görə çox sağolun, marağlı oldu. | Müsbət |
| Marağlı mövzudur, lazimi mövzudur          | Müsbət |
| Çox sağolun, uğurlar.                      | Müsbət |
| Xoşuma gəlmədi, marağsız oldu              | Mənfi  |
| Çox pis məqalə oldu                        | Mənfi  |
| Məqalə pis oldu                            | Mənfi  |
| Məqalə marağlı yazılıb                     | Müsbət |
| Marağlı olmadı,  marağsız oldu             | Mənfi  |
| Yaxşı mövzuya toxundunuz                   | Müsbət |
| Məqalənizə yaxşı demək olar                | Müsbət |
| Əhsən!                                     | Müsbət |
| Sağolun xoşuma gəldi                       | Müsbət |

Gördüyümüz kimi 12 şərh yazan oxuyucudan şəkkizi məqaləm haqqında "müsbət", dördü isə "mənfi" fikir bildirib. Mən məqalələrdə səhvlərin və ya çatışmamazlıqların olduğunu nəzərə aldığımdan və kritikanı yalnız inkişaf etmə üsulu qəbul etdiyimdən üzülmürəm, əksinə yeni SBK başa salmaq üçün istifadə edirəm.

İlk öncə vektorlaşdırma aparaq. Bunun üçün bütün sözləri **təkrarlanmadan** ard-arda yazaq və şərhdə sözlər üzrə qarşılaşma sayın qeyd edək.

| Məqalənizə | görə | çox | sağolun | marağlı | oldu | mövzudur | lazimi | uğurlar | xoşuma | gəlmədi | marağsız | pis | məqalə | yazılıb | yaxşı | mövzuya | toxundunuz | demək | olar | əhsən | gəldi | Klass |          |
|------------|------|-----|---------|---------|------|----------|--------|---------|--------|---------|----------|-----|--------|---------|-------|---------|------------|-------|------|-------|-------|-------|----------|
| 1          | 1    | 1   | 1       | 1       | 1    | 1        |        |         |        |         |          |     |        |         |       |         |            |       |      |       |       |       | Positive |
| 2          |      |     |         |         | 1    |          | **2**      | 1       |        |         |          |     |        |         |       |         |            |       |      |       |       |       | Positive |
| 3          |      |     | 1       | 1       |      |          |        |         | 1      |         |          |     |        |         |       |         |            |       |      |       |       |       | Positive |
| 4          |      |     |         |         |      | 1        |        |         |        | 1       | 1        | 1   |        |         |       |         |            |       |      |       |       |       | Negative |
| 5          |      |     | 1       |         |      | 1        |        |         |        |         |          |     | 1      | 1       |       |         |            |       |      |       |       |       | Negative |
| 6          |      |     |         |         |      | 1        |        |         |        |         |          |     | 1      | 1       |       |         |            |       |      |       |       |       | Negative |
| 7          |      |     |         |         | 1    |          |        |         |        |         |          |     |        | 1       | 1     |         |            |       |      |       |       |       | Positive |
| 8          |      |     |         |         | 1    | 1        |        |         |        |         | 1        | 1   |        |         |       |         |            |       |      |       |       |       | Negative |
| 9          |      |     |         |         |      |          |        |         |        |         |          |     |        |         |       | 1       | 1          | 1     |      |       |       |       | Positive |
| 10         | 1    |     |         |         |      |          |        |         |        |         |          |     |        |         |       | 1       |            |       | 1    | 1     |       |       | Positive |
| 11         |      |     |         |         |      |          |        |         |        |         |          |     |        |         |       |         |            |       |      |       | 1     |       | Positive |
| 12         |      |     |         | 1       |      |          |        |         |        | 1       |          |     |        |         |       |         |            |       |      |       |       | 1     | Positive |

Ümumi baxış edək:

* Unikal söz sayı - 23
* Müsbət söz sayı- 27
    * Orijinal söz sayı - 18
* Mənfi söz sayı- 15
    * Orijinal söz sayı - 8
* Ethimal (Pozitiv şərh) - 8/12 = 0.66(66)
* Ehtimal (Negativ şərh) - 4/12 = 0.33(33)

Multinomial modeldən istifadə edək (yaddan çıxarmayaq ki "+1" Laplas sakitləşməsi və qarşılaşmadığımız sözlərin ehtimalı sıfırlamaması üçündür):

![ML_2_10.png](https://github.com/limpapud/data_science_tutorials_projects/blob/master/ML_Tutorials/Articles/Language_AZ/assets/ML_2_10.png)

Pozitiv şərhləri ayıraq və siyahısın tərtib edək:

|      |            |             |            |             |             |             |            |             |             |             |             |             |             |             |             |            |             |             |             |             |             |             |             |
|---------|------------|-------------|------------|-------------|-------------|-------------|------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|
| **Söz**     | Məqalənizə | görə        | çox        | sağolun     | marağlı     | oldu        | mövzudur   | lazimi      | uğurlar     | xoşuma      | gəlmədi     | marağsız    | pis         | məqalə      | yazılıb     | yaxşı      | mövzuya     | toxundunuz  | demək       | olar        | əhsən       | gəldi       | Klass       |
| **Say  **   | 3          | 2           | 3          | 4           | 4           | 2           | 3          | 2           | 2           | 2           | 1           | 1           | 1           | 2           | 2           | 3          | 2           | 2           | 2           | 2           | 2           | 2           | 1           |
| **Ehtimal **| 0,06122449 | 0,040816327 | 0,06122449 | 0,081632653 | 0,081632653 | 0,040816327 | 0,06122449 | 0,040816327 | 0,040816327 | 0,040816327 | 0,020408163 | 0,020408163 | 0,020408163 | 0,040816327 | 0,040816327 | 0,06122449 | 0,040816327 | 0,040816327 | 0,040816327 | 0,040816327 | 0,040816327 | 0,040816327 | 0,020408163 |

Negativ şərhlər ilə eynisin edək:

|      |             |             |             |             |             |             |             |             |             |             |             |             |             |             |             |             |             |             |             |             |             |             |
|---------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|
| **Söz**     | Məqalənizə  | görə        | çox         | sağolun     | marağlı     | oldu        | mövzudur    | lazimi      | uğurlar     | xoşuma      | gəlmədi     | marağsız    | pis         | məqalə      | yazılıb     | yaxşı       | mövzuya     | toxundunuz  | demək       | olar        | əhsən       | gəldi       |
| **Say  **   | 1           | 1           | 2           | 1           | 2           | 5           | 1           | 1           | 1           | 2           | 4           | 3           | 3           | 3           | 1           | 1           | 1           | 1           | 1           | 1           | 1           | 1           |
| **Ehtimal** | 0,027027027 | 0,027027027 | 0,054054054 | 0,027027027 | 0,054054054 | 0,135135135 | 0,027027027 | 0,027027027 | 0,027027027 | 0,054054054 | 0,108108108 | 0,081081081 | 0,081081081 | 0,081081081 | 0,027027027 | 0,027027027 | 0,027027027 | 0,027027027 | 0,027027027 | 0,027027027 | 0,027027027 | 0,027027027 |

Biz bu əməliyyatları icra edincə mənim keçmiş məqaləmə yeni şərh gəldi "Demək olar xoşuma gəlmədi". Mən bu şərhin Müsbət ya Mənfi olmağına tam əmin olmadığımdan təklif edirəm artıq öyrəndiyimiz SBK-dan istifadə edək.

İlk öncə sözlər üzrə şərti klass ehtimallarına baxaq:

| Söz| Müsbət klass ehtimalı| Müsbət klass ehtimalı |
|--------------|-------------|-------------|
| Demək        | 0,040816327 | 0,027027027 |
| Olar         | 0,040816327 | 0,027027027 |
| Xoşuma       | 0,040816327 | 0,054054054 |
| Gəlmədi      | 0,020408163 | 0,108108108 |

![ML_2_11.png](https://github.com/limpapud/data_science_tutorials_projects/blob/master/ML_Tutorials/Articles/Language_AZ/assets/ML_2_11.png)

İlk öncə Müsbət klass üzrə klass ehtimalının sayılmasından başlayaq:

![ML_2_12.png](https://github.com/limpapud/data_science_tutorials_projects/blob/master/ML_Tutorials/Articles/Language_AZ/assets/ML_2_12.png)

Sonra ayrıca Mənfi klass üzrə:

![ML_2_13.png](https://github.com/limpapud/data_science_tutorials_projects/blob/master/ML_Tutorials/Articles/Language_AZ/assets/ML_2_13.png)

Hesablamalar bitdi, artıq müqaisə etmə zamanıdır : 

![ML_2_14.png](https://github.com/limpapud/data_science_tutorials_projects/blob/master/ML_Tutorials/Articles/Language_AZ/assets/ML_2_14.png)

SBK ehtimalları sayıb girişdə olan şərhi ən böyük dəyərə malik olan klas ehtimalına aid edir. Bu deməkdir ki klassifikator şərhi lazım olan "Mənfi" klasa ayırdı. 
### Təbriklər! İlk manual maşın öyrənməsi alqoritmi üzərindən keçdik və klassifikasiya etdik!

Özünüzdə gördüyünüz kimi Sadəlöv Bayes Klassifikatoru asandır, amma asanlığına baxmayaraq bəzi hallarda ən güclu, çətin,təkminləşmiş və müasir alqotitmləri üstələyir və öz nişini indiyənədək saxlayır. Bu nişləri sənəd, mətn klassifikasiyası saymaq olar. SBK-nın tez genişlənmə və hətta böyük həcm verilənləri üzərində ayrı alqoritmlərlə müqaisədə dəfələrlə tez işləməsi ayrı çətin və "ağır" alqoritmlər üzərindən seçilməyə imkan verir. Tez işləməsinin səbəbi vaxtın daha çox ehtimalları hesablamaya xərcləməsi və xərclənən vaxtın girişdə verilən həcmindən aslı olaraq xətti artmasından irəli gəlir. Məsəl üçün ayrı binar klassifikator olan "AdaBoost" artıq hesabladığı sətrlərə yenidən qayıdıb ümumi modeli möhkəmlətdiyindən müqaisə olunmaz çox vaxt tələb edir.

Burada Sadəlöv Bayes Alqoritmi üzrə ilk tanışlıq hissəsi bitdi. Növbəti "Maşın öyrənməsi və alqoritmlər: Sadə(löv) Bayes alqoritmi" məqaləsində klassifikatorla scikit-learn və Orange3 vasitəsi ilə iş başa salınacaq.
Sual/təklif olduqda şərh yaza, səhv/»GitHub»-da repozitoriyada yerləşən bu məqaləni dəyişə bilərsiniz. Və əlbəttə ki həmişə omarbayramov@hotmail.com ünvanına yaza bilərsiniz.
