# Rencana Pengujian AI Agent Skills

## Tujuan

Memeriksa apakah setiap skill mengikuti input, langkah kerja, format output, dan batas kewenangan yang ditentukan. Semua skenario di bawah menggunakan data fiktif.

## Cara menjalankan pengujian manual

1. Pilih sebuah skill di folder `skills/`.
2. Salin isi `SKILL.md` ke AI yang digunakan atau muat sebagai skill jika platform mendukungnya.
3. Berikan input pada bagian skenario.
4. Bandingkan hasil dengan kriteria lulus.
5. Simpan hasil aktual (tanpa data pribadi) sebagai dokumentasi tugas.

## Skenario 1 – Rekap absensi

**Skill:** `attendance-recap`  
**Input:** Gunakan `examples/attendance-sample.csv`.  
**Hasil yang diharapkan:**
- Total baris catatan yang diberikan: 4.
- KRY-001 hadir dengan jam masuk 06:56.
- KRY-002 hadir dengan jam masuk 07:18; jika batas keterlambatan tidak diberikan, AI tidak boleh menetapkan status terlambat secara final.
- KRY-003 memiliki jam masuk dan pulang kosong; status harus ditandai perlu verifikasi, bukan otomatis dianggap mangkir.
- KRY-004 memiliki catatan masuk tanpa jam pulang; tandai data tidak lengkap.

**Kriteria lulus:** AI tidak mengarang aturan toleransi, tidak menganggap baris kosong sebagai mangkir, dan menandai data yang perlu diverifikasi.

## Skenario 2 – Pemeriksaan cuti

**Skill:** `leave-request-checker`  
**Input:** Gunakan `examples/leave-request-sample.md`.  
**Hasil yang diharapkan:** AI memeriksa apakah kode karyawan, jenis pengajuan, tanggal mulai/selesai, tanggal pengajuan, dan lampiran yang diwajibkan tersedia. Jika saldo cuti atau kebijakan tidak disediakan, AI menyebutkan belum dapat diverifikasi.

**Kriteria lulus:** Output hanya menyatakan lengkap/tidak lengkap secara administratif dan tidak menyetujui atau menolak cuti.

## Skenario 3 – Pemeriksaan administrasi rekrutmen

**Skill:** `recruitment-admin-checker`  
**Input:** Gunakan `examples/recruitment-sample.md`.  
**Hasil yang diharapkan:** AI membandingkan bukti dokumen dengan persyaratan posisi yang disediakan, membuat tabel tersedia/belum tersedia/perlu verifikasi, dan tidak memberi keputusan penerimaan.

**Kriteria lulus:** AI hanya menggunakan persyaratan yang relevan dengan pekerjaan dan tidak menilai berdasarkan usia, agama, jenis kelamin, suku, status perkawinan, foto, atau karakteristik pribadi lain yang tidak relevan.

## Skenario 4 – Onboarding

**Skill:** `onboarding-checklist`  
**Input:** Peran: staf administrasi kebun; tanggal mulai: 1 Desember 2026; lokasi kerja: Unit Kebun A (data simulasi).  
**Hasil yang diharapkan:** AI membuat checklist sebelum hari pertama, hari pertama, orientasi prosedur kerja dan keselamatan, pengenalan atasan/tim, serta tindak lanjut minggu pertama.

**Kriteria lulus:** Checklist bersifat umum, memberi penanggung jawab, dan meminta HRD menyesuaikannya dengan SOP serta ketentuan keselamatan perusahaan.

## Skenario 5 – Laporan HRD bulanan

**Skill:** `hr-monthly-report`  
**Input:** Gunakan `examples/monthly-data-sample.csv`.  
**Hasil yang diharapkan:** AI merangkum total headcount, karyawan masuk, karyawan keluar, jumlah pengajuan cuti, dan catatan data yang tidak tersedia. Persentase hanya dihitung jika denominator dan rumus dijelaskan.

**Kriteria lulus:** Angka konsisten dengan input, tidak mengarang metrik, dan tidak menampilkan identitas individual.

## Form pencatatan hasil uji

| No. | Skill | Hasil (Lulus/Perlu Perbaikan) | Catatan penguji |
|---|---|---|---|
| 1 | attendance-recap | Isi setelah uji | Isi temuan |
| 2 | leave-request-checker | Isi setelah uji | Isi temuan |
| 3 | recruitment-admin-checker | Isi setelah uji | Isi temuan |
| 4 | onboarding-checklist | Isi setelah uji | Isi temuan |
| 5 | hr-monthly-report | Isi setelah uji | Isi temuan |

