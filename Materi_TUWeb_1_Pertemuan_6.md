# 📚 Materi TUWeb 1 – Pertemuan 6  
## 🌐 Fundamental HTML, CSS, dan JavaScript DOM  
**🎯 Studi Kasus Praktis: Aplikasi Pemesanan Bahan Ajar SITTA Universitas Terbuka**

---

## 📋 **Overview Pertemuan**

Pertemuan ini adalah fondasi dari pemrograman berbasis web modern. Kita akan mempelajari tiga pilar utama pengembangan web:
- **HTML5** untuk struktur konten yang semantik
- **CSS3** untuk desain visual yang menarik dan responsif
- **JavaScript DOM** untuk interaktivitas dan manipulasi dinamis

**🎯 Metode Pembelajaran:** Learning by Doing dengan studi kasus nyata aplikasi SITTA

---

## 🎯 **Tujuan Pembelajaran (Capaian Pembelajaran)**

### 🎓 **Kompetensi Utama**
Setelah mengikuti pertemuan ini, mahasiswa diharapkan mampu:

#### 📝 **Kognitif (Pengetahuan)**
- ✅ Menjelaskan konsep HTML5 semantic dan struktur dokumen yang valid
- ✅ Memahami prinsip CSS3 dan metode styling (inline, internal, external)
- ✅ Mengidentifikasi konsep DOM (Document Object Model) dan manipulasi JavaScript
- ✅ Menganalisis best practices dalam pengembangan web modern

#### 🛠️ **Psikomotorik (Keterampilan)**
- ✅ Membuat struktur HTML5 yang semantik dan valid W3C
- ✅ Mengimplementasikan CSS3 dengan berbagai teknik styling
- ✅ Menggunakan JavaScript untuk manipulasi DOM yang efektif
- ✅ Membangun form dengan validasi yang komprehensif
- ✅ Mengintegrasikan ketiga teknologi dalam satu aplikasi fungsional

#### 💡 **Afektif (Sikap)**
- ✅ Menghargai pentingnya kode yang bersih dan terstruktur
- ✅ Mengembangkan mindset problem-solving dalam pengembangan web
- ✅ Menunjukkan etika dalam penggunaan teknologi web

---

## 🗓️ **Struktur Pembelajaran**

| ⏰ Waktu | 📂 Topik | 🎯 Aktivitas | 📝 Output |
|---------|----------|-------------|-----------|
| 30 menit | **HTML5 Fundamentals** | Teori + Demo | Struktur HTML semantik |
| 45 menit | **CSS3 Styling** | Praktik langsung | Desain responsif |
| 60 menit | **JavaScript DOM** | Hands-on coding | Interaktivitas dinamis |
| 45 menit | **Integrasi SITTA** | Studi kasus | Aplikasi lengkap |

---

## 📚 **Materi Pembelajaran Detail**

### 📖 **MATERI 1: HTML5 SEMANTIK DAN VALID**

---

## 📖 **Materi 1: HTML Semantik dan Valid**

#### 🔍 **Konsep HTML Semantik**

**📖 Definisi:** HTML semantik adalah penggunaan tag HTML yang sesuai dengan makna dan tujuan konten, bukan hanya untuk tampilan visual.

**🎯 Mengapa HTML Semantik Penting?**

| 💡 Manfaat | 📝 Penjelasan | 🌟 Contoh Implementasi |
|-----------|-------------|---------------------|
| **SEO Friendly** | Mesin pencari lebih mudah memahami struktur konten | `<article>` untuk konten utama, `<nav>` untuk navigasi |
| **Accessibility** | Screen reader bisa membaca dengan lebih baik | `<header>`, `<footer>`, `<main>` untuk landmark |
| **Maintainability** | Kode lebih mudah dibaca dan dikelola | Struktur yang jelas dan terorganisir |
| **Future-Proof** | Siap untuk teknologi web masa depan | HTML5 elements yang modern |

#### 🏗️ **Struktur Dokumen HTML5 Lengkap**

**📋 Komponen Essensial:**

```html
<!DOCTYPE html>                              <!-- Deklarasi tipe dokumen -->
<html lang="id">                             <!-- Bahasa utama konten -->
<head>                                       <!-- Metadata dokumen -->
    <meta charset="UTF-8">                   <!-- Encoding karakter -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0"> <!-- Responsif -->
    <meta name="description" content="SITTA - Sistem Informasi Tiras dan Transaksi Bahan Ajar Universitas Terbuka"> <!-- SEO -->
    <meta name="author" content="Universitas Terbuka"> <!-- Author -->
    <meta name="keywords" content="bahan ajar, universitas terbuka, SITTA"> <!-- Keywords -->
    <title>SITTA - Pemesanan Bahan Ajar | Universitas Terbuka</title> <!-- Judul halaman -->
    
    <!-- Favicon -->
    <link rel="icon" href="favicon.ico" type="image/x-icon">
    
    <!-- External CSS -->
    <link rel="stylesheet" href="css/style.css">
</head>
<body>                                       <!-- Konten visible -->
    
    <!-- Header Section -->
    <header class="site-header">
        <div class="container">
            <h1 class="logo">📚 SITTA</h1>
            <p class="tagline">Sistem Informasi Tiras dan Transaksi Bahan Ajar</p>
        </div>
    </header>
    
    <!-- Navigation -->
    <nav class="main-navigation" role="navigation" aria-label="Main navigation">
        <div class="container">
            <ul class="nav-menu">
                <li><a href="#beranda" class="nav-link active">🏠 Beranda</a></li>
                <li><a href="#stok" class="nav-link">📦 Stok Bahan Ajar</a></li>
                <li><a href="#tracking" class="nav-link">📍 Tracking Pesanan</a></li>
                <li><a href="#kontak" class="nav-link">📞 Kontak</a></li>
            </ul>
        </div>
    </nav>
    
    <!-- Main Content -->
    <main class="main-content" role="main">
        <div class="container">
            
            <!-- Hero Section -->
            <section id="beranda" class="hero-section" aria-labelledby="hero-title">
                <h2 id="hero-title">Selamat Datang di SITTA</h2>
                <p class="hero-description">
                    Platform digital untuk pemesanan bahan ajar Universitas Terbuka
                </p>
                
                <!-- Call to Action -->
                <div class="cta-container">
                    <button class="cta-button primary" onclick="scrollToSection('stok')">
                        🛒 Mulai Pemesanan
                    </button>
                    <button class="cta-button secondary" onclick="showInfo()">
                        ℹ️ Informasi Lebih Lanjut
                    </button>
                </div>
            </section>
            
            <!-- Featured Products Section -->
            <section id="stok" class="products-section" aria-labelledby="products-title">
                <h2 id="products-title">📦 Stok Bahan Ajar Tersedia</h2>
                
                <!-- Product Grid -->
                <div class="products-grid" id="products-container">
                    <!-- Konten akan di-generate dengan JavaScript -->
                </div>
            </section>
            
            <!-- Information Section -->
            <section class="info-section" aria-labelledby="info-title">
                <h2 id="info-title">ℹ️ Informasi Penting</h2>
                
                <div class="info-grid">
                    <article class="info-card">
                        <h3>🚚 Pengiriman Gratis</h3>
                        <p>Gratis ongkir untuk pembelian minimal 5 buku dalam satu kali transaksi.</p>
                    </article>
                    
                    <article class="info-card">
                        <h3>💰 Harga Terjangkau</h3>
                        <p>Dapatkan bahan ajar berkualitas dengan harga subsidi dari Universitas Terbuka.</p>
                    </article>
                    
                    <article class="info-card">
                        <h3>📚 Koleksi Lengkap</h3>
                        <p>Akses ribuan judul bahan ajar dari berbagai program studi.</p>
                    </article>
                </div>
            </section>
            
        </div>
    </main>
    
    <!-- Sidebar (Optional) -->
    <aside class="sidebar" role="complementary" aria-label="Sidebar">
        <div class="sidebar-widget">
            <h3>📊 Statistik</h3>
            <div class="stats">
                <p>Total Bahan Ajar: <strong>1,247</strong></p>
                <p>Pengguna Aktif: <strong>5,832</strong></p>
                <p>Pesanan Hari Ini: <strong>127</strong></p>
            </div>
        </div>
    </aside>
    
    <!-- Footer -->
    <footer class="site-footer" role="contentinfo">
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>Tentang SITTA</h3>
                    <p>Sistem Informasi Tiras dan Transaksi Bahan Ajar Universitas Terbuka</p>
                </div>
                
                <div class="footer-section">
                    <h3>Link Cepat</h3>
                    <ul>
                        <li><a href="#beranda">Beranda</a></li>
                        <li><a href="#stok">Stok Bahan Ajar</a></li>
                        <li><a href="#tracking">Tracking</a></li>
                    </ul>
                </div>
                
                <div class="footer-section">
                    <h3>Kontak</h3>
                    <p>📧 sitta@ut.ac.id</p>
                    <p>📞 (021) 7490941</p>
                    <p>📍 Jakarta, Indonesia</p>
                </div>
            </div>
            
            <div class="footer-bottom">
                <p>&copy; 2025 Universitas Terbuka. All rights reserved.</p>
            </div>
        </div>
    </footer>
    
</body>
</html>
```

#### 📝 **Penjelasan Detail Setiap Element**

| 🏷️ Tag | 📝 Fungsi | 🎯 Penggunaan di SITTA | ✅ Best Practice |
|--------|-----------|---------------------|-----------------|
| `<!DOCTYPE html>` | Deklarasi dokumen HTML5 | Standar modern | Selalu di awal dokumen |
| `<html lang="id">` | Bahasa konten | Bahasa Indonesia | Penting untuk SEO & accessibility |
| `<head>` | Metadata | Info dokumen, CSS, JS | Tidak visible di browser |
| `<meta charset="UTF-8">` | Encoding karakter | Support huruf Indonesia | Wajib untuk multi-bahasa |
| `<meta name="viewport">` | Responsif | Mobile-friendly | Essential untuk mobile |
| `<title>` | Judul halaman | SEO dan browser tab | Unik dan deskriptif |
| `<header>` | Header situs | Logo dan navigasi utama | Landmark element |
| `<nav>` | Navigasi | Menu utama | Gunakan ARIA labels |
| `<main>` | Konten utama | Konten unik halaman | Hanya satu per halaman |
| `<section>` | Bagian konten | Hero, produk, info | Grouping related content |
| `<article>` | Konten mandiri | Card produk, artikel | Standalone content |
| `<aside>` | Sidebar/konten tambahan | Statistik, info | Complementary content |
| `<footer>` | Footer situs | Copyright, kontak | Closing information |

#### 🎯 **Latihan Praktis 1: Membuat Struktur HTML SITTA**

**📋 Instruksi Langkah-demi-Langkah:**

1. **Buat file baru** bernama `index.html`
2. **Copy struktur HTML5** di atas
3. **Simpan dan buka di browser**
4. **Inspect dengan Developer Tools** (F12)
5. **Analisis struktur semantic** yang telah dibuat

**🔍 Checklist Validasi:**
- [ ] DOCTYPE declaration ada
- [ ] Lang attribute sesuai
- [ ] Meta charset UTF-8
- [ ] Meta viewport untuk responsif
- [ ] Title yang deskriptif
- [ ] Semantic tags digunakan dengan benar
- [ ] ARIA labels untuk accessibility
- [ ] Struktur heading yang hierarkis (h1 → h2 → h3)

#### 🛠️ **Hands-On Lab 1: Membuat Struktur HTML SITTA**

**🎯 Tujuan:** Menerapkan konsep HTML5 semantic dalam proyek nyata

**📋 Langkah Praktik:**

**Step 1: Setup Project**
```bash
# Buat folder project
mkdir tugas1-sitta
cd tugas1-sitta

# Buat struktur folder
mkdir css js img
```

**Step 2: Buat File HTML**
```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="SITTA - Sistem Informasi Tiras dan Transaksi Bahan Ajar Universitas Terbuka">
    <meta name="author" content="Universitas Terbuka">
    <meta name="keywords" content="bahan ajar, universitas terbuka, SITTA, pemesanan online">
    <title>SITTA - Pemesanan Bahan Ajar | Universitas Terbuka</title>
    
    <!-- External CSS -->
    <link rel="stylesheet" href="css/style.css">
    
    <!-- Favicon -->
    <link rel="icon" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><text y='.9em' font-size='90'>📚</text></svg>">
</head>
<body>
    <!-- Skip to content link untuk accessibility -->
    <a href="#main-content" class="skip-link">Skip to main content</a>
    
    <!-- Header dengan branding -->
    <header class="site-header" role="banner">
        <div class="container">
            <div class="header-content">
                <div class="branding">
                    <h1 class="logo">📚 SITTA</h1>
                    <p class="tagline">Sistem Informasi Tiras dan Transaksi Bahan Ajar</p>
                    <p class="institution">Universitas Terbuka</p>
                </div>
                
                <!-- User actions -->
                <div class="user-actions">
                    <button class="btn-login" aria-label="Login">👤 Masuk</button>
                    <button class="btn-register" aria-label="Register">📝 Daftar</button>
                </div>
            </div>
        </div>
    </header>
    
    <!-- Navigasi utama -->
    <nav class="main-navigation" role="navigation" aria-label="Main navigation">
        <div class="container">
            <ul class="nav-menu">
                <li><a href="#beranda" class="nav-link active" aria-current="page">🏠 Beranda</a></li>
                <li><a href="#stok" class="nav-link">📦 Stok Bahan Ajar</a></li>
                <li><a href="#tracking" class="nav-link">📍 Tracking Pesanan</a></li>
                <li><a href="#bantuan" class="nav-link">❓ Bantuan</a></li>
                <li><a href="#kontak" class="nav-link">📞 Kontak</a></li>
            </ul>
            
            <!-- Mobile menu toggle -->
            <button class="mobile-menu-toggle" aria-label="Toggle mobile menu">
                <span class="hamburger-line"></span>
                <span class="hamburger-line"></span>
                <span class="hamburger-line"></span>
            </button>
        </div>
    </nav>
    
    <!-- Main content area -->
    <main id="main-content" class="main-content" role="main">
        <div class="container">
            
            <!-- Hero Section -->
            <section id="beranda" class="hero-section" aria-labelledby="hero-heading">
                <div class="hero-content">
                    <h2 id="hero-heading" class="hero-title">
                        Selamat Datang di SITTA
                    </h2>
                    <p class="hero-subtitle">
                        Platform digital untuk pemesanan bahan ajar Universitas Terbuka
                    </p>
                    <p class="hero-description">
                        Dapatkan modul kuliah berkualitas dengan mudah, cepat, dan terjangkau
                    </p>
                    
                    <!-- Call to Action Buttons -->
                    <div class="cta-container">
                        <button class="cta-button primary" onclick="scrollToSection('stok')">
                            🛒 Mulai Pemesanan
                        </button>
                        <button class="cta-button secondary" onclick="showVideoGuide()">
                            🎥 Panduan Video
                        </button>
                    </div>
                </div>
                
                <!-- Hero Image/Illustration -->
                <div class="hero-visual">
                    <img src="img/hero-illustration.svg" alt="Ilustrasi platform SITTA" class="hero-image">
                </div>
            </section>
            
            <!-- Features Section -->
            <section class="features-section" aria-labelledby="features-heading">
                <h2 id="features-heading" class="section-title">🌟 Fitur Unggulan</h2>
                
                <div class="features-grid">
                    <article class="feature-card">
                        <div class="feature-icon">📚</div>
                        <h3 class="feature-title">Koleksi Lengkap</h3>
                        <p class="feature-description">
                            Akses ribuan modul kuliah dari berbagai program studi Universitas Terbuka
                        </p>
                        <a href="#stok" class="feature-link">Jelajahi Koleksi →</a>
                    </article>
                    
                    <article class="feature-card">
                        <div class="feature-icon">🚀</div>
                        <h3 class="feature-title">Pengiriman Cepat</h3>
                        <p class="feature-description">
                            Pesanan diproses dan dikirim dalam waktu 24 jam ke seluruh Indonesia
                        </p>
                        <a href="#tracking" class="feature-link">Track Pesanan →</a>
                    </article>
                    
                    <article class="feature-card">
                        <div class="feature-icon">📱</div>
                        <h3 class="feature-title">Mudah Diakses</h3>
                        <p class="feature-description">
                            Platform responsif yang bisa diakses dari berbagai perangkat
                        </p>
                        <a href="#bantuan" class="feature-link">Cara Menggunakan →</a>
                    </article>
                    
                    <article class="feature-card">
                        <div class="feature-icon">💰</div>
                        <h3 class="feature-title">Harga Terjangkau</h3>
                        <p class="feature-description">
                            Dapatkan bahan ajar berkualitas dengan harga subsidi dari UT
                        </p>
                        <a href="#kontak" class="feature-link">Info Harga →</a>
                    </article>
                </div>
            </section>
            
            <!-- Products Section -->
            <section id="stok" class="products-section" aria-labelledby="products-heading">
                <div class="section-header">
                    <h2 id="products-heading" class="section-title">📦 Stok Bahan Ajar Tersedia</h2>
                    <p class="section-subtitle">
                        Temukan bahan ajar yang Anda butuhkan untuk mendukung perkuliahan
                    </p>
                </div>
                
                <!-- Search and Filter -->
                <div class="search-filter-container">
                    <div class="search-box">
                        <input 
                            type="search" 
                            id="search-input"
                            placeholder="Cari bahan ajar..." 
                            aria-label="Cari bahan ajar"
                            class="search-input"
                        >
                        <button class="search-button" aria-label="Cari">🔍</button>
                    </div>
                    
                    <div class="filter-options">
                        <select id="category-filter" class="filter-select" aria-label="Filter kategori">
                            <option value="">Semua Kategori</option>
                            <option value="bmp">BMP</option>
                            <option value="modul">Modul Praktikum</option>
                            <option value="referensi">Buku Referensi</option>
                        </select>
                        
                        <select id="sort-filter" class="filter-select" aria-label="Urutkan">
                            <option value="nama">Urutkan: Nama</option>
                            <option value="stok">Urutkan: Stok</option>
                            <option value="harga">Urutkan: Harga</option>
                        </select>
                    </div>
                </div>
                
                <!-- Products Grid -->
                <div id="daftar-bahan-ajar" class="products-grid" role="region" aria-label="Daftar bahan ajar">
                    <!-- Konten akan di-generate dengan JavaScript -->
                    <div class="loading-placeholder">
                        <p>🔄 Memuat data bahan ajar...</p>
                    </div>
                </div>
                
                <!-- Load More Button -->
                <div class="load-more-container">
                    <button class="load-more-button" onclick="loadMoreProducts()">
                        Muat Lebih Banyak
                    </button>
                </div>
            </section>
            
            <!-- Statistics Section -->
            <section class="statistics-section" aria-labelledby="stats-heading">
                <h2 id="stats-heading" class="section-title">📊 Statistik Platform</h2>
                
                <div class="stats-grid">
                    <div class="stat-card">
                        <div class="stat-number" data-target="1247">0</div>
                        <div class="stat-label">Total Bahan Ajar</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number" data-target="5832">0</div>
                        <div class="stat-label">Pengguna Aktif</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number" data-target="98">0</div>
                        <div class="stat-label">% Kepuasan</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number" data-target="24">0</div>
                        <div class="stat-label">Jam Pengiriman</div>
                    </div>
                </div>
            </section>
            
        </div>
    </main>
    
    <!-- Footer -->
    <footer class="site-footer" role="contentinfo">
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3 class="footer-title">Tentang SITTA</h3>
                    <p class="footer-description">
                        Sistem Informasi Tiras dan Transaksi Bahan Ajar adalah platform resmi 
                        Universitas Terbuka untuk pemesanan bahan ajar digital.
                    </p>
                    <div class="social-links">
                        <a href="#" aria-label="Facebook">📘</a>
                        <a href="#" aria-label="Twitter">🐦</a>
                        <a href="#" aria-label="Instagram">📷</a>
                        <a href="#" aria-label="YouTube">📺</a>
                    </div>
                </div>
                
                <div class="footer-section">
                    <h3 class="footer-title">Link Cepat</h3>
                    <nav class="footer-nav" aria-label="Footer navigation">
                        <ul>
                            <li><a href="#beranda">Beranda</a></li>
                            <li><a href="#stok">Stok Bahan Ajar</a></li>
                            <li><a href="#tracking">Tracking Pesanan</a></li>
                            <li><a href="#bantuan">Bantuan</a></li>
                            <li><a href="#kontak">Kontak</a></li>
                        </ul>
                    </nav>
                </div>
                
                <div class="footer-section">
                    <h3 class="footer-title">Kontak Kami</h3>
                    <div class="contact-info">
                        <p class="contact-item">
                            <span class="contact-icon">📍</span>
                            Jl. Pamulang Permai IV, Tangerang Selatan
                        </p>
                        <p class="contact-item">
                            <span class="contact-icon">📧</span>
                            sitta@ut.ac.id
                        </p>
                        <p class="contact-item">
                            <span class="contact-icon">📞</span>
                            (021) 7490941
                        </p>
                        <p class="contact-item">
                            <span class="contact-icon">⏰</span>
                            Senin - Jumat, 08:00 - 16:00 WIB
                        </p>
                    </div>
                </div>
            </div>
            
            <div class="footer-bottom">
                <p class="copyright">
                    &copy; 2025 Universitas Terbuka. All rights reserved. | 
                    <a href="#privacy">Privacy Policy</a> | 
                    <a href="#terms">Terms of Service</a>
                </p>
            </div>
        </div>
    </footer>
    
    <!-- Back to Top Button -->
    <button id="back-to-top" class="back-to-top" aria-label="Back to top">
        ↑
    </button>
    
    <!-- JavaScript -->
    <script src="js/data.js"></script>
    <script src="js/app.js"></script>
</body>
</html>
```

