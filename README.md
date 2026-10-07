# Lapor Tamu RT 1x24 Jam - Tahap 1 (Dasar)

Halo semua! 👋

Proyek ini adalah aplikasi web sederhana untuk mencatat tamu di lingkungan RT dengan batas waktu 1x24 jam. Awalnya, proyek ini saya buat untuk mengikuti **program lomba di kampus saya**. Sebagai seorang **pemula** dalam dunia pengembangan web, saya sangat terbuka jika ada teman-teman yang ingin melihat, memakai, atau bahkan mengembangkan proyek ini lebih lanjut.

## 🌟 Status Proyek
Saat ini proyek ini sudah **Open Source / Terbuka untuk Umum**. Siapa pun boleh mempelajari kodenya, menggunakan untuk keperluan RT masing-masing, atau berkontribusi mengembangkannya.

Fitur yang sudah ada di Tahap 1:
- Input data tamu dengan validasi NIK (16 digit).
- Wajib centang KTP.
- Penomoran dokumen otomatis (contoh: `LT-RT05-tanggal-0001`).
- Pencegahan duplikasi NIK yang masih aktif.
- Fitur "Tandai keluar".

## 🚀 Ingin Ikut Mengembangkan?
Saya sangat senang jika ada yang ingin membantu mengembangkan proyek ini, baik untuk memperbaiki bug, menambah fitur Tahap 2 (seperti konfirmasi tuan rumah, log audit, penanda lewat 1x24 jam, dll), atau sekadar memberikan masukan.

**Cara Berkontribusi:**
1. Fork repositori ini.
2. Buat branch baru (`git checkout -b fitur-baru`).
3. Commit perubahan Anda (`git commit -m 'Menambah fitur X'`).
4. Push ke branch (`git push origin fitur-baru`).
5. Buat Pull Request.

## 📬 Kontak & Kerja Sama
Jika Anda ingin berdiskusi, memberikan saran, atau tertarik untuk bekerja sama mengembangkan proyek ini, silakan hubungi saya melalui email:

📧 **hilfulwarday009@gmail.com**

Saya akan sangat berterima kasih atas segala bantuan, masukan, dan dukungannya. Terima kasih banyak! 🙏

## 🛠️ Teknologi yang Digunakan
- **Database & Auth:** Supabase
- **Frontend:** HTML, JavaScript
- **Hosting:** Vercel
- **Version Control:** GitHub

## ⚠️ Catatan Keamanan
- Jangan pernah membagikan password petugas ke sembarang orang.
- NIK sudah tersamarkan (4 digit awal dan akhir saja) di daftar tamu.
- Jangan memfoto atau menulis NIK di tempat lain selain aplikasi ini.
