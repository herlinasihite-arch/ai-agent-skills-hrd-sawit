---
name: attendance-recap
description: Merangkum data absensi karyawan dari catatan yang diberikan, memeriksa kelengkapan jam masuk dan pulang, serta menandai anomali untuk diverifikasi staf HRD.
---

# Attendance Recap Skill

## Tujuan
Membantu staf HRD menyusun rekap absensi harian, mingguan, atau bulanan dari data yang diberikan.

## Kapan digunakan
Gunakan skill ini ketika pengguna meminta rekap kehadiran, pemeriksaan catatan jam masuk/pulang, ringkasan absensi per unit, atau daftar catatan absensi yang perlu diverifikasi.

## Input yang diperlukan
- File/tabel catatan absensi.
- Periode rekap.
- Definisi kode status (misalnya HADIR, CUTI, IZIN, SAKIT) jika digunakan.
- Jadwal/shift kerja dan batas toleransi keterlambatan hanya jika pengguna meminta analisis keterlambatan.
- Nama unit/lokasi bila diperlukan.

Jika jadwal atau aturan keterlambatan tidak tersedia, jangan menetapkan status terlambat secara final. Sampaikan bahwa aturan belum diberikan.

## Langkah kerja
1. Periksa kolom yang tersedia dan periode data.
2. Hitung jumlah baris/catatan yang diterima.
3. Kelompokkan catatan berdasarkan kode karyawan dan tanggal, jika kedua kolom tersedia.
4. Periksa jam masuk atau jam pulang yang kosong, catatan ganda, format waktu tidak wajar, dan status yang tidak dikenal.
5. Hitung ringkasan hanya berdasarkan baris yang tersedia.
6. Bandingkan jam masuk dengan jadwal hanya jika jadwal dan toleransi resmi disertakan.
7. Pisahkan hasil perhitungan dari anomali yang memerlukan verifikasi.
8. Jangan menyimpulkan bahwa karyawan mangkir hanya karena tidak ada catatan. Mungkin ada kesalahan perangkat, sinkronisasi, atau data belum masuk.

## Format output

### Ringkasan
- Periode:
- Jumlah catatan yang diterima:
- Jumlah kode karyawan unik (jika dapat dihitung):
- Ringkasan status yang tercatat:

### Catatan yang perlu diverifikasi
| Kode karyawan | Tanggal | Temuan pada data | Tindak lanjut verifikasi |
|---|---|---|---|

### Catatan batasan
Jelaskan jika jadwal, toleransi, atau definisi status tidak tersedia.

## Aturan dan batasan
- Gunakan kode karyawan; hindari menampilkan identitas pribadi.
- Jangan mengisi jam yang kosong atau memperbaiki data sumber tanpa bukti.
- Jangan menyimpulkan pelanggaran, mangkir, atau menjatuhkan sanksi.
- Jangan menghitung potongan gaji atau lembur final.
- Tandai data meragukan dengan label **Perlu Verifikasi HRD**.
- Hasil akhir harus diperiksa petugas HRD.
