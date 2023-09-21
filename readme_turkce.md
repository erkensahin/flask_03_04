# Hands-on Flask-03-04: If-For structure, Handling Routes and Get-Post Methods (Uygulamalı flask-03-04: If-For yapısı, Yolları Kullanma ve Get-Post Yöntemleri)

Bu uygulamalı eğitimin amacı öğrencilere formların nasıl kullanılacağına dair giriş bilgisi vermektir.

![HTTP Methods in Flask](./http-methods-flask.png)

## Learning Outcomes (Öğrenme Çıktıları)

Bu uygulamalı eğitimin sonunda öğrenciler;

Flask frameworküyle basit bir web uygulaması oluşturun.

HTTP istek-yanıt döngüsünü ve URL'nin yapısını anlayın.

Flask ile rotalar (veya görünümler) oluşturun.

Flask'ı kullanarak statik içerik ve dosyalar sunar.

HTML şablonlarını kullanarak dinamik içerik sunun.

Jinja Templating Engine'i kullanarak html şablonları yazın.

Python Flask frameworküyle bir web uygulaması oluşturun.

flask ile if koşulları ve for döngüleri oluşturun.

flask kullanarak formları ve GET-POST yöntemlerini yönetin.

uygulama sürümlendirmesini yönetmek için git repo'yu kullanın.


## Outline (Öğrenme Çıktıları)

Bölüm 1 - Yönlendirmeyi ve HTTP URL'lerini tanıma.

Bölüm 2 - HTTP yöntemlerini tanıma (GET & POST).

Bölüm 3 - If koşullarını ve for döngülerini kullanarak bir Web Uygulaması yazın

Bölüm 4 - GitHub Repo'da Örnek Yönlendirmeler ve Şablon Oluşturma İçeren Bir Web Uygulaması Yazma

Bölüm 5 - GET ve POST HTTP Yöntemini kullanmayı öğrenin

Bölüm 6 - Formlarla Örnek Web Uygulaması Yazın

## Part 1 - Getting to know routing and HTTP URLs.(Bölüm 1 - Yönlendirmeyi ve HTTP URL'lerini tanıma.)

HTTP (Köprü Metni Aktarım Protokolü) bir istek-yanıt protokolüdür. Bir taraftaki istemci (web tarayıcısı) bir sunucudan bir şey ister veya talep eder, diğer taraftaki sunucu ise o istemciye bir yanıt gönderir. Tarayıcımızı açıp URL’yi (Tekdüzen Kaynak Bulucu) yazdığımızda, bir sunucudan bir kaynak talep ediyoruz ve URL o kaynağın adresidir. Tipik URL'nin yapısı aşağıdaki gibidir.

![URL anatomy](./url-structure.png)

Sunucu bu isteğe bir HTTP yanıt mesajıyla yanıt verir. Yanıt içerisinde, aşağıda gösterildiği gibi yanıtın kategorisini tanımlayan 3 basamaklı bir tamsayı olan durum kodu öğesi bulunur.

1xx -> Bilgilendirme ---> Talebin alındığı ve sürecin devam ettiği anlamına gelir.

2xx -> Başarılı ---> Eylemin başarıyla alındığı, anlaşıldığı ve kabul edildiği anlamına gelir.

3xx -> Yönlendirme ---> İsteğin tamamlanması için daha fazla işlem yapılması gerektiği anlamına gelir.

4xx -> İstemci Hatası ---> İsteğin yanlış sözdizimi içerdiği veya yerine getirilemeyeceği anlamına gelir.

5xx -> Sunucu Hatası ---> Sunucunun görünüşte geçerli bir isteği yerine getiremediği anlamına gelir.

O kodları birer birer öğrenseydiniz. Size bir URL gönderebilirim. Ayrıca farklı kaynaklar da bulabilirsiniz.

https://www.w3schools.com/tags/ref_httpmessages.asp

