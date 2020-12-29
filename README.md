# Üretim Kalitesi

## Nedir?

Kalite, bir mal veya hizmetin, önceden belirlenmiş ihtiyaç ve beklentileri karşılayacak özelliklerinin bütünüdür. (ISO-9001 Kalite Sözlüğü)

"Üretim kalitesi"nden kasıt, üretim tekrar edilirken veya geliştirilirken ortaya çıkabilecek her türlü problemin baştan öngörülmesi ve bunlara karşı önlem alınmasıdır. 

### Tekrar eden üretimde çıkabilecek problemler

Bir ürünün elektronik, yazılımsal ve mekanik kısımlarının olduğunu düşünelim. Üretimin tamamlanmasından 1 yıl sonra aynı üründen isteniyor olsun. Kalite tanımına dönersek, hem müşterinin şirket sahibinin beklentisi, son üretimi dün yapmış gibi rahatça üretimi yapabilmektir. Bu beklentiyi karşılamadaki problemler şunlardır: 

1. Ürünle ilgili üretim dosyaları nerede? Ürünün bir kodu var mıydı?
2. Ürünle ilgili dosyaların olması gereken yer bulundu (sunucu/projeler/ürün-1), peki dosyalar burada mı, yoksa 6 ay önce o projeyle ilgilenen mühendisin bilgisayarı çalındığı için kayıp mı oldu? Yedekleri var mıydı? 
3. Dosyalar bulundu. Bu üretimin yapılması için 300 tane parça 20 ayrı yerden sipariş ediliyordu, 400 ayrı işlem adımı vardı. Bunlar neydi? Hiçbirini hatırlamıyoruz. Belki de bu işi şirkete 3 ay önce girmiş bir çalışan icra edecek, dolayısıyla eskiye dair hiçbir bilgisi olmayacak. Bu kişi bu işe nereden başlayacağını nereden bilecek? 
4. İşe başlandı. 
    1. Yazılım:
        1. Kaynak kodlar bulundu. Derlenerek mikrodenetleyiciye yüklenecek. Son 1 yıl içerisinde derleyiciler güncellenmiş. Eski kodu artık derleyemiyoruz, bir hata oluşmuş. En son üretimde derleyicinin hangi versiyonunu kullanmıştık? 
        2. Kullandığımız kütüphaneler güncellenmiş ve bizim eski kodumuzla artık uyumlu değil. O tarihteki kütüphaneleri nereden bulacağız? Bazıları sitesinden kaldırılmış. 
        3. Tüm kütüphaneleri ve derleyicileri bulduk. Hangi komutlarla derliyorduk? 
        4. Derleme tamamlandı. Hangi fiziksel bağlantıları yaparak yazılımı cihaza yüklüyorduk?
        5. Doğru çalıştığını nasıl test ediyorduk? 
    2. Elektronik donanım:
        1. Malzeme listesini bulabiliyor muyuz, yoksa o tarihteki e-posta yazışmalarından mı bulmamız gerekiyor? Malzemelerin bir kısmını kağıtlara mı yazmıştık?
        2. Malzeme listesindeki bir malzemeyi bulamıyoruz, üretimden kalkmış. Onun yerine muadil eleman kullanacağız. Önceki seçtiğimizle uyumlu olacağını nasıl garanti edeceğiz? O tarihte elemanı seçerken hangi kriterlere dikkat etmiştik, hangi parametreleri bizim için önemliydi? (bkz. [Malzeme listesinde üretici kodunun önemi (İng.)](https://electronics.stackexchange.com/q/539726/20285))
        3. Dışarıda ürettireceğimiz parçalarla alakalı üretim notları açıkça bulunuyor mu, yoksa o tarihte tedarikçimize sözlü olarak (ya da yazışırken) söylediğimiz bir ayrıntıyı şimdi söylemeyi unuttuğumuz için hatalı ürün mü alacağız? 
        4. Test prosedürleri neydi? 
    3. Mekanik donanım:
        1. Kaynak veya büküm işi var mıydı? Bu işlemlerde aparat kullanıyor muyduk? Kullanıyorduysak bu aparatlar şu an nerede? Bulamıyorsak bunları yeniden üretmek için gerekli belgeler mevcut mu? Eğer aparatları yeniden üreteceksek bunlar ek maliyet getirecek, müşterinin siparişini onaylarken bu durumu hesaba katmış mıydık?
        2. Üretim dökümanlarından üretilen imalat dosyaları (örn. GCode dosyaları) tedarikçinin tarafında, kendi CNC makinasına göre oluşturulur/oluşturulabilir. Tedarikçinin tarafında üretilen dosyaları almış mıydık? Üretici aynı üretim dosyalarımızdan GCode üretirken yine hata olabilir, bunu kontrol edebilecek durumda mıyız?
    
    
### Ürün geliştirilirken karşılaşılan sorunlar

Problem: Bir otomobil üretmiştik. Müşteri tavanın 10cm daha yüksek olmasını, böylece aracın daha ferah olmasını istiyor. Bunun bize getireceği maliyeti hesaplarken: 

   * Bu maliyeti hesaplamanın maliyeti en az olmalıdır. 
   * Bu hesabı yaparken hata yaparsak sorumluluk bize ait olacağından çıkan ek masrafları bizim karşılamamız gerekir. Hata yapmamalıyız. 

Bu nedenle, projenin tasarım dökümanlarının elektronik ortamda ve doğru proje yönetim aracı altında mevcut olması gerekir. Şu ana başlığın altındaki tüm kalemler, alakalı olduğu başlığın altındaki alakalı olduğu hususa atıfta bulunmalıdır:
1. Tasarım gereksinimleri: Bu ürünün hangi özellikleri olmalı? 
2. Tasarım kararları: Neler yaparsak bu tasarım gereksinimlerini yerine getiririz?
3. Test prosedürleri: Hangi tasarım kararlarını hangi testlerden geçirmeliyiz?

(DEVAM EDİLECEKTİR)
  
# Dökümantasyonun ve dökümantasyon araçlarının seçiminin önemi 

[<img src="http://i3.ytimg.com/vi/bYNEdhxP6U0/hqdefault.jpg" width="50%" />](https://youtu.be/bYNEdhxP6U0)
