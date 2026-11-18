# Sistem Informasi Masjid Digital

Aplikasi web satu layar untuk jadwal salat, hitung mundur, alarm, pengumuman, dan tayangan foto/video kegiatan masjid. Dibuat sebagai situs statis sehingga dapat di-host gratis menggunakan GitHub Pages.

## Cara menjalankan di komputer
1. Ekstrak folder proyek.
2. Buka `index.html` menggunakan browser modern. Untuk penggunaan harian, disarankan hosting melalui GitHub Pages agar HTTPS dan API berjalan konsisten.

## Publikasi melalui GitHub Pages
1. Login ke https://github.com lalu buat repository baru, misalnya `digital-masjid`.
2. Pilih **Public** dan buat repository.
3. Upload `index.html`, `style.css`, dan `app.js` (README boleh ikut diunggah).
4. Buka **Settings → Pages**.
5. Pada **Build and deployment**, pilih **Deploy from a branch**.
6. Pilih branch **main**, folder **/(root)**, lalu klik **Save**.
7. Tunggu proses selesai. Situs akan tersedia di `https://USERNAME.github.io/digital-masjid/`.

## Pengaturan awal
- Klik ikon roda gigi di kanan bawah.
- Isi nama masjid, kota, negara, metode perhitungan, dan zona waktu.
- Metode Kementerian Agama RI tersedia sebagai pilihan awal. Cocokkan hasil jadwal dengan ketetapan resmi/otoritas setempat; bila diperlukan gunakan penyesuaian jadwal manual di sistem rujukan masjid.
- Tambahkan foto/video kegiatan dan pengumuman.
- Klik **Aktifkan Suara** satu kali pada perangkat layar masjid agar browser mengizinkan audio.

## Catatan penting
- Jadwal salat diambil dari AlAdhan API berdasarkan kota/negara dan metode perhitungan. Koneksi internet diperlukan.
- Alarm berjalan selama halaman terbuka dan perangkat aktif. Browser/OS dapat menunda audio ketika tab tidur, perangkat terkunci, atau komputer masuk mode hemat daya. Untuk penggunaan masjid, gunakan komputer khusus, nonaktifkan sleep, biarkan tab tetap terbuka, dan uji alarm sebelum dipakai.
- Browser mewajibkan interaksi pengguna sebelum memutar suara otomatis. Klik **Aktifkan Suara** setelah halaman dibuka.
- File media dan file suara yang dipilih tersimpan sementara di memori browser saat sesi berjalan; tidak diunggah ke GitHub dan perlu dipilih ulang setelah halaman dimuat ulang.
- Untuk tayangan video, browser dapat membisukan audio otomatis. Video diputar dalam keadaan mute agar tayangan berjalan otomatis; gunakan video tanpa audio atau tambahkan sistem pemutar khusus jika audio video diperlukan.
- GitHub Pages hanya meng-host file statis. Pengaturan lokal tidak tersinkron ke perangkat lain.


Identitas awal aplikasi telah disesuaikan untuk **MASJID AZZIKRA – Ust. ARIFIN ILHAM**. Logo berada pada file `logo-azzikra.jpeg` di folder yang sama dengan `index.html`; jangan pisahkan file tersebut saat mengunggah ke GitHub Pages.

## Modul Laporan Keuangan Jumat
- Ringkasan saldo kas, kas masuk, dan kas keluar tampil pada dashboard.
- Buka ikon pengaturan (⚙), isi saldo awal kas, lalu pilih **Kelola Laporan Keuangan**.
- Catat transaksi dengan tanggal, jenis (kas masuk/kas keluar), keterangan, dan nominal.
- Rekap otomatis memakai periode Sabtu sampai Jumat.
- Laporan dapat dicetak atau diunduh sebagai CSV.
- Data transaksi dan saldo disimpan di `localStorage` browser/perangkat ini. GitHub Pages hanya menjadi hosting statis; data tidak otomatis tersinkron antarperangkat. Untuk bendahara menginput dari beberapa HP dan layar TV menerima pembaruan yang sama, hubungkan aplikasi ke Google Sheets + Google Apps Script atau database online.
