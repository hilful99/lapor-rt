# Lapor Tamu RT 1x24 Jam - Tahap 1 (Dasar)

Isi folder: `schema.sql` (database), `index.html` (aplikasi), `README.md` (panduan ini).

## A. Siapkan database (Supabase)

1. Buka project Supabase kamu > **SQL Editor** > **New query**.
2. Buka `schema.sql`, cari tulisan `RT00` lalu ganti dengan kode RT kamu (misal `RT05`).
3. Paste seluruh isinya ke SQL Editor > klik **Run**. Harus muncul "Success".
4. **Matikan pendaftaran bebas** supaya orang luar tidak bisa membuat akun sendiri: menu **Authentication**, di pengaturan Email/Providers matikan opsi "Allow new users to sign up".
5. Buat akun petugas: **Authentication > Users > Add user**. Di kolom email tulis `ID@petugas.rt` (contoh: `4ipul4@petugas.rt`), isi password, centang auto confirm. Petugas cukup login dengan ID-nya saja (`4ipul4`), akhiran `@petugas.rt` ditambahkan otomatis oleh aplikasi. Ulangi untuk setiap petugas. Gunakan huruf kecil semua.
6. Isi data warga: **Table Editor > warga**, hapus dua baris contoh, lalu tambahkan warga asli (kolom `nama` dan `blok`).
7. Ambil kunci: **Project Settings > API**. Salin **Project URL** dan **anon / publishable key**.

## B. Isi kunci di aplikasi

Buka `index.html`, cari dua baris ini dan ganti isinya:

```js
const SUPABASE_URL = 'ISI_PROJECT_URL';
const SUPABASE_KEY = 'ISI_ANON_PUBLIC_KEY';
```

Kunci anon memang boleh ada di file web, karena data dilindungi aturan keamanan (RLS) yang sudah dibuat `schema.sql`. Jangan pernah memakai kunci `service_role` di sini.

## C. Simpan ke GitHub

1. GitHub > **New repository**, beri nama `lapor-rt`, pilih **Private**.
2. Klik **uploading an existing file**, upload `index.html` dan `README.md`, lalu **Commit**.

## D. Online-kan dengan Vercel

1. Vercel > **Add New > Project** > pilih repository `lapor-rt` > **Import**.
2. Framework Preset: **Other**. Klik **Deploy**.
3. Selesai, kamu dapat alamat seperti `lapor-rt.vercel.app`.

## E. Cek apakah sudah jalan

- [ ] Login dengan akun petugas berhasil
- [ ] NIK kurang dari 16 digit ditolak
- [ ] Simpan tamu tanpa centang KTP ditolak
- [ ] Simpan tamu normal: muncul nomor dokumen `LT-RT05-tanggal-0001`
- [ ] Tamu kedua di hari yang sama dapat nomor `0002`
- [ ] NIK yang sama diinput lagi ditolak (masih aktif)
- [ ] "Tandai keluar" mengubah status jadi Selesai, lalu NIK itu bisa dilaporkan lagi

## Catatan keamanan

- Jangan bagikan alamat web dan password petugas ke sembarang orang.
- Di daftar, NIK sudah tersamarkan (4 digit awal dan akhir saja).
- Jangan memfoto atau menulis NIK di tempat lain selain aplikasi ini.

## Belum ada di Tahap 1 (masuk Tahap 2)

Konfirmasi tuan rumah, peran pengurus RT, log audit, penanda lewat 1x24 jam, pencarian dan filter.