**🔍 Validation Checklist:**
- [ ] Semantic HTML5 tags digunakan dengan benar
- [ ] ARIA labels untuk accessibility
- [ ] Meta tags untuk SEO
- [ ] Responsive viewport meta
- [ ] Proper heading hierarchy
- [ ] Alt text untuk images
- [ ] Skip navigation link
- [ ] Semantic form controls

---

## 🎨 **MATERI 2: CSS3 - STYLING YANG MODERN DAN RESPONSIF**

### 🎯 **Konsep Dasar CSS3**

**📖 Definisi:** CSS (Cascading Style Sheets) adalah bahasa stylesheet yang digunakan untuk mengatur tampilan dan layout halaman web. CSS3 adalah versi terbaru dengan fitur-fitur modern.

**🌟 Mengapa CSS3 Penting?**
- **Separation of Concerns**: Memisahkan struktur (HTML) dari presentasi (CSS)
- **Consistency**: Tampilan konsisten di seluruh halaman
- **Maintainability**: Mudah maintenance dan update
- **Performance**: Loading lebih cepat dengan caching
- **Responsiveness**: Support untuk berbagai device dan screen size

### 📋 **3 Metode Implementasi CSS**

#### 1️⃣ **Inline CSS** 
**📍 Kapan Digunakan:** Testing cepat, email templates, atau styling spesifik element

**✅ Kelebihan:**
- Quick prototyping
- Specificity tinggi
- Tidak perlu file tambahan

**❌ Kekurangan:**
- Sulit di-maintain
- Tidak reusable
- Mixing concerns

**💡 Contoh Implementasi:**
```html
<!-- Inline CSS untuk styling spesifik -->
<div style="
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    padding: 2rem;
    border-radius: 15px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.2);
    text-align: center;
    color: white;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
">
    <h1 style="
        font-size: 2.5rem;
        margin-bottom: 1rem;
        text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
    ">
        🎨 Styling dengan Inline CSS
    </h1>
    <p style="
        font-size: 1.1rem;
        opacity: 0.9;
        line-height: 1.6;
    ">
        Inline CSS cocok untuk testing dan styling spesifik
    </p>
</div>
```

#### 2️⃣ **Internal CSS**
**📍 Kapan Digunakan:** Single page application, styling spesifik halaman

**✅ Kelebihan:**
- Organized dalam satu file
- Specificity baik
- Tidak perlu HTTP request tambahan

**❌ Kekurangan:**
- Tidak reusable antar halaman
- File HTML menjadi besar

**💡 Contoh Implementasi:**
```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Internal CSS Example</title>
    
    <!-- Internal CSS -->
    <style>
        /* CSS Reset */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        /* CSS Variables untuk konsistensi */
        :root {
            --primary-color: #2c3e50;
            --secondary-color: #3498db;
            --accent-color: #e74c3c;
            --success-color: #27ae60;
            --warning-color: #f39c12;
            --light-color: #ecf0f1;
            --dark-color: #2c3e50;
            --font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            --border-radius: 8px;
            --transition: all 0.3s ease;
            --shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            --shadow-hover: 0 8px 15px rgba(0, 0, 0, 0.2);
        }
        
        /* Base Styles */
        body {
            font-family: var(--font-family);
            line-height: 1.6;
            color: var(--dark-color);
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 2rem;
        }
        
        /* Container */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: white;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow-hover);
            overflow: hidden;
        }
        
        /* Header Styles */
        .header {
            background: var(--primary-color);
            color: white;
            padding: 2rem;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .header::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
            animation: pulse 4s ease-in-out infinite;
        }
        
        @keyframes pulse {
            0%, 100% { transform: scale(1); opacity: 0.5; }
            50% { transform: scale(1.1); opacity: 0.8; }
        }
        
        .header h1 {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
            position: relative;
            z-index: 1;
        }
        
        .header p {
            font-size: 1.2rem;
            opacity: 0.9;
            position: relative;
            z-index: 1;
        }
        
        /* Button Styles */
        .btn {
            display: inline-block;
            padding: 0.75rem 2rem;
            border: none;
            border-radius: var(--border-radius);
            font-size: 1rem;
            font-weight: 600;
            text-decoration: none;
            text-align: center;
            cursor: pointer;
            transition: var(--transition);
            position: relative;
            overflow: hidden;
        }
        
        .btn::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 0;
            height: 0;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.3);
            transform: translate(-50%, -50%);
            transition: width 0.6s, height 0.6s;
        }
        
        .btn:hover::before {
            width: 300px;
            height: 300px;
        }
        
        .btn-primary {
            background: var(--secondary-color);
            color: white;
        }
        
        .btn-primary:hover {
            background: #2980b9;
            transform: translateY(-2px);
            box-shadow: var(--shadow-hover);
        }
        
        .btn-success {
            background: var(--success-color);
            color: white;
        }
        
        .btn-success:hover {
            background: #229954;
            transform: translateY(-2px);
            box-shadow: var(--shadow-hover);
        }
        
        /* Card Styles */
        .card {
            background: white;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
            padding: 2rem;
            margin: 1rem 0;
            transition: var(--transition);
            border: 1px solid #e0e0e0;
        }
        
        .card:hover {
            transform: translateY(-5px);
            box-shadow: var(--shadow-hover);
        }
        
        .card-header {
            border-bottom: 2px solid var(--light-color);
            padding-bottom: 1rem;
            margin-bottom: 1rem;
        }
        
        .card-title {
            font-size: 1.5rem;
            color: var(--primary-color);
            margin-bottom: 0.5rem;
        }
        
        /* Grid Layout */
        .grid {
            display: grid;
            gap: 2rem;
            padding: 2rem;
        }
        
        .grid-2 {
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        }
        
        .grid-3 {
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .header h1 {
                font-size: 2rem;
            }
            
            .header p {
                font-size: 1rem;
            }
            
            .grid {
                padding: 1rem;
                gap: 1rem;
            }
            
            .grid-2,
            .grid-3 {
                grid-template-columns: 1fr;
            }
        }
        
        /* Animation Classes */
        .fade-in {
            animation: fadeIn 0.5s ease-in;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .slide-in-left {
            animation: slideInLeft 0.5s ease-out;
        }
        
        @keyframes slideInLeft {
            from { transform: translateX(-100%); }
            to { transform: translateX(0); }
        }
    </style>
</head>
<body>
    <div class="container fade-in">
        <header class="header">
            <h1>🎨 Internal CSS Showcase</h1>
            <p>Styling modern dengan CSS3 features</p>
        </header>
        
        <div class="grid grid-2">
            <div class="card slide-in-left">
                <div class="card-header">
                    <h2 class="card-title">🚀 Modern Features</h2>
                </div>
                <p>CSS3 variables, gradients, animations, dan responsive design dalam satu package.</p>
                <button class="btn btn-primary">Learn More</button>
            </div>
            
            <div class="card slide-in-left">
                <div class="card-header">
                    <h2 class="card-title">✨ Best Practices</h2>
                </div>
                <p>CSS reset, semantic naming, component-based styling, dan performance optimization.</p>
                <button class="btn btn-success">Get Started</button>
            </div>
        </div>
    </div>
</body>
</html>
```

#### 3️⃣ **External CSS (Recommended)**
**📍 Kapan Digunakan:** Production, multi-page applications, large projects

**✅ Kelebihan:**
- Reusable across pages
- Better organization
- Caching benefits
- Separation of concerns
- Team collaboration friendly

**❌ Kekurangan:**
- Additional HTTP request
- Need proper file management

**💡 Struktur File External CSS:**
```
css/
├── style.css              ← Main stylesheet
├── components/             ← Component-specific styles
│   ├── buttons.css
│   ├── cards.css
│   └── forms.css
├── layout/                 ← Layout styles
│   ├── header.css
│   ├── navigation.css
│   └── footer.css
├── pages/                  ← Page-specific styles
│   ├── home.css
│   └── about.css
└── utils/                  ← Utility classes
    ├── variables.css
    ├── mixins.css
    └── responsive.css
```

