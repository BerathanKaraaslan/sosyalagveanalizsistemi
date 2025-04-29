
 # 📘 Kullanıcı Sosyal Ağ Simülasyonu (Red-Black Tree & Graph)

Bu proje, C programlama dili kullanılarak geliştirilen bir **sosyal ağ analiz uygulamasıdır**. Uygulama, kullanıcılar arası arkadaşlık ilişkilerini hem **Red-Black Tree** (kırmızı-siyah ağaç) ile sıralı şekilde depolar hem de **graph (graf)** yapısı üzerinden ilişkileri temsil eder. Aynı zamanda sosyal ağ üzerinde çeşitli analizler gerçekleştirir.

## 🎯 Amaç

Bu uygulamanın amacı:
- Kullanıcıları Red-Black Tree ile verimli bir şekilde saklamak.
- Arkadaşlık ilişkilerini grafik (graph) yapısı ile modellemek.
- DFS (Depth-First Search) algoritması ile sosyal bağlantı analizleri yapmak.
- Ortak arkadaş, etki alanı ve topluluk gibi sosyal analizleri kullanıcıya sunmak.
- Sistemdeki tüm verileri bir dosyaya (`veriseti.txt`) yazmak ve dosya içeriğini göstererek kullanıcıyı bilgilendirmek.

## 🛠️ Derleme ve Çalıştırma

Bu uygulamayı GCC derleyicisi ile terminalde aşağıdaki komutlarla derleyip çalıştırabilirsiniz:

```bash
gcc -o sosyal_ag sosyal_ag.c
./sosyal_ag
```

## 📌 Özellikler

### ✅ Kullanıcı Yönetimi
- Kullanıcılar, `id` numaralarına göre Red-Black Tree yapısında sıralanarak depolanır.
- Kullanıcılar arasında çift yönlü arkadaşlık ilişkisi tanımlanabilir.

### ✅ Red-Black Tree
- Dengeli ağaç yapısı ile kullanıcı ekleme, arama ve sıralama işlemleri logaritmik zaman karmaşıklığında gerçekleştirilir.
- Ağaçta her ekleme işleminden sonra dengeleme algoritmaları çalıştırılır (`sola_dondur`, `saga_dondur`, `ekleme_duzelt`).

### ✅ Arkadaşlık Grafı
- Her kullanıcı, maksimum 100 arkadaş tutabilen bir listeye sahiptir.
- İki kullanıcı arasında kurulan ilişki çift yönlü olarak graf yapısında kaydedilir.

### ✅ Derinlik Öncelikli Arama (DFS)
- Belirli bir derinliğe kadar arkadaşlar listelenebilir.
- DFS algoritması kullanılarak etki alanı ve topluluk tespiti yapılır.

### ✅ Ortak Arkadaş Analizi
- İki kullanıcı arasında bulunan ortak arkadaşlar ekrana yazdırılır.

### ✅ Etki Alanı (Reachability)
- Bir kullanıcının 10 seviyeye kadar ulaşabileceği toplam kullanıcı sayısı hesaplanır ve yazdırılır.

### ✅ Topluluk Tespiti (Connected Components)
- Arkadaşlık ilişkilerine göre sosyal ağdaki ayrık topluluklar (connected components) belirlenir.

### ✅ Dosya Kaydı
- Program, kullanıcıları ve arkadaşlık ilişkilerini `veriseti.txt` adlı bir dosyaya yazar.
- Dosya sonunda terminale okunup gösterilir.

## 🧪 Örnek Kullanım Senaryosu

1. Program kaç kullanıcı ekleneceğini sorar.
2. Her kullanıcı için bir ID girilir.
3. Arkadaşlık ilişkileri çiftler halinde girilir.
4. DFS ile 2 derinliğe kadar arkadaşlar yazdırılır.
5. Ortak arkadaş analizi yapılacak iki ID girilir.
6. Bir kullanıcı için etki alanı hesaplanır.
7. Topluluklar belirlenir.
8. `veriseti.txt` dosyasının içeriği terminalde gösterilir.

## 📁 Örnek `veriseti.txt` Dosya Çıktısı

```text
# Kullanicilar
KULLANICI 1
KULLANICI 2
KULLANICI 3
KULLANICI 4

# Arkadaslik Iliskileri
ARKADAS 1 2
ARKADAS 2 3
ARKADAS 3 4
```

## 🧱 Dosya Yapısı

```
.
├── sosyal_ag.c           # Ana kaynak kod dosyası
├── veriseti.txt          # Program tarafından oluşturulan dosya
└── README.md             # Projeye dair detaylı açıklama (bu dosya)
```

## ❗ Notlar

- Maksimum kullanıcı sayısı `#define MAX_KULLANICI 100` ile sınırlandırılmıştır.
- Red-Black Tree uygulaması, kullanıcıların ID’lerine göre sıralı saklanması için kullanılır.
- DFS derinlik limiti etki alanı için 10, kullanıcı tanımlı DFS için değişkendir.
- Arkadaşlıklar çift yönlü (bidirectional) olarak eklenir.
- Kullanıcı ID’leri benzersiz olmalıdır.

## 👨‍💻 Katkı ve Geliştirme

Kod geliştirilmeye açıktır. Aşağıdaki ek özellikler ilerleyen sürümlerde eklenebilir:
- Kullanıcı silme işlemi.
- Arkadaş silme işlemi.
- BFS (Breadth-First Search) ile mesafe hesaplamaları.
- Dosyadan veri okuma ve yükleme.

## 📞 İletişim

Eğer bu projeyle ilgili önerileriniz veya katkılarınız varsa GitHub üzerinden pull request göndererek katkı sağlayabilirsiniz.

