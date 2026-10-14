# Rancangan Tabel Basis Data SIAKAD

## 1. MAHASISWA
- Atribut: NIM, Nama_Mahasiswa, Tempat_Lahir, Tanggal_Lahir, Alamat, No_HP, Email, Program_Studi, Angkatan, Status
- Primary key: NIM

## 2. DOSEN
- Atribut: NIDN, Nama_Dosen, Alamat, No_HP, Email, Jabatan_Fungsional
- Primary key: NIDN

## 3. MATA_KULIAH
- Atribut: Kode_MK, Nama_MK, SKS, Semester, Program_Studi
- Primary key: Kode_MK

## 4. KELAS
- Atribut: ID_Kelas, Kode_MK, NIDN, Tahun_Akademik, Hari, Jam_Mulai, Jam_Selesai, Ruang
- Primary key: ID_Kelas
- Foreign key: Kode_MK -> MATA_KULIAH(Kode_MK), NIDN -> DOSEN(NIDN)

## 5. KRS
- Atribut: ID_KRS, NIM, ID_Kelas, Tanggal_Pengisian, Nilai_Tugas, Nilai_UTS, Nilai_UAS, Nilai_Akhir, Nilai_Huruf
- Primary key: ID_KRS
- Foreign key: NIM -> MAHASISWA(NIM), ID_Kelas -> KELAS(ID_Kelas)

## 6. AKUN_MAHASISWA (tambahan)
- Atribut: NIM, Username, Password_Hash, Terakhir_Login
- Primary key: NIM (sekaligus foreign key)
- Foreign key: NIM -> MAHASISWA(NIM)
- Relasi: One-to-One dengan MAHASISWA (satu mahasiswa memiliki satu akun login)
