Praktikum Navigasi Flutter

Project ini merupakan aplikasi Flutter untuk mempraktikkan navigasi, routing, dan responsive layout menggunakan Flutter Material 3.

Fitur Utama

Named Route untuk perpindahan halaman.

onGenerateRoute untuk route dengan parameter.

onUnknownRoute untuk menangani route yang tidak ditemukan.

Navigation Bar pada layar kecil.

Navigation Rail pada layar lebar.

Navigation Drawer sebagai menu samping.

TabBar dan TabBarView pada halaman jadwal.

Pengiriman data ke halaman detail dan pengembalian data ke halaman sebelumnya.

Halaman catatan dengan Floating Action Button.

Halaman pengaturan dan profil.

Teknologi

Flutter

Dart

Material 3

Navigator / Named Routes

Struktur Folder

lib/
├── main.dart
├── navigation/
│   ├── app_routes.dart
│   └── kerangka_navigasi.dart
└── pages/
    ├── halaman_beranda.dart
    ├── halaman_catatan.dart
    ├── halaman_detail.dart
    ├── halaman_jadwal.dart
    ├── halaman_pengaturan.dart
    └── halaman_profil.dart

Penjelasan File

File

Fungsi

main.dart

Menjalankan aplikasi dan konfigurasi utama MaterialApp.

app_routes.dart

Mengatur named route, route dinamis, dan route tidak ditemukan.

kerangka_navigasi.dart

Mengatur navigasi utama, drawer, navigation bar, dan navigation rail.

halaman_beranda.dart

Halaman utama dan contoh navigasi ke detail.

halaman_jadwal.dart

Menampilkan jadwal berdasarkan hari menggunakan TabBar.

halaman_profil.dart

Menampilkan profil mahasiswa dan akses ke catatan.

halaman_detail.dart

Menampilkan detail dan mengirim data kembali ke halaman sebelumnya.

halaman_catatan.dart

Halaman catatan dengan Floating Action Button dan BottomAppBar.

halaman_pengaturan.dart

Halaman pengaturan aplikasi.

Struktur Navigasi

                    Kerangka Navigasi
                           │
             ┌─────────────┼─────────────┐
             │             │             │
          Beranda        Jadwal        Profil
                                         │
                                         ▼
                                      Catatan

Drawer
  └── Pengaturan

Beranda / Jadwal
      │
      ▼
    Detail

Routing

Route utama yang digunakan:

/              → KerangkaNavigasi
/detail        → HalamanDetail
/pengaturan    → HalamanPengaturan
/catatan       → HalamanCatatan

Route /detail menerima data:

{
  'judul': '...',
  'keterangan': '...'
}

Halaman detail juga dapat mengirim nilai kembali menggunakan:

Navigator.pop(context, 'Data dari halaman detail');

Responsive Layout

Aplikasi menyesuaikan tampilan berdasarkan lebar layar:

Layar < 600 px → menggunakan NavigationBar.

Layar ≥ 600 px → menggunakan NavigationRail.

Selain itu, NavigationDrawer tersedia sebagai menu samping.

Cara Menjalankan

Pastikan Flutter sudah terinstall, kemudian jalankan:

flutter pub get
flutter run

Untuk mengecek konfigurasi Flutter:

flutter doctor

Status Project

Project ini merupakan project praktikum Flutter yang berfokus pada penerapan:

Navigasi antarhalaman

Named Route

Passing arguments

Return value dari halaman

Navigation Drawer

Navigation Bar

Navigation Rail

Responsive layout

TabBar

Error handling pada route