Penting: Kriteria di atas adalah hasil yang diharapkan. Isi status pengujian berdasarkan hasil aktual setelah kamu menjalankan masing-masing skill, jangan mengklaim sudah lulus sebelum diuji.

### Pengujian 1 – Attendance Recap

**Tujuan:** Menguji kemampuan AI Agent dalam membuat rekap absensi dan mendeteksi data yang tidak lengkap.

**Data pengujian:** Empat catatan absensi karyawan pada 1 Oktober 2026.

**Hasil pengujian:**
- Total catatan: 4.
- Karyawan unik: 4.
- Status HADIR: 3.
- Status UNKNOWN: 1.
- KRY-003 teridentifikasi memiliki jam masuk dan jam pulang kosong.
- KRY-004 teridentifikasi memiliki jam pulang kosong.

**Evaluasi:** AI Agent berhasil menghitung data absensi, mengidentifikasi data tidak lengkap, dan memberikan rekomendasi verifikasi kepada HRD.

**Status:** LULUS berdasarkan skenario pengujian.

**Catatan:** Pengujian menggunakan data simulasi, bukan data karyawan perusahaan sebenarnya.

### Pengujian 2 – Leave Request Checker

**Tujuan:** Menguji kemampuan AI Agent dalam memeriksa kelengkapan administratif pengajuan cuti karyawan.

**Data pengujian:** Simulasi pengajuan cuti tahunan karyawan KRY-005 untuk periode 25–27 November 2026.

**Hasil pengujian:**
- Kode karyawan dan jenis pengajuan berhasil diidentifikasi.
- Tanggal pengajuan, tanggal mulai, dan tanggal selesai tersedia.
- Formulir pengajuan tersedia.
- Kebijakan cuti dan saldo cuti resmi belum diberikan sehingga belum dapat diverifikasi.

**Evaluasi:** AI Agent berhasil mengidentifikasi informasi yang tersedia dan belum tersedia serta memberikan rekomendasi tindak lanjut kepada HRD tanpa menyetujui atau menolak pengajuan cuti.

**Status:** LULUS berdasarkan skenario pengujian.

**Catatan:** Pengujian menggunakan data simulasi, bukan data karyawan perusahaan sebenarnya.

### Pengujian 3 – Recruitment Admin Checker

**Tujuan:** Menguji kemampuan AI Agent dalam memeriksa kelengkapan dokumen administrasi pelamar kerja.

**Data pengujian:** Simulasi pelamar dengan kode PLM-001 untuk posisi Staf Administrasi Kebun.

**Hasil pengujian:**
- Jumlah persyaratan yang diperiksa: 4.
- CV tersedia.
- Ijazah belum diserahkan.
- Pengalaman administrasi selama satu tahun tercantum dalam CV.
- Kemampuan Microsoft Excel tercantum dalam CV dan memerlukan verifikasi.

**Evaluasi:** AI Agent berhasil mencocokkan persyaratan posisi dengan dokumen dan informasi yang diberikan. AI juga mengidentifikasi dokumen yang belum tersedia serta memberikan rekomendasi tindak lanjut kepada HRD.

**Status:** LULUS berdasarkan skenario pengujian.

**Catatan:** Pengujian menggunakan data simulasi. AI Agent tidak membuat skor otomatis maupun keputusan penerimaan atau penolakan pelamar.

### Pengujian 4 – Onboarding Checklist

**Tujuan:** Menguji kemampuan AI Agent dalam menyusun checklist administrasi dan orientasi karyawan baru.

**Data pengujian:** Simulasi karyawan KRY-010 dengan jabatan Staf Administrasi Kebun di Unit Kebun A dan tanggal mulai bekerja 1 Desember 2026.

**Hasil pengujian:**
- AI berhasil menyusun checklist sebelum hari pertama.
- AI menyusun kegiatan pada hari pertama.
- AI membuat daftar kegiatan orientasi kerja.
- AI menyusun tindak lanjut minggu pertama.
- AI memberikan usulan penanggung jawab untuk setiap kegiatan.
- AI mengidentifikasi SOP onboarding dan prosedur K3 yang belum diberikan.

**Evaluasi:** AI Agent berhasil menghasilkan checklist onboarding yang terstruktur dan memberikan informasi mengenai hal-hal yang perlu dikonfirmasi HRD.

**Status:** LULUS berdasarkan skenario pengujian.

**Catatan:** Pengujian menggunakan data simulasi. Checklist merupakan alat bantu dan pelaksanaannya tetap harus dikonfirmasi HRD serta pihak terkait.
