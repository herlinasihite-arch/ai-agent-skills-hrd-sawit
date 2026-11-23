---
name: hr-monthly-report
description: Menyusun ringkasan laporan HRD bulanan dari data agregat yang diberikan, memeriksa konsistensi angka, dan menandai metrik yang belum memiliki data pendukung.
---

# HR Monthly Report Skill

## Tujuan
Membantu staf HRD membuat draf laporan bulanan yang ringkas dan konsisten dari data agregat.

## Kapan digunakan
Gunakan skill ini ketika pengguna memberikan rekap jumlah karyawan, perubahan headcount, absensi, cuti/izin, rekrutmen, atau onboarding untuk periode tertentu.

## Input yang diperlukan
- Bulan dan tahun pelaporan.
- Data agregat per unit/lokasi bila tersedia.
- Definisi setiap metrik dan periode pembanding bila diminta.
- Data awal/akhir periode untuk menghitung perubahan headcount, jika tersedia.

## Langkah kerja
1. Identifikasi periode dan kolom data.
2. Periksa nilai kosong, duplikasi, dan konsistensi antarjumlah.
3. Hitung hanya metrik yang didukung oleh input.
4. Tunjukkan rumus dan denominator untuk setiap persentase.
5. Bandingkan dengan periode sebelumnya hanya jika data pembanding tersedia.
6. Kelompokkan hasil menjadi ringkasan, tabel metrik, catatan data, dan tindak lanjut.
7. Gunakan data agregat; jangan menampilkan identitas individu.

## Format output

### Ringkasan eksekutif
Tulis 3–5 kalimat berdasarkan angka yang tersedia.

### Tabel indikator
| Indikator | Nilai | Periode/rumus | Catatan |
|---|---:|---|---|

### Kualitas data
Tuliskan kolom yang kosong, definisi yang belum tersedia, atau angka yang perlu diverifikasi.

### Tindak lanjut yang disarankan
Sampaikan daftar tindak lanjut administratif, bukan keputusan kepegawaian.

## Aturan dan batasan
- Jangan mengarang angka atau tren.
- Jangan menghitung persentase tanpa denominator yang jelas.
- Jangan menampilkan data personal atau rincian individual.
- Jangan menetapkan gaji, bonus, potongan, sanksi, atau keputusan kepegawaian.
- Nyatakan asumsi dan keterbatasan data.
- Draf laporan harus diperiksa dan disahkan petugas HRD.
