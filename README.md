# Template Dev Container Fullstack

Template ini dirancang untuk membantu Anda membuat lingkungan kerja (development environment) pemrograman fullstack tanpa ribet. 

Jika Anda baru di dunia IT, bayangkan Dev Container ini seperti ruangan kerja virtual di dalam komputer Anda. Di dalam ruangan tersebut, semua alat, bahasa pemrograman, dan database yang dibutuhkan sudah terpasang rapi. Komputer utama Anda tetap bersih, dan Anda tidak perlu pusing menginstal banyak aplikasi satu per satu.

---

## Kenapa Menggunakan Template Ini?

- Komputer Tetap Bersih: Anda tidak perlu menginstal Node.js, Python, database, atau runtime lain langsung di laptop. Semuanya berjalan di dalam wadah (container) tersendiri.
- Mengurangi Masalah Error Lingkungan: Masalah klasik seperti "di laptop saya jalan, tapi di laptop teman kok error" tidak akan terjadi lagi karena semua orang menggunakan pengaturan ruangan kerja yang sama persis.
- Siap Pakai: Begitu proyek dibuka, Anda bisa langsung mulai menulis kode tanpa harus menghabiskan waktu berjam-jam untuk setup awal.
- Mendukung Banyak Layanan: Anda bisa dengan mudah menghubungkan backend, frontend, dan database secara bersamaan.

---

## Aplikasi yang Perlu Disiapkan

Sebelum mulai, pastikan dua aplikasi ini sudah terpasang di komputer Anda:

1. Docker Desktop: Program untuk menjalankan ruangan kerja virtual (container).
   Jika Anda memakai Windows, pastikan fitur WSL2 sudah aktif.
2. Visual Studio Code (VS Code): Aplikasi editor teks untuk menulis kode.
3. Ekstensi Dev Containers di VS Code: Cari ekstensi bernama "Dev Containers" buatan Microsoft di menu Extensions (ikon kotak-kotak di sebelah kiri VS Code), lalu klik Install.

---

## Langkah Memulai

1. Unduh atau clone repositori ini ke komputer Anda:
   git clone <URL_REPOSITORI_ANDA>
   cd fullstack-devcontainer-template

2. Buka folder proyek menggunakan VS Code:
   Buka VS Code, pilih menu File > Open Folder, lalu pilih folder proyek ini.

3. Masuk ke dalam Container:
   - Saat folder terbuka, biasanya muncul kotak pesan kecil di pojok kanan bawah yang bertuliskan "Reopen in Container". Klik tombol tersebut.
   - Jika pesan tersebut tidak muncul, tekan tombol F1 atau Ctrl+Shift+P di keyboard, ketik "Reopen in Container", lalu tekan Enter.

4. Tunggu proses instalasi selesai:
   Pada percobaan pertama, Docker akan mengunduh dan menyiapkan semuanya secara otomatis. Proses ini membutuhkan koneksi internet. Setelah selesai, terminal di VS Code sudah siap digunakan untuk ngoding.

---

## Penjelasan Isi Folder

Berikut gambaran sederhana struktur folder pada proyek ini:

- .devcontainer/ : Folder utama yang berisi instruksi untuk Docker dan VS Code.
  - devcontainer.json : Berisi daftar ekstensi VS Code yang otomatis dipasang, pengaturan port, dan perintah awal.
- .gitignore : Daftar file yang tidak perlu diunggah ke Git (seperti file rahasia, password, atau file sampah sistem).
- README.md : Panduan yang sedang Anda baca ini.

---

## Cara Menyesuaikan Kebutuhan

### Menambahkan Ekstensi VS Code Tambahan
Jika Anda butuh ekstensi tambahan saat bekerja di dalam container, buka file .devcontainer/devcontainer.json, lalu tambahkan nama ekstensi pada bagian customizations.vscode.extensions.

### Membuka Port Akses
Jika aplikasi web Anda berjalan di port tertentu (misalnya port 3000 untuk frontend atau port 8000 untuk backend), Anda bisa melihat dan mengaturnya pada bagian forwardPorts di file devcontainer.json agar bisa dibuka lewat browser laptop Anda.

---

## Lisensi

Proyek ini menggunakan lisensi MIT. Anda bebas menggunakan, memodifikasi, dan membagikannya untuk keperluan belajar maupun proyek pribadi.