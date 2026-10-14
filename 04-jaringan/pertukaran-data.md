# Pertukaran Data: Pengguna - Jaringan - Server - Basis Data

1. Pengguna mengirim permintaan (login, pilih mata kuliah, input nilai) melalui browser atau aplikasi.
2. Jaringan membawa permintaan ke server memakai TCP/IP dan HTTPS.
3. Server aplikasi memvalidasi permintaan dan membuat perintah SQL (SELECT, INSERT, UPDATE).
4. Basis data memproses perintah dan mengembalikan hasilnya ke server.
5. Server mengirim respons (jadwal, KRS, KHS, konfirmasi) kembali melalui jaringan ke pengguna.

Pengguna tidak mengakses basis data secara langsung; semua akses melalui server aplikasi.
