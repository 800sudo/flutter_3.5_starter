# 🚀 Flutter 3.5+ Master Starter Kit

> **Production-Ready & Offline-First Starter Template for Flutter (Android, Web & Desktop)**

Sebuah starter kit Flutter modern yang dirancang untuk mempercepat proses pengembangan aplikasi mulai dari tahap *scaffolding* hingga *production*. Dilengkapi dengan arsitektur terstruktur (*Clean Architecture*), manajemen state standar industri, utilitas formulir & validasi lengkap, serta dikonfigurasi khusus agar **ramah kuota (Offline-First development)**.

---

## ✨ Fitur Utama & Ekosistem Terintegrasi

Starter kit ini sudah memuat dependensi esensial yang siap pakai tanpa perlu download ulang:

### 🧠 State Management & Arsitektur
* **`flutter_bloc` & `bloc`**: Standar arsitektur reactive berbasis event & state yang scalable.
* **`provider`**: Alternatif state management ringan untuk state lokal/sederhana.
* **`equatable`**: Value equality comparison untuk state dan model tanpa boilerplate.

### 🧭 Navigasi & Routing
* **`go_router`**: Routing deklaratif resmi dengan dukungan dynamic route parameters, redirects, sub-routes, dan web deep-linking.

### 🌐 Jaringan & Konektivitas (Network & API)
* **`dio`**: HTTP client canggih dengan dukungan interceptors (global token & error handling), request cancellation, dan transformer.
* **`connectivity_plus`**: Pemantau status koneksi internet (WiFi, Cellular, Offline).
* **`http`**: Client HTTP standar untuk kebutuhan request ringan.

### 💾 Database & Penyimpanan Lokal (Offline Storage)
* **`sqflite`**: Relational SQLite database untuk data terstruktur dengan performa tinggi.
* **`shared_preferences`**: Penyimpanan key-value persisten untuk pengaturan aplikasi & sesi.
* **`hive` & `hive_flutter`**: Database NoSQL super cepat berbasis binary storage.
* **`path_provider`**: Akses direktori penyimpanan lokal (documents, cache, storage).

### 📝 Formulir, Validasi & Format Data
* **`flutter_form_builder`**: Ekosistem form deklaratif terlengkap untuk Flutter.
* **`form_builder_validators`**: Kumpulan validator siap pakai (email, required, numeric, regex, min/max).
* **`intl`**: Internasionalisasi, pelokalan bahasa, format mata uang, serta tanggal & waktu.
* **`mask_text_input_formatter`**: Masking input nomor telepon, NPWP, plat nomor, tanggal, dll.

### 🎨 Desain, UI, Ikon & Animasi
* **`flutter_svg`**: Render file SVG vector tajam tanpa pecah di semua resolusi.
* **`font_awesome_flutter`**: Ribuan ikon FontAwesome siap pakai.
* **`cached_network_image`**: Pemuat gambar online otomatis dengan local cache dan placeholder.
* **`shimmer`**: Efek shimmer loading placeholder modern.
* **`gap`**: Spacer widget fleksibel pengganti `SizedBox(width: ..., height: ...)`.

### 🛠️ Dependency Injection, Code Gen & Testing
* **`get_it` & `injectable`**: Service locator & Dependency Injection otomatis.
* **`json_serializable` & `json_annotation`**: Otomasi serialisasi JSON (fromJson / toJson).
* **`build_runner`**: Tool CLI code generation.
* **`bloc_test` & `mocktail`**: Kerangka pengujian unit & widget test tanpa boilerplate mock.

---

## 📁 Struktur Folder Rekomendasi (Clean Architecture)

```text
lib/
├── main.dart
├── app/
│   ├── routes/              # Konfigurasi GoRouter
│   └── theme/               # ThemeData, palet warna, tipografi
├── core/
│   ├── constants/           # Konstanta global aplikasi
│   ├── errors/              # Custom Exceptions & Failures
│   ├── network/             # Dio client & Interceptors
│   └── utils/               # Helper functions & extension methods
├── features/
│   └── <nama_fitur>/
│       ├── data/            # Data sources (API/DB), Models, Repository Impl
│       ├── domain/          # Entities, Contracts / Abstract Repositories, UseCases
│       └── presentation/    # BLoC / Cubit, Pages / Screens, Feature Widgets
└── shared/
    └── widgets/             # Reusable UI components global
```

---

## ⚡ Cara Memulai (Quick Start)

### 1. Clone Repositori
```bash
git clone https://github.com/800sudo/flutter_3.5_starter.git
cd flutter_3.5_starter
```

### 2. Dapatkan Dependensi (Offline Friendly)
Jika dependensi sudah pernah di-cache sebelumnya di komputer Anda, jalankan:
```bash
flutter pub get --offline
```
Atau jalankan `flutter pub get` biasa jika Anda terhubung ke internet.

### 3. Jalankan Aplikasi
* **Di Perangkat Android:**
  ```bash
  flutter run -d android
  ```
* **Di Browser (Web):**
  ```bash
  flutter run -d chrome
  ```
* **Di Desktop Windows:**
  ```bash
  flutter run -d windows
  ```

### 4. Build untuk Production
* **Build APK Android:**
  ```bash
  flutter build apk --release
  ```
* **Build Web:**
  ```bash
  flutter build web --release
  ```

---

## 💡 Filosofi Offline-First

Starter kit ini dibuat dengan kesadaran penuh akan pentingnya stabilitas dan efisiensi kuota data:
1. **Zero Unexpected Downloads**: Paket-paket dasar CRUD, navigasi, form, autentikasi, dan UI sudah tercakup tanpa perlu penambahan plugin baru di awal.
2. **Stable Native Dependencies**: Konfigurasi Android Gradle dan Kotlin telah dioptimalkan untuk kompatibilitas penyimpanan lokal / eksternal disk.

---

## 📄 Lisensi
Didistribusikan di bawah lisensi MIT. Bebas digunakan untuk proyek komersial maupun personal.
