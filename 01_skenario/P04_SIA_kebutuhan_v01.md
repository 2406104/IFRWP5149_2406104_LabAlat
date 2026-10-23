ID Aktor	Nama Aktor	                Tujuan terhadap Sistem
ACT-01	    Civitas Akademika	        Melihat kalender akademik.
ACT-02	    Mahasiswa	                Melihat jadwal kuliah, mengajukan KRS, mengunduh bukti pengajuan KRS, dan melihat KHS.
ACT-03	    Dosen	                    Melihat kalender akademik dan menginput nilai mata kuliah yang diampunya.
ACT-04	    Admin Akademik	            Mengelola jadwal kuliah serta menambah, mengubah, dan menghapus data mahasiswa sesuai ketentuan sistem.
ACT-05	    Dosen Wali	                Memproses persetujuan atau penolakan KRS

#identifikasi Aktor
AAktor	Kedudukan	Tujuan terhadap sistem
Civitas Akademika	Umum (general), baru pada Pertemuan 4	Peran umum bagi Mahasiswa dan Dosen. Dapat melihat kalender akademik dan mewariskan fungsi tersebut kepada Mahasiswa dan Dosen.
Mahasiswa	Khusus dari Civitas Akademika, tetap dari Pertemuan 3	Melihat jadwal kuliah, mengajukan KRS, dan mengunduh bukti pengajuan KRS. Sebagai aktor khusus, Mahasiswa juga dapat melihat KHS. Fungsi melihat kalender akademik diwarisi dari Civitas Akademika.
Dosen	Khusus dari Civitas Akademika, baru pada Pertemuan 4	Melihat kalender akademik yang diwarisi dari Civitas Akademika dan menginput nilai mata kuliah yang diampunya.
Admin Akademik	Tetap dari Pertemuan 2	Mengelola jadwal kuliah serta mengelola data mahasiswa, meliputi tambah, ubah, dan hapus data mahasiswa sesuai ketentuan sistem.
Dosen Wali	Tetap dari Pertemuan 3	Memproses persetujuan atau penolakan KRS mahasiswa.

#Katalog Usecase
ID	         Nama Use Case	                 Aktor Terkait	            Sumber Kebutuhan	Status
SIA-UC01	Lihat Jadwal Kuliah             	Mahasiswa	            SIA-R01	            Tetap
SIA-UC02	Kelola Jadwal Kuliah	        Admin Akademik	            SIA-R02	            Tetap
SIA-UC03	Ajukan KRS	                        Mahasiswa	            SIA-R03	            Tetap
SIA-UC04	Validasi KRS	                    Sistem	                SIA-R04	            Tetap
SIA-UC05	Unduh Bukti Pengajuan KRS	        Mahasiswa	            SIA-R05	            Tetap
SIA-UC06	Proses Keputusan KRS	            Dosen Wali	            SIA-R06	            Tetap
SIA-UC07	Lihat Kalender Akademik	         Civitas Akademika	        SIA-R07	            Baru
SIA-UC08	Input Nilai Mata Kuliah	            Dosen	                SIA-R08	            Baru
SIA-UC09	Lihat KHS	                        Mahasiswa	            SIA-R09	            Baru
SIA-UC10	Kelola Data Mahasiswa	            Admin Akademik	        SIA-R10	            Baru
SIA-UC11	Tambah Data Mahasiswa	            Admin Akademik	        SIA-R11	            Baru
SIA-UC12	Ubah Data Mahasiswa             	Admin Akademik	        SIA-R11	            Baru
SIA-UC13	Hapus Data Mahasiswa	            Admin Akademik	        SIA-R11	            Baru

