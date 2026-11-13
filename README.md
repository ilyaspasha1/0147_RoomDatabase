# 0147_RoomDatabase - Aplikasi Data Siswa

Aplikasi Android berbasis Jetpack Compose dan Room Database untuk pengelolaan data siswa (Meeting 9).

## Fitur Aplikasi
- **Tambah Data Siswa**: Formulir input data siswa (Nama, Alamat, Nomor Telpon) dengan validasi input.
- **Tampilkan Daftar Siswa**: Menampilkan seluruh data siswa yang tersimpan di dalam Room Database.
- **Peta Navigasi Jetpack Compose**: Navigasi antar layar (Halaman Home & Halaman Entry) menggunakan Jetpack Navigation Compose.
- **Arsitektur MVVM & Offline Repository**: Pemisahan logika UI, ViewModel, dan Repository offline berbasis Room DAO.

## Tangkapan Layar (Screenshot)
![Running App Screenshot](app_screenshot.png)

## Struktur Proyek (`com.example.roomdb`)
- `room/`: Data Entity (`Siswa`), Data Access Object (`SiswaDao`), dan Room Database (`DatabaseSiswa`).
- `repositori/`: Interface `RepositoriSiswa` & implementation `OfflineRepositoriSiswa`, serta `ContainerApp` (Dependency Container).
- `viewmodel/`: `HomeViewModel`, `EntryViewModel`, `PenyediaViewModel` (ViewModel Factory), `UIStateSiswa`, dan `DetailSiswa`.
- `uicontroller/`: TopAppBar (`SiswaTopAppBar`), `DestinasiNavigasi`, `DestinasiHome`, `DestinasiEntry`, dan `PetaNavigasi` (`SiswaApp`, `HostNavigasi`).
- `view/`: Composable Views (`HalamanHome.kt`, `HalamanEntry.kt`).

## Cara Menjalankan
1. Buka proyek ini di Android Studio.
2. Lakukan Gradle Sync.
3. Jalankan aplikasi pada Emulator atau Perangkat Android fisik.