## Part 2 - Getting to know HTTP methods (GET & POST) (Bölüm 2 - HTTP yöntemlerini tanıma (GET & POST))

HTTP (Köprü Metni Aktarım Protokolü) bir istek-yanıt protokolüdür. Bir taraftaki istemci (web tarayıcısı) bir sunucudan bir şey ister veya talep eder, diğer taraftaki sunucu ise o istemciye bir yanıt gönderir.

İstemci istek gönderirken farklı http yöntemlerini kullanarak veri gönderebilir GET, POST, PUT, HEAD, DELETE, PATCH, OPTIONSancak en yaygın olanları GET ve POST.

![Get and Post Requests](./get-post-request.jpg)

HTTP GETyöntemi isteği;

Belirli bir kaynaktan veri istemek için kullanılır.

önbelleğe alınabilir.

tarayıcı geçmişinde kalır.

yer imlerine eklenebilir

hassas verilerle uğraşırken asla kullanılmamalıdır.

uzunluk sınırlaması vardır.

yalnızca veri istemek için kullanılır, değiştirmek için değil.

HTTP POSTyöntemi isteği;

asla önbelleğe alınmadı.

tarayıcı geçmişinde kalmaz.

yer imlerine eklenemiyor

hassas verilerle uğraşırken kullanılabilir.

uzunluk sınırlaması yoktur.

## Part 3 - Write a Web Application using If conditions and for loops (Bölüm 3 - If koşullarını ve for döngülerini kullanarak bir Web Uygulaması yazın)

Depo flask-03-handling-routes-and-if-foriçinde kopyalamy-repository

Repo Flask_If_for_structureiçindeki klasörün altındaflask-03-handling-routes-and-if-for

Adlı python dosyası oluşturun app.py

``` python
# Flask modüllerini içe aktar

# Uygulama adında bir nesne oluşturun

# `index.html`de masajı "Bu benim ilk durum deneyimim" olarak gösteren head adında bir fonksiyon oluşturun
# ve ('/') rotasına atayın

# `index.html'de listenin sayı elemanlarını birer birer yazdıran başlık adında bir fonksiyon oluşturun
# ve ('/') rotasına atayın

# bu uygulamayı yerel cihazınızda hata ayıklama modunda çalıştırın.
```


## Part 4 - Write a Web Application with Sample Routings and Templating on GitHub Repo (Bölüm 4 - GitHub Repo'da Örnek Yönlendirmeler ve Şablon Oluşturma İçeren Bir Web Uygulaması Yazma)

Repo flask-03-handling-routesiçindeki klasöre bakalımflask-03-handling-routes-and-if-for

Adlı python dosyası oluşturunapp.py

```python
#Import Flask modülleri

#Uygulama adında bir nesne oluştur


# 'Bu, yol olmayan ana sayfadır, <h1> Ana Sayfaya Hoş Geldiniz</h1>' dizesini döndüren home adında bir işlev oluşturun
# ve yolu olmayan rota atayın ('/')


# '<h1>Bu benim hakkında sayfam </h1>' biçimlendirilmiş dizesini döndüren, hakkında adında bir işlev oluşturun
# ve ('about') öğesinin statik rotasına atayın


# '<h1>Ya bir hatayla karşılaştınız ya da yetkiniz yok.</h1>' biçiminde bir dize döndüren error adlı bir işlev oluşturun.
# ve ('hata') statik yoluna atayın


# İsteği hata yoluna yönlendiren admin adında bir işlev oluşturun
# ve ('/admin') rotasına atayın


# Biçimlendirilmiş satır içi html dizesini döndüren, selamlama adında bir işlev oluşturun
# ve ('/<name>') dinamik rotasına atayın


# İsteği 'Ana Yönetici!!!!' parametresiyle merhaba yoluna yönlendiren greet_admin adında bir işlev oluşturun.
# ve ('/greet-admin') rotasına atayın