//Batas dan Asumsi
Batas dan Asumsi
-Kode kebutuhan dimulai dari SIA-R07 agar SIA-R01 dan SIA-R02 dari Pertemuan 2 serta SIA-R03 sampai SIA-R06 dari Pertemuan 3 tetap memiliki identitas berbeda.
-Pengguna telah terautentikasi dan memiliki hak akses sesuai perannya.
-Kalender akademik merupakan agenda resmi institusi, seperti awal semester, batas KRS, dan masa ujian. Kalender akademik tidak sama dengan jadwal kuliah pada Pertemuan 2.
-Nilai hanya dapat diinput oleh dosen pengampu mata kuliah terkait.
-Nilai yang diinput belum dianggap terpublikasi sebelum dinyatakan resmi sesuai ketentuan tugas. KHS hanya menampilkan nilai yang sudah dipublikasikan.
-Penghapusan data mahasiswa hanya diperbolehkan untuk mahasiswa yang tidak memiliki data akademik aktif. Ketentuan ini bersifat fiktif untuk latihan.
-Pengajuan KRS tetap ditampilkan dalam diagram kumulatif dari Pertemuan 3.
-Pembayaran dan perancangan basis data berada di luar ruang lingkup tugas ini.

//Pemeriksaan Situasi
Pemeriksaan Situasi
Situasi A — Mahasiswa melihat kalender akademik tanpa asosiasi langsung
Hal ini tetap benar karena Mahasiswa merupakan aktor khusus dari Civitas Akademika. Mahasiswa mewarisi fungsi yang terhubung ke aktor umum, termasuk melihat kalender akademik. Oleh karena itu, asosiasi kalender akademik cukup digambar satu kali dari Civitas Akademika dan tidak perlu digambar ulang dari Mahasiswa.
Situasi B — Dosen yang bukan pengampu mencoba menginput nilai
Penginputan nilai harus ditolak karena hanya dosen pengampu mata kuliah tersebut yang memiliki kewenangan untuk menginput nilainya. Tidak boleh ada nilai yang tersimpan sebagai hasil penginputan yang tidak sah.
Situasi C — Admin Akademik menghapus data mahasiswa yang masih memiliki data akademik aktif
Penghapusan harus ditolak karena aturan tugas hanya memperbolehkan penghapusan data mahasiswa yang tidak memiliki data akademik aktif.


//Katalog Use Case

| ID | Nama Use Case | Aktor Terkait | Sumber Kebutuhan | Status |
|---|---|---|---|---|
| SIA-UC01 | Lihat Jadwal Kuliah | Mahasiswa | SIA-R01 (P02) | Tetap |
| SIA-UC02 | Kelola Jadwal Kuliah | Admin Akademik | SIA-R02 (P02) | Tetap |
| SIA-UC03 | Ajukan KRS | Mahasiswa | SIA-R03 (P03) | Tetap |
| SIA-UC04 | Validasi KRS | Sistem | SIA-R04 (P03) | Tetap |
| SIA-UC05 | Unduh Bukti Pengajuan KRS | Mahasiswa | SIA-R05 (P03) | Tetap |
| SIA-UC06 | Proses Keputusan KRS | Dosen Wali | SIA-R06 (P03) | Tetap |
| SIA-UC07 | Lihat Kalender Akademik | Civitas Akademika | SIA-R07 (P04) | Baru |
| SIA-UC08 | Input Nilai Mata Kuliah | Dosen | SIA-R08 (P04) | Baru |
| SIA-UC09 | Lihat KHS | Mahasiswa | SIA-R09 (P04) | Baru |
| SIA-UC10 | Kelola Data Mahasiswa | Admin Akademik | SIA-R10 (P04) | Baru |
| SIA-UC11 | Tambah Data Mahasiswa | Admin Akademik | SIA-R11 (P04) | Baru |
| SIA-UC12 | Ubah Data Mahasiswa | Admin Akademik | SIA-R11 (P04) | Baru |
| SIA-UC13 | Hapus Data Mahasiswa | Admin Akademik | SIA-R11 (P04) | Baru |

//Generalization Aktor

| Aktor Umum | Aktor Khusus | Fungsi yang Diwarisi | Alasan |
|---|---|---|---|
| Civitas Akademika | Mahasiswa | Melihat kalender akademik | Mahasiswa merupakan bagian dari Civitas Akademika sehingga dapat menggunakan fungsi yang tersedia bagi aktor umum. |
| Civitas Akademika | Dosen | Melihat kalender akademik | Dosen merupakan bagian dari Civitas Akademika sehingga dapat menggunakan fungsi yang tersedia bagi aktor umum. |

// Generalization Use Case

