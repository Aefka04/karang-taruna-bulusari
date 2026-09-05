# Panduan Setup: Situs dengan Admin Panel (CMS)

Folder ini adalah versi situs yang bisa diedit lewat halaman admin di web
(tanpa Notepad++), menggunakan tiga layanan gratis: **GitHub** (penyimpanan
kode), **Netlify** (hosting + sistem login), dan **Decap CMS** (panel admin,
sudah termasuk dalam folder `admin/`).

Desain situs sama persis dengan versi sebelumnya. Bedanya, teks kegiatan,
galeri, kontak, dan tentang kami sekarang disimpan di file-file kecil di
`src/_data/*.json`, dan itulah yang muncul sebagai form isian di panel admin.

Setup ini hanya perlu dilakukan **sekali**. Setelah itu, admin cukup buka
`https://nama-situs-kamu.netlify.app/admin/`, login, dan mengisi form.

## Langkah 1 — Buat akun & repository GitHub
1. Daftar di github.com jika belum punya akun.
2. Buat repository baru (mis. `karang-taruna-bulusari`), pilih **Private** atau **Public** (keduanya bisa).
3. Unggah seluruh isi folder ini ke repository tersebut. Cara termudah: di halaman repo GitHub, klik "uploading an existing file", lalu seret semua file dan folder (termasuk folder tersembunyi `.eleventy.js`) ke sana.

## Langkah 2 — Hubungkan ke Netlify
1. Daftar di netlify.com, bisa langsung pakai akun GitHub.
2. Klik "Add new site" → "Import an existing project" → pilih repository yang tadi dibuat.
3. Netlify otomatis membaca `netlify.toml`: build command `npm run build`, folder terbit `_site`. Klik "Deploy".
4. Tunggu proses build selesai (1-2 menit). Situs akan online di alamat seperti `nama-acak.netlify.app` — bisa diganti nama di Site settings → Change site name.

## Langkah 3 — Aktifkan login admin (Netlify Identity)
1. Di dashboard Netlify, buka menu **Identity** → klik "Enable Identity".
2. Di bagian **Registration**, pilih "Invite only" (supaya tidak sembarang orang bisa daftar jadi admin).
3. Buka tab **Services** → **Git Gateway** → klik "Enable Git Gateway". Ini yang memungkinkan panel admin menyimpan perubahan langsung ke GitHub.
4. Kembali ke tab **Identity** → klik "Invite users" → masukkan email admin (bisa email kamu sendiri atau bendahara/sekretaris). Mereka akan menerima email undangan untuk membuat password.

## Langkah 4 — Login dan mulai edit
1. Buka `https://nama-situs-kamu.netlify.app/admin/`.
2. Login dengan email & password yang dibuat dari undangan tadi.
3. Akan muncul daftar koleksi: Pengaturan Situs, Kegiatan, Galeri, Kontak, Tentang Kami, Absensi & Kas — masing-masing berupa form, bukan kode.
4. Setelah isi form, klik "Publish" (atau "Save" lalu "Publish"). Situs akan otomatis rebuild dalam waktu singkat dan perubahan tampil di web.

## Menambahkan admin baru di kemudian hari
Ulangi Langkah 3.4 — undang email baru dari Netlify Identity. Tidak perlu mengulang setup lainnya.

## Catatan
- Semua perubahan tersimpan sebagai riwayat di GitHub, jadi kalau ada yang salah edit, bisa dikembalikan ke versi sebelumnya.
- Kalau butuh saya bantu proses upload ke GitHub atau konfigurasi Netlify secara langsung, saya perlu akses akun tersebut — biasanya lebih mudah kamu ikuti langkah di atas sendiri sambil saya bantu jika ada pesan error yang muncul (screenshot saja errornya).
