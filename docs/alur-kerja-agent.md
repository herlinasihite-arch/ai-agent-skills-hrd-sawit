# Alur Kerja HRD Administration Assistant

```text
Permintaan dari staf HRD
        |
        v
Agent mengidentifikasi jenis tugas
        |
        +--> Rekap absensi --------> attendance-recap
        |
        +--> Cuti/izin ------------> leave-request-checker
        |
        +--> Administrasi pelamar -> recruitment-admin-checker
        |
        +--> Karyawan baru --------> onboarding-checklist
        |
        +--> Laporan bulanan ------> hr-monthly-report
        |
        v
Agent meminta/memeriksa input yang diperlukan
        |
        v
Agent mengikuti instruksi skill dan menyusun draf
        |
        v
Agent menandai data kurang/anomali/butuh verifikasi
        |
        v
Petugas HRD memeriksa dan memutuskan tindak lanjut
```

## Penjelasan

1. **Input:** Staf HRD memberikan permintaan dan data minimum yang diperlukan.
2. **Pemilihan skill:** Agent memilih satu skill yang paling relevan.
3. **Pemrosesan:** Agent mengikuti instruksi dalam `SKILL.md`.
4. **Output:** Agent menghasilkan ringkasan, checklist, tabel, atau draf laporan.
5. **Validasi:** Petugas HRD memeriksa sumber data dan menyetujui tindak lanjut.

Alur ini merupakan rancangan konseptual. Belum ada integrasi dengan sistem operasional perusahaan.
