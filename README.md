# Lab8Web.

**Menambahkan Data**
- CREATE DATABASE membuat wadah data.
- CREATE TABLE mendefinisikan kolom dan tipe datanya; id_barang auto_increment memastikan setiap record punya ID unik (primary key).
- Tipe data (varchar, int, decimal) menentukan bentuk data yang boleh disimpan.
<img width="678" height="154" alt="Cuplikan layar 2025-11-17 125312" src="https://github.com/user-attachments/assets/29a68647-2271-4789-85f0-184b7e5ffada" />
<br><br>

**Membuat file koneksi database**
<img width="1919" height="1076" alt="Cuplikan layar 2025-11-17 130932" src="https://github.com/user-attachments/assets/94c56222-42df-41b4-b584-37504262b05a" />
Skrip ini membuka koneksi antara PHP dan MySQL; semua file lain akan include("koneksi.php") agar bisa menjalankan query.


**Membuat file index untuk menampilkan data (Read)**
<img width="1920" height="1080" alt="Cuplikan layar 2025-11-17 131653" src="https://github.com/user-attachments/assets/aa6e4cfd-06ac-40e4-8f27-cdf8b542251f" />
SELECT * FROM mengambil semua record; mysqli_query mengeksekusi SQL; mysqli_fetch_array mengambil baris hasil satu-per-satu untuk ditampilkan di HTML.


**Menambah Data (Create)**
<img width="1920" height="1080" alt="Cuplikan layar 2025-11-17 132124" src="https://github.com/user-attachments/assets/cb1a9a52-7f9c-4347-91d4-372142b6a56f" />
- Form mengumpulkan input user; enctype="multipart/form-data" diperlukan agar file bisa diupload.
- $_FILES menyimpan info file; move_uploaded_file memindahkan file dari temporary ke folder proyek.
- Setelah insert, redirect ke index agar pengguna melihat data terbaru.


**Mengubah Data (Update)**
<img width="1920" height="1080" alt="Cuplikan layar 2025-11-17 132951" src="https://github.com/user-attachments/assets/58f3fc98-9527-4ca5-96ba-b9ec777e897b" />
SELECT mengambil data saat ini untuk di-prefill; UPDATE mengubah kolom pada baris dengan WHERE tertentu sehingga hanya record target terpengaruh.


**Menghapus Data (Delete)**
<img width="1919" height="1079" alt="Cuplikan layar 2025-11-17 133744" src="https://github.com/user-attachments/assets/37dac9f5-eaa9-4835-99b0-d4cbe2f71c30" />
DELETE menghapus baris; WHERE penting agar tidak menghapus seluruh tabel. Setelah itu redirect ke index untuk lihat perubahan.
