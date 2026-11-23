# Analisis Jobdesk dan Aktivitas Repetitif HRD Perusahaan Kelapa Sawit

## 1. Latar belakang studi kasus

Perusahaan perkebunan kelapa sawit memiliki kegiatan operasional yang dapat tersebar di kantor pusat, kebun, afdeling, dan fasilitas pendukung. Bagian HRD membantu pengelolaan administrasi sumber daya manusia, antara lain data karyawan, absensi, cuti/izin, proses administrasi rekrutmen, orientasi karyawan baru, dan pelaporan.

Analisis berikut merupakan pemetaan umum untuk keperluan tugas kuliah. Pemetaan ini bukan hasil wawancara atau audit terhadap perusahaan tertentu. Prosedur aktual, istilah jabatan, jadwal kerja, dan aturan perusahaan harus dikonfirmasi kepada pihak HRD.

## 2. Identifikasi jobdesk

| No. | Jobdesk HRD | Aktivitas repetitif | Kendala yang mungkin terjadi | Peluang bantuan AI |
|---|---|---|---|---|
| 1 | Administrasi absensi | Menggabungkan catatan hadir, memeriksa jam masuk/keluar, merangkum per unit/periode | Format data berbeda, catatan kosong/ganda, pemeriksaan manual memakan waktu | Mengelompokkan data, menghitung ringkasan dari data yang tersedia, menandai anomali untuk verifikasi |
| 2 | Administrasi cuti dan izin | Memeriksa kolom formulir, tanggal, alasan administratif, lampiran sesuai kebijakan | Formulir tidak lengkap dan data tersebar | Memeriksa kelengkapan berkas dan membuat daftar informasi yang masih kurang |
| 3 | Administrasi rekrutmen | Memeriksa berkas lamaran dan bukti kualifikasi yang disyaratkan | Banyak dokumen dengan format berbeda | Membuat checklist kelengkapan terhadap kriteria posisi yang sudah ditetapkan HRD |
| 4 | Onboarding karyawan baru | Menyiapkan daftar dokumen, jadwal orientasi, dan pengenalan prosedur | Banyak item yang harus disiapkan lintas bagian | Menghasilkan checklist onboarding berdasarkan jabatan dan tanggal mulai |
| 5 | Pelaporan HRD | Menggabungkan jumlah karyawan, absensi, cuti, rekrutmen, dan onboarding per bulan | Rekap manual berulang dan risiko salah salin | Membuat ringkasan, tabel, dan draf laporan berdasarkan data agregat |
| 6 | Pembaruan data karyawan | Mencatat perubahan unit, jabatan, atau status administratif | Data tidak konsisten atau perubahan belum diverifikasi | Menyusun daftar perubahan dan menandai dokumen pendukung yang dibutuhkan; perubahan final dilakukan petugas |
| 7 | Informasi/FAQ karyawan | Menjawab pertanyaan berulang tentang prosedur administrasi dan alur pengajuan | Pertanyaan yang sama datang berulang | Menyusun draf jawaban berdasarkan SOP/FAQ resmi yang disediakan HRD |

## 3. Prioritas aktivitas untuk prototipe

Penilaian prioritas berikut bersifat kualitatif. "Tinggi" berarti aktivitas cukup berulang dan dapat dibantu dengan input terstruktur; bukan berarti AI boleh mengambil keputusan final.

| Aktivitas | Frekuensi indikatif | Potensi bantuan AI | Risiko jika salah | Kontrol manusia |
|---|---|---|---|---|
| Rekap absensi | Harian/mingguan/bulanan | Tinggi | Sedang–tinggi | Verifikasi data sumber, jadwal, dan anomali |
| Pemeriksaan cuti/izin | Setiap ada pengajuan | Tinggi | Sedang | HRD memutuskan sesuai kebijakan |
| Checklist administrasi lamaran | Setiap ada pelamar | Tinggi | Sedang–tinggi | HRD memeriksa kriteria dan seluruh keputusan seleksi |
| Checklist onboarding | Setiap karyawan baru | Tinggi | Rendah–sedang | HRD dan atasan memastikan pelaksanaan |
| Laporan HRD bulanan | Bulanan | Tinggi | Sedang | HRD memeriksa definisi metrik dan angka final |

## 4. Aktivitas yang tidak diotomatisasi sebagai keputusan

Prototipe tidak mengotomatisasi keputusan yang berdampak langsung terhadap hak dan status karyawan. Contohnya persetujuan/penolakan cuti, sanksi disiplin, penetapan upah, pemutusan hubungan kerja, dan keputusan penerimaan kandidat. AI hanya membantu menyiapkan informasi dan menandai hal yang perlu diperiksa.

## 5. Rancangan solusi

Dibuat satu AI Agent bernama **HRD Administration Assistant** dengan lima skill:

1. `attendance-recap` – rekap absensi.
2. `leave-request-checker` – pemeriksaan administrasi cuti/izin.
3. `recruitment-admin-checker` – pemeriksaan kelengkapan administrasi lamaran.
4. `onboarding-checklist` – penyusunan checklist karyawan baru.
5. `hr-monthly-report` – penyusunan ringkasan laporan HRD.

## 6. Manfaat yang diharapkan

- Mengurangi waktu untuk menyusun draf rekap dan daftar periksa.
- Membuat format administrasi lebih konsisten.
- Membantu staf menemukan data kosong atau tidak konsisten lebih awal.
- Memudahkan penyusunan laporan berdasarkan data yang tersedia.
- Memberikan lebih banyak waktu bagi staf HRD untuk verifikasi dan pelayanan yang membutuhkan pertimbangan manusia.

Manfaat tersebut merupakan tujuan rancangan dan belum merupakan hasil pengukuran implementasi nyata.
