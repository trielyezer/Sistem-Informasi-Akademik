# Relasi Antar Tabel

| No | Tabel induk (sisi 1) | Tabel anak (sisi N) | Jenis relasi | Foreign key |
|---|---|---|---|---|
| 1 | MAHASISWA | KRS | One-to-Many | NIM |
| 2 | KELAS | KRS | One-to-Many | ID_Kelas |
| 3 | MATA_KULIAH | KELAS | One-to-Many | Kode_MK |
| 4 | DOSEN | KELAS | One-to-Many | NIDN |
| 5 | MAHASISWA - KELAS | | Many-to-Many | dipecah melalui tabel KRS |
| 6 | MAHASISWA | AKUN_MAHASISWA | One-to-One | NIM (PK sekaligus FK) |

Relasi Many-to-Many antara mahasiswa dan kelas dipecah menggunakan tabel KRS sebagai tabel penghubung (junction table).
