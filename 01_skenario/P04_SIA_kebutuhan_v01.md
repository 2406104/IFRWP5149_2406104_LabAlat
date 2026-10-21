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