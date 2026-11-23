# AI Agent Skills untuk Administrasi HRD Perusahaan Kelapa Sawit

**Jenis proyek:** Prototipe pembelajaran / tingkat pemula  
**Studi kasus:** Administrasi Human Resources Department (HRD) pada perusahaan perkebunan kelapa sawit  
**Agent utama:** HRD Administration Assistant  
**Bahasa:** Indonesia

## 1. Deskripsi proyek

Proyek ini merancang kumpulan *Agent Skills* untuk membantu pekerjaan administratif HRD yang berulang, seperti rekap absensi, pemeriksaan kelengkapan pengajuan cuti, pemeriksaan administratif berkas lamaran, checklist onboarding, dan penyusunan laporan HRD bulanan.

Skills disimpan dalam format folder yang masing-masing memiliki file `SKILL.md`. Format Agent Skills menggunakan metadata `name` dan `description` pada bagian awal file, lalu instruksi kerja dalam Markdown. Skills merupakan paket instruksi yang dapat digunakan oleh AI Agent yang mendukung format Agent Skills; repository ini **bukan** aplikasi HRIS dan belum terhubung ke sistem perusahaan.

## 2. Tujuan

- Mengidentifikasi aktivitas HRD yang repetitif dan berpotensi dibantu AI.
- Menyusun lima kemampuan AI Agent yang memiliki input, alur kerja, dan format output yang jelas.
- Menunjukkan contoh pengujian menggunakan data fiktif.
- Menjaga keputusan kepegawaian tetap berada pada petugas HRD yang berwenang.

## 3. Daftar Skills

| Skill | Fungsi |
|---|---|
| `attendance-recap` | Merangkum catatan absensi dan menandai data yang perlu diverifikasi. |
| `leave-request-checker` | Memeriksa kelengkapan administratif permohonan cuti/izin. |
| `recruitment-admin-checker` | Memeriksa kelengkapan dokumen dan bukti kualifikasi berdasarkan persyaratan posisi. |
| `onboarding-checklist` | Membuat checklist administrasi dan orientasi karyawan baru. |
| `hr-monthly-report` | Menyusun ringkasan HRD bulanan dari data agregat yang diberikan. |

## 4. Struktur repository

```text
ai-agent-skills-hrd-sawit/
├── README.md
├── AGENT_PROFILE.md
├── ANALISIS_JOBDESK.md
├── TESTING.md
├── PRIVACY_AND_LIMITATIONS.md
├── skills/
│   ├── attendance-recap/SKILL.md
│   ├── leave-request-checker/SKILL.md
│   ├── recruitment-admin-checker/SKILL.md
│   ├── onboarding-checklist/SKILL.md
│   └── hr-monthly-report/SKILL.md
├── examples/
│   ├── attendance-sample.csv
│   ├── leave-request-sample.md
│   ├── recruitment-sample.md
│   └── monthly-data-sample.csv
└── docs/
    └── alur-kerja-agent.md
```

## 5. Cara menggunakan untuk pengujian pemula

1. Buka salah satu folder pada `skills/` dan baca `SKILL.md`.
2. Salin instruksi skill yang relevan ke AI yang digunakan, atau muat folder skill pada platform AI Agent yang mendukung format Agent Skills.
3. Berikan input fiktif dari folder `examples/`.
4. Minta AI mengikuti langkah dan format output di dalam `SKILL.md`.
5. Periksa hasilnya menggunakan kriteria pada `TESTING.md`.
6. Jangan mengunggah data karyawan, pelamar, atau perusahaan yang sebenarnya ke layanan AI publik.

Contoh prompt untuk menjalankan pengujian:

> Gunakan instruksi pada `skills/attendance-recap/SKILL.md`. Analisis data contoh absensi yang saya berikan. Jangan membuat kesimpulan yang tidak didukung data dan tandai catatan yang perlu diverifikasi petugas HRD.

## 6. Ruang lingkup dan batasan

- Studi kasus ini bersifat simulasi akademik dan tidak mewakili SOP perusahaan sawit tertentu.
- Data contoh sepenuhnya fiktif dan menggunakan kode pegawai, bukan nama atau identitas nyata.
- AI membantu pekerjaan administratif, bukan menggantikan kewenangan HRD.
- AI tidak boleh menetapkan sanksi, menyetujui cuti, memutuskan penerimaan kandidat, menghitung atau menetapkan gaji final, maupun mengambil keputusan ketenagakerjaan otomatis.
- Setiap hasil harus diperiksa oleh petugas HRD dan disesuaikan dengan kebijakan perusahaan serta ketentuan yang berlaku.

## 7. Dokumentasi

- Analisis pekerjaan: [`ANALISIS_JOBDESK.md`](ANALISIS_JOBDESK.md)
- Profil dan instruksi Agent utama: [`AGENT_PROFILE.md`](AGENT_PROFILE.md)
- Alur penggunaan: [`docs/alur-kerja-agent.md`](docs/alur-kerja-agent.md)
- Pengujian: [`TESTING.md`](TESTING.md) dan [contoh hasil yang diharapkan](examples/expected-results.md)
- Privasi dan batasan: [`PRIVACY_AND_LIMITATIONS.md`](PRIVACY_AND_LIMITATIONS.md)

## 8. Referensi format

- Agent Skills specification: <https://agentskills.io/specification>
- Repository dokumentasi Agent Skills: <https://github.com/agentskills/agentskills>
- GitHub Docs – membuat repository: <https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository>

---

**Catatan akademik:** Silakan sesuaikan identitas penyusun, nama mata kuliah, dan uraian studi kasus sesuai instruksi dosen. Jangan menyatakan bahwa sistem sudah diterapkan di perusahaan; proyek ini adalah rancangan/prototipe berbasis data simulasi.
