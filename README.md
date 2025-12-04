# lab10_php_oop
# nama : keysia nurhayati br panjaitan
# kelas : TI 24 A4
# nim : 312410350

      lab10_php_oop/
      │
      ├── mobil.php
      ├── form.php
      ├── form_input.php
      ├── config.php
      ├── database.php
      └── index.php
      
# Membuat Program OOP Sederhana (mobil.php)
Program berisi deklarasi class Mobil, atribut (warna, merk, harga) dan method (gantiWarna, tampilWarna) serta pemanggilannya.

![WhatsApp Image 2025-12-05 at 01 50 15](https://github.com/user-attachments/assets/045a9de3-adfa-4912-8e2d-dc998b7301ff)

# Membuat Class Library Form (form.php)
Class ini digunakan untuk membuat input form secara dinamis menggunakan konsep modularisasi.

# Implementasi Form (form_input.php)
Pemanggilan class Form dan menampilkan form input mahasiswa.

![WhatsApp Image 2025-12-05 at 01 49 24](https://github.com/user-attachments/assets/09b6dcb2-c9bd-4c65-b539-dc6d4c624e71)

# Membuat Konfigurasi Database (config.php)
       <?php
      $config = [
          'host' => 'localhost',
          'username' => 'root',
          'password' => '',
          'db_name' => 'db_mahasiswa'
      ];
      ?>

# Membuat class Database (database.php)
Berfungsi menyimpan data hasil input form ke MySQL.     

# Proses Simpan Data (index.php)
      <?php
      include "database.php";
      
      $db = new Database();
      $data = [
          'nim' => $_POST['txtnim'],
          'nama' => $_POST['txtnama'],
          'alamat' => $_POST['txtalamat']
      ];
      
      $db->insert("mahasiswa", $data);
      
      echo "Data berhasil disimpan!";
      ?>
