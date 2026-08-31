🛡️ VaultX - Güvenli & Çevrimdışı Şifre Yöneticisi
VaultX, verilerinizi hiçbir bulut sunucusuna (Cloud) göndermeden, tamamen yerel diskinizde askeri sınıf şifreleme algoritmalarıyla koruyan modern bir şifre ve kimlik doğrulama (2FA) yöneticisidir.

Bulut tabanlı şifre yöneticilerindeki veri sızıntısı risklerine karşı geliştirilmiştir. Sadece size ait olan, çevrimdışı ve taşınabilir bir güvenlik kasasıdır.

✨ Temel Özellikler
🔒 Tamamen Çevrimdışı: Verileriniz asla internete yüklenmez. Sadece cihazınızdaki şifreli SQLite veritabanında (.db) saklanır.

📱 Benzersiz Mobil Kasa: Uygulama içindeki QR kod okuyucu sayesinde, kasanızın AES-256 GCM ile şifrelenmiş bir kopyasını telefonunuza indirebilir ve internet olmadan mobil cihazınızda şifrelerinizi görüntüleyebilirsiniz.

🔐 Dahili 2FA (TOTP) Desteği: Google Authenticator'a ihtiyaç duymadan, iki adımlı doğrulama kodlarınızı (TOTP) doğrudan VaultX üzerinden üretebilirsiniz.

🛡️ Gelişmiş Şifreleme: Fernet ve AES-GCM simetrik şifreleme algoritmaları, PBKDF2HMAC anahtar türetme ve SHA-256 hashing ile maksimum güvenlik.

🔑 Özel Kurtarma Anahtarı: Ana şifrenizi unutma ihtimalinize karşı, kasanıza erişebilmeniz için benzersiz bir Kurtarma Anahtarı (Recovery Key) altyapısı.

⏱️ Otomatik Kilit (Zaman Aşımı): Belirlenen süre boyunca fare/klavye hareketi algılanmazsa kasanız kendini otomatik olarak kilitler.

🎨 Modern Arayüz (UI): CustomTkinter ile geliştirilmiş karanlık/aydınlık mod destekli, akıcı ve şık kullanıcı deneyimi.

📝 Geçmiş & Ek Notlar: Eski şifrelerinizi görebilme ve her hesaba özel şifrelenmiş notlar ekleyebilme özelliği.

🏗️ Güvenlik Mimarisi
VaultX'in güvenlik yapısı "Sıfır Bilgi" (Zero-Knowledge) prensibine dayanır:

Ana Şifre (Master Password): Veritabanına hiçbir zaman açık metin olarak kaydedilmez. PBKDF2 algoritması ve rastgele üretilen bir Salt değeri ile 100.000 iterasyondan geçirilerek hashlenir.

Vault Key (Kasa Anahtarı): Şifreleri çözmek için gereken asıl anahtar, kullanıcının Ana Şifresi ile şifrelenerek (enc_vault_key_mp) saklanır.

Mobil Senkronizasyon: Kasa telefona aktarılırken veriler düz metin veya statik Base64 olarak değil, Web Crypto API (JavaScript) ve Python Cryptography (AES-256 GCM) arasında uçtan uca şifrelenerek taşınır.

📲 Mobil Senkronizasyon (Telefon ile Bağlantı)
VaultX'in en güçlü yanlarından biri olan Mobil Kasa'yı kullanmak için:

VaultX ana ekranından "Hesap Ayarları" (⚙️) menüsüne girin.

"QR ile Mobil Kasa İndir" butonuna tıklayın.

Çıkan QR kodu telefonunuzun kamerasıyla okutun ve açılan çevrimdışı HTML dosyasını cihazınıza kaydedin (iOS Kestirmeler veya Android Tarayıcı ile Ana Ekrana Ekle).

Mobil arayüzde kendinize yerel bir PIN belirleyin ve kasanızı cebinizde taşıyın!
