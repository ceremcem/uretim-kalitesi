# Üretim Kalitesi

## Nedir?

> Kalite, bir mal veya hizmetin, önceden belirlenmiş ihtiyaç ve beklentileri karşılayacak özelliklerinin bütünüdür. (ISO-9001 Kalite Sözlüğü)

"Üretim kalitesi"nden kasıt, üretim tekrar edilirken veya geliştirilirken ortaya çıkabilecek her türlü problemin baştan öngörülmesi ve bunlara karşı önlem alınmasıdır. 

### Tekrar eden üretimde çıkabilecek problemler

Bir ürünün elektronik, yazılımsal ve mekanik kısımlarının olduğunu düşünelim. Üretimin tamamlanmasından 1 yıl sonra aynı üründen isteniyor olsun. Kalite tanımına dönersek, hem müşterinin hem şirket sahibinin beklentisi son üretim dün yapılmış gibi sorunsuzca üretim yapılmasıdır. Bu beklentiyi karşılamadaki problemler şunlardır: 

1. Ürünle ilgili üretim dosyaları nerede? Ürünün bir kodu var mıydı?
2. Ürünle ilgili dosyaların olması gereken yer bulundu (`sunucu/projeler/ürün-b3871a6`), peki dosyalar burada mı, yoksa 6 ay önce o projeyle ilgilenen mühendisin bilgisayarı çalındığı için kayıp mı oldu? Yedekleri var mıydı? Var olan yedekler son (güncel) yedekler miydi?
3. Dosyalar bulundu. Bu üretimin yapılması için 300 tane parça 20 ayrı yerden sipariş ediliyordu, 400 ayrı işlem adımı vardı. Bunlar neydi? Hiçbirini hatırlamıyoruz. Belki de bu işi şirkete 3 ay önce girmiş bir çalışan icra edecek, dolayısıyla eskiye dair hiçbir bilgisi olmayacak. Bu kişi bu işe nereden başlayacağını nereden bilecek? 
4. İşe başlandı. 
    1. Yazılım:
        1. Kaynak kodlar bulundu. Derlenerek mikrodenetleyiciye yüklenecek. Son 1 yıl içerisinde derleyiciler güncellenmiş. Eski kodu artık derleyemiyoruz, bir hata oluşmuş. En son üretimde derleyicinin hangi versiyonunu kullanmıştık? 
        2. Kullandığımız kütüphaneler güncellenmiş ve bizim eski kodumuzla artık uyumlu değil. O tarihteki kütüphaneleri nereden bulacağız? Bazıları sitesinden kaldırılmış. 
        3. Tüm kütüphaneleri ve derleyicileri bulduk. Hangi komutlarla derliyorduk? 
        4. Derleme tamamlandı. Hangi fiziksel bağlantıları yaparak yazılımı cihaza yüklüyorduk?
        5. Doğru çalıştığını nasıl test ediyorduk? Hangi test araçlarını kullanıyorduk? O test araçları şu an bu projede kullanmaya müsait mi, yoksa şu an başka bir projede mi kullanılıyor? Ya da bozulmuştu da şu an tamirde mi, hatta tamirde bile değil mi, tamirin tamamlanması ne kadar sürer? Bu durumdan şimdi mi haberimiz oldu, başta süre verirken biliyor muyduk? Süre sıkıntısına düşersek testleri yapmayacak mıyız? Testleri yapmazsak teslim ettiğimiz ürünlerin kalitesini nasıl ölçeceğiz?
    2. Elektronik donanım:
        1. Malzeme listesini bulabiliyor muyuz, yoksa o tarihteki e-posta yazışmalarından mı bulmamız gerekiyor? Malzemelerin bir kısmını kağıtlara mı yazmıştık?
        2. Malzeme listesindeki bir malzemeyi bulamıyoruz, üretimden kalkmış. Onun yerine muadil eleman kullanacağız. Önceki seçtiğimizle uyumlu olacağını nasıl garanti edeceğiz? O tarihte elemanı seçerken hangi kriterlere dikkat etmiştik, hangi parametreleri bizim için önemliydi? (bkz. [Malzeme listesinde üretici kodunun önemi (İng.)](https://electronics.stackexchange.com/q/539726/20285))
        3. Dışarıda ürettireceğimiz parçalarla alakalı üretim notları açıkça bulunuyor mu, yoksa o tarihte tedarikçimize sözlü olarak (ya da yazışırken) söylediğimiz bir ayrıntıyı şimdi söylemeyi unuttuğumuz için hatalı ürün mü alacağız? 
        4. Test prosedürleri neydi? 
    3. Mekanik donanım:
        1. Kaynak veya büküm işi var mıydı? Bu işlemlerde aparat kullanıyor muyduk? Kullanıyor idiysek bu aparatlar şu an nerede? Bulamıyorsak bunları yeniden üretmek için gerekli belgeler mevcut mu? Eğer aparatları yeniden üreteceksek bunlar ek maliyet getirecek, müşterinin siparişini onaylarken bu durumu hesaba katmış mıydık?
        2. Tasarım dosyalarından üretilen imalat dosyaları (örn. 3D çizimden üretilen GCode dosyaları) tedarikçinin tarafında, kendi CNC makinasına göre oluşturulur/oluşturulabilir. Tedarikçinin tarafında üretilen dosyaları almış mıydık? Üretici aynı üretim dosyalarımızdan GCode üretirken yine hata olabilir, bunu kontrol edebilecek durumda mıyız?
    
    
### Ürün geliştirilirken karşılaşılan sorunlar

Üretimde yaşanan problemlerin yanısıra geliştirmede şu problemler de yaşanır: 

1. Maliyet hesaplama, işgücü belirleme ve iş parçalarının doğru belirlenmesi:

    Problem: Bir otomobil üretmiştik. Müşteri tavanın 10cm daha yüksek olmasını, böylece aracın daha ferah olmasını istiyor. Bunun müşteriye getireceği maliyeti hesaplarken: 

      * Maliyeti hesaplamanın maliyeti en az olmalıdır. Maliyet hesaplamaya ayrılan işgücü her zaman kısıtlıdır, bu nedenle hataya mahal verir.
      * Maliyet hesabı yaparken hata yaparsak sorumluluk bize ait olacağından çıkan ek masrafları bizim karşılamamız gerekir. Hata yapmamalıyız. 

    Bu nedenle, projenin tasarım belgelerinin elektronik ortamda ve doğru proje yönetim aracı altında mevcut olması gerekir. Tasarım belgeleri 3 ana başlıkta toplanır:
    1. Tasarım gereksinimleri: Bu ürünün hangi özellikleri olmalı? (Şartname)
    2. Tasarım kararları: Neler yaparsak bu tasarım gereksinimlerini yerine getiririz? (Ekleyeceğimiz hangi unsur hangi şartname maddelerini karşılıyor?)
    3. Test prosedürleri: Hangi tasarım kararlarını hangi testlerden geçirmeliyiz?
    
2. Sürekli yedekleme: Çalışanlardan birinin bilgisayarının çalışmalar esnasında çökmesi, çalınması, virüs nedeniyle verilerin bozulması veya yanlışlıkla silinmesi durumunda üretim süreci ciddi zarar görecektir. Çalışanların verileri ne sıklıkla, hangi maliyetle ve ne seviyede yedeklenmektedir? 
    1. Yedekleme seviyesi: Diski çöken bir çalışan yedeklediği dosyalara ulaşsa bile ihtiyaç duyduğu programları kurması ve sistemini tekrar çalışabileceği hale getirmesi için kaç saat (genellikle "gün") kurulum yapacak, tekrar ne zaman kaldığı yerden çalışmaya başlayabilecektir? Bu çalışanın bu zaman kaybı esnasında ekip ne kadar yavaşlayacaktır veyahut duracak mıdır? 
    2. Yedekleme sıklığı: Yedeklerine dönen çalışan kaç saatlik çalışmayı kaybetmiş olacaktır? Bu kaybı kaç saat çalışarak telafi edecektir?
    3. Yedekleme maliyeti: Yedekleme işlemi ne kadar sürmektedir, bu süreçte çalışan ne kadar süreyle işini yapamamaktadır? Yedekleme maliyetleri ağırsa çalışan yedeklemeyi es geçmek isteyecektir. Benzer şekilde yedekleme işlemi iyi bir internet bağlantısına ihtiyaç duyuyorsa (sahada her zaman iyi internet bağlantısı olmaz) bu esnalarda yedek alınamayacak mıdır? 
    4. Yedeklere dönüş: İnternet bağlantısına ihtiyaç duyan bir yedekleme altyapısında, internet bağlantısının kötü olduğu veya hiç olmadığı bir yerde yedeklere dönme ihtiyacı hissedilirse ne yapılacaktır?
    
3. Birbirini etkileyen değişiklikler: 

    1. Devredeki filtrenin değerini arttırmak için kondansatörü büyütmeye karar verdik. Meğer bu değişikliğimiz nedeniyle kutuya sığmayacakmış. Bunu ne zaman fark ettik? Bu durum mevcut piyasada sıklıkla üretimden sonra fark edilir. 
    2. Mekanik olarak bir değişiklik yaptık ve devrenin 3 boyutlu modelini hesaba kattığımızda yeni çıkıntımız devreye dokunmuyor. Harika. Peki kaçak kapasitansları etkileyip etkilemediğini, elektriksel güvenlik için konan mesafeleri ihlal edip etmediğini nereden biliyoruz? Bunu nihai testler esnasında mı öğreneceğiz, yoksa elektronik tasarım bölümüne zamanında haber verilmiş miydi? 
    3. Yazılımlarımızı modüller halinde yapmıştık. Böylece tekrar kullanılabilir parçaları farklı projelerimizde kullanabilmiştik. Bir başka projede, bu projede kullandığımız modüllerden birini geliştirmiştik. Fakat yaptığımız geliştirme şu an bu projenin çalışmamasına neden oluyor. Son çalışan versiyona nasıl dönebiliriz?
            
# Belgelendirmenin ve araç gereç seçiminin önemi 

[<img src="http://i3.ytimg.com/vi/bYNEdhxP6U0/hqdefault.jpg" width="50%" />](https://youtu.be/bYNEdhxP6U0)

Doğru araçlar kullanılmazsa ve/veya yeteri kadar pratik yapılmazsa birimler arasındaki iletişim çok ağırlaşır. Yukarıda komedisi yapılan durum gerçekte sıklıkla (çok sıklıkla) yaşanmaktadır. 

Peki üretim esnasında ortaya çıkan böylesi değişiklikleri hangi yöntemleri izleyerek uygularsak o değişiklikleri hem belgelendirmeye zaman maliyeti eklemeksizin dahil edebilir, hem de belirlenmiş test prosedürlerimizden de geçirebiliriz? 

# Çözümler 

Nasıl ki farklı işler yaparken giyilen kıyafetler farklı olmalıysa, nasıl ki her iş kendine özel düzenlenmiş mekan gerektiriyorsa, her proje ekibi kendi araç gerecini belirlemelidir. "En doğru" sistem diye bir şey yoktur, "maliyeti (zaman, para, işgücü) en uygun" sistem diye bir şey vardır. 

1. Kodlar sürümlenmelidir. Bunun için dağınık kod sürümleme sistemleri (örn. Git) kullanılır.
2. Tüm proje sürümlenmelidir. Her bir derleme esnasında derleyicinin ve işlemde kullanılan tüm programların versiyonları otomatik olarak not alınmalıdır. Daha iyisi, Docker, LXC, VirtualBox ya da benzeri bir altyapı aracılığıyla tüm gereksinimler biraraya toplanmalı, tüm akış her zaman tekrar edilebilir kılınmalıdır. 
3. Yazılım ve donanımlar için test prosedürleri oluşturulmalıdır. (bkz. Test Driven Development)
4. İş akışları yönerge haline getirilmelidir. Yönergeler çok ayrıntılı olamaz, çok ayrıntılı olursa okunur olmazlar. Yeterince mesai harcanarak mümkün olduğunca kısaltılmalıdır. Yönergeler hem fiziken basılı hem de elektronik ortamda bulunmalıdır. 
5. Devre şemalarında malzeme listelerinin yanısıra o devre şemasının hangi marka/model malzemelerle yapıldığı ayrıca bilgi olarak yazılmalıdır. 
6. Tüm yazışmalar yazılı olarak yapılmalı, sözlü yapılan görüşmeler yazıya dökülerek teyitleşilmelidir. Projeye verilmiş olan proje kodu mutlaka konuya eklenmelidir. Böylece daha sonradan o projeyle ilgili yazışmalar aramalarda bulunabilir. Konu kısmına proje kodu eklenmeden yazışma yapılamaması için uygun mekanizmalar bulunmalıdır.
7. Oluşturulan iş akışlarında "acele etmek" değil, "zamandan tasarruf etmek" değil "hataya mahal vermemek" amaçlanmalıdır. Unutulmamalıdır ki aslında en hızlı iş, en az hatayla yürüyen akışla yapılır. 
8. Büyük çaplı projelerde "Proje Gereksinim Yönetim Sistemi" kullanılmalıdır. (bkz. IBM DOORS)

# Vurgulanan Noktalar

1. İşbu belge "Test driven development" mantığı ile yazılmıştır. Bahsedilen "sorunlar", "test maddeleri" olarak kabul edilebilir. Ekibin tercih ettiği yöntemler kombinasyonu değiştikçe ve geliştikçe, "hala yukarıdaki isteklere yanıt verebiliyor mu" diye kontrol edilebilir. 
2. İşbu belge Git kullanılarak sürümlenmiştir. Böylelikle sonradan yapılacak değişiklik ve iyileştirmeler takip edilebilir kılınmıştır. 
