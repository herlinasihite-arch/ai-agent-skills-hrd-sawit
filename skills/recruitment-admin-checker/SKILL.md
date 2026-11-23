---
name: recruitment-admin-checker
description: Memeriksa kelengkapan dokumen lamaran dan mencocokkan bukti kualifikasi dengan persyaratan posisi yang telah ditentukan HRD tanpa membuat keputusan penerimaan.
---

# Recruitment Admin Checker Skill

## Tujuan
Membantu staf HRD memeriksa kelengkapan administrasi berkas pelamar dan menyusun daftar bukti kualifikasi yang tersedia atau belum tersedia.

## Kapan digunakan
Gunakan skill ini ketika pengguna memberikan daftar persyaratan posisi dan ringkasan berkas pelamar untuk pemeriksaan administrasi awal.

## Input yang diperlukan
- Kode pelamar anonim.
- Nama/judul posisi.
- Daftar persyaratan posisi yang telah disahkan HRD.
- Daftar dokumen atau ringkasan bukti kualifikasi yang diserahkan pelamar.

## Langkah kerja
1. Baca persyaratan posisi yang diberikan.
2. Kelompokkan persyaratan menjadi dokumen wajib dan kualifikasi yang relevan dengan pekerjaan.
3. Cocokkan satu per satu dengan bukti yang tersedia.
4. Gunakan status: Tersedia, Belum tersedia, atau Perlu verifikasi.
5. Jangan menyamakan dokumen yang tidak diserahkan dengan bukti bahwa pelamar tidak memiliki kemampuan.
6. Buat ringkasan administratif dan daftar klarifikasi untuk HRD.

## Format output

### Ringkasan pemeriksaan
- Kode pelamar:
- Posisi:
- Jumlah persyaratan yang diperiksa:
- Status umum administrasi: Lengkap / Belum lengkap / Perlu verifikasi

### Matriks persyaratan
| Persyaratan posisi | Bukti yang diberikan | Status | Catatan |
|---|---|---|---|

### Tindak lanjut HRD
Daftar dokumen atau informasi yang perlu diklarifikasi.

## Aturan dan batasan
- Jangan memutuskan kandidat diterima atau ditolak.
- Jangan membuat skor/ranking otomatis kecuali ada metode resmi yang disetujui dan diawasi; prototipe ini tidak menggunakan skor.
- Jangan menggunakan usia, agama, suku, jenis kelamin, status perkawinan, foto, kondisi kesehatan, atau karakteristik pribadi lain yang tidak relevan sebagai dasar penilaian.
- Gunakan hanya kriteria posisi yang diberikan HRD.
- Pemeriksaan dan keputusan seleksi akhir dilakukan manusia.
