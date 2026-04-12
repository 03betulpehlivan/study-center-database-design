Student Study Center Information System – Database Project

This project is a comprehensive relational database management system (automation) developed for use in a university-affiliated study center. The system digitizes student and instructor study processes, ensuring data integrity and operational efficiency.

🎯 Project Objective and Scope

The system enables students to make study session reservations, manage sessions conducted with instructors, track course content, record attendance, collect feedback, and securely store payment transactions.

🏗️ Database Architecture

A robust Entity-Relationship (E-R) model was used in the project. The main entities are:

Entity	Description
Students	Identity, contact, and academic department information
Instructors	Areas of expertise, contact details, and faculty information
Courses	Course codes, credit information, semester details
Study Sessions	Date, time, duration, and capacity information
Session Reservations	Students enrolled in sessions
Attendance Records	Students who actually attended sessions
Payments	Financial transactions after attendance
Feedback	Evaluations of course and instructor performance
⚙️ Technical Details and Advanced Features
1. Normalization Process

Tables were designed according to 1NF, 2NF, and 3NF normalization rules.
To ensure data integrity and eliminate redundancy, multi-valued attributes were decomposed into atomic structures.

2. Stored Procedures

Dynamic stored procedures were implemented to optimize system functionality:

Procedure	Description
GetStudentInfo	Retrieves detailed information of a specific student
GetInstructorSchedule	Lists instructor’s course schedule and session information
GetSessionReservations	Shows reservation and capacity details for a session
GetStudentPaymentInfo	Displays a student’s payment history
3. Triggers

Several database triggers were developed to automate business rules:

Automatic Email: Sends a welcome email when a new student is added
Capacity Control: Raises an exception if course capacity is full during enrollment
Payment Status Update: Updates student status to “Paid” after a new payment
Dynamic Satisfaction Score: Updates average rating for instructors and courses when new feedback is added
Automatic Capacity Update: Increases participant count when a new reservation is made
💻 Usage
Clone the project to your computer
Open a query window in an SQL client (SQL Server Management Studio, MySQL Workbench, etc.)
Run CREATE DATABASE and table creation scripts to build the schema
Insert test data using INSERT queries
Compile and execute stored procedures and triggers to activate automation

All successful operations and error test outputs are documented in the project.

👩‍💻 Developer

Fatma Betül Pehlivan
Selçuk University – Faculty of Technology
Department of Computer Engineering

📂 Alternative Access

The detailed project report can be accessed via the links below:

📄 Google Drive:
https://drive.google.com/file/d/1zc0E1d5bXWWKiSOGSsaz5OyiodPmXl8t/view?usp=sharing

📄 GitHub:
If the PDF preview does not open on GitHub, use the “Download” or “View Raw” option on the file page to download and view it.


TÜRKÇE*****

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

