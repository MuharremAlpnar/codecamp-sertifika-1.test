# DÜZEN #
* HTML SAYFASI DÜZENİ
* CSS SAYFSI DÜZENİ


## HTML SAYFASI DÜZENİ ##

* içeriğin tamamı .container elementinin içine alındı
* içerik **header** ve **form** olacak şekilde iki parçaya bölündü 
  * header elementinin içinde **başlık için h** etiketi **tanım için p** etiketi kullanıldı
    * başlık ve tanım için etiketlere id eklendi
  * form elementine **survey-form** idsi verildi ve *9 alt başlığa* bölündü bunlar
    * isim
    * email
    * Age
    * role
    * reccomend
    * fav
    * want improve
    * comment
    * button
 
  kolay erişilebilinmesi açısından hespsi div olarak parçalandı ve ortal class **form-group** olarak seçildi 
---
* isim, email, Age divleri label ve inputlardan oluşuyor. inputlar label içine alınmadı, label ve **inputları ilişkilendirmek için labelde for** attributuna inputun id'si verildi
* label id'leri neyi temsil ediyorsa o ad ile yazıldı ex(name inputu için label id'si=name-label). bu hangi labelin hangi inpu için yazıldığını görmemizi kolaylaştırır.
* **inputun label içine alınmaması** ise css yazarken işimizi kolaylaştırması.
* input attributelerinde **name özelliğini unutma** çünkü form gönderilirken input değeri bu attributeye kaydedilerek backendde işlem görürür
* formun zorunlu olarak doldurulmasını istediğimiz kısımlarını **required** attributeleri ekledik
* yaş inputunda girilecek **max min** değerlerini unutmamak önemli

* role divi p ve select etiketleriyle oluşturuldu. p etiketinde soru dropdown için oluşturduğumuz select elementinde ise sorunun olası cevapları yer almaktadır.
* ilk seçeneğe **placeholder gibi bir option** eklenebilir. seçeneklerde bir **value, select elementinde ise name** attributesi verinin işlenmesi için önemli


* reccomend bölümüde soru için p etiketi, her cevap için birer label eklendi. bu sefer inputlar labele dahil edilerek ilişkilendirildi **"for attributesine ihtiyaç kalmadı**".
* inputta yer alan cevaplar 1 sorunun olası cevapları olduğundan **name değeri ortak seçildi**. value değerleri ise label ifadeleri seçildi
* **input türleri radio olduğundan name değerlerinin ortak olması radio butonlarına aynı anda 1den fazla seçmememizi sağlar**

* fav içerik için role divinde yapılan işlemlerin aynısı yapıldı

* want improve divinde birden **fazla cevap** olabileceğinden **checkboxlar oluşturuldu** labellerle ilişkilendirmek için her bir input labelin içine yazıldı. name attributuna ortak değer verildiğine dikkat et, checkbox olduğundan bir tanenin seçilmesi **diğerlerinin seçilmesine engel değil.**

* yorum için textarea oluşturulup p etiketi ile bir div içine alındı

* son olarak button div içine alındı, birden fazla buton olması halında **submit butonunun karıştırılmaması** için type attributesine submit değeri verildi 
---
## CSS SAYFSI DÜZENİ ##  
* google font import edilmiş
* :**root** selector ile **html elementini temsil eder** bu selector içine sayfada kullanılacak olan **renkler değişkenlerle temsil** edilmiş. aynı değeri birden fazla stil tanımında tekrar etmek yerine bu değişkenler üzerinden erişilebilir. color: **var(--color-darkblue)**; gibi var fonksyonunun içinde bu değişkenler kullanılabilir.
* **rem** birimi **varsayılanın oranı** olarak ifade edilebilir. ex(varsayılan font-size=16px ise 1rem 16px, 2rem 32px'i ifade eder)
* line-height: 1.4; birimin olmaması bunu bir **unitless** olduğunu gösteriri. unitless kullanılan özelliğe göre ifade ettiği anlam değişebilir. burada kastedilen anlam, satırlar arası mesafe yazı fontunun 1.4 katı olmasıdır.
* @media sorgusu farklı ekranlarda stillerin farklı şekillerde ayarlanmasına olanak sağlar.
* şu ana kadar box-shadow özelliği kullanarak kutulara veya butonlara gölge ekledik. buna benzer bir özellik ise **text-shadowdur** bu özellik metinlere gölge eklememizi sağlar.
* css'de 154. satırda ease-in-out özelliği bir **geçiş eğrisidir**. bir özelliğin bir durumdan başka bir duruma geçerkenki özelliği(animasyonunu) tanımlar
* outline : focus psuedo classında kullanılan özelliklerden biridir. tarayızınin **varsayılan vurgusunu** temsil eder. genellikle border özelliği gibi bir çerçeve oluştursada , focus psuedo classı ile kullanıldığında outline:0; dediğimizde. bir inputa odaklandığımız zaman **varsayılan focus özelliklerini devre dışı** bıralır.
* **resize**:textareanin boyutunun kullanıcı tarafından ayarlanıp ayarlanmamasını sağladığımız bir özelliktir. resize:vertical; kullanıcının textareayı sadece dikey olarak büyütüp küçülteceğini bildirir
* herhangi bir css özelliğinde **inherit** ifadesi: bazı özellikler kalıtım yoluyla çocuklara kalıtılmaz. kalıtılmayan özelliklerin kalıtımını sağlamak için bu özellikler inherit edilir css:183