**📝 File: `css/style.css`**
```css
/* ===================================
   CSS UTAMA SITTA - Universitas Terbuka
   =================================== */

/* CSS Reset & Base Styles */
@import url('https://fonts.googleapis.com/css2?family=Segoe+UI:wght@300;400;500;600;700&display=swap');

/* CSS Variables untuk Design System */
:root {
    /* Color Palette */
    --primary-50: #f0f9ff;
    --primary-100: #e0f2fe;
    --primary-200: #bae6fd;
    --primary-300: #7dd3fc;
    --primary-400: #38bdf8;
    --primary-500: #0ea5e9;
    --primary-600: #0284c7;
    --primary-700: #0369a1;
    --primary-800: #075985;
    --primary-900: #0c4a6e;
    
    --secondary-50: #f8fafc;
    --secondary-100: #f1f5f9;
    --secondary-200: #e2e8f0;
    --secondary-300: #cbd5e1;
    --secondary-400: #94a3b8;
    --secondary-500: #64748b;
    --secondary-600: #475569;
    --secondary-700: #334155;
    --secondary-800: #1e293b;
    --secondary-900: #0f172a;
    
    /* Semantic Colors */
    --success: #10b981;
    --warning: #f59e0b;
    --error: #ef4444;
    --info: #3b82f6;
    
    /* Neutral Colors */
    --white: #ffffff;
    --gray-50: #f9fafb;
    --gray-100: #f3f4f6;
    --gray-200: #e5e7eb;
    --gray-300: #d1d5db;
    --gray-400: #9ca3af;
    --gray-500: #6b7280;
    --gray-600: #4b5563;
    --gray-700: #374151;
    --gray-800: #1f2937;
    --gray-900: #111827;
    
    /* Typography */
    --font-family-base: 'Segoe UI', system-ui, -apple-system, sans-serif;
    --font-family-mono: 'Fira Code', 'Courier New', monospace;
    
    /* Font Sizes */
    --text-xs: 0.75rem;     /* 12px */
    --text-sm: 0.875rem;    /* 14px */
    --text-base: 1rem;      /* 16px */
    --text-lg: 1.125rem;    /* 18px */
    --text-xl: 1.25rem;     /* 20px */
    --text-2xl: 1.5rem;     /* 24px */
    --text-3xl: 1.875rem;   /* 30px */
    --text-4xl: 2.25rem;    /* 36px */
    --text-5xl: 3rem;       /* 48px */
    
    /* Spacing */
    --space-1: 0.25rem;     /* 4px */
    --space-2: 0.5rem;      /* 8px */
    --space-3: 0.75rem;     /* 12px */
    --space-4: 1rem;        /* 16px */
    --space-5: 1.25rem;     /* 20px */
    --space-6: 1.5rem;      /* 24px */
    --space-8: 2rem;        /* 32px */
    --space-10: 2.5rem;     /* 40px */
    --space-12: 3rem;       /* 48px */
    --space-16: 4rem;       /* 64px */
    --space-20: 5rem;       /* 80px */
    
    /* Border Radius */
    --radius-none: 0;
    --radius-sm: 0.125rem;   /* 2px */
    --radius-base: 0.25rem;  /* 4px */
    --radius-md: 0.375rem;   /* 6px */
    --radius-lg: 0.5rem;     /* 8px */
    --radius-xl: 0.75rem;    /* 12px */
    --radius-2xl: 1rem;      /* 16px */
    --radius-full: 9999px;
    
    /* Shadows */
    --shadow-sm: 0 1px 2px 0 rgba(0, 0, 0, 0.05);
    --shadow-base: 0 1px 3px 0 rgba(0, 0, 0, 0.1), 0 1px 2px 0 rgba(0, 0, 0, 0.06);
    --shadow-md: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
    --shadow-lg: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
    --shadow-xl: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
    --shadow-2xl: 0 25px 50px -12px rgba(0, 0, 0, 0.25);
    
    /* Transitions */
    --transition-fast: 150ms ease-in-out;
    --transition-base: 250ms ease-in-out;
    --transition-slow: 350ms ease-in-out;
    
    /* Z-Index Scale */
    --z-dropdown: 1000;
    --z-sticky: 1020;
    --z-fixed: 1030;
    --z-modal-backdrop: 1040;
    --z-modal: 1050;
    --z-popover: 1060;
    --z-tooltip: 1070;
    --z-toast: 1080;
}

/* CSS Reset */
*,
*::before,
*::after {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

html {
    line-height: 1.15;
    -webkit-text-size-adjust: 100%;
    scroll-behavior: smooth;
}

body {
    font-family: var(--font-family-base);
    font-size: var(--text-base);
    line-height: 1.6;
    color: var(--gray-800);
    background-color: var(--gray-50);
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
}

/* Base Typography */
h1, h2, h3, h4, h5, h6 {
    font-weight: 600;
    line-height: 1.25;
    color: var(--gray-900);
    margin-bottom: var(--space-4);
}

h1 { font-size: var(--text-4xl); }
h2 { font-size: var(--text-3xl); }
h3 { font-size: var(--text-2xl); }
h4 { font-size: var(--text-xl); }
h5 { font-size: var(--text-lg); }
h6 { font-size: var(--text-base); }

p {
    margin-bottom: var(--space-4);
    color: var(--gray-600);
}

a {
    color: var(--primary-600);
    text-decoration: none;
    transition: var(--transition-fast);
}

a:hover {
    color: var(--primary-700);
    text-decoration: underline;
}

/* Layout Components */
.container {
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 var(--space-4);
}

@media (min-width: 640px) {
    .container { padding: 0 var(--space-6); }
}

@media (min-width: 1024px) {
    .container { padding: 0 var(--space-8); }
}

/* Grid System */
.grid {
    display: grid;
    gap: var(--space-6);
}

.grid-cols-1 { grid-template-columns: repeat(1, minmax(0, 1fr)); }
.grid-cols-2 { grid-template-columns: repeat(2, minmax(0, 1fr)); }
.grid-cols-3 { grid-template-columns: repeat(3, minmax(0, 1fr)); }
.grid-cols-4 { grid-template-columns: repeat(4, minmax(0, 1fr)); }

@media (max-width: 768px) {
    .grid-cols-2,
    .grid-cols-3,
    .grid-cols-4 {
        grid-template-columns: 1fr;
    }
}

/* Flexbox Utilities */
.flex { display: flex; }
.flex-col { flex-direction: column; }
.flex-wrap { flex-wrap: wrap; }
.items-center { align-items: center; }
.justify-center { justify-content: center; }
.justify-between { justify-content: space-between; }
.gap-2 { gap: var(--space-2); }
.gap-4 { gap: var(--space-4); }
.gap-6 { gap: var(--space-6); }

/* Button Components */
.btn {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    gap: var(--space-2);
    padding: var(--space-3) var(--space-6);
    font-size: var(--text-base);
    font-weight: 500;
    font-family: inherit;
    line-height: 1;
    border: 1px solid transparent;
    border-radius: var(--radius-lg);
    cursor: pointer;
    text-decoration: none;
    transition: var(--transition-base);
    white-space: nowrap;
    user-select: none;
    position: relative;
    overflow: hidden;
}

.btn:focus {
    outline: 2px solid var(--primary-500);
    outline-offset: 2px;
}

.btn:disabled {
    opacity: 0.5;
    cursor: not-allowed;
}

/* Button Variants */
.btn-primary {
    background-color: var(--primary-600);
    color: var(--white);
    border-color: var(--primary-600);
}

.btn-primary:hover:not(:disabled) {
    background-color: var(--primary-700);
    border-color: var(--primary-700);
    transform: translateY(-1px);
    box-shadow: var(--shadow-lg);
}

.btn-secondary {
    background-color: var(--gray-100);
    color: var(--gray-800);
    border-color: var(--gray-300);
}

.btn-secondary:hover:not(:disabled) {
    background-color: var(--gray-200);
    border-color: var(--gray-400);
}

.btn-success {
    background-color: var(--success);
    color: var(--white);
    border-color: var(--success);
}

.btn-success:hover:not(:disabled) {
    background-color: #059669;
    border-color: #059669;
    transform: translateY(-1px);
    box-shadow: var(--shadow-lg);
}

/* Button Sizes */
.btn-sm {
    padding: var(--space-2) var(--space-4);
    font-size: var(--text-sm);
}

.btn-lg {
    padding: var(--space-4) var(--space-8);
    font-size: var(--text-lg);
}

/* Card Components */
.card {
    background: var(--white);
    border: 1px solid var(--gray-200);
    border-radius: var(--radius-xl);
    box-shadow: var(--shadow-sm);
    overflow: hidden;
    transition: var(--transition-base);
}

.card:hover {
    box-shadow: var(--shadow-md);
    transform: translateY(-2px);
}

.card-header {
    padding: var(--space-6);
    border-bottom: 1px solid var(--gray-200);
    background-color: var(--gray-50);
}

.card-body {
    padding: var(--space-6);
}

.card-footer {
    padding: var(--space-6);
    border-top: 1px solid var(--gray-200);
    background-color: var(--gray-50);
}

/* Form Components */
.form-group {
    margin-bottom: var(--space-4);
}

.form-label {
    display: block;
    font-size: var(--text-sm);
    font-weight: 500;
    color: var(--gray-700);
    margin-bottom: var(--space-2);
}

.form-input {
    width: 100%;
    padding: var(--space-3);
    font-size: var(--text-base);
    border: 1px solid var(--gray-300);
    border-radius: var(--radius-lg);
    background-color: var(--white);
    transition: var(--transition-fast);
}

.form-input:focus {
    outline: none;
    border-color: var(--primary-500);
    box-shadow: 0 0 0 3px rgba(14, 165, 233, 0.1);
}

.form-input:invalid {
    border-color: var(--error);
}

.form-textarea {
    resize: vertical;
    min-height: 100px;
}

/* Utility Classes */
.text-center { text-align: center; }
.text-left { text-align: left; }
.text-right { text-align: right; }

.font-bold { font-weight: 700; }
.font-semibold { font-weight: 600; }
.font-medium { font-weight: 500; }

.text-xs { font-size: var(--text-xs); }
.text-sm { font-size: var(--text-sm); }
.text-base { font-size: var(--text-base); }
.text-lg { font-size: var(--text-lg); }
.text-xl { font-size: var(--text-xl); }
.text-2xl { font-size: var(--text-2xl); }

.text-gray-500 { color: var(--gray-500); }
.text-gray-600 { color: var(--gray-600); }
.text-gray-700 { color: var(--gray-700); }
.text-gray-800 { color: var(--gray-800); }
.text-gray-900 { color: var(--gray-900); }

.bg-white { background-color: var(--white); }
.bg-gray-50 { background-color: var(--gray-50); }
.bg-gray-100 { background-color: var(--gray-100); }

.rounded { border-radius: var(--radius-base); }
.rounded-lg { border-radius: var(--radius-lg); }
.rounded-xl { border-radius: var(--radius-xl); }
.rounded-full { border-radius: var(--radius-full); }

.shadow-sm { box-shadow: var(--shadow-sm); }
.shadow { box-shadow: var(--shadow-base); }
.shadow-md { box-shadow: var(--shadow-md); }
.shadow-lg { box-shadow: var(--shadow-lg); }
.shadow-xl { box-shadow: var(--shadow-xl); }

.p-2 { padding: var(--space-2); }
.p-4 { padding: var(--space-4); }
.p-6 { padding: var(--space-6); }
.p-8 { padding: var(--space-8); }

.m-2 { margin: var(--space-2); }
.m-4 { margin: var(--space-4); }
.m-6 { margin: var(--space-6); }
.m-8 { margin: var(--space-8); }

.mb-2 { margin-bottom: var(--space-2); }
.mb-4 { margin-bottom: var(--space-4); }
.mb-6 { margin-bottom: var(--space-6); }
.mb-8 { margin-bottom: var(--space-8); }

.mt-2 { margin-top: var(--space-2); }
.mt-4 { margin-top: var(--space-4); }
.mt-6 { margin-top: var(--space-6); }
.mt-8 { margin-top: var(--space-8); }

/* Responsive Utilities */
.hidden { display: none; }

@media (max-width: 640px) {
    .sm\:hidden { display: none; }
}

@media (max-width: 768px) {
    .md\:hidden { display: none; }
    .md\:block { display: block; }
}

@media (max-width: 1024px) {
    .lg\:hidden { display: none; }
}

/* Animation Classes */
@keyframes fadeIn {
    from { opacity: 0; transform: translateY(10px); }
    to { opacity: 1; transform: translateY(0); }
}

@keyframes slideInLeft {
    from { transform: translateX(-100%); opacity: 0; }
    to { transform: translateX(0); opacity: 1; }
}

@keyframes slideInRight {
    from { transform: translateX(100%); opacity: 0; }
    to { transform: translateX(0); opacity: 1; }
}

@keyframes bounce {
    0%, 20%, 53%, 80%, 100% { transform: translate3d(0, 0, 0); }
    40%, 43% { transform: translate3d(0, -30px, 0); }
    70% { transform: translate3d(0, -15px, 0); }
    90% { transform: translate3d(0, -4px, 0); }
}

.animate-fade-in { animation: fadeIn 0.5s ease-out; }
.animate-slide-in-left { animation: slideInLeft 0.5s ease-out; }
.animate-slide-in-right { animation: slideInRight 0.5s ease-out; }
.animate-bounce { animation: bounce 1s infinite; }

/* Custom Scrollbar */
::-webkit-scrollbar {
    width: 8px;
    height: 8px;
}

::-webkit-scrollbar-track {
    background: var(--gray-100);
}

::-webkit-scrollbar-thumb {
    background: var(--gray-400);
    border-radius: var(--radius-full);
}

::-webkit-scrollbar-thumb:hover {
    background: var(--gray-500);
}

/* Focus Styles for Accessibility */
.focus\:outline-none:focus {
    outline: none;
}

.focus\:ring:focus {
    outline: 2px solid var(--primary-500);
    outline-offset: 2px;
}

/* Print Styles */
@media print {
    .no-print {
        display: none !important;
    }
    
    body {
        font-size: 12pt;
        line-height: 1.4;
    }
    
    .card {
        break-inside: avoid;
        border: 1px solid #ccc;
        margin-bottom: 1rem;
    }
}
```

**🔗 Cara Menghubungkan External CSS:**
```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SITTA - External CSS</title>
    
    <!-- External CSS -->
    <link rel="stylesheet" href="css/style.css">
    
    <!-- Alternative dengan media queries -->
    <link rel="stylesheet" href="css/print.css" media="print">
    <link rel="stylesheet" href="css/mobile.css" media="max-width: 768px">
</head>
<body>
    <!-- Konten HTML -->
</body>
</html>
```

### 📊 **Perbandingan Metode CSS**

| 📋 Kriteria | 🎯 Inline CSS | 🏠 Internal CSS | 🌐 External CSS |
|-------------|---------------|------------------|-----------------|
| **Maintainability** | ❌ Sangat Sulit | ⚠️ Sedang | ✅ Mudah |
| **Reusability** | ❌ Tidak Bisa | ⚠️ Terbatas | ✅ Penuh |
| **Performance** | ✅ Cepat | ✅ Cepat | ⚠️ Perlu HTTP Request |
| **Caching** | ❌ Tidak Bisa | ❌ Tidak Bisa | ✅ Bisa |
| **Best For** | Testing, Email | Single Page | Production Apps |
| **File Size** | ❌ Besar | ⚠️ Sedang | ✅ Terpisah |
| **Team Work** | ❌ Sulit | ⚠️ Sedang | ✅ Mudah |

### 🎯 **Best Practices CSS**

1. **✅ Gunakan External CSS untuk production**
2. **✅ Organisir CSS dengan logical structure**
3. **✅ Gunakan CSS variables untuk consistency**
4. **✅ Implement responsive design**
5. **✅ Optimize untuk performance**
6. **✅ Gunakan semantic class names**
7. **✅ Consider accessibility dalam styling**

### 🎨 **Praktik: Buat CSS untuk SITTA**

**File: `css/style.css`**
```css
/* Reset CSS */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Variabel CSS */
:root {
    --primary-color: #2c3e50;
    --secondary-color: #3498db;
    --success-color: #27ae60;
    --warning-color: #f39c12;
    --danger-color: #e74c3c;
    --light-color: #ecf0f1;
    --dark-color: #2c3e50;
    --font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

/* Base Styles */
body {
    font-family: var(--font-family);
    line-height: 1.6;
    color: var(--dark-color);
    background-color: #f8f9fa;
}

.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

/* Header Styles */
.header {
    background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
    color: white;
    padding: 2rem 0;
    text-align: center;
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
}

.logo {
    font-size: 2.5rem;
    margin-bottom: 0.5rem;
    font-weight: bold;
}

.subtitle {
    font-size: 1.1rem;
    opacity: 0.9;
}

/* Navigation Styles */
.navigation {
    background-color: var(--primary-color);
    padding: 0;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    position: sticky;
    top: 0;
    z-index: 100;
}

.navigation ul {
    list-style: none;
    display: flex;
    justify-content: center;
    margin: 0;
}

.navigation ul li {
    margin: 0;
}

.navigation ul li a {
    display: block;
    color: white;
    text-decoration: none;
    padding: 1rem 1.5rem;
    transition: background-color 0.3s ease;
    border-bottom: 3px solid transparent;
}

.navigation ul li a:hover,
.navigation ul li a.active {
    background-color: var(--secondary-color);
    border-bottom-color: var(--success-color);
}

/* Main Content */
.main-content {
    min-height: calc(100vh - 200px);
    padding: 2rem 0;
}

.hero-section {
    text-align: center;
    padding: 3rem 0;
    background: white;
    border-radius: 10px;
    box-shadow: 0 5px 15px rgba(0,0,0,0.1);
    margin-bottom: 2rem;
}

.hero-section h2 {
    font-size: 2.5rem;
    color: var(--primary-color);
    margin-bottom: 1rem;
}

.hero-section p {
    font-size: 1.2rem;
    color: #666;
    margin-bottom: 2rem;
}

.cta-button {
    background: linear-gradient(45deg, var(--success-color), #2ecc71);
    color: white;
    padding: 1rem 2rem;
    border: none;
    border-radius: 50px;
    font-size: 1.1rem;
    cursor: pointer;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    box-shadow: 0 4px 15px rgba(39, 174, 96, 0.3);
}

.cta-button:hover {
    transform: translateY(-2px);
    box-shadow: 0 6px 20px rgba(39, 174, 96, 0.4);
}

/* Stok Section */
.stok-section {
    background: white;
    padding: 2rem;
    border-radius: 10px;
    box-shadow: 0 5px 15px rgba(0,0,0,0.1);
}

.stok-section h2 {
    color: var(--primary-color);
    margin-bottom: 2rem;
    text-align: center;
    font-size: 2rem;
}

.bahan-ajar-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 2rem;
    margin-top: 2rem;
}

.bahan-ajar-card {
    background: white;
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 5px 15px rgba(0,0,0,0.1);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    border: 1px solid #e0e0e0;
}

.bahan-ajar-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 25px rgba(0,0,0,0.15);
}

.bahan-ajar-image {
    width: 100%;
    height: 200px;
    object-fit: cover;
    background-color: var(--light-color);
}

.bahan-ajar-content {
    padding: 1.5rem;
}

.bahan-ajar-title {
    font-size: 1.3rem;
    color: var(--primary-color);
    margin-bottom: 0.5rem;
    font-weight: bold;
}

.bahan-ajar-info {
    margin-bottom: 1rem;
}

.bahan-ajar-info p {
    margin: 0.25rem 0;
    color: #666;
    font-size: 0.9rem;
}

.bahan-ajar-stok {
    background-color: var(--success-color);
    color: white;
    padding: 0.25rem 0.75rem;
    border-radius: 20px;
    font-size: 0.8rem;
    display: inline-block;
    margin-bottom: 1rem;
}

.btn-pesan {
    background: linear-gradient(45deg, var(--secondary-color), #5dade2);
    color: white;
    padding: 0.75rem 1.5rem;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 1rem;
    transition: background-color 0.3s ease;
    width: 100%;
    font-weight: bold;
}

.btn-pesan:hover {
    background: linear-gradient(45deg, #2980b9, var(--secondary-color));
}

/* Footer */
.footer {
    background-color: var(--primary-color);
    color: white;
    text-align: center;
    padding: 2rem 0;
    margin-top: 3rem;
}

/* Responsive Design */
@media (max-width: 768px) {
    .navigation ul {
        flex-direction: column;
        text-align: center;
    }
    
    .navigation ul li a {
        padding: 0.75rem 1rem;
    }
    
    .bahan-ajar-grid {
        grid-template-columns: 1fr;
    }
    
    .hero-section h2 {
        font-size: 2rem;
    }
    
    .logo {
        font-size: 2rem;
    }
}
```

