# Mutluluk Projesi Raporu Analizi

- Projenin amacı ;
Bu veri seti ilk kez 2012 yılında yayınlanan 155 ülkeyi mutluluk seviyelerine göre sıralayan dünya mutluluk raporlarından oluşmaktadır. Bizde burda 6 faktör olarak belirlenen  -ekonomik üretim, sosyal destek, yaşam beklentisi, özgürlük, yolsuzluğun olmaması ve cömertlik  gibi kriterler ile raporu analiz edeciğiz 

Bu veri setlerimizde düzenlenmesi gereken sütun isimlerini düzenledik verileri sıraladık ve analiz edilebilir hale getirdik. Şimdide  Gelelim bizlere verilen sorulara


- İlk olarak import yapılması gereken kütüphaneleri importluyoruz.

- Pandas üzerinden verilerimizi bir değişkene atayıp okutuyoruz.

- Sütunları kontrol ediyoruz.

- null değer olup olmadığını kontrol ediyoruz.

- Sorumuzdaki ülkeleri gruplamak için ilk olarak groupby kullandık. Ülkelere göre sıraladığımız için contry parantez içinde ayrı alıyoruz daha sonra bizden isteden 6 kriteri, köşeli parantez içinde dahil ediyoruz. Daha sonra toplamlarından ortalama değeri almak için mean() kulanıyoruz. Sonra sort_values kullanıyoruz buradaki temel amaç ise bir veri  çerçevesini bir veya daha fazla sütuna göre sıralamanıza izin veren bir işlev bu şekilde verilerimizi rahat bir şekilde mutluluk skorlarına göre sıralayabiliyoruz.

Ve bu şekilde sonuç tablomuz bize yansıyor elde ettiğimiz veriler ile de her kriteri karşılayan en fazla olan ülkeleri rahat bir şekilde gözleyebiliyoruz.


- Pandas üzerinde dataframe tablosundan “urban_or_rural_area”  sütunun value_counts değerlerini yani benzersiz değerlerin sayımlarını içeren nesneyi döndürerek kazalar veri setimizden çağırdık. sütun ve satırı kaldırmak içn burda drop kullanıyoruz drop değerimiz ise 3

- Daha sonra  figsize 10 a 10  değeri  veriyoruz bu da pilot içerisinde tablo genişliğini ayarlamamızı sağlıyor.

- Tablomuzun başlığını ayarlıyoruz. Daha sonra üst sağ taraftaki legend tablosunun değerlerini giriyoruz. 

- Daha sonra  subplots ile 2’ye iki tablolama yaptık. Figsize ise tablo boyutunu 10’na 10 yaprak düzenliyoruz. Barplot kullanarak ,  X eksenine ülkeleri y ekseninine de mutluluk skorunu ekliyoruz . Tablo sıralamasıda [0,0] dan başlayarak arttırıyoruz. 
Ve ardından tablo titlelerini yani tablo ismlerini yazıyoruz bu şekilde kodlama yaptığımızda 2015 ve 2016, 2016 ve 2017 yılları arasında değer farklılıkları görsel bir şekilde analiz edilebilir hale getiriyoruz.

2016 ve 2017 yıllarına baktığımızda isviçre 2015’te birinci 2016 yılında ikinci olmuş bir düşüş var gördüğümüz üzere, 2016’da Danimarka birinci olmuş.2017 ise Norveç birincilik de yerini almış. 

- Bu analizi yaparken Shift kullandım veriler içinde herhangi bir azalış ve artış olup olmadığını öğrenebilmem için kulanabilecek en iyi fonksiyon olduğuna karar verdim.
Bu şekilde2015 yılından 2016 yılını çıkarak farkları elde ettik fark ne kadar eksi  değerde olursa o kadar büyük fark vardır.

Bu grafikte de anladığımız kadarı ile 100’ uncu İndexe doğru verilerin ne kadar eksi aldığını rahat bir şekilde görebiliyoruz 

Loc kullanarak 100’üncü indexte hangi ülke olduğuna baktığımızda isviçre olduğunu görüyruz. 

Bu da demek oluyor ki yıllar geçtikçe bir sert bir düşüş olduğunun verisi elde ettik.
