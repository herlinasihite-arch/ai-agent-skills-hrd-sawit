---
name: leave-request-checker
description: Memeriksa kelengkapan administratif permohonan cuti atau izin berdasarkan formulir dan kebijakan yang secara eksplisit diberikan oleh staf HRD.
---

# Leave Request Checker Skill

## Tujuan
Membantu staf HRD menemukan bagian formulir cuti/izin yang belum diisi atau dokumen administratif yang belum tersedia.

## Kapan digunakan
Gunakan skill ini saat pengguna meminta pemeriksaan awal permohonan cuti, izin, atau ketidakhadiran terencana.

## Input yang diperlukan
- Kode karyawan anonim.
- Jenis pengajuan.
- Tanggal pengajuan.
- Tanggal mulai dan tanggal selesai.
- Formulir atau daftar persyaratan administrasi.
- Kebijakan perusahaan yang relevan, bila pemeriksaan harus didasarkan pada kebijakan.
- Saldo cuti hanya bila pengguna meminta pemeriksaan saldo dan data saldo resmi tersedia.

Jangan meminta diagnosis atau rincian medis. Untuk izin yang memerlukan dokumen pendukung, cukup catat apakah dokumen yang diwajibkan tersedia tanpa menyalin isi sensitifnya.

## Langkah kerja
1. Periksa apakah kode karyawan dan jenis pengajuan tersedia.
2. Periksa tanggal pengajuan, tanggal mulai, dan tanggal selesai.
3. Pastikan tanggal dapat dibaca dan urutannya masuk akal.
4. Cocokkan persyaratan dokumen hanya dengan kebijakan yang diberikan pengguna.
5. Jika kebijakan, saldo cuti, atau lampiran wajib tidak disediakan, tandai **Belum dapat diverifikasi**.
6. Buat daftar kekurangan atau pertanyaan klarifikasi.
7. Sajikan status kelengkapan administratif, bukan keputusan persetujuan.

## Format output

### Hasil pemeriksaan administratif
- Kode karyawan:
- Jenis pengajuan:
- Periode:
- Status kelengkapan: Lengkap / Belum lengkap / Belum dapat diverifikasi

### Checklist
| Komponen | Status | Catatan |
|---|---|---|

### Informasi yang perlu dilengkapi
Tuliskan butir yang belum tersedia.

### Tindak lanjut
Berikan saran administratif, misalnya meminta formulir diperbaiki atau meminta dokumen yang tercantum dalam kebijakan.

## Aturan dan batasan
- Jangan menyetujui atau menolak cuti/izin.
- Jangan menyatakan saldo cuti tanpa data resmi.
- Jangan membuat kebijakan perusahaan sendiri.
- Jangan menilai alasan pribadi atau kondisi medis.
- Keputusan dan validasi akhir tetap oleh petugas HRD berwenang.
