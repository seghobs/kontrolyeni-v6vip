# Kontrol v4 Yeni (Premium Instagram Automation & Analysis)

Kontrol v4 Yeni, en güncel **Shadcn Zinc Pure Dark** tasarım diliyle yeniden inşa edilmiş, gelişmiş bir Instagram Otomasyon, Yorum/Beğeni Kontrol ve Token Yönetim platformudur. Orijinal Instagram mobil uygulamasının (Android) API başlıklarını ve session yönetimini birebir taklit ederek çalışan, oldukça kararlı, güvenli ve estetik bir sistemdir.

## 🚀 Proje Ne İşe Yarıyor?
Bu proje, **Instagram yardımlaşma ve etkileşim gruplarını** profesyonel bir düzeyde yönetmek için tasarlanmıştır. Üyelerin görevlerini (beğeni/yorum) yapıp yapmadıklarını saniyeler içinde tespit eder.

*   **Toplu Beğeni ve Yorum Denetimi:** Birden fazla gönderiyi aynı anda tarar, kimin eksik olduğunu detaylı raporlar.
*   **Kopya Yorum Tespiti:** "Toplu Kontrol" modunda, kullanıcıların farklı postlara aynı (kopyala-yapıştır) yorumu atıp atmadığını otomatik belirler ve uyarır.
*   **Favori Gruplar:** Sık kullandığınız Instagram gruplarını favoriye ekleyerek listenin en üstünde tutabilirsiniz.
*   **Premium UI/UX:** Shadcn UI Zinc teması, cam dokulu (glassmorphism) bileşenler ve yumuşak animasyonlarla donatılmış modern arayüz.
*   **DM Grubu Entegrasyonu:** Bağlı hesapların bulunduğu grupları otomatik tespit eder, üye listelerini ve paylaşılan postları anında çeker.

---

## ✨ Yeni Nesil Özellikler (v4)
-   **Shadcn Zinc Design:** Saf siyah (#09090b) arka plan ve yüksek kaliteli tipografi ile premium bir deneyim.
*   **Gelişmiş Animasyonlar:** Sayfa geçişleri ve modal açılışlarında `cubic-bezier` tabanlı pürüzsüz geçiş efektleri.
*   **Kopya Yorum Analizi:** Toplu kontrollerde aynı metni kullanan "spam" davranışlarını anında yakalar.
*   **Favori Yönetimi:** Grupları favorileyerek zaman tasarrufu sağlar (LocalStorage tabanlı).
*   **Failover Mekanizması:** Instagram'ın `429` (Rate Limit) veya `403` hatalarını akıllıca yönetir, sadece gerçek oturum kayıplarında token'ı pasife alır.

---

## 🛠️ Kurulum

### Tek Komutla Kurulum (Linux/Bash/PythonAnywhere)
```bash
bash -c "$(curl -sL https://raw.githubusercontent.com/seghobs/kontrolyeni-v4/main/setup.sh)"
```

### Manuel Kurulum
```bash
git clone https://github.com/seghobs/kontrolyeni-v4.git kontrol
cd kontrol
pip install -r requirements.txt
python flask_app.py
```

---

## 💻 Kullanım
Sunucu veya lokal makinede projeyi başlattıktan sonra:

**Ana Kontrol Paneli:**
```text
http://localhost:5000
```

**Admin Paneli (Token & Muafiyetler):**
```text
http://localhost:5000/admin
```

---

## 📁 Proje Yapısı
-   `flask_app.py`: Uygulamanın giriş noktası.
-   `app_core/`: Sistemin mantıksal çekirdeği (Routes, API, Storage).
-   `static/css/`: Shadcn Zinc tabanlı modern stil dosyaları.
-   `static/js/`: Dinamik arama, sürükle-bırak (SortableJS) ve favorileme mantığı.
-   `templates/`: Modernize edilmiş Jinja2 HTML şablonları.

---

## 🔒 Güvenlik Notu
Bu proje eğitim ve analiz amaçlıdır. Instagram kullanım koşullarına uygun şekilde kullanılması kullanıcının sorumluluğundadır. Verileriniz (Tokenlar, muafiyetler) yerel bir SQLite veritabanında (`app.db`) şifrelenmiş veya güvenli şekilde saklanır.
