assalamuallaikum kembali lagi ke github saya mastio1836 kali ini saya akan mengakhiri dari project ini yaitu menambahkan pagianation di labs seblumnya saya sudah mendeklarasikan semua program dari header,footer,isi,css,crud,hingga yang terakhir sekarang adalah pagiantion

Membuat Pagination
Pagination merupakan proses yang digunakan untuk membatasi tampilan yang panjang
dari data yang banyak pada sebuah website. Fungsi pagination adalah memecah
tampilan menjadi beberapa halaman tergantung banyaknya data yang akan ditampilkan
pada setiap halaman.
Pada Codeigniter 4, fungsi pagination sudah tersedia pada Library sehingga cukup
mudah menggunakannya.

# STEP KE 1
Untuk membuat pagination, buka Kembali Controller Artikel (htdocs\lab11_php_ci\ci4\Controllers\Artikel.php), kemudian modifikasi kode pada method admin_index seperti berikut.



![Input admin index](https://user-images.githubusercontent.com/56244106/124551068-d1e88980-de5b-11eb-934f-b30341475ec6.JPG)

Kemudian buka file views/artikel/admin_index.php dan tambahkan kode berikut dibawah deklarasi tabel data.


                           <?= $pager->links(); ?>


![page links admin index 1](https://user-images.githubusercontent.com/56244106/124551214-02c8be80-de5c-11eb-9b95-45a36ebe09f2.JPG)


Kemudian buka file public/admin.css input kode berikut untuk memperindah 

![CSS PAGINATION](https://user-images.githubusercontent.com/56244106/124551792-dc575300-de5c-11eb-861a-af36589ce54d.JPG)

 buka menu daftar artikel, tambahkan data lagi untuk melihat hasilnya.

![output menu daftar artikel](https://user-images.githubusercontent.com/56244106/124552023-2cceb080-de5d-11eb-96b7-9b2b1c3ccb0f.JPG)

# STEP KE 2

Membuat Pencarian
Pencarian data digunakan untuk memfilter data.
Untuk membuat pencarian data, buka kembali Controller Artikel, pada method
admin_index ubah kodenya seperti berikut

![ADMIN INDEX 2 INPUT](https://user-images.githubusercontent.com/56244106/124554246-f7779200-de5f-11eb-91bc-ca4fc39d4bdd.JPG)


buka kembali file views/artikel/admin_index.php dan tambahkan form pencarian sebelum deklarasi tabel seperti berikut:

![form method admin index input](https://user-images.githubusercontent.com/56244106/124556892-11ff3a80-de63-11eb-8fef-21abab8fd71d.JPG)


Ubah link page nya seperti berikut

       <?= $pager->only(['q'])->links(); ?>

![link page admin index](https://user-images.githubusercontent.com/56244106/124556259-43c3d180-de62-11eb-9d5b-147bc979a9d8.JPG)

buka file public/admin.css tambahkan kode berikut untuk memperindah tampilan pencarian

![CSS SEARCH INPUT](https://user-images.githubusercontent.com/56244106/124557259-7f12d000-de63-11eb-9faf-ca71e73e971f.JPG)

ujicoba dengan membuka kembali halaman admin artikel, masukkan kata kunci tertentu pada form pencarian.

![Tampilan dashboard search](https://user-images.githubusercontent.com/56244106/124557328-9356cd00-de63-11eb-81cc-4cf013bc6601.JPG)

# STEP KE 3 
UPLOAD GAMBAR
Menambahkan fungsi unggah gambar pada tambah artikel. Buka kembali Controller Artikel (htdocs\lab11_php_ci\ci4\Controllers\Artikel.php), sesuaikan kode pada method add seperti berikut:

![form add input](https://user-images.githubusercontent.com/56244106/124557503-c8631f80-de63-11eb-8b35-bd038490453e.JPG)


Kemudian pada file views/artikel/form_add.php tambahkan field input file seperti berikut.

       <p>
      <input type="file" name="gambar">
       </p>

sesuaikan tag form dengan menambahkan ecrypt type seperti berikut.

<form action="" method="post" enctype="multipart/form-data">

![form add input](https://user-images.githubusercontent.com/56244106/124557786-1546f600-de64-11eb-8810-40623cf78d26.JPG)

buka file public/admin.css tambahkan kode berikut untuk mempercantik tampilan tomboll upload gambar

![CSS UPLOAD GAMBAR](https://user-images.githubusercontent.com/56244106/124557859-2e4fa700-de64-11eb-902a-1ad2457ab7d5.JPG)

Lalu kita uji coba untuk ouput ini dengan mengakses menu artikel

![tampilan output gambar](https://user-images.githubusercontent.com/56244106/124557915-3d365980-de64-11eb-9cdd-7c81329a0341.JPG)