---

## 🧠 **MATERI 3: JAVASCRIPT DOM - INTERAKTIVITAS DINAMIS**

### 🎯 **Konsep Fundamental DOM**

**📖 Definisi:** DOM (Document Object Model) adalah programming interface yang merepresentasikan dokumen HTML/XML sebagai tree structure. Setiap elemen dalam dokumen menjadi node dalam tree ini.

**🌟 Mengapa DOM Penting?**
- **Dynamic Content**: Mengubah konten tanpa reload
- **User Interaction**: Respon terhadap aksi user
- **Data Manipulation**: Update data secara real-time
- **Animation & Effects**: Membuat pengalaman interaktif
- **Form Validation**: Validasi input user
- **AJAX Integration**: Komunikasi dengan server

### 🏗️ **Struktur DOM Tree**

```
Document
├── html
│   ├── head
│   │   ├── meta
│   │   ├── title
│   │   └── link
│   └── body
│       ├── header
│       │   ├── h1
│       │   └── nav
│       │       └── ul
│       │           └── li
│       ├── main
│       │   ├── section
│       │   │   ├── h2
│       │   │   └── div
│       │   └── article
│       │       ├── h3
│       │       └── p
│       └── footer
│           └── p
```

### 🔍 **DOM Selectors - Cara Mengakses Elements**

#### **1. Classic Selectors (Legacy)**
```javascript
// getElementById - Paling cepat untuk single element
const header = document.getElementById('site-header');
console.log('Header element:', header);

// getElementsByClassName - Return HTMLCollection (live)
const buttons = document.getElementsByClassName('btn');
console.log('All buttons:', buttons);

// getElementsByTagName - Return HTMLCollection (live)
const images = document.getElementsByTagName('img');
console.log('All images:', images);

// getElementsByName - Return NodeList (static)
const inputs = document.getElementsByName('username');
console.log('Username inputs:', inputs);
```

#### **2. Modern Selectors (Recommended)**
```javascript
// querySelector - Return first matching element
const firstButton = document.querySelector('.btn');
console.log('First button:', firstButton);

const mainTitle = document.querySelector('#main-title');
console.log('Main title:', mainTitle);

const firstCard = document.querySelector('.card[data-id="1"]');
console.log('First card:', firstCard);

// querySelectorAll - Return NodeList (static)
const allButtons = document.querySelectorAll('.btn');
console.log('All buttons:', allButtons);

const allCards = document.querySelectorAll('.card');
console.log('All cards:', allCards);

// Complex selectors
const specificElements = document.querySelectorAll('main .card:not(.featured)');
console.log('Non-featured cards:', specificElements);

const linksInNavigation = document.querySelectorAll('nav a[href^="#"]');
console.log('Anchor links:', linksInNavigation);
```

#### **3. Traversal Methods**
```javascript
// Parent traversal
const card = document.querySelector('.card');
const cardParent = card.parentElement;
console.log('Card parent:', cardParent);

// Child traversal
const container = document.querySelector('.container');
const containerChildren = container.children;
console.log('Container children:', containerChildren);

// Sibling traversal
const firstCard = document.querySelector('.card');
const nextCard = firstCard.nextElementSibling;
const prevCard = firstCard.previousElementSibling;
console.log('Next card:', nextCard);
console.log('Previous card:', prevCard);

// First and last child
const list = document.querySelector('ul');
const firstItem = list.firstElementChild;
const lastItem = list.lastElementChild;
console.log('First item:', firstItem);
console.log('Last item:', lastItem);
```

### 🛠️ **DOM Manipulation - Mengubah Konten & Atribut**

#### **Content Manipulation**
```javascript
// textContent - Plain text, faster, safer
const title = document.querySelector('h1');
title.textContent = '🎉 Judul Baru dengan Emoji!';
title.textContent += ' Teks tambahan';

// innerHTML - HTML content, slower, security risk
const content = document.querySelector('.content');
content.innerHTML = `
    <div class="new-content">
        <h3>Subjudul Dinamis</h3>
        <p>Paragraf dengan <strong>formatting</strong> HTML.</p>
        <ul>
            <li>Item 1</li>
            <li>Item 2</li>
            <li>Item 3</li>
        </ul>
    </div>
`;

// innerText - Like textContent but respects CSS
const description = document.querySelector('.description');
description.innerText = 'Teks yang memperhatikan styling CSS';

// outerHTML - Include the element itself
const card = document.querySelector('.card');
card.outerHTML = `
    <section class="card enhanced">
        <h2>Enhanced Card</h2>
        <p>Card yang sudah di-replace.</p>
    </section>
`;
```

#### **Attribute Manipulation**
```javascript
// getAttribute
const link = document.querySelector('a');
const href = link.getAttribute('href');
const target = link.getAttribute('target');
console.log('Link href:', href);
console.log('Link target:', target);

// setAttribute
link.setAttribute('href', 'https://www.example.com');
link.setAttribute('target', '_blank');
link.setAttribute('rel', 'noopener noreferrer');
link.setAttribute('data-custom', 'custom-value');

// hasAttribute
if (link.hasAttribute('target')) {
    console.log('Link has target attribute');
}

// removeAttribute
link.removeAttribute('target');

// Direct property access (faster for common attributes)
const image = document.querySelector('img');
image.src = 'images/new-image.jpg';
image.alt = 'Deskripsi gambar baru';
image.width = 300;
image.height = 200;
image.loading = 'lazy';

// Dataset for data-* attributes
const card = document.querySelector('.card');
card.dataset.id = '123';
card.dataset.category = 'books';
card.dataset.featured = 'true';

console.log('Card ID:', card.dataset.id);
console.log('Card category:', card.dataset.category);
console.log('Is featured:', card.dataset.featured === 'true');
```

#### **Style Manipulation**
```javascript
// Direct style property
const button = document.querySelector('.btn');
button.style.color = '#ffffff';
button.style.backgroundColor = '#007bff';
button.style.border = 'none';
button.style.padding = '12px 24px';
button.style.borderRadius = '6px';
button.style.fontSize = '16px';
button.style.cursor = 'pointer';
button.style.transition = 'all 0.3s ease';

// CSS Text property
button.style.cssText = `
    color: #ffffff;
    background-color: #007bff;
    border: none;
    padding: 12px 24px;
    border-radius: 6px;
    font-size: 16px;
    cursor: pointer;
    transition: all 0.3s ease;
`;

// getComputedStyle
const computedStyle = window.getComputedStyle(button);
console.log('Computed color:', computedStyle.color);
console.log('Computed background:', computedStyle.backgroundColor);

// Class manipulation (recommended)
button.className = 'btn btn-primary btn-large';
button.classList.add('active');
button.classList.remove('disabled');
button.classList.toggle('featured');
button.classList.contains('btn-primary'); // true
button.classList.replace('btn-primary', 'btn-secondary');

// Multiple class operations
button.classList.add('animated', 'bounce', 'infinite');
button.classList.remove('disabled', 'loading');
```

### 🎪 **Event Handling - Interaksi User**

#### **Event Listeners**
```javascript
// Basic event listener
const button = document.querySelector('.btn');
button.addEventListener('click', function(event) {
    console.log('Button clicked!', event);
    console.log('Event type:', event.type);
    console.log('Target element:', event.target);
    console.log('Current target:', event.currentTarget);
});

// Arrow function (no 'this' binding)
button.addEventListener('click', (event) => {
    console.log('Arrow function click');
    // 'this' refers to window, not the button
});

// Named function (reusable)
function handleClick(event) {
    console.log('Handled by named function');
    event.preventDefault(); // Prevent default behavior
    event.stopPropagation(); // Stop event bubbling
}

button.addEventListener('click', handleClick);

// Multiple listeners on same element
button.addEventListener('click', function() {
    console.log('First listener');
});

button.addEventListener('click', function() {
    console.log('Second listener');
});

// Remove event listener
button.removeEventListener('click', handleClick);
```

#### **Event Types & Examples**
```javascript
// Mouse Events
const card = document.querySelector('.card');

card.addEventListener('click', function(e) {
    console.log('Card clicked at:', e.clientX, e.clientY);
    this.classList.toggle('selected');
});

card.addEventListener('dblclick', function() {
    console.log('Double clicked');
    this.style.transform = 'scale(1.05)';
});

card.addEventListener('mouseenter', function() {
    this.style.boxShadow = '0 10px 30px rgba(0,0,0,0.2)';
});

card.addEventListener('mouseleave', function() {
    this.style.boxShadow = '0 4px 6px rgba(0,0,0,0.1)';
});

card.addEventListener('mousemove', function(e) {
    const rect = this.getBoundingClientRect();
    const x = e.clientX - rect.left;
    const y = e.clientY - rect.top;
    console.log(`Mouse position: ${x}, ${y}`);
});

// Keyboard Events
const input = document.querySelector('input');

input.addEventListener('keydown', function(e) {
    console.log('Key pressed:', e.key);
    console.log('Key code:', e.keyCode);
    console.log('Shift pressed:', e.shiftKey);
    console.log('Ctrl pressed:', e.ctrlKey);
    
    if (e.key === 'Enter') {
        console.log('Enter pressed!');
    }
});

input.addEventListener('keyup', function(e) {
    console.log('Key released:', e.key);
});

input.addEventListener('keypress', function(e) {
    console.log('Key character:', e.charCode);
});

// Form Events
const form = document.querySelector('form');

form.addEventListener('submit', function(e) {
    e.preventDefault(); // Prevent form submission
    
    const formData = new FormData(this);
    const data = Object.fromEntries(formData);
    console.log('Form data:', data);
    
    // Validate form
    if (!data.name || !data.email) {
        alert('Please fill all required fields');
        return;
    }
    
    // Submit form via AJAX
    submitForm(data);
});

// Input Events
input.addEventListener('input', function(e) {
    console.log('Input value changed:', this.value);
    validateInput(this);
});

input.addEventListener('focus', function() {
    this.parentElement.classList.add('focused');
});

input.addEventListener('blur', function() {
    this.parentElement.classList.remove('focused');
    validateInput(this);
});

// Window Events
window.addEventListener('load', function() {
    console.log('Page fully loaded');
    initializeApp();
});

window.addEventListener('resize', function() {
    console.log('Window resized:', window.innerWidth, window.innerHeight);
    adjustLayout();
});

window.addEventListener('scroll', function() {
    const scrolled = window.pageYOffset;
    console.log('Scrolled:', scrolled);
    
    if (scrolled > 100) {
        document.body.classList.add('scrolled');
    } else {
        document.body.classList.remove('scrolled');
    }
});

// Document Events
document.addEventListener('DOMContentLoaded', function() {
    console.log('DOM fully loaded');
    setupEventListeners();
});

document.addEventListener('click', function(e) {
    // Event delegation
    if (e.target.matches('.btn-delete')) {
        const id = e.target.dataset.id;
        deleteItem(id);
    }
});
```

#### **Event Delegation**
```javascript
// Instead of adding listeners to each button
const buttons = document.querySelectorAll('.btn');
buttons.forEach(btn => {
    btn.addEventListener('click', handleClick);
});

// Use event delegation on parent
const container = document.querySelector('.container');
container.addEventListener('click', function(e) {
    // Check if clicked element is a button
    if (e.target.matches('.btn')) {
        const action = e.target.dataset.action;
        const id = e.target.dataset.id;
        
        switch(action) {
            case 'edit':
                editItem(id);
                break;
            case 'delete':
                deleteItem(id);
                break;
            case 'view':
                viewItem(id);
                break;
        }
    }
    
    // Handle dynamic elements
    if (e.target.matches('.card')) {
        selectCard(e.target);
    }
});
```

### 🏗️ **DOM Creation & Modification**

#### **Creating Elements**
```javascript
// Create element
const newDiv = document.createElement('div');
newDiv.className = 'card new-card';
newDiv.id = 'card-' + Date.now();
newDiv.textContent = 'New Card';

// Set attributes
newDiv.setAttribute('data-id', '123');
newDiv.dataset.category = 'books';

// Add styles
newDiv.style.cssText = `
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    padding: 20px;
    border-radius: 10px;
    margin: 10px 0;
`;

// Create complex structure
const card = document.createElement('article');
card.className = 'product-card';
card.innerHTML = `
    <div class="card-image">
        <img src="images/product.jpg" alt="Product Image" loading="lazy">
    </div>
    <div class="card-content">
        <h3 class="card-title">Product Title</h3>
        <p class="card-description">Product description goes here...</p>
        <div class="card-price">$19.99</div>
        <button class="btn btn-primary">Add to Cart</button>
    </div>
`;

// Create with document fragment (better performance)
function createProductList(products) {
    const fragment = document.createDocumentFragment();
    
    products.forEach(product => {
        const card = createProductCard(product);
        fragment.appendChild(card);
    });
    
    return fragment;
}

const container = document.querySelector('.products-container');
const productList = createProductList(products);
container.appendChild(productList);
```

#### **Inserting Elements**
```javascript
// appendChild - Add to end of children
const parent = document.querySelector('.container');
const newChild = document.createElement('div');
parent.appendChild(newChild);

// insertBefore - Insert before reference element
const reference = document.querySelector('#reference-element');
const newElement = document.createElement('div');
parent.insertBefore(newElement, reference);

// prepend - Add to beginning of children (modern)
parent.prepend(newElement);

// after - Insert after element (modern)
reference.after(newElement);

// before - Insert before element (modern)
reference.before(newElement);

// append - Append multiple elements (modern)
parent.append(newElement1, newElement2, newElement3);

// Example: Insert at specific position
function insertAt(parent, element, index) {
    if (index >= parent.children.length) {
        parent.appendChild(element);
    } else {
        parent.insertBefore(element, parent.children[index]);
    }
}
```

#### **Removing & Replacing Elements**
```javascript
// remove - Remove element (modern)
const element = document.querySelector('.remove-me');
element.remove();

// removeChild - Traditional way
const parent = element.parentElement;
parent.removeChild(element);

// replaceWith - Replace element (modern)
const oldElement = document.querySelector('.old-element');
const newElement = document.createElement('div');
newElement.textContent = 'New content';
oldElement.replaceWith(newElement);

// replaceChild - Traditional way
parent.replaceChild(newElement, oldElement);

// Remove all children
const container = document.querySelector('.container');
while (container.firstChild) {
    container.removeChild(container.firstChild);
}

// Modern way
container.innerHTML = '';
```

#### **Cloning Elements**
```javascript
const original = document.querySelector('.card-template');

// Shallow clone (no event listeners)
const shallowClone = original.cloneNode(false);

// Deep clone (includes descendants)
const deepClone = original.cloneNode(true);

// Clone with modifications
const newCard = original.cloneNode(true);
newCard.querySelector('.card-title').textContent = 'New Title';
newCard.querySelector('.card-image img').src = 'new-image.jpg';
newCard.classList.add('cloned');
newCard.id = 'card-' + Date.now();

// Insert clone
document.querySelector('.cards-container').appendChild(newCard);
```

### 🎯 **Advanced DOM Techniques**

#### **Mutation Observer**
```javascript
// Watch for DOM changes
const observer = new MutationObserver(function(mutations) {
    mutations.forEach(function(mutation) {
        console.log('Mutation type:', mutation.type);
        console.log('Mutation target:', mutation.target);
        
        if (mutation.type === 'childList') {
            mutation.addedNodes.forEach(node => {
                if (node.nodeType === Node.ELEMENT_NODE) {
                    console.log('Element added:', node);
                    initializeNewElement(node);
                }
            });
            
            mutation.removedNodes.forEach(node => {
                if (node.nodeType === Node.ELEMENT_NODE) {
                    console.log('Element removed:', node);
                    cleanupRemovedElement(node);
                }
            });
        }
    });
});

// Start observing
const target = document.querySelector('.dynamic-container');
observer.observe(target, {
    childList: true,    // Observe child nodes
    attributes: true,   // Observe attributes
    subtree: true,      // Observe descendants
    attributeOldValue: true // Record old attribute values
});

// Stop observing
observer.disconnect();
```

#### **Custom Events**
```javascript
// Create custom event
const customEvent = new CustomEvent('dataLoaded', {
    detail: { data: [1, 2, 3], source: 'api' },
    bubbles: true,
    cancelable: true
});

// Dispatch custom event
document.dispatchEvent(customEvent);

// Listen for custom event
document.addEventListener('dataLoaded', function(e) {
    console.log('Data loaded:', e.detail);
    updateUI(e.detail.data);
});

// Event-driven architecture
class EventBus {
    constructor() {
        this.events = {};
    }
    
    on(eventName, callback) {
        if (!this.events[eventName]) {
            this.events[eventName] = [];
        }
        this.events[eventName].push(callback);
    }
    
    emit(eventName, data) {
        if (this.events[eventName]) {
            this.events[eventName].forEach(callback => {
                callback(data);
            });
        }
    }
    
    off(eventName, callback) {
        if (this.events[eventName]) {
            this.events[eventName] = this.events[eventName].filter(cb => cb !== callback);
        }
    }
}

const eventBus = new EventBus();
eventBus.on('userLoggedIn', user => console.log('User logged in:', user));
eventBus.emit('userLoggedIn', { id: 1, name: 'John' });
```