# `templates` klasörü altındaki `greet.html` isimli şablon dosyasını kullanan greet isimli fonksiyonu yeniden yazın
# ve ('/<name>') dinamik rotasına atayın.
# Lütfen 'şablonlar' klasörü altında parametre olarak 'ad'ı alan 'greet.html' adında bir şablon html dosyası bulun


# `list10.html` içerisinde 1'den 10'a kadar sayılan bir liste oluşturan list10 adında bir fonksiyon oluşturun
# ve ('/list10') rotasına atayın.
# Lütfen `templates` klasörü altında 1'den 10'a kadar sayılan listeyi gösteren `list10.html` adlı şablon html dosyasını bulun


# `evens.html` içerisinde 1'den 10'a kadar olan çift sayıları gösteren evens adında bir fonksiyon oluşturun
# ve ('/evens') rotasına atayın.
# Lütfen `templates` klasörü altında 1'den 10'a kadar çift sayıların listesini gösteren `evens.html` adında bir şablon html dosyası bulun


# 80 numaralı bağlantı noktasındaki herhangi bir ana bilgisayardan erişilebilen Flask uygulamasını çalıştırmak için bir ifade ekleyin.
```

## Part 5 - Learn to use GET and POST HTTP Method (Bölüm 5 - GET ve POST HTTP Yöntemini kullanmayı öğrenin)

Klasörün Flask_GET_POST_Methodsaltındaki klasöre gitflask-04-handling-forms-POST-GET-Methods

app.py Burada adlı dosyayı oluşturun .

```python
# Flask modüllerini içe aktar


# Uygulama adında bir nesne oluşturun


# iki sayının en küçük ortak kat değerlerini hesaplayan "lcm" adında bir fonksiyon yaratın.


# `index.html` adlı şablon dosyasını kullanan `index` adlı bir işlev oluşturun
# app.py dosyasına şablon değişkeni olarak iki sayı gönderin ve yolu olmayan rotayı ('/') atayın


# "lcm" fonksiyonunu kullanarak bunların toplamını hesaplayın, ardından sonucu
# "result.hmtl" dosyasını seçin ve yolun rotasını ('/calc') atayın.
# Kullanıcı doğrudan "/calc" yoluna geldiğinde "Bu bir GET isteği olduğu için LCM hesaplanmamıştır" stringi "result.html" dosyasıyla birlikte kendisine döner


# Flask uygulamasını çalıştırmak için hata ayıklanabilecek bir ifade ekleyin.

```

## Part 6 - Write a Sample Web Application with forms (Bölüm 6 - Formlarla Örnek Web Uygulaması Yazın)

Klasörün flask-04-handling-formsiçine gitflask-04-handling-forms-POST-GET-Methods

Şimdi form işlemeli bir uygulama yazacağız ve kodun tamamını klasöre app-form-handling.pykaydedeceğiz flask-04-handling-forms.

```python
# Flask modüllerini içe aktar


# Uygulama adında bir nesne oluşturun


# Aşağıda verilen `greet.html` adlı şablon dosyasını kullanan `greet` adında bir fonksiyon yazın.
# 'şablonlar' klasörü. URL'deki sorgu dizesinden parametreleri alır, bu parametreyi atayın
# 'user' değişkenine ekledim ve bu kullanıcı adını html dosyasına gönderdim. Herhangi bir parametresi yoksa uyarı masajı yükseltilir


# `templates` klasörü altında verilen `greet.html` adlı şablon dosyasını kullanan `greet` adında bir fonksiyon yazın


# `GET` ve `POST` metodlarını kullanan `login` adında bir fonksiyon yazın,
# ve `templates` klasörü altında verilen `login.html` ve `secure.html` adlı şablon dosyaları
# ve ('giriş') statik yoluna atayın


# 80 numaralı bağlantı noktasındaki herhangi bir ana bilgisayardan erişilebilen Flask uygulamasını çalıştırmak için bir ifade ekleyin.


# app.run(host='0.0.0.0', port=80)
```

