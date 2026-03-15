

# Etüt Merkezi Öğrenci Bilgi Sistemi – Veritabanı Projesi

Bu proje, bir üniversiteye bağlı etüt merkezinde kullanılmak üzere geliştirilmiş kapsamlı bir **ilişkisel veritabanı yönetim sistemi otomasyonudur**. Sistem, öğrencilerin ve eğitmenlerin etüt süreçlerini dijital ortama taşıyarak veri bütünlüğü ve operasyonel verimlilik sağlar.

---

## 🎯 Proje Amacı ve Kapsamı

Sistem; öğrencilerin etüt rezervasyonları yapabilmesini, eğitmenlerle gerçekleştirilen oturumların yönetilmesini, ders içeriklerinin takibini, katılım yoklamalarının tutulmasını, geri bildirimlerin toplanmasını ve ödeme işlemlerinin güvenli bir şekilde saklanmasını sağlar.

---

## 🏗️ Veritabanı Mimarisi

Projede sağlam bir **Varlık-İlişki (E-R) modeli** kullanılmıştır. Temel varlıklar:

| Varlık | Açıklama |
|--------|----------|
| **Öğrenciler** | Kimlik, iletişim ve akademik bölüm bilgileri |
| **Eğitmenler** | Uzmanlık alanları, iletişim bilgileri ve fakülte bilgileri |
| **Dersler** | Ders kodları, kredi bilgileri, dönem bilgileri |
| **Etüt Oturumları** | Tarih, saat, süre ve kontenjan bilgileri |
| **Etüt Rezervasyonları** | Oturumlara kayıt olan öğrenciler |
| **Katılım Bilgileri** | Öğrencilerin fiilen katıldığı oturumlar |
| **Ödemeler** | Katılım sonrası finansal işlemler |
| **Geri Bildirimler** | Ders ve eğitmen performansına yönelik değerlendirmeler |

---

## ⚙️ Teknik Detaylar ve Gelişmiş Özellikler

### 1. Normalizasyon Süreci
- Tablolar **1NF, 2NF ve 3NF kurallarına** uygun olarak tasarlanmıştır.  
- Veri tekrarını önlemek ve veri bütünlüğünü sağlamak için çok değerli (multi-valued) alanlar ayrıştırılmış ve atomik hâle getirilmiştir.

### 2. Saklı Yordamlar (Stored Procedures)
Sistem işlevselliğini optimize etmek için dinamik saklı yordamlar kullanılmıştır:

| Yordam | Açıklama |
|--------|----------|
| `GetStudentInfo` | Belirli bir öğrencinin tüm detaylı bilgilerini getirir |
| `GetInstructorSchedule` | Eğitmenin ders programı ve oturum bilgilerini listeler |
| `GetSessionReservations` | Oturuma ait rezervasyon ve kontenjan detaylarını sunar |
| `GetStudentPaymentInfo` | Öğrencinin geçmiş ödeme hareketlerini listeler |

### 3. Tetikleyiciler (Triggers)
Veritabanı iş kurallarını otomatikleştirmek için çeşitli tetikleyiciler geliştirilmiştir:

- **Otomatik E-posta:** Yeni öğrenci kaydı eklendiğinde hoş geldiniz mesajı gönderir.  
- **Kontenjan Kontrolü:** Ders kaydı sırasında kontenjan dolmuşsa exception fırlatır.  
- **Ödeme Durumu Güncelleme:** Yeni ödeme girildiğinde öğrencinin derse ait statüsü "Ödendi" olarak güncellenir.  
- **Dinamik Memnuniyet Puanı:** Yeni geri bildirim girildiğinde eğitmen ve ders için ortalama puan anlık olarak güncellenir.  
- **Otomatik Kontenjan Düşümü:** Ders kaydı yapıldığında oturum katılımcı sayısı otomatik artırılır.

---

## 💻 Kullanım

1. Projeyi bilgisayarınıza klonlayın.  
2. SQL istemcinizde (SQL Server Management Studio, MySQL Workbench vb.) yeni bir sorgu penceresi açın.  
3. `CREATE DATABASE` ve tablo oluşturma scriptlerini çalıştırarak veritabanı şemasını oluşturun.  
4. `INSERT` sorgularını çalıştırarak test verilerini yükleyin.  
5. Prosedür ve tetikleyici scriptlerini derleyerek otomasyonu aktif hâle getirin.

> Terminal veya GUI üzerinde tüm başarılı işlem çıktıları ve hata testleri dokümantasyonda mevcuttur.

---

## 👩‍💻 Geliştirici

**Fatma Betül Pehlivan**  
Selçuk Üniversitesi – Teknoloji Fakültesi  
Bilgisayar Mühendisliği Bölümü  

---

## 📂 Alternatif Erişim (Opsiyonel)


Bu projenin detaylı raporu aşağıdaki bağlantılardan erişilebilir:

📄 Google Drive üzerinden görüntülemek için:

📄 Detaylı proje raporu: https://drive.google.com/file/d/1zc0E1d5bXWWKiSOGSsaz5OyiodPmXl8t/view?usp=sharing

📄 GitHub üzerinden indirmek için:
Eğer GitHub sayfasında PDF ön izleme açılmazsa, dosya sayfasındaki "Download" veya "View Raw" seçeneğini kullanarak dosyayı indirip görüntüleyebilirsiniz.

