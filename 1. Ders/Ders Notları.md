30.09.2025 tarihinde işlediğimiz dersin önemli başlıkları:

* Değişkenler
* Değişken türleri
* Değişkenler arasında toplama
* Değişkenleri +1 olarak arttırma
* Akış Diyagramları

---

### **Değişken Nedir?**

Programlamada **değişken**, bilgisayarın hafızasında veri saklamak için kullandığımız **isimlendirilmiş alan**dır. Yani, bir değeri geçici olarak tutmak ve gerektiğinde bu değeri kullanmak için değişkenlere ihtiyaç duyarız.

* Değişkenler, bilgisayarın **RAM (Random Access Memory)** bileşeninde geçici olarak saklanır.
* Bir değişken tanımlamak için önce **değişkenin türünü** ve **adını** belirtiriz.

#### **Java Örneği:**

```java
int A; // 'A' adında bir tam sayı değişkeni tanımlandı
```

* Bu işlemden sonra, **RAM’de bilgisayar bizim için bir hafıza yeri ayırır** ve değişken için bir "yuva" oluşturur.
* Değişkene değer atamak için:

```java
A = 10; // 'A' değişkenine 10 değeri atandı
```

* Artık RAM’deki o yuvada **10 değeri saklanır** ve program boyunca bu değeri kullanabiliriz.

---

### **Değişken Türleri**

Bu derste sadece iki temel değişken türü işlenmiştir:

1. **Int (Integer)**

   * Tam sayı değerleri saklamak için kullanılır.
   * Örnek:

   ```java
   int sayi = 25;
   ```

2. **String**

   * Metin veya karakter dizilerini saklamak için kullanılır.
   * Örnek:

   ```java
   String isim = "Mert";
   ```

---

### **Değişkenler Arasında Toplama**

Değişkenler üzerinde matematiksel işlemler yapabiliriz. Örneğin iki sayıyı toplamak için:

```java
int a = 10;
int b = 5;
int toplam = a + b;
System.out.println(toplam); // Ekrana 15 yazdırır
```

* Burada `a` ve `b` değişkenlerinin değerleri toplanıp `toplam` değişkenine atanır.

---

### **Değişkeni +1 Arttırma**

Bir değişkenin değerini 1 arttırmak için şu yöntem kullanılır:

```java
int sayi = 7;
sayi = sayi + 1; // sayi şimdi 8
```

Java’da daha kısa bir yazım da vardır:

```java
sayi++; // sayi değerini 1 arttırır
```

---

### **Akış Diyagramları**

Programlarda yapılan işlemleri **görsel olarak** göstermek için **akış diyagramları** kullanılır. Akış diyagramları:

* İşlemlerin sırasını gösterir
* Karar noktalarını ve döngüleri ifade eder
* Kod yazmadan önce mantığı anlamak için çok faydalıdır

Örnek akış diyagramı sembolleri:

* Oval → Başlangıç/Bitiş
* Dikdörtgen → İşlem/Komut
* Paralelkenar → Girdi/Çıktı
* Elmas → Karar noktası (if, koşul)    # Bu derste işlenilmedi. #

Akış diyagramları, programın mantığını görselleştirip hataları önlemeye yardımcı olur.

Dersimizde **Flowgorithm** uygulamasını kullandık.

Bu uygulamayı Windows Kullanıcıları http://www.flowgorithm.org/download/ adresine giderek, "Recommended (Önerilen)" versiyonu indirebilirler.
MacOS kullanıcıları için bir github projesi mevcut fakat güvenilirliği konusunda bir bilgim bulunmamakta. İlgili Proje: https://github.com/jostasik/Flowgorithm-macOS/releases/tag/v4.5

---

### **Derste Yaptığımız Akış Diyagramları**

Derste basit ve anlaşılması kolay girdi verileri olan ve girilen verilerle matematiksel işlem yapıp sonucunu ekrana yazdıran diyagramlar üzerinde çalıştık.

* 1 - İki Sayı Tanımlayıp Toplama
    1. Öncelikle `A` ve `B` adında iki değişken tanımlıyoruz ve türlerini **Sayı (Int)** olarak belirliyoruz.
    2. Kullanıcıdan `A` ve `B` değerlerini girmesini istiyoruz (Giriş A, Giriş B).
    3. `C` adında bir değişken tanımlıyoruz.
    4. Atama özelliğini kullanarak `C` değişkenine `A + B` işlemini yapacak şekilde değer atıyoruz.
    5. Son olarak, Çıktı özelliğini kullanarak `C` değişkeninin değerini ekrana yazdırıyoruz.

* 2 - Değişkenleri Aynı Yerde Toplama
    1. Önceki akış diyagramına çok benzer, fakat daha basit ve okunması kolay bir yöntemdir.
    2. Tüm değişkenleri tek bir kare içinde tanımlayabiliriz.
    3. Tanımlama menüsünde **Değişken İsimleri** kısmında değişkenleri virgül ile ayırarak birden fazla değişkeni aynı anda atayabilirsiniz.

* 3 - Öğrenci Bilgilerini Alıp Ortalama Hesaplama
    Bu akış diyagramında öğrenciden bazı bilgileri alıp vize ve final notlarına göre ortalama hesaplayacağız.
    
    1. **Değişkenleri Tanımlama:**

    * `ogrNo`, `isim`, `soyisim` → **String** türünde
    * `vizeNotu`, `finalNotu` → **Integer** türünde
    * `ortalama` → **Real** türünde (ondalık sayı için)

    2. **Kullanıcıdan Veri Alma:**

    * Ekrana mesaj yazarak kullanıcıdan bilgileri alıyoruz:

        * Öğrenci numarası
        * İsim
        * Soyisim
        * Vize notu
        * Final notu

    3. **Ortalama Hesaplama:**

    * Atama işlemi kullanılarak ortalama hesaplanır:

    ```
    ortalama = vizeNotu*0.4 + finalNotu*0.6
    ```

    * Burada vizenin ağırlığı %40, finalin ağırlığı %60’dır.

    4. **Sonucu Gösterme:**

    * Ekrana öğrencinin numarasını ve ortalamasını yazdırıyoruz:

    ```
    "Öğrenci Numaranız: " + ogrNo + " | Not Ortalamanız: " + ortalama
    ```

    > Bu örnek, hem String hem Integer değişkenlerin bir arada nasıl kullanılacağını gösterir ve kullanıcıdan alınan verilerle basit bir hesaplama yapmayı öğretir.


# 3 -2 - Öğrenci Bilgilerini Alıp Ortalama Hesaplama (Ekstra olarak "Eğer" özelliği kullanılarak Dersten geçip geçmediğini de not etmektedir.)

# 4 - String Birleştirme