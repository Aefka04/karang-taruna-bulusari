# Panduan: Membangun Versi Google Sites (untuk Pembanding)

Google Sites adalah editor visual dari Google (mirip Google Docs) — tidak perlu
kode sama sekali, dan siapa pun dengan akun Google bisa diberi akses edit.
Kekurangannya: tampilan/desain tidak bisa dibuat sedetail versi HTML kustom
(warna, tipografi, ilustrasi SVG di beranda tidak bisa dipertahankan persis).

## Langkah 1 — Buat situs baru
1. Buka sites.google.com, login dengan akun Google.
2. Klik "+ Blank" untuk membuat situs kosong.
3. Beri nama situs, misalnya "Karang Taruna Merah Putih Bulusari" (klik teks di kiri atas).

## Langkah 2 — Buat 5 halaman
Di panel kanan, klik ikon "Pages", lalu klik "+" untuk menambah halaman. Buat halaman berikut, ini juga bisa jadi susunan menu navigasi otomatis:
1. Beranda (biasanya halaman utama sudah otomatis ada)
2. Tentang Kami
3. Kegiatan
4. Galeri
5. Kontak

(Kalau mau menambah halaman Absensi & Kas juga, tinggal tambah satu halaman lagi — lihat Langkah 5.)

## Langkah 3 — Isi konten tiap halaman
Struktur dan draf teks di bawah ini bisa langsung disalin-tempel ke masing-masing halaman, lalu sesuaikan dengan data organisasi yang sebenarnya.

**Beranda**
- Judul besar: "Wadah pemuda & pemudi [Nama Desa] untuk bergerak bersama"
- Paragraf: deskripsi singkat organisasi
- Bagian "Sorotan Kegiatan": tambahkan 2-3 kegiatan terbaru (judul, tanggal, deskripsi singkat)

**Tentang Kami**
- Sejarah singkat organisasi
- Visi & Misi
- Struktur organisasi (bisa pakai fitur "Table" di Insert menu untuk daftar pengurus)

**Kegiatan**
- Daftar kegiatan yang sudah dan akan dilaksanakan, urutkan dari terbaru
- Bisa pakai heading per kegiatan + paragraf deskripsi

**Galeri**
- Insert → Images, unggah foto kegiatan langsung dari komputer atau Google Drive
- Atau Insert → Google Photos kalau foto sudah tersimpan di album Google Photos

**Kontak**
- Alamat sekretariat, nomor WA, email, link Instagram/Facebook
- Insert → Maps untuk menyematkan lokasi (tinggal cari alamat di kotak pencarian)

## Langkah 4 — Publikasikan
1. Klik tombol "Publish" di kanan atas.
2. Pilih alamat web (mis. sites.google.com/view/karangtaruna-bulusari).
3. Klik "Publish" lagi untuk konfirmasi.

## Langkah 5 — Menambahkan Absensi & Kas dari Google Sheets
Ini justru lebih mudah di Google Sites dibanding versi CMS, karena satu ekosistem Google:
1. Buat halaman baru "Absensi & Kas".
2. Klik Insert → Sheets.
3. Pilih file Google Sheets absensi/kas kamu, pilih rentang sel atau seluruh sheet yang ingin ditampilkan.
4. Klik Insert — tabel akan tampil di halaman dan otomatis memperbarui data setiap kali Sheets aslinya diubah (tidak perlu publish ulang setiap saat, walau kadang perlu klik ikon refresh di pojok tabel).

## Langkah 6 — Memberi akses edit ke admin lain
1. Klik ikon "Share" (pojok kanan atas, sebelah "Publish").
2. Masukkan email Google admin lain, beri akses "Editor".
3. Admin baru bisa langsung login ke sites.google.com dan mengedit tanpa setup tambahan apa pun.

## Perbandingan singkat dengan versi CMS

| | Google Sites | CMS (Decap + Netlify) |
|---|---|---|
| Kemudahan setup awal | Sangat mudah, 15-30 menit | Perlu setup GitHub + Netlify sekali, ~1 jam |
| Kemudahan edit harian | Sangat mudah (seperti Google Docs) | Mudah (isi form), tapi harus login ke alamat /admin/ |
| Desain custom | Terbatas pada template Google Sites | Bebas, sama seperti desain yang sudah dibuat |
| Biaya | Gratis selama pakai akun Google biasa | Gratis (GitHub + Netlify free tier cukup untuk situs kecil) |
| Menambah admin baru | Tinggal share akses Google | Undang via Netlify Identity |
| Cocok untuk | Prioritas kemudahan & kecepatan | Prioritas tampilan/branding khas organisasi |
