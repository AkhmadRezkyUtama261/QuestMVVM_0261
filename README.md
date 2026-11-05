# QuestMVVM - Praktikum Pemrograman Aplikasi Mobile (PAM)

Proyek aplikasi Android berbasis **Jetpack Compose** dengan arsitektur **Model-View-ViewModel (MVVM)** dan navigasi Jetpack Compose.

## 📌 Deskripsi Proyek
Aplikasi ini merupakan tugas praktikum PAM (*Pemrograman Aplikasi Mobile*) yang mengimplementasikan arsitektur MVVM untuk pengelolaan data formulir pendaftaran siswa. Aplikasi terdiri dari dua alur layar utama:
1. **Formulir Pendaftaran Siswa (`FormSiswa`)**: Pengguna memasukkan nama lengkap, memilih jenis kelamin (menggunakan Radio Button), dan mengisi alamat lengkap.
2. **Detail Data Siswa (`TampilSiswa`)**: Menampilkan rincian data yang telah diinput sebelumnya menggunakan `StateFlow` dari ViewModel, disertai tombol kembali ke formulir.

## 🏛️ Arsitektur & Struktur Direktori
Aplikasi mengadopsi struktur arsitektur MVVM:

```
com.example.questmvvm
│
├── model/
│   ├── DataJK.kt          # Object daftar sumber daya pilihan Jenis Kelamin
│   └── Siswa.kt           # Data class entitas data Siswa (nama, gender, alamat)
│
├── view/
│   ├── FormSiswa.kt       # Layar input form pendaftaran siswa
│   ├── TampilSiswa.kt     # Layar rincian penampilan data siswa
│   └── uicontroller/
│       └── Navigasi.kt    # Rute navigasi NavHost dan container SiswaApp
│
├── viewmodel/
│   └── SiswaViewModel.kt  # ViewModel pengelola MutableStateFlow & StateFlow
│
├── ui.theme/              # Tema warna, tipografi, dan gaya aplikasi
│
└── MainActivity.kt        # Entry point aplikasi dengan Jetpack Compose
```

## 🚀 Fitur & Komponen Utama
- **State Management**: Menggunakan `MutableStateFlow` dan `asStateFlow()` dari Kotlin Coroutines untuk memastikan unidirectional data flow (UDF).
- **Jetpack Compose Navigation**: Menggunakan `NavHost`, `composable`, dan `NavHostController` untuk perpindahan antar rute formulir dan detail.
- **Material 3 UI**: Implementasi `TopAppBar`, `OutlinedTextField`, `RadioButton`, `HorizontalDivider`, dan komponen Material 3 modern lainnya.
- **Resource Management**: Pemisahan teks (`strings.xml`), dimensi layout (`dimens.xml`), dan palet warna (`colors.xml`).
