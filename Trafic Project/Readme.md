# Traffic Project
- İlk aşamada projediki 3 farklı csv dosyasını "csv_read" etiketi ile okutuyourz. Bu şekilde verileri eklemiş olduk bu 3 veriyi birleştirme işlemi yapmamız lazım bunun içincede "concat" kullanıyorz ki tek bir veri setimiz olsun. <br/>

- Daha sonra düzenlenmesi gerek data başlıklarını düzenliyoruz "loc" kullanarak.

- Null değerleri "dropna" kullnarak kaldırıyourz.

- Düzenlenmesi gereken "time" veri türünü düzenledik.

- Eksik olan verilerin düzenlenmesini sağlıyoruz.

- Seaborn: istatistiksel veri görselleştirme bunun için kullanıyoruz

- y değerine toplam kaza değerlerini "sayı" değerini getiriyoruz x se ise toplam kaza yıllarını

- Yıllar geçtikçe kaza sayısını düştüğünü rahat bir şekilde gözlemliyoruz.

- "Hız sınırına göre kazanın şiddeti" nasıl hesaplanıcağını plot kullanarak elde ettik.

- Döngünün içindeki koşul, geçerli yineleme sayısının listede olup olmadığını kontrol edetmek için "unique" değerini kullandık.

- Daha sonra Yol tipine göre, ışık koşullarına göre, hava durumuna göre , yol yüzeyine göre, saate ve aylara göre bir veri gösrselleştirme yaparak verilerinin sütun grafiklerinde gösterimlerini sergiledim.

- "kazalar.Speed_limit = kazalar.Speed_limit.astype(str)" Bunu yapmamızın en önemli sebebi değerin okunabilir değer olarak plt değerini göstermek ve bu şekilde veriyi hıza göre veri analizi yaparak veriyi görseleştirdik.

- "unique" kullanarak yalnızca benzersiz sayılar eklenir, kayıp değerleri çağırıyoruz.

- "get_dummies" verileri analiz edilebilir bir pozisyona getirebilmek için kulladığımız bir fonk. bunun sayesinde 1-0 şekilde verileri toplayabiliyoruz ve görselleştirme işlemini yapabiliyoruz.

- Speed limit obcet iken int değerlerine çeviriyoruz ki veri oknabilir ol.

- "to_csv('sonhali.csv')"  dışa aktarma için kulanılan bu sistem ile verileri daha düzenli bir sistcsv dosyası haline getirdik.

- Bizden istenilen bir diğer veriler olan verileri düzenledik ve grafikleştirme işlemi yaptık.

- "Road_Surface_Conditions" ile hava Olayları Yolları Nasıl Etkiler sorusu ile elde ettiğimiz veri setlerini pasta grafiği haline getirdik.

- "road_cond = kazalar["Road_Surface_Conditions"].value_counts() " Yol Koşullarına Göre Kaza Oranının nasıl değiştiğini bu şekilde irdeledik.

- What Weather Conditions Cause the Most Traffic Accidents

- Trafik Kazalarında Yol Türüne Göre Zayiat Sayısı hesaplarken "Road_Type","Number_of_Casualties" değerlienden dönen sonuçları sum kullanarak topluyoruz.

- Daha sorna seanborn kullanarak görselleştirme işlemi yapıyoruz.

- Kentsel ve Kırsal Alan Trafik Kazaları Riskleri Arasındaki Fark Nedir sorusunda cevap veririken plot ve seanborn kullanrak yardım aldım bu şekilde ilişkisel ver görselleştirme elde ettim.