### 📊 **Performance Optimization**

#### **Efficient DOM Operations**
```javascript
// Bad: Multiple DOM operations
for (let i = 0; i < 1000; i++) {
    const div = document.createElement('div');
    div.textContent = `Item ${i}`;
    document.body.appendChild(div); // Expensive!
}

// Good: Use document fragment
const fragment = document.createDocumentFragment();
for (let i = 0; i < 1000; i++) {
    const div = document.createElement('div');
    div.textContent = `Item ${i}`;
    fragment.appendChild(div);
}
document.body.appendChild(fragment); // Single operation

// Good: Batch DOM updates
function updateElements(elements, data) {
    // Remove from DOM
    elements.forEach(el => el.style.display = 'none');
    
    // Update all elements
    elements.forEach((el, index) => {
        el.textContent = data[index];
    });
    
    // Re-add to DOM
    elements.forEach(el => el.style.display = '');
}

// Use requestAnimationFrame for animations
function animateElement(element, duration) {
    const start = performance.now();
    
    function animate(currentTime) {
        const elapsed = currentTime - start;
        const progress = Math.min(elapsed / duration, 1);
        
        element.style.transform = `translateX(${progress * 100}px)`;
        
        if (progress < 1) {
            requestAnimationFrame(animate);
        }
    }
    
    requestAnimationFrame(animate);
}
```

### 🛠️ **Hands-On Lab: DOM Manipulation**

**🎯 Tujuan:** Menerapkan semua konsep DOM dalam aplikasi SITTA

**📝 Latihan Interaktif:**
```javascript
// Complete DOM manipulation example for SITTA
class SITTAApp {
    constructor() {
        this.products = [];
        this.cart = [];
        this.init();
    }
    
    init() {
        this.loadProducts();
        this.setupEventListeners();
        this.renderProducts();
    }
    
    setupEventListeners() {
        // Search functionality
        const searchInput = document.querySelector('#search');
        searchInput.addEventListener('input', this.debounce(this.handleSearch.bind(this), 300));
        
        // Filter functionality
        const filterSelect = document.querySelector('#filter');
        filterSelect.addEventListener('change', this.handleFilter.bind(this));
        
        // Cart functionality with event delegation
        const container = document.querySelector('.products-container');
        container.addEventListener('click', this.handleCartAction.bind(this));
        
        // Form submission
        const form = document.querySelector('#order-form');
        form.addEventListener('submit', this.handleFormSubmit.bind(this));
    }
    
    handleSearch(e) {
        const query = e.target.value.toLowerCase();
        const filtered = this.products.filter(product => 
            product.name.toLowerCase().includes(query) ||
            product.description.toLowerCase().includes(query)
        );
        this.renderProducts(filtered);
    }
    
    handleFilter(e) {
        const category = e.target.value;
        const filtered = category ? 
            this.products.filter(p => p.category === category) : 
            this.products;
        this.renderProducts(filtered);
    }
    
    handleCartAction(e) {
        if (e.target.matches('.btn-add-cart')) {
            const productId = e.target.dataset.id;
            this.addToCart(productId);
        }
    }
    
    handleFormSubmit(e) {
        e.preventDefault();
        const formData = new FormData(e.target);
        const order = Object.fromEntries(formData);
        this.processOrder(order);
    }
    
    renderProducts(products = this.products) {
        const container = document.querySelector('.products-container');
        const fragment = document.createDocumentFragment();
        
        products.forEach(product => {
            const card = this.createProductCard(product);
            fragment.appendChild(card);
        });
        
        container.innerHTML = '';
        container.appendChild(fragment);
    }
    
    createProductCard(product) {
        const card = document.createElement('article');
        card.className = 'product-card';
        card.dataset.id = product.id;
        
        card.innerHTML = `
            <div class="card-image">
                <img src="${product.image}" alt="${product.name}" loading="lazy">
                <span class="stock-badge ${this.getStockClass(product.stock)}">
                    ${this.getStockStatus(product.stock)}
                </span>
            </div>
            <div class="card-content">
                <h3 class="card-title">${product.name}</h3>
                <p class="card-description">${product.description}</p>
                <div class="card-meta">
                    <span class="price">Rp ${product.price.toLocaleString('id-ID')}</span>
                    <span class="stock">Stok: ${product.stock}</span>
                </div>
                <button class="btn btn-primary btn-add-cart" data-id="${product.id}">
                    🛒 Tambah ke Keranjang
                </button>
            </div>
        `;
        
        return card;
    }
    
    addToCart(productId) {
        const product = this.products.find(p => p.id === productId);
        if (product && product.stock > 0) {
            this.cart.push(product);
            product.stock--;
            this.updateCartUI();
            this.showNotification(`${product.name} ditambahkan ke keranjang!`, 'success');
        }
    }
    
    updateCartUI() {
        const cartCount = document.querySelector('.cart-count');
        const cartTotal = document.querySelector('.cart-total');
        
        cartCount.textContent = this.cart.length;
        const total = this.cart.reduce((sum, item) => sum + item.price, 0);
        cartTotal.textContent = `Rp ${total.toLocaleString('id-ID')}`;
    }
    
    showNotification(message, type = 'info') {
        const notification = document.createElement('div');
        notification.className = `notification notification-${type}`;
        notification.textContent = message;
        
        document.body.appendChild(notification);
        
        setTimeout(() => {
            notification.classList.add('show');
        }, 100);
        
        setTimeout(() => {
            notification.classList.remove('show');
            setTimeout(() => notification.remove(), 300);
        }, 3000);
    }
    
    debounce(func, wait) {
        let timeout;
        return function executedFunction(...args) {
            const later = () => {
                clearTimeout(timeout);
                func(...args);
            };
            clearTimeout(timeout);
            timeout = setTimeout(later, wait);
        };
    }
    
    getStockClass(stock) {
        if (stock === 0) return 'out-of-stock';
        if (stock < 10) return 'low-stock';
        return 'in-stock';
    }
    
    getStockStatus(stock) {
        if (stock === 0) return 'Habis';
        if (stock < 10) return `Terbatas (${stock})`;
        return `Tersedia (${stock})`;
    }
}

// Initialize app when DOM is ready
document.addEventListener('DOMContentLoaded', () => {
    new SITTAApp();
});
```

### 🔍 **Debugging DOM Issues**

#### **Common Problems & Solutions**
```javascript
// 1. Element not found
const element = document.querySelector('#non-existent');
if (!element) {
    console.error('Element not found!');
    // Solution: Check if element exists before using it
}

// 2. Null/undefined errors
element.addEventListener('click', handler); // Error if element is null
// Solution:
element?.addEventListener('click', handler);

// 3. Event listener not working
button.addEventListener('click', function() {
    console.log(this); // 'this' might not be button in arrow functions
});
// Solution: Use regular function or bind context

// 4. DOM not ready
document.addEventListener('DOMContentLoaded', function() {
    // Safe to access DOM here
});

// 5. Performance issues with many elements
// Bad: Adding listeners to each element
document.querySelectorAll('.item').forEach(item => {
    item.addEventListener('click', handler);
});

// Good: Use event delegation
document.querySelector('.container').addEventListener('click', function(e) {
    if (e.target.matches('.item')) {
        handler(e);
    }
});
```

### 📋 **DOM Manipulation Checklist**

**✅ Best Practices:**
- [ ] Use `querySelector` and `querySelectorAll` for consistency
- [ ] Prefer event delegation for dynamic content
- [ ] Use `documentFragment` for multiple DOM insertions
- [ ] Cache DOM references to avoid repeated queries
- [ ] Use `classList` instead of `className` manipulation
- [ ] Remove event listeners when no longer needed
- [ ] Use `requestAnimationFrame` for animations
- [ ] Validate elements exist before manipulation
- [ ] Use semantic HTML5 elements
- [ ] Consider accessibility in DOM changes

**❌ Common Mistakes to Avoid:**
- [ ] Creating memory leaks with event listeners
- [ ] Using `innerHTML` with untrusted content (XSS risk)
- [ ] Manipulating DOM in loops without batching
- [ ] Not checking if elements exist before use
- [ ] Using synchronous operations for large DOM changes
- [ ] Ignoring performance implications of DOM queries
- [ ] Forgetting to clean up when removing elements
- [ ] Not considering mobile touch events

### 📝 **Praktik: JavaScript untuk SITTA**

