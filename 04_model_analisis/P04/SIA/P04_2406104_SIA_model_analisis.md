Spesifikasi Hubungan Diagram Kumulatif SIA (16 Hubungan)

No.	Sumber	Hubungan	Tujuan
1	Civitas Akademik	Association	SIA-UC02 Lihat Kalender Akademik
2	Mahasiswa	Association	SIA-UC01 Lihat Jadwal Kuliah
3	Mahasiswa	Association	SIA-UC03 Ajukan KRS
4	Mahasiswa	Association	SIA-UC04 Unduh Bukti Pengajuan KRS
5	Mahasiswa	Association	SIA-UC09 Lihat KHS
6	Dosen	Association	SIA-UC06 Input Nilai Mata Kuliah
7	Admin Akademik	Association	SIA-UC07 Kelola Jadwal Kuliah
8	Admin Akademik	Association	SIA-UC08 Kelola Data Mahasiswa
9	Dosen Wali	Association	SIA-UC05 Proses Keputusan KRS
10	Mahasiswa	Generalization →	Civitas Akademik
11	Dosen	Generalization →	Civitas Akademik
12	SIA-UC03 Ajukan KRS	«include»	SIA-UC10 Validasi KRS
13	SIA-UC04 Unduh Bukti Pengajuan KRS	«extend»	SIA-UC03 Ajukan KRS
14	SIA-UC11 Tambah Data Mahasiswa	Generalization →	SIA-UC08 Kelola Data Mahasiswa
15	SIA-UC12 Ubah Data Mahasiswa	Generalization →	SIA-UC08 Kelola Data Mahasiswa
16	SIA-UC13 Hapus Data Mahasiswa	Generalization →	SIA-UC08 Kelola Data Mahasiswa