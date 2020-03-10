## Dibuat Oleh Nur Hadi

**1.Pengertian**

REST, singkatan bahasa Inggris dari _Representational State Transfer_, adalah suatu gaya arsitektur perangkat lunak untuk untuk pendistibusian sistem hipermedia, sedangkan CodeIgniter merupakan aplikasi sumber terbuka yang berupa framework PHP dengan model MVC (Model, View, Controller) untuk membangun website dinamis dengan menggunakan PHP. Repository ini adalah penerapan REST API pada Codeigniter 3.

**2. Instalasi** 
- XAMPP, saya menggunakan XAMPP versi 7.1.32 anda dapat mengunduhnya [*disini.*](https://www.apachefriends.org/download.html)
- Text Editor, saya menggunakan Visual Studio Code versi 1.43.0 anda dapat mengunduhnya [*disini.*](https://code.visualstudio.com/download) 
 - Code Igniter 3 anda dapat mendownloadnya [*disini.*](https://codeigniter.com/download)
 - Browser, disini saya menggunakan Google Chrome versi 80.0.3987.132 anda dapat mengunduhnya [*disini.*](https://www.google.com/intl/id_id/chrome/)
 - Postman sebagai aplikasi (plugin) Google Chrome yang digunakan untuk melakukan uji coba REST API anda dapat mengunduhnya *[disini.](https://www.postman.com/downloads/)*
 

**3. Implementasi**

1. Download repository ini,  lalu simpan ke dalam folder htdocs anda.
2. Akses *http://localhost/rest/* pada browser yang anda gunakan,  maka akan muncul halaman Wellcome to CodeIgniter.
3. Jalankan XAMPP, klik start pada apache dan MySQL.
4. Buat database baru dengan nama ***kontak***, lalu import file `kontak.sql` ke dalamnya.
5. Jalankan Visual Studio Code, Buka Folder rest.
6. Buka file pada Visual Studio Code `application/config/database.php` lakukan konfigurasi berikut ini.
``` php
defined('BASEPATH') OR exit('No direct script access allowed');
$active_group = 'default';
$query_builder = TRUE;

$db['default'] = array(
    'dsn'   => '',
    'hostname' => 'localhost',
    'username' => 'root',
    'password' => '',
    'database' => 'kontak',
    'dbdriver' => 'mysqli',
    'dbprefix' => '',
    'pconnect' => FALSE,
    'db_debug' => (ENVIRONMENT !== 'production'),
    'cache_on' => FALSE,
    'cachedir' => '',
    'char_set' => 'utf8',
    'dbcollat' => 'utf8_general_ci',
    'swap_pre' => '',
    'encrypt' => FALSE,
    'compress' => FALSE,
    'stricton' => FALSE,
    'failover' => array(),
    'save_queries' => TRUE
);
```

4. Saya telah membuat function untuk melakukan ***Get, Post, Put,*** dan ***Delete*** pada file `application/controllers/Kontak.php`
5. Buka Postman,  lakukan pendaftaran dll, jika sudah selesai klik ***tombol +***  untuk membuka tab baru.
6. Masukkan link berikut http://localhost/rest/index.php/kontak dan silahkan mencoba untuk melakukan ***Get, Post, Put,*** dan ***Delete.***
7. Coba satu persatu dan lihat perubahan data pada database  ***kontak*** tabel ***telepon***, pastikan perubahan data sesuai dengan aksi yang anda lakukan pada Postman.

## Selamat Mencoba