**File: `js/app.js`**
```javascript
// Data bahan ajar (dari data.js)
// Asumsikan dataBahanAjar sudah tersedia dari file data.js

// Fungsi untuk menampilkan daftar bahan ajar
function tampilkanBahanAjar() {
    const container = document.getElementById('daftar-bahan-ajar');
    container.innerHTML = ''; // Kosongkan container terlebih dahulu
    
    if (dataBahanAjar.length === 0) {
        container.innerHTML = '<p class="no-data">Belum ada data bahan ajar.</p>';
        return;
    }
    
    dataBahanAjar.forEach((bahan, index) => {
        const card = document.createElement('div');
        card.className = 'bahan-ajar-card';
        card.innerHTML = `
            <img src="${bahan.cover}" alt="${bahan.namaBarang}" class="bahan-ajar-image">
            <div class="bahan-ajar-content">
                <h3 class="bahan-ajar-title">${bahan.namaBarang}</h3>
                <div class="bahan-ajar-info">
                    <p><strong>Kode:</strong> ${bahan.kodeBarang}</p>
                    <p><strong>Edisi:</strong> ${bahan.edisi}</p>
                    <p><strong>Lokasi:</strong> ${bahan.kodeLokasi}</p>
                </div>
                <span class="bahan-ajar-stok">Stok: ${bahan.stok} buah</span>
                <button class="btn-pesan" onclick="pesanBahanAjar('${bahan.kodeBarang}', ${index})">
                    🛒 Pesan Sekarang
                </button>
            </div>
        `;
        container.appendChild(card);
    });
}

// Fungsi untuk memesan bahan ajar
function pesanBahanAjar(kodeBarang, index) {
    const bahan = dataBahanAjar[index];
    
    // Validasi stok
    if (bahan.stok <= 0) {
        tampilkanNotifikasi('Maaf, stok habis!', 'error');
        return;
    }
    
    // Tampilkan konfirmasi
    const konfirmasi = confirm(`Apakah Anda yakin ingin memesan "${bahan.namaBarang}"?`);
    
    if (konfirmasi) {
        // Kurangi stok
        bahan.stok--;
        
        // Tampilkan notifikasi sukses
        tampilkanNotifikasi(`Pesanan "${bahan.namaBarang}" berhasil! Stok tersisa: ${bahan.stok}`, 'success');
        
        // Refresh tampilan
        tampilkanBahanAjar();
        
        // Simpan ke localStorage (simulasi database)
        simpanPesanan(bahan);
    }
}

// Fungsi untuk menampilkan notifikasi
function tampilkanNotifikasi(pesan, tipe = 'info') {
    // Buat elemen notifikasi
    const notifikasi = document.createElement('div');
    notifikasi.className = `notifikasi notifikasi-${tipe}`;
    notifikasi.textContent = pesan;
    
    // Style notifikasi
    notifikasi.style.cssText = `
        position: fixed;
        top: 20px;
        right: 20px;
        padding: 1rem 1.5rem;
        border-radius: 5px;
        color: white;
        font-weight: bold;
        z-index: 1000;
        transform: translateX(100%);
        transition: transform 0.3s ease;
        max-width: 300px;
    `;
    
    // Warna berdasarkan tipe
    switch(tipe) {
        case 'success':
            notifikasi.style.backgroundColor = '#27ae60';
            break;
        case 'error':
            notifikasi.style.backgroundColor = '#e74c3c';
            break;
        case 'warning':
            notifikasi.style.backgroundColor = '#f39c12';
            break;
        default:
            notifikasi.style.backgroundColor = '#3498db';
    }
    
    // Tambahkan ke body
    document.body.appendChild(notifikasi);
    
    // Animasi masuk
    setTimeout(() => {
        notifikasi.style.transform = 'translateX(0)';
    }, 100);
    
    // Hapus setelah 3 detik
    setTimeout(() => {
        notifikasi.style.transform = 'translateX(100%)';
        setTimeout(() => {
            notifikasi.remove();
        }, 300);
    }, 3000);
}

// Fungsi untuk menyimpan pesanan ke localStorage
function simpanPesanan(bahan) {
    // Ambil pesanan yang sudah ada
    let pesanan = JSON.parse(localStorage.getItem('pesananSITTA')) || [];
    
    // Tambahkan pesanan baru
    const pesananBaru = {
        id: Date.now(),
        kodeBarang: bahan.kodeBarang,
        namaBarang: bahan.namaBarang,
        tanggal: new Date().toISOString(),
        status: 'Diproses'
    };
    
    pesanan.push(pesananBaru);
    
    // Simpan ke localStorage
    localStorage.setItem('pesananSITTA', JSON.stringify(pesanan));
}

// Fungsi untuk validasi form
function validasiForm(form) {
    const inputs = form.querySelectorAll('input[required]');
    let isValid = true;
    
    inputs.forEach(input => {
        // Reset error
        input.style.borderColor = '';
        
        // Validasi
        if (!input.value.trim()) {
            input.style.borderColor = '#e74c3c';
            isValid = false;
        }
        
        // Validasi email
        if (input.type === 'email' && input.value) {
            const emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            if (!emailPattern.test(input.value)) {
                input.style.borderColor = '#e74c3c';
                isValid = false;
            }
        }
        
        // Validasi angka
        if (input.type === 'number' && input.value) {
            if (isNaN(input.value) || parseInt(input.value) < 1) {
                input.style.borderColor = '#e74c3c';
                isValid = false;
            }
        }
    });
    
    return isValid;
}

// Fungsi untuk membuat form pemesanan
function buatFormPemesanan() {
    const formHTML = `
        <div class="form-container">
            <h3>Form Pemesanan</h3>
            <form id="form-pemesanan">
                <div class="form-group">
                    <label for="nama">Nama Lengkap:</label>
                    <input type="text" id="nama" name="nama" required>
                </div>
                
                <div class="form-group">
                    <label for="email">Email:</label>
                    <input type="email" id="email" name="email" required>
                </div>
                
                <div class="form-group">
                    <label for="telepon">No. Telepon:</label>
                    <input type="tel" id="telepon" name="telepon" required>
                </div>
                
                <div class="form-group">
                    <label for="alamat">Alamat Pengiriman:</label>
                    <textarea id="alamat" name="alamat" rows="3" required></textarea>
                </div>
                
                <div class="form-group">
                    <label for="jumlah">Jumlah:</label>
                    <input type="number" id="jumlah" name="jumlah" min="1" value="1" required>
                </div>
                
                <div class="form-buttons">
                    <button type="submit" class="btn-submit">Pesan Sekarang</button>
                    <button type="button" class="btn-cancel" onclick="tutupForm()">Batal</button>
                </div>
            </form>
        </div>
    `;
    
    // Buat modal
    const modal = document.createElement('div');
    modal.className = 'modal';
    modal.innerHTML = formHTML;
    
    // Style modal
    modal.style.cssText = `
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-color: rgba(0,0,0,0.5);
        display: flex;
        justify-content: center;
        align-items: center;
        z-index: 1000;
    `;
    
    // Style form container
    const formContainer = modal.querySelector('.form-container');
    formContainer.style.cssText = `
        background: white;
        padding: 2rem;
        border-radius: 10px;
        max-width: 500px;
        width: 90%;
        max-height: 90vh;
        overflow-y: auto;
    `;
    
    // Tambahkan ke body
    document.body.appendChild(modal);
    
    // Event listener untuk form
    const form = modal.querySelector('#form-pemesanan');
    form.addEventListener('submit', function(e) {
        e.preventDefault();
        
        if (validasiForm(form)) {
            // Proses pemesanan
            const formData = new FormData(form);
            const data = Object.fromEntries(formData);
            
            tampilkanNotifikasi('Pesanan berhasil diproses!', 'success');
            tutupForm();
        } else {
            tampilkanNotifikasi('Mohon lengkapi semua field dengan benar!', 'error');
        }
    });
}

// Fungsi untuk menutup form
function tutupForm() {
    const modal = document.querySelector('.modal');
    if (modal) {
        modal.remove();
    }
}

// Inisialisasi saat halaman dimuat
document.addEventListener('DOMContentLoaded', function() {
    // Tampilkan daftar bahan ajar
    tampilkanBahanAjar();
    
    // Event listener untuk navigasi
    const navLinks = document.querySelectorAll('.nav-link');
    navLinks.forEach(link => {
        link.addEventListener('click', function(e) {
            e.preventDefault();
            
            // Hapus class active dari semua link
            navLinks.forEach(l => l.classList.remove('active'));
            
            // Tambahkan class active ke link yang diklik
            this.classList.add('active');
            
            // Scroll ke section
            const targetId = this.getAttribute('href').substring(1);
            const targetSection = document.getElementById(targetId);
            
            if (targetSection) {
                targetSection.scrollIntoView({ behavior: 'smooth' });
            }
        });
    });
    
    // Event listener untuk CTA button
    const ctaButton = document.querySelector('.cta-button');
    if (ctaButton) {
        ctaButton.addEventListener('click', function() {
            document.getElementById('stok').scrollIntoView({ behavior: 'smooth' });
        });
    }
    
    // Tambahkan style untuk form
    const formStyle = document.createElement('style');
    formStyle.textContent = `
        .form-group {
            margin-bottom: 1rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: bold;
            color: #2c3e50;
        }
        
        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 0.75rem;
            border: 2px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
            transition: border-color 0.3s ease;
        }
        
        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: #3498db;
        }
        
        .form-buttons {
            display: flex;
            gap: 1rem;
            margin-top: 1.5rem;
        }
        
        .btn-submit,
        .btn-cancel {
            flex: 1;
            padding: 0.75rem;
            border: none;
            border-radius: 5px;
            font-size: 1rem;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        
        .btn-submit {
            background-color: #27ae60;
            color: white;
        }
        
        .btn-submit:hover {
            background-color: #229954;
        }
        
        .btn-cancel {
            background-color: #e74c3c;
            color: white;
        }
        
        .btn-cancel:hover {
            background-color: #c0392b;
        }
        
        .no-data {
            text-align: center;
            color: #666;
            font-style: italic;
            padding: 2rem;
        }
    `;
    document.head.appendChild(formStyle);
});

// Export fungsi untuk digunakan di file lain
window.tampilkanBahanAjar = tampilkanBahanAjar;
window.pesanBahanAjar = pesanBahanAjar;
window.buatFormPemesanan = buatFormPemesanan;
window.tutupForm = tutupForm;
```

---

## 🛠️ **STUDI KASUS LENGKAP: APLIKASI SITTA**

### 🎯 **Project Overview**

**📖 Deskripsi:** Membangun aplikasi web lengkap untuk SITTA (Sistem Informasi Tiras dan Transaksi Bahan Ajar) Universitas Terbuka dengan menerapkan semua konsep HTML5, CSS3, dan JavaScript DOM yang telah dipelajari.

**🌟 Fitur Utama:**
- 📚 Katalog bahan ajar interaktif
- 🔍 Pencarian dan filter dinamis
- 🛒 Sistem pemesanan dengan validasi
- 📊 Statistik real-time
- 📱 Responsive design untuk semua device
- ♿ Accessibility features
- 💾 Local storage untuk data persistence

### 📂 **Struktur Proyek Professional**

```
tugas1-sitta/
├── 📄 index.html                    ← Halaman utama aplikasi
├── 📁 css/                          ← Stylesheets
│   ├── style.css                   ← Main stylesheet
│   ├── components.css              ← Component styles
│   ├── responsive.css              ← Media queries
│   └── animations.css              ← Animations & transitions
├── 📁 js/                           ← JavaScript files
│   ├── data.js                     ← Data bahan ajar & pengguna
│   ├── app.js                      ← Main application logic
│   ├── components/                 ← Reusable components
│   │   ├── navbar.js              ← Navigation component
│   │   ├── product-card.js        ← Product card component
│   │   ├── modal.js               ← Modal component
│   │   └── notification.js        ← Notification system
│   └── utils/                      ← Utility functions
│       ├── dom.js                 ← DOM helpers
│       ├── validation.js          ← Form validation
│       └── storage.js             ← Local storage utilities
├── 📁 img/                          ← Images & assets
│   ├── covers/                     ← Book cover images
│   │   ├── pengantar_komunikasi.jpg
│   │   ├── manajemen_keuangan.jpg
│   │   ├── kepemimpinan.jpg
│   │   ├── mikrobiologi.jpg
│   │   └── paud_perkembangan.jpg
│   ├── icons/                      ← Icon images
│   └── placeholders/               ← Placeholder images
├── 📄 README.md                     ← Project documentation
├── 📄 CHANGELOG.md                  ← Version history
└── 📄 .gitignore                    ← Git ignore file
```

### 📄 **File Lengkap: index.html**

```html
<!DOCTYPE html>
<html lang="id">
<head>
    <!-- Meta Tags -->
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    
    <!-- SEO Meta Tags -->
    <title>SITTA - Sistem Informasi Tiras dan Transaksi Bahan Ajar | Universitas Terbuka</title>
    <meta name="description" content="Platform resmi pemesanan bahan ajar digital Universitas Terbuka. Akses ribuan modul kuliah dengan mudah, cepat, dan terjangkau.">
    <meta name="keywords" content="SITTA, Universitas Terbuka, bahan ajar, modul kuliah, pemesanan online, UT">
    <meta name="author" content="Universitas Terbuka">
    <meta name="robots" content="index, follow">
    
    <!-- Open Graph Meta Tags -->
    <meta property="og:title" content="SITTA - Universitas Terbuka">
    <meta property="og:description" content="Platform pemesanan bahan ajar digital Universitas Terbuka">
    <meta property="og:image" content="https://sitta.ut.ac.id/img/og-image.jpg">
    <meta property="og:url" content="https://sitta.ut.ac.id">
    <meta property="og:type" content="website">
    
    <!-- Twitter Card Meta Tags -->
    <meta name="twitter:card" content="summary_large_image">
    <meta name="twitter:title" content="SITTA - Universitas Terbuka">
    <meta name="twitter:description" content="Platform pemesanan bahan ajar digital">
    <meta name="twitter:image" content="https://sitta.ut.ac.id/img/twitter-image.jpg">
    
    <!-- Favicon -->
    <link rel="icon" type="image/svg+xml" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><text y='.9em' font-size='90'>📚</text></svg>">
    <link rel="apple-touch-icon" href="img/apple-touch-icon.png">
    
    <!-- Preconnect to external domains -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    
    <!-- CSS Files -->
    <link rel="stylesheet" href="css/style.css">
    <link rel="stylesheet" href="css/components.css">
    <link rel="stylesheet" href="css/responsive.css">
    <link rel="stylesheet" href="css/animations.css">
    
    <!-- Theme Color for Mobile Browsers -->
    <meta name="theme-color" content="#2c3e50">
    
    <!-- Apple Safari Theme Color -->
    <meta name="apple-mobile-web-app-status-bar-style" content="#2c3e50">
    
    <!-- Manifest for PWA -->
    <link rel="manifest" href="manifest.json">
</head>
<body>
    <!-- Skip to main content for accessibility -->
    <a href="#main-content" class="skip-link">Skip to main content</a>
    
    <!-- Loading Screen -->
    <div id="loading-screen" class="loading-screen">
        <div class="loading-content">
            <div class="loading-spinner">
                <div class="spinner"></div>
            </div>
            <h2>Loading SITTA...</h2>
            <p>Mempersiapkan platform pemesanan bahan ajar</p>
        </div>
    </div>
    
    <!-- Header with Navigation -->
    <header class="site-header" role="banner">
        <div class="container">
            <div class="header-content">
                <!-- Branding Section -->
                <div class="branding">
                    <div class="logo-container">
                        <img src="img/logo.svg" alt="SITTA Logo" class="logo-image">
                        <div class="logo-text">
                            <h1 class="logo-title">📚 SITTA</h1>
                            <p class="logo-subtitle">Universitas Terbuka</p>
                        </div>
                    </div>
                </div>
                
                <!-- User Actions -->
                <div class="user-actions">
                    <button class="btn btn-outline btn-sm" id="btn-search" aria-label="Search">
                        🔍
                    </button>
                    <button class="btn btn-outline btn-sm" id="btn-notifications" aria-label="Notifications">
                        🔔
                        <span class="notification-badge">3</span>
                    </button>
                    <button class="btn btn-primary btn-sm" id="btn-login">
                        👤 Masuk
                    </button>
                    <button class="btn btn-secondary btn-sm" id="btn-register">
                        📝 Daftar
                    </button>
                </div>
                
                <!-- Mobile Menu Toggle -->
                <button class="mobile-menu-toggle" id="mobile-menu-toggle" aria-label="Toggle mobile menu">
                    <span class="hamburger-line"></span>
                    <span class="hamburger-line"></span>
                    <span class="hamburger-line"></span>
                </button>
            </div>
        </div>
        
        <!-- Main Navigation -->
        <nav class="main-navigation" role="navigation" aria-label="Main navigation">
            <div class="container">
                <ul class="nav-menu" id="nav-menu">
                    <li class="nav-item">
                        <a href="#beranda" class="nav-link active" data-section="beranda">
                            <span class="nav-icon">🏠</span>
                            <span class="nav-text">Beranda</span>
                        </a>
                    </li>
                    <li class="nav-item">
                        <a href="#stok" class="nav-link" data-section="stok">
                            <span class="nav-icon">📦</span>
                            <span class="nav-text">Stok Bahan Ajar</span>
                        </a>
                    </li>
                    <li class="nav-item">
                        <a href="#tracking" class="nav-link" data-section="tracking">
                            <span class="nav-icon">📍</span>
                            <span class="nav-text">Tracking Pesanan</span>
                        </a>
                    </li>
                    <li class="nav-item">
                        <a href="#bantuan" class="nav-link" data-section="bantuan">
                            <span class="nav-icon">❓</span>
                            <span class="nav-text">Bantuan</span>
                        </a>
                    </li>
                    <li class="nav-item">
                        <a href="#kontak" class="nav-link" data-section="kontak">
                            <span class="nav-icon">📞</span>
                            <span class="nav-text">Kontak</span>
                        </a>
                    </li>
                </ul>
            </div>
        </nav>
    </header>
    
    <!-- Search Overlay -->
    <div class="search-overlay" id="search-overlay">
        <div class="search-container">
            <div class="search-header">
                <h2>Cari Bahan Ajar</h2>
                <button class="search-close" id="search-close" aria-label="Close search">&times;</button>
            </div>
            <div class="search-form">
                <input 
                    type="search" 
                    id="global-search-input"
                    class="search-input" 
                    placeholder="Ketik judul, kode, atau pengarang..."
                    autocomplete="off"
                    autofocus
                >
                <div class="search-suggestions" id="search-suggestions">
                    <!-- Search suggestions will appear here -->
                </div>
            </div>
        </div>
    </div>
    
    <!-- Main Content Area -->
    <main id="main-content" class="main-content" role="main">
        <div class="container">
            
            <!-- Hero Section -->
            <section id="beranda" class="hero-section" data-section="beranda">
                <div class="hero-content">
                    <div class="hero-text">
                        <h2 class="hero-title animate-fade-in">
                            Selamat Datang di <span class="highlight">SITTA</span>
                        </h2>
                        <p class="hero-subtitle animate-fade-in animate-delay-1">
                            Sistem Informasi Tiras dan Transaksi Bahan Ajar Universitas Terbuka
                        </p>
                        <p class="hero-description animate-fade-in animate-delay-2">
                            Platform digital terpercaya untuk pemesanan bahan ajar berkualitas. 
                            Akses ribuan modul kuliah dengan mudah, cepat, dan terjangkau.
                        </p>
                        
                        <!-- Call to Action Buttons -->
                        <div class="cta-container animate-fade-in animate-delay-3">
                            <button class="btn btn-primary btn-lg cta-button" id="cta-browse">
                                🛒 Jelajahi Koleksi
                            </button>
                            <button class="btn btn-outline btn-lg cta-button" id="cta-guide">
                                🎥 Panduan Video
                            </button>
                        </div>
                        
                        <!-- Trust Indicators -->
                        <div class="trust-indicators animate-fade-in animate-delay-4">
                            <div class="trust-item">
                                <span class="trust-icon">✅</span>
                                <span class="trust-text">Resmi UT</span>
                            </div>
                            <div class="trust-item">
                                <span class="trust-icon">🔒</span>
                                <span class="trust-text">Pembayaran Aman</span>
                            </div>
                            <div class="trust-item">
                                <span class="trust-icon">🚚</span>
                                <span class="trust-text">Pengiriman Cepat</span>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Hero Visual -->
                    <div class="hero-visual animate-slide-in-right">
                        <div class="hero-image-container">
                            <img src="img/hero-illustration.svg" alt="SITTA Platform Illustration" class="hero-image">
                            <div class="floating-elements">
                                <div class="floating-element floating-book">📚</div>
                                <div class="floating-element floating-laptop">💻</div>
                                <div class="floating-element floating-graduation">🎓</div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Statistics Section -->
                <div class="stats-section">
                    <div class="stats-grid">
                        <div class="stat-card animate-counter" data-target="1247">
                            <div class="stat-number">0</div>
                            <div class="stat-label">Total Bahan Ajar</div>
                            <div class="stat-icon">📚</div>
                        </div>
                        <div class="stat-card animate-counter" data-target="5832">
                            <div class="stat-number">0</div>
                            <div class="stat-label">Pengguna Aktif</div>
                            <div class="stat-icon">👥</div>
                        </div>
                        <div class="stat-card animate-counter" data-target="98">
                            <div class="stat-number">0</div>
                            <div class="stat-label">% Kepuasan</div>
                            <div class="stat-icon">⭐</div>
                        </div>
                        <div class="stat-card animate-counter" data-target="24">
                            <div class="stat-number">0</div>
                            <div class="stat-label">Jam Pengiriman</div>
                            <div class="stat-icon">🚚</div>
                        </div>
                    </div>
                </div>
            </section>
            
            <!-- Features Section -->
            <section class="features-section" aria-labelledby="features-heading">
                <div class="section-header">
                    <h2 id="features-heading" class="section-title">🌟 Fitur Unggulan</h2>
                    <p class="section-subtitle">Kemudahan dan kenyamanan dalam satu platform</p>
                </div>
                
                <div class="features-grid">
                    <article class="feature-card animate-fade-in">
                        <div class="feature-icon-container">
                            <div class="feature-icon">📚</div>
                        </div>
                        <h3 class="feature-title">Koleksi Lengkap</h3>
                        <p class="feature-description">
                            Akses ribuan modul kuliah dari berbagai program studi Universitas Terbuka. 
                            Dari dasar hingga lanjutan, semua tersedia dalam satu platform.
                        </p>
                        <ul class="feature-list">
                            <li>1,247+ judul bahan ajar</li>
                            <li>10+ program studi</li>
                            <li>Update konten berkala</li>
                        </ul>
                        <button class="btn btn-outline feature-link">Jelajahi Koleksi →</button>
                    </article>
                    
                    <article class="feature-card animate-fade-in animate-delay-1">
                        <div class="feature-icon-container">
                            <div class="feature-icon">🚀</div>
                        </div>
                        <h3 class="feature-title">Pengiriman Cepat</h3>
                        <p class="feature-description">
                            Pesanan diproses dan dikirim dalam waktu 24 jam ke seluruh Indonesia. 
                            Tracking real-time untuk memantau status pengiriman.
                        </p>
                        <ul class="feature-list">
                            <li>Proses 24 jam</li>
                            <li>Cover seluruh Indonesia</li>
                            <li>Tracking real-time</li>
                        </ul>
                        <button class="btn btn-outline feature-link">Info Pengiriman →</button>
                    </article>
                    
                    <article class="feature-card animate-fade-in animate-delay-2">
                        <div class="feature-icon-container">
                            <div class="feature-icon">📱</div>
                        </div>
                        <h3 class="feature-title">Mudah Diakses</h3>
                        <p class="feature-description">
                            Platform responsif yang bisa diakses dari berbagai perangkat. 
                            Aplikasi mobile-friendly dengan user interface yang intuitif.
                        </p>
                        <ul class="feature-list">
                            <li>Responsive design</li>
                            <li>Mobile apps</li>
                            <li>Offline mode</li>
                        </ul>
                        <button class="btn btn-outline feature-link">Download Apps →</button>
                    </article>
                    
                    <article class="feature-card animate-fade-in animate-delay-3">
                        <div class="feature-icon-container">
                            <div class="feature-icon">💰</div>
                        </div>
                        <h3 class="feature-title">Harga Terjangkau</h3>
                        <p class="feature-description">
                            Dapatkan bahan ajar berkualitas dengan harga subsidi dari Universitas Terbuka. 
                            Berbagai metode pembayaran yang aman dan mudah.
                        </p>
                        <ul class="feature-list">
                            <li>Harga subsidi</li>
                            <li>Multiple payment</li>
                            <li>Installment options</li>
                        </ul>
                        <button class="btn btn-outline feature-link">Info Harga →</button>
                    </article>
                </div>
            </section>
            
            <!-- Products Section -->
            <section id="stok" class="products-section" data-section="stok">
                <div class="section-header">
                    <h2 class="section-title">📦 Stok Bahan Ajar Tersedia</h2>
                    <p class="section-subtitle">Temukan bahan ajar yang Anda butuhkan</p>
                </div>
                
                <!-- Search and Filter Controls -->
                <div class="search-filter-container">
                    <div class="search-box">
                        <div class="search-input-group">
                            <input 
                                type="search" 
                                id="product-search"
                                class="search-input" 
                                placeholder="Cari bahan ajar..."
                                aria-label="Cari bahan ajar"
                            >
                            <button class="search-button" id="product-search-btn" aria-label="Cari">
                                🔍
                            </button>
                        </div>
                    </div>
                    
                    <div class="filter-controls">
                        <div class="filter-group">
                            <label for="category-filter" class="filter-label">Kategori:</label>
                            <select id="category-filter" class="filter-select" aria-label="Filter kategori">
                                <option value="">Semua Kategori</option>
                                <option value="bmp">BMP</option>
                                <option value="modul">Modul Praktikum</option>
                                <option value="referensi">Buku Referensi</option>
                                <option value="cd">CD/DVD Materi</option>
                            </select>
                        </div>
                        
                        <div class="filter-group">
                            <label for="program-filter" class="filter-label">Program Studi:</label>
                            <select id="program-filter" class="filter-select" aria-label="Filter program studi">
                                <option value="">Semua Program</option>
                                <option value="ti">Teknik Informatika</option>
                                <option value="si">Sistem Informasi</option>
                                <option value="mi">Manajemen Informatika</option>
                                <option value="tk">Teknik Komputer</option>
                            </select>
                        </div>
                        
                        <div class="filter-group">
                            <label for="sort-filter" class="filter-label">Urutkan:</label>
                            <select id="sort-filter" class="filter-select" aria-label="Urutkan hasil">
                                <option value="relevance">Relevansi</option>
                                <option value="name-asc">Nama (A-Z)</option>
                                <option value="name-desc">Nama (Z-A)</option>
                                <option value="price-low">Harga Terendah</option>
                                <option value="price-high">Harga Tertinggi</option>
                                <option value="stock-high">Stok Terbanyak</option>
                                <option value="newest">Terbaru</option>
                            </select>
                        </div>
                        
                        <div class="filter-group">
                            <label for="view-toggle" class="filter-label">Tampilan:</label>
                            <div class="view-toggle">
                                <button class="view-btn active" data-view="grid" aria-label="Grid view">
                                    ⊞
                                </button>
                                <button class="view-btn" data-view="list" aria-label="List view">
                                    ☰
                                </button>
                            </div>
                        </div>
                        
                        <button class="btn btn-outline btn-sm" id="reset-filters">
                            🔄 Reset
                        </button>
                    </div>
                </div>
                
                <!-- Active Filters Display -->
                <div class="active-filters" id="active-filters">
                    <!-- Active filter tags will appear here -->
                </div>
                
                <!-- Results Summary -->
                <div class="results-summary">
                    <p class="results-count">
                        Menampilkan <span id="results-count">0</span> dari <span id="total-count">0</span> bahan ajar
                    </p>
                    <div class="results-actions">
                        <button class="btn btn-sm btn-outline" id="compare-btn">
                            ⚖️ Bandingkan (<span id="compare-count">0</span>)
                        </button>
                    </div>
                </div>
                
                <!-- Loading State -->
                <div class="loading-state" id="products-loading" style="display: none;">
                    <div class="loading-spinner">
                        <div class="spinner"></div>
                    </div>
                    <p>Memuat data bahan ajar...</p>
                </div>
                
                <!-- Products Grid/List -->
                <div class="products-container" id="products-container">
                    <!-- Products will be dynamically loaded here -->
                    <div class="products-placeholder">
                        <div class="placeholder-card">
                            <div class="placeholder-image"></div>
                            <div class="placeholder-content">
                                <div class="placeholder-title"></div>
                                <div class="placeholder-text"></div>
                                <div class="placeholder-price"></div>
                            </div>
                        </div>
                        <div class="placeholder-card">
                            <div class="placeholder-image"></div>
                            <div class="placeholder-content">
                                <div class="placeholder-title"></div>
                                <div class="placeholder-text"></div>
                                <div class="placeholder-price"></div>
                            </div>
                        </div>
                        <div class="placeholder-card">
                            <div class="placeholder-image"></div>
                            <div class="placeholder-content">
                                <div class="placeholder-title"></div>
                                <div class="placeholder-text"></div>
                                <div class="placeholder-price"></div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Pagination -->
                <div class="pagination-container" id="pagination-container">
                    <div class="pagination">
                        <button class="pagination-btn prev-btn" id="prev-page" disabled>
                            ← Previous
                        </button>
                        <div class="pagination-info">
                            Halaman <span id="current-page">1</span> dari <span id="total-pages">1</span>
                        </div>
                        <button class="pagination-btn next-btn" id="next-page">
                            Next →
                        </button>
                    </div>
                </div>
            </section>
            
            <!-- How It Works Section -->
            <section class="how-it-works-section">
                <div class="section-header">
                    <h2 class="section-title">🔄 Cara Pemesanan</h2>
                    <p class="section-subtitle">Mudah dan cepat dalam 4 langkah sederhana</p>
                </div>
                
                <div class="steps-container">
                    <div class="step-card animate-fade-in">
                        <div class="step-number">1</div>
                        <div class="step-icon">🔍</div>
                        <h3 class="step-title">Cari Bahan Ajar</h3>
                        <p class="step-description">
                            Gunakan fitur pencarian untuk menemukan bahan ajar yang Anda butuhkan. 
                            Filter berdasarkan kategori, program studi, atau harga.
                        </p>
                    </div>
                    
                    <div class="step-card animate-fade-in animate-delay-1">
                        <div class="step-number">2</div>
                        <div class="step-icon">📋</div>
                        <h3 class="step-title">Pilih & Detail</h3>
                        <p class="step-description">
                            Lihat detail bahan ajar, cek stok tersedia, dan tambahkan ke keranjang. 
                            Bandingkan beberapa produk jika perlu.
                        </p>
                    </div>
                    
                    <div class="step-card animate-fade-in animate-delay-2">
                        <div class="step-number">3</div>
                        <div class="step-icon">🛒</div>
                        <h3 class="step-title">Checkout</h3>
                        <p class="step-description">
                            Isi form pemesanan dengan data lengkap. Pilih metode pembayaran 
                            yang tersedia dan konfirmasi pesanan.
                        </p>
                    </div>
                    
                    <div class="step-card animate-fade-in animate-delay-3">
                        <div class="step-number">4</div>
                        <div class="step-icon">📦</div>
                        <h3 class="step-title">Terima Pesanan</h3>
                        <p class="step-description">
                            Pesanan akan diproses dan dikirim dalam 24 jam. 
                            Track status pengiriman secara real-time.
                        </p>
                    </div>
                </div>
                
                <div class="cta-section">
                    <h3>Siap Memulai?</h3>
                    <p>Bergabung dengan ribuan mahasiswa yang telah menggunakan SITTA</p>
                    <button class="btn btn-primary btn-lg" id="start-ordering">
                        🚀 Mulai Pemesanan Sekarang
                    </button>
                </div>
            </section>
            
        </div>
    </main>
    
    <!-- Shopping Cart Sidebar -->
    <div class="cart-sidebar" id="cart-sidebar">
        <div class="cart-header">
            <h3>🛒 Keranjang Belanja</h3>
            <button class="cart-close" id="cart-close" aria-label="Close cart">&times;</button>
        </div>
        
        <div class="cart-content">
            <div class="cart-items" id="cart-items">
                <!-- Cart items will be dynamically added here -->
                <div class="empty-cart">
                    <div class="empty-cart-icon">🛒</div>
                    <p>Keranjang belanja kosong</p>
                    <button class="btn btn-outline btn-sm" id="continue-shopping">
                        Lanjut Belanja
                    </button>
                </div>
            </div>
            
            <div class="cart-summary">
                <div class="summary-row">
                    <span>Subtotal:</span>
                    <span id="cart-subtotal">Rp 0</span>
                </div>
                <div class="summary-row">
                    <span>Ongkir:</span>
                    <span id="cart-shipping">Rp 0</span>
                </div>
                <div class="summary-row total">
                    <span>Total:</span>
                    <span id="cart-total">Rp 0</span>
                </div>
            </div>
            
            <div class="cart-actions">
                <button class="btn btn-outline btn-block" id="view-cart">
                    Lihat Keranjang
                </button>
                <button class="btn btn-primary btn-block" id="checkout" disabled>
                    Checkout
                </button>
            </div>
        </div>
    </div>
    
    <!-- Footer -->
    <footer class="site-footer" role="contentinfo">
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <div class="footer-branding">
                        <h3 class="footer-title">📚 SITTA</h3>
                        <p class="footer-description">
                            Sistem Informasi Tiras dan Transaksi Bahan Ajar adalah platform resmi 
                            Universitas Terbuka untuk pemesanan bahan ajar digital.
                        </p>
                        <div class="footer-stats">
                            <div class="footer-stat">
                                <strong>1,247+</strong>
                                <span>Bahan Ajar</span>
                            </div>
                            <div class="footer-stat">
                                <strong>5,832+</strong>
                                <span>Pengguna Aktif</span>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="footer-section">
                    <h3 class="footer-title">Link Cepat</h3>
                    <nav class="footer-nav" aria-label="Footer navigation">
                        <ul>
                            <li><a href="#beranda">Beranda</a></li>
                            <li><a href="#stok">Stok Bahan Ajar</a></li>
                            <li><a href="#tracking">Tracking Pesanan</a></li>
                            <li><a href="#bantuan">Bantuan</a></li>
                            <li><a href="#kontak">Kontak</a></li>
                        </ul>
                    </nav>
                </div>
                
                <div class="footer-section">
                    <h3 class="footer-title">Layanan</h3>
                    <ul class="footer-links">
                        <li><a href="#">Panduan Pemesanan</a></li>
                        <li><a href="#">Metode Pembayaran</a></li>
                        <li><a href="#">Info Pengiriman</a></li>
                        <li><a href="#">Kebijakan Retur</a></li>
                        <li><a href="#">FAQ</a></li>
                    </ul>
                </div>
                
                <div class="footer-section">
                    <h3 class="footer-title">Hubungi Kami</h3>
                    <div class="contact-info">
                        <div class="contact-item">
                            <span class="contact-icon">📍</span>
                            <div class="contact-details">
                                <strong>Alamat:</strong>
                                <p>Jl. Pamulang Permai IV, Tangerang Selatan, Banten 15415</p>
                            </div>
                        </div>
                        <div class="contact-item">
                            <span class="contact-icon">📧</span>
                            <div class="contact-details">
                                <strong>Email:</strong>
                                <p>sitta@ut.ac.id</p>
                            </div>
                        </div>
                        <div class="contact-item">
                            <span class="contact-icon">📞</span>
                            <div class="contact-details">
                                <strong>Telepon:</strong>
                                <p>(021) 7490941</p>
                            </div>
                        </div>
                        <div class="contact-item">
                            <span class="contact-icon">⏰</span>
                            <div class="contact-details">
                                <strong>Jam Operasional:</strong>
                                <p>Senin - Jumat, 08:00 - 16:00 WIB</p>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="footer-section">
                    <h3 class="footer-title">Ikuti Kami</h3>
                    <div class="social-links">
                        <a href="#" class="social-link" aria-label="Facebook">
                            <svg class="social-icon" viewBox="0 0 24 24">
                                <path d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z"/>
                            </svg>
                        </a>
                        <a href="#" class="social-link" aria-label="Twitter">
                            <svg class="social-icon" viewBox="0 0 24 24">
                                <path d="M23.953 4.57a10 10 0 01-2.825.775 4.958 4.958 0 002.163-2.723c-.951.555-2.005.959-3.127 1.184a4.92 4.92 0 00-8.384 4.482C7.69 8.095 4.067 6.13 1.64 3.162a4.822 4.822 0 00-.666 2.475c0 1.71.87 3.213 2.188 4.096a4.904 4.904 0 01-2.228-.616v.06a4.923 4.923 0 003.946 4.827 4.996 4.996 0 01-2.212.085 4.936 4.936 0 004.604 3.417 9.867 9.867 0 01-6.102 2.105c-.39 0-.779-.023-1.17-.067a13.995 13.995 0 007.557 2.209c9.053 0 13.998-7.496 13.998-13.985 0-.21 0-.42-.015-.63A9.935 9.935 0 0024 4.59z"/>
                            </svg>
                        </a>
                        <a href="#" class="social-link" aria-label="Instagram">
                            <svg class="social-icon" viewBox="0 0 24 24">
                                <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zM5.838 12a6.162 6.162 0 1112.324 0 6.162 6.162 0 01-12.324 0zM12 16a4 4 0 110-8 4 4 0 010 8zm4.965-10.405a1.44 1.44 0 112.881.001 1.44 1.44 0 01-2.881-.001z"/>
                            </svg>
                        </a>
                        <a href="#" class="social-link" aria-label="YouTube">
                            <svg class="social-icon" viewBox="0 0 24 24">
                                <path d="M23.498 6.186a3.016 3.016 0 0 0-2.122-2.136C19.505 3.545 12 3.545 12 3.545s-7.505 0-9.377.505A3.017 3.017 0 0 0 .502 6.186C0 8.07 0 12 0 12s0 3.93.502 5.814a3.016 3.016 0 0 0 2.122 2.136c1.871.505 9.376.505 9.376.505s7.505 0 9.377-.505a3.015 3.015 0 0 0 2.122-2.136C24 15.93 24 12 24 12s0-3.93-.502-5.814zM9.545 15.568V8.432L15.818 12l-6.273 3.568z"/>
                            </svg>
                        </a>
                    </div>
                    
                    <div class="newsletter">
                        <h4>Newsletter</h4>
                        <p>Dapatkan info terbaru tentang bahan ajar dan promo</p>
                        <form class="newsletter-form" id="newsletter-form">
                            <input 
                                type="email" 
                                placeholder="Email Anda" 
                                class="newsletter-input"
                                required
                            >
                            <button type="submit" class="newsletter-btn">
                                📧
                            </button>
                        </form>
                    </div>
                </div>
            </div>
            
            <div class="footer-bottom">
                <div class="footer-bottom-content">
                    <p class="copyright">
                        &copy; 2025 Universitas Terbuka. All rights reserved.
                    </p>
                    <div class="footer-links-bottom">
                        <a href="#">Privacy Policy</a>
                        <span class="separator">|</span>
                        <a href="#">Terms of Service</a>
                        <span class="separator">|</span>
                        <a href="#">Cookie Policy</a>
                        <span class="separator">|</span>
                        <a href="#">Accessibility</a>
                    </div>
                </div>
            </div>
        </div>
    </footer>
    
    <!-- Back to Top Button -->
    <button class="back-to-top" id="back-to-top" aria-label="Back to top">
        <svg class="back-to-top-icon" viewBox="0 0 24 24">
            <path d="M7 14l5-5 5 5z"/>
        </svg>
    </button>
    
    <!-- Notification Container -->
    <div class="notification-container" id="notification-container">
        <!-- Notifications will appear here -->
    </div>
    
    <!-- Modal Container -->
    <div class="modal-container" id="modal-container">
        <!-- Modals will appear here -->
    </div>
    
    <!-- JavaScript Files -->
    <script src="js/data.js"></script>
    <script src="js/utils/dom.js"></script>
    <script src="js/utils/validation.js"></script>
    <script src="js/utils/storage.js"></script>
    <script src="js/components/navbar.js"></script>
    <script src="js/components/product-card.js"></script>
    <script src="js/components/modal.js"></script>
    <script src="js/components/notification.js"></script>
    <script src="js/app.js"></script>
</body>
</html>
```
/tugas1-sitta/
├── index.html              ← Halaman utama
├── css/
│   └── style.css          ← File CSS eksternal
├── js/
│   ├── data.js            ← Data bahan ajar
│   └── app.js             ← Logika JavaScript
├── img/
│   ├── pengantar_komunikasi.jpg
│   ├── manajemen_keuangan.jpg
│   ├── kepemimpinan.jpg
│   ├── mikrobiologi.jpg
│   └── paud_perkembangan.jpg
└── README.md              ← Dokumentasi proyek
```

### 📄 **File Lengkap: index.html**
```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SITTA - Sistem Informasi Tiras dan Transaksi Bahan Ajar</title>
    <meta name="description" content="Sistem Informasi Tiras dan Transaksi Bahan Ajar Universitas Terbuka">
    <meta name="author" content="Universitas Terbuka">
    
    <!-- CSS Eksternal -->
    <link rel="stylesheet" href="css/style.css">
    
    <!-- Favicon -->
    <link rel="icon" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><text y='.9em' font-size='90'>📚</text></svg>">
</head>
<body>
    <!-- Header -->
    <header class="header">
        <div class="container">
            <h1 class="logo">📚 SITTA</h1>
            <p class="subtitle">Sistem Informasi Tiras dan Transaksi Bahan Ajar</p>
            <p class="institution">Universitas Terbuka</p>
        </div>
    </header>
    
    <!-- Navigation -->
    <nav class="navigation">
        <div class="container">
            <ul>
                <li><a href="#beranda" class="nav-link active">🏠 Beranda</a></li>
                <li><a href="#stok" class="nav-link">📦 Stok Bahan Ajar</a></li>
                <li><a href="#tracking" class="nav-link">📍 Tracking Pesanan</a></li>
                <li><a href="#kontak" class="nav-link">📞 Kontak</a></li>
            </ul>
        </div>
    </nav>
    
    <!-- Main Content -->
    <main class="main-content">
        <div class="container">
            <!-- Hero Section -->
            <section id="beranda" class="hero-section">
                <h2>Selamat Datang di SITTA</h2>
                <p>Platform pemesanan bahan ajar digital Universitas Terbuka</p>
                <p>Dapatkan modul kuliah berkualitas dengan mudah dan cepat</p>
                <button class="cta-button" onclick="scrollToStok()">🛒 Mulai Pemesanan</button>
            </section>
            
            <!-- Features Section -->
            <section class="features-section">
                <h2>Fitur Unggulan</h2>
                <div class="features-grid">
                    <div class="feature-card">
                        <div class="feature-icon">📚</div>
                        <h3>Koleksi Lengkap</h3>
                        <p>Akses ribuan modul kuliah dari berbagai program studi</p>
                    </div>
                    <div class="feature-card">
                        <div class="feature-icon">🚀</div>
                        <h3>Pengiriman Cepat</h3>
                        <p>Pesanan diproses dan dikirim dalam waktu 24 jam</p>
                    </div>
                    <div class="feature-card">
                        <div class="feature-icon">📱</div>
                        <h3>Mudah Diakses</h3>
                        <p>Platform responsif yang bisa diakses dari berbagai perangkat</p>
                    </div>
                </div>
            </section>
            
            <!-- Stok Section -->
            <section id="stok" class="stok-section">
                <h2>📦 Stok Bahan Ajar Tersedia</h2>
                <div class="filter-container">
                    <input type="text" id="search-input" placeholder="Cari bahan ajar..." class="search-input">
                    <select id="filter-jenis" class="filter-select">
                        <option value="">Semua Jenis</option>
                        <option value="BMP">BMP</option>
                        <option value="Modul">Modul</option>
                    </select>
                </div>
                <div id="daftar-bahan-ajar" class="bahan-ajar-grid">
                    <!-- Konten akan diisi dengan JavaScript -->
                </div>
            </section>
            
            <!-- Tracking Section -->
            <section id="tracking" class="tracking-section">
                <h2>📍 Tracking Pesanan</h2>
                <div class="tracking-container">
                    <input type="text" id="tracking-input" placeholder="Masukkan nomor pesanan..." class="tracking-input">
                    <button onclick="trackPesanan()" class="tracking-button">Track</button>
                </div>
                <div id="tracking-result" class="tracking-result">
                    <!-- Hasil tracking akan ditampilkan di sini -->
                </div>
            </section>
            
            <!-- Kontak Section -->
            <section id="kontak" class="kontak-section">
                <h2>📞 Hubungi Kami</h2>
                <div class="kontak-grid">
                    <div class="kontak-info">
                        <h3>Informasi Kontak</h3>
                        <p><strong>Alamat:</strong> Jl. Pamulang Permai IV, Tangerang Selatan</p>
                        <p><strong>Email:</strong> sitta@ut.ac.id</p>
                        <p><strong>Telepon:</strong> (021) 7490941</p>
                        <p><strong>Jam Operasional:</strong> Senin - Jumat, 08:00 - 16:00 WIB</p>
                    </div>
                    <div class="kontak-form">
                        <h3>Kirim Pesan</h3>
                        <form id="kontak-form">
                            <div class="form-group">
                                <label for="nama-kontak">Nama:</label>
                                <input type="text" id="nama-kontak" required>
                            </div>
                            <div class="form-group">
                                <label for="email-kontak">Email:</label>
                                <input type="email" id="email-kontak" required>
                            </div>
                            <div class="form-group">
                                <label for="pesan-kontak">Pesan:</label>
                                <textarea id="pesan-kontak" rows="4" required></textarea>
                            </div>
                            <button type="submit" class="btn-submit">Kirim Pesan</button>
                        </form>
                    </div>
                </div>
            </section>
        </div>
    </main>
    
    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>Tentang SITTA</h3>
                    <p>Sistem Informasi Tiras dan Transaksi Bahan Ajar Universitas Terbuka</p>
                </div>
                <div class="footer-section">
                    <h3>Link Cepat</h3>
                    <ul>
                        <li><a href="#beranda">Beranda</a></li>
                        <li><a href="#stok">Stok Bahan Ajar</a></li>
                        <li><a href="#tracking">Tracking</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h3>Ikuti Kami</h3>
                    <div class="social-links">
                        <a href="#">📘 Facebook</a>
                        <a href="#">🐦 Twitter</a>
                        <a href="#">📷 Instagram</a>
                    </div>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2025 Universitas Terbuka. All rights reserved.</p>
            </div>
        </div>
    </footer>
    
    <!-- JavaScript -->
    <script src="js/data.js"></script>
    <script src="js/app.js"></script>
</body>
</html>
```

---

## 🧪 **Latihan Praktik Interaktif**

### ✅ **Latihan 1: Membuat Form Pemesanan Dinamis**
```javascript
// Fungsi untuk membuat form pemesanan dinamis
function buatFormPemesananDinamis(kodeBarang) {
    const bahan = dataBahanAjar.find(item => item.kodeBarang === kodeBarang);
    
    if (!bahan) {
        tampilkanNotifikasi('Bahan ajar tidak ditemukan!', 'error');
        return;
    }
    
    const formHTML = `
        <div class="modal">
            <div class="modal-content">
                <div class="modal-header">
                    <h3>Form Pemesanan</h3>
                    <span class="close" onclick="tutupModal()">&times;</span>
                </div>
                <div class="modal-body">
                    <div class="bahan-info">
                        <h4>${bahan.namaBarang}</h4>
                        <p>Kode: ${bahan.kodeBarang}</p>
                        <p>Stok tersedia: ${bahan.stok} buah</p>
                    </div>
                    <form id="form-pemesanan-detail">
                        <div class="form-group">
                            <label for="jumlah-pesan">Jumlah:</label>
                            <input type="number" id="jumlah-pesan" min="1" max="${bahan.stok}" value="1" required>
                            <small>Maksimal: ${bahan.stok} buah</small>
                        </div>
                        <div class="form-group">
                            <label for="nama-pemesan">Nama Lengkap:</label>
                            <input type="text" id="nama-pemesan" required>
                        </div>
                        <div class="form-group">
                            <label for="email-pemesan">Email:</label>
                            <input type="email" id="email-pemesan" required>
                        </div>
                        <div class="form-group">
                            <label for="telepon-pemesan">No. Telepon:</label>
                            <input type="tel" id="telepon-pemesan" required>
                        </div>
                        <div class="form-group">
                            <label for="alamat-pemesan">Alamat Lengkap:</label>
                            <textarea id="alamat-pemesan" rows="3" required></textarea>
                        </div>
                        <div class="total-harga">
                            <h4>Total Harga: Rp <span id="total">0</span></h4>
                        </div>
                    </form>
                </div>
                <div class="modal-footer">
                    <button type="button" class="btn-cancel" onclick="tutupModal()">Batal</button>
                    <button type="button" class="btn-confirm" onclick="konfirmasiPemesanan()">Konfirmasi Pesanan</button>
                </div>
            </div>
        </div>
    `;
    
    // Tambahkan ke body
    document.body.insertAdjacentHTML('beforeend', formHTML);
    
    // Event listener untuk perubahan jumlah
    document.getElementById('jumlah-pesan').addEventListener('input', function() {
        updateTotalHarga(this.value, 50000); // Asumsi harga per buku Rp 50.000
    });
    
    // Inisialisasi total harga
    updateTotalHarga(1, 50000);
}

// Fungsi untuk update total harga
function updateTotalHarga(jumlah, hargaPerBuku) {
    const total = jumlah * hargaPerBuku;
    document.getElementById('total').textContent = total.toLocaleString('id-ID');
}
```

### ✅ **Latihan 2: Validasi Form Lengkap**
```javascript
// Fungsi validasi form lengkap
function validasiFormLengkap() {
    const form = document.getElementById('form-pemesanan-detail');
    const inputs = form.querySelectorAll('input[required], textarea[required]');
    let errors = [];
    
    // Reset error
    inputs.forEach(input => {
        input.style.borderColor = '#ddd';
        const errorElement = input.parentNode.querySelector('.error-message');
        if (errorElement) {
            errorElement.remove();
        }
    });
    
    // Validasi setiap input
    inputs.forEach(input => {
        const value = input.value.trim();
        const name = input.name || input.id;
        
        // Validasi required
        if (!value) {
            tambahError(input, 'Field ini wajib diisi');
            errors.push(`${name} tidak boleh kosong`);
            return;
        }
        
        // Validasi khusus berdasarkan type
        switch(input.type) {
            case 'email':
                const emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
                if (!emailPattern.test(value)) {
                    tambahError(input, 'Format email tidak valid');
                    errors.push('Email tidak valid');
                }
                break;
                
            case 'tel':
                const phonePattern = /^[0-9+()-\s]+$/;
                if (!phonePattern.test(value) || value.length < 10) {
                    tambahError(input, 'Format nomor telepon tidak valid');
                    errors.push('Nomor telepon tidak valid');
                }
                break;
                
            case 'number':
                const min = parseInt(input.min);
                const max = parseInt(input.max);
                const numValue = parseInt(value);
                
                if (isNaN(numValue)) {
                    tambahError(input, 'Harus berupa angka');
                    errors.push(`${name} harus berupa angka`);
                } else if (min && numValue < min) {
                    tambahError(input, `Minimal ${min}`);
                    errors.push(`${name} minimal ${min}`);
                } else if (max && numValue > max) {
                    tambahError(input, `Maksimal ${max}`);
                    errors.push(`${name} maksimal ${max}`);
                }
                break;
        }
        
        // Validasi panjang minimal
        if (value.length < 3) {
            tambahError(input, 'Minimal 3 karakter');
            errors.push(`${name} minimal 3 karakter`);
        }
    });
    
    return {
        isValid: errors.length === 0,
        errors: errors
    };
}

// Fungsi untuk menambahkan error message
function tambahError(input, message) {
    input.style.borderColor = '#e74c3c';
    
    const errorElement = document.createElement('small');
    errorElement.className = 'error-message';
    errorElement.style.color = '#e74c3c';
    errorElement.style.display = 'block';
    errorElement.style.marginTop = '0.25rem';
    errorElement.textContent = message;
    
    input.parentNode.appendChild(errorElement);
}
```

### ✅ **Latihan 3: Animasi dan Interaksi**
```javascript
// Fungsi untuk animasi scroll smooth
function scrollToStok() {
    const stokSection = document.getElementById('stok');
    stokSection.scrollIntoView({ 
        behavior: 'smooth',
        block: 'start'
    });
}

// Fungsi untuk animasi loading
function tampilkanLoading() {
    const loadingHTML = `
        <div class="loading-overlay">
            <div class="loading-spinner">
                <div class="spinner"></div>
                <p>Sedang memproses...</p>
            </div>
        </div>
    `;
    
    document.body.insertAdjacentHTML('beforeend', loadingHTML);
    
    // Style loading
    const style = document.createElement('style');
    style.textContent = `
        .loading-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.5);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 9999;
        }
        
        .loading-spinner {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            text-align: center;
        }
        
        .spinner {
            width: 50px;
            height: 50px;
            border: 5px solid #f3f3f3;
            border-top: 5px solid #3498db;
            border-radius: 50%;
            animation: spin 1s linear infinite;
            margin: 0 auto 1rem;
        }
        
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
    `;
    document.head.appendChild(style);
}

// Fungsi untuk menyembunyikan loading
function sembunyikanLoading() {
    const loading = document.querySelector('.loading-overlay');
    if (loading) {
        loading.remove();
    }
}

// Fungsi untuk animasi card
function animasiCard() {
    const cards = document.querySelectorAll('.bahan-ajar-card');
    
    const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                entry.target.style.opacity = '1';
                entry.target.style.transform = 'translateY(0)';
            }
        });
    }, {
        threshold: 0.1
    });
    
    cards.forEach((card, index) => {
        card.style.opacity = '0';
        card.style.transform = 'translateY(20px)';
        card.style.transition = `opacity 0.5s ease ${index * 0.1}s, transform 0.5s ease ${index * 0.1}s`;
        observer.observe(card);
    });
}
```

---

## 📋 **Tugas Praktik Mandiri**

### 🎯 **Tugas 1: Membuat Aplikasi SITTA Lengkap**
Buat aplikasi SITTA dengan ketentuan:

1. **Struktur HTML Semantik (15 poin)**
   - Gunakan tag HTML5 semantik (header, nav, main, section, article, footer)
   - Struktur yang valid dan terorganisir
   - Meta tag yang lengkap

2. **Desain CSS Menarik (15 poin)**
   - Menggunakan CSS eksternal
   - Responsive design untuk mobile dan desktop
   - Animasi dan transisi yang halus
   - Warna dan tipografi yang konsisten

3. **JavaScript DOM Interaktif (25 poin)**
   - Manipulasi DOM untuk menampilkan data
   - Event handling untuk interaksi user
   - Validasi form yang lengkap
   - Local storage untuk menyimpan data

4. **Validasi Form & Alert (15 poin)**
   - Validasi input yang komprehensif
   - Feedback error yang jelas
   - Notifikasi yang user-friendly

5. **Struktur File Modular (5 poin)**
   - Pemisahan file HTML, CSS, JavaScript
   - Organisasi folder yang rapi
   - Penamaan file yang konsisten

6. **Kreativitas Tambahan (10 poin)**
   - Fitur tambahan yang inovatif
   - Desain yang menarik
   - User experience yang baik

7. **Penjelasan Video (15 poin)**
   - Durasi maksimal 15 menit
   - Penjelasan sistematika dan alur berpikir
   - Demonstrasi fitur-fitur yang dibuat

---

## 🎯 **Kesimpulan**

Pada pertemuan ini kita telah mempelajari:

### ✅ **HTML Semantik**
- Penggunaan tag HTML5 yang sesuai makna
- Struktur dokumen yang valid dan terorganisir
- Meta tag untuk SEO dan aksesibilitas

### ✅ **CSS Komprehensif**
- 3 cara menggunakan CSS (inline, internal, external)
- Responsive design dengan flexbox dan grid
- Animasi dan transisi untuk UX yang lebih baik
- CSS variables untuk konsistensi desain

### ✅ **JavaScript DOM Manipulation**
- Selector DOM yang efisien
- Event handling untuk interaktivitas
- Manipulasi konten dan struktur
- Validasi form yang komprehensif
- Local storage untuk persistensi data

### ✅ **Studi Kasus SITTA**
- Implementasi konsep dalam proyek nyata
- Best practices dalam pengembangan web
- Problem solving dalam pembuatan aplikasi

---

## 📚 **Referensi Pembelajaran**

### 📖 **Referensi Utama**
- [W3Schools HTML](https://www.w3schools.com/html/)
- [W3Schools CSS](https://www.w3schools.com/css/)
- [W3Schools JavaScript DOM](https://www.w3schools.com/js/js_dom_intro.asp)
- [MDN Web Docs](https://developer.mozilla.org/)

### 📚 **Referensi Tambahan**
- [CSS Tricks](https://css-tricks.com/)
- [JavaScript.info](https://javascript.info/)
- [FreeCodeCamp](https://www.freecodecamp.org/)

### 🎥 **Video Tutorial**
- [HTML & CSS Tutorial](https://www.youtube.com/playlist)
- [JavaScript DOM Tutorial](https://www.youtube.com/playlist)

---

## 🚀 **Persiapan Pertemuan Selanjutnya**

Pertemuan 10 akan membahas:
- **Vue.js Framework**
- **Data Binding (One-way & Two-way)**
- **Conditional Rendering**
- **Computed Properties & Methods**
- **Studi Kasus: Aplikasi Stok dengan Vue.js**

**Persiapan:**
- Pelajari konsep JavaScript framework
- Install Node.js dan Vue CLI (opsional)
- Baca dokumentasi Vue.js basics

---

**Selamat belajar dan semoga sukses! 🎉**

*Universitas Terbuka - Program Studi Sistem Informasi*