| Use Case Umum | Use Case Khusus | Perilaku Pembeda |
|---|---|---|
| SIA-UC10 Kelola Data Mahasiswa | SIA-UC11 Tambah Data Mahasiswa | Menambahkan data mahasiswa baru ke dalam sistem. |
| SIA-UC10 Kelola Data Mahasiswa | SIA-UC12 Ubah Data Mahasiswa | Memperbarui data mahasiswa yang sudah tersimpan. |
| SIA-UC10 Kelola Data Mahasiswa | SIA-UC13 Hapus Data Mahasiswa | Menghapus data mahasiswa yang tidak memiliki data akademik aktif. |

// Collaboration

| ID Collaboration | Nama Collaboration | Use Case yang Direalisasikan | Sumber Kebutuhan |
|---|---|---|---|
| SIA-CO01 | Input Nilai Mata Kuliah | SIA-UC08 Input Nilai Mata Kuliah | SIA-R12 (P04) |
| SIA-CO02 | Lihat KHS | SIA-UC09 Lihat KHS | SIA-R12 (P04) |

// Catatan Relasi

1. SIA-UC03 Ajukan KRS memiliki relasi `<<include>>` ke SIA-UC04 Validasi KRS.
2. SIA-UC05 Unduh Bukti Pengajuan KRS memiliki relasi `<<extend>>` ke SIA-UC03 Ajukan KRS.
3. Kondisi relasi `<<extend>>` adalah `[mahasiswa memilih mengunduh bukti]`.
4. Extension point pada SIA-UC03 adalah `Bukti pengajuan tersedia`.
5. Mahasiswa dan Dosen merupakan aktor khusus dari Civitas Akademika.
6. SIA-UC11 Tambah Data Mahasiswa, SIA-UC12 Ubah Data Mahasiswa, dan SIA-UC13 Hapus Data Mahasiswa merupakan use case khusus dari SIA-UC10 Kelola Data Mahasiswa.
7. SIA-CO01 merealisasikan SIA-UC08, sedangkan SIA-CO02 merealisasikan SIA-UC09.
8. KHS hanya menampilkan nilai yang sudah dipublikasikan.
9. Nilai mata kuliah hanya dapat diinput oleh dosen pengampu mata kuliah tersebut.
10. Penghapusan data mahasiswa hanya diperbolehkan jika mahasiswa tidak memiliki data akademik aktif.


//Deskripsi Use Case SIA-UC08 — Input Nilai Mata Kuliah

| Elemen | Deskripsi |
|---|---|
| ID Use Case | SIA-UC08 |
| Nama Use Case | Input Nilai Mata Kuliah |
| Tujuan | Memungkinkan dosen memasukkan nilai mahasiswa untuk mata kuliah yang diampunya setelah masa perkuliahan berakhir. |
| Aktor Utama | Dosen |
| Sumber Kebutuhan | SIA-R08 |
| Collaboration | SIA-CO01 Input Nilai Mata Kuliah |
| Pemicu | Dosen memilih fungsi input nilai untuk mata kuliah yang diampunya. |
| Prasyarat | Dosen telah terautentikasi, memiliki hak akses yang sesuai, dan merupakan dosen pengampu mata kuliah yang nilainya akan diinput. Masa perkuliahan untuk mata kuliah tersebut telah berakhir. |
| Pascakondisi Berhasil | Nilai yang valid berhasil disimpan sebagai nilai yang belum dipublikasikan sampai dinyatakan resmi sesuai ketentuan tugas. |
| Pascakondisi Gagal | Nilai tidak berhasil disimpan atau perubahan nilai ditolak. Data nilai yang tidak sah tidak menjadi nilai tersimpan. |

//Alur Utama

1. Dosen membuka fungsi Input Nilai Mata Kuliah.
2. Sistem memeriksa hak akses dosen dan memastikan dosen merupakan pengampu mata kuliah tersebut.
3. Sistem menampilkan mata kuliah yang diampu dosen dan data mahasiswa yang terkait.
4. Dosen memasukkan nilai mahasiswa.
5. Sistem memeriksa apakah nilai berada dalam rentang nilai yang sah.
6. Sistem menyimpan nilai yang valid dengan status belum dipublikasikan.
7. Sistem menampilkan pemberitahuan bahwa nilai berhasil disimpan.
