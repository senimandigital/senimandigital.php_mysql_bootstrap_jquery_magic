### Magic Meta

Hal pertama yang harus kita ketahui saat menggunakan Magic Frontend dari senimandigital adalah: "Magic Meta" kita menggunakan meta untuk berkomunikasi satu arah dari backend ke frontend. Magic Meta di klasifikasikan kedalam 2 kelompok utama, yaitu: Magic Meta Tanpa Login dan Magic Meta Dengan Login:

#### Magic Meta Tanpa Login
```html
<meta name="domain_site" content="https://senimandigital.com/" />
<meta name="domain_sub" content="templates" />
<meta name="domain_gambar" content="https://images.senimandigital.com/" />
<meta name="domain_templates" content="https://senimandigital.kom/Templates/" />
```
#### Magic Meta Dengan Login
```html
<meta name="domain_administrator" content="https://administrator.senimandigital.kom/" />
```
Diatas hanya contoh, dalam prakteknya anda dapat menambahkan costume meta anda sendiri. Hal yang paling penting dari Magic Meta ini adalah: Javascript yang kita tulis harus beraksi sesuai nilai yang didefinisikan pada "Magic Meta", sehingga pada javascript tidak perlu lagi mendefinisikan variable global.

### Contoh Komplek Penggunaan Artribute Magic
Magic Attribute, membantu programmer untuk tidak berurusan dengan algoritma saat memprogram tapi fokus berurusan dengan html saja. Perhatikan contoh berikut:
```html
<ul horizontal_slider="infinite_autoplay" height="64">
  <li><img height="64" addsrc="meta[name=domain_gambar]" src="logo/ace-logo.png" /></li>
  <li><img height="64" addsrc="meta[name=domain_gambar]" src="logo/ajaxplorer.png" /></li>
  <li><img height="64" addsrc="meta[name=domain_gambar]" src="logo/aksiide.png" /></li>
  <li><img height="64" addsrc="meta[name=domain_gambar]" src="logo/aloha-editor.png" /></li>
  <li><img height="64" addsrc="meta[name=domain_gambar]" src="logo/apache-http-server.png" /></li>
  <li><img height="64" addsrc="meta[name=domain_gambar]" src="logo/arsitek-tas.png" /></li>
</ul>
```
Diatas kita bisa melihat ada banyak sekali attribute yang tidak standard dan tidak dikenali oleh browser. Seperti:
1. Attribute \[height\] pada tag ul: Jika anda tidak menggunakan script javascrip magic maka penambahan attribute height pada elemen ul tidak akan menghasilkan apa-apa, tapi jika anda sudah meload javascript magic maka attribute ini akan bekerja dan otomatis mengatur tinggi element ul sesai angka yang anda definisikan.
2. Attribute \[horizontal_slider\] pada tag \<ul\> Jika anda tidak menggunakan script javascrip magic maka penambahan attribute \[horizontal_slider\] pada elemen ul tidak akan menghasilkan apa-apa, tapi jika anda sudah meload javascript magic maka attribute ini akan bekerja dan otomatis mengatur display list menjadi horizontal dan mengaktifkan fitur slider dengan auto play.
3. Attribute \[addsrc\] pada tag \<img\> Jika anda tidak menggunakan script javascrip magic maka penambahan attribute \[horizontal_slider\] pada elemen ul tidak akan menghasilkan apa-apa, tapi jika anda sudah meload javascript magic maka attribute ini akan bekerja dan otomatis menambahkan alamat domain gambar diawalan attribute src.

Dari beberapa contoh diatas anda seharusnya sudah mengerti perbedaan Frontend Framework diluar sana dengan Frontend Magic dari Senimandigital, tapi untuk memastikan perbedaan tersebut kami akan jelaskan dalam beberapa point:

1. Frontend Framework hanya memindahkan algoritma javascript ke attribute html, ini berarti kita masih perlu menulis algoritma didalam attribute html, sedangkan "Frontend Magic" berusaha mengambil alih proses pemrograman.

### Magic Attribute: [href-prev-for] & [href-next-for]

Ketika membangun aplikasi sering kita butuh menyediakan tombol next dan prev, tapi tidak semua-nya perlu di proses dari backend, apabila kita punya list pada halaman yang sama
maka kita bisa membuat tombol next dan prev hanya dengan menggunakan kode html seperti ini:

```html
<a href-prev-for="#list_directory">Prev</a>
<a href-next-for="#list_directory">Next</a>
```

### Magic Attribute [href-dialog], [href-popup], [href-dialog-ajax], [href-dialog-ajax]

Senimandigital menyediakan berbagai cara interaksi dengan form yang berbeda, secara default attribute href tetap digunakan untuk mengantisifasi aksi berdasarkan klik kanan.
apabila attribute seperti: hrefp-popup di klik, maka attribute href akan dibatalkan dan yang diproses adalah even on click yang targetnya diambil dari attribute href dialog.

```html
<a href-dialog="http://">Text</a>
<a href-dialog-ajax="https://">Text</a>
<a href-panel-left="#element">Test</a>
<a href-panel-top".element">Test</a>
<a href-panel-right="=">Text</a>
<a href-popup="/filename.php">Text</a>
```

### Magic Attribute [children=reverse]

Dalam banyak kasus, kita ingin meletakan Element seperti link agar rata kanan menggunakan css, tapi yang css lakukan justru adalah membuat urutan children menjadi terbalik, dengan magic attribute [children=reverse] kita bisa membalik lagi urutan children pada sebuah element.

```html
<nav children="reverse">
  <a target="_blank" href="/search_replace_project_edit.php?search_replace_project_id=">Edit</a>
  <a target="_blank" href="/project_file_rename_recursive.php">Recursive File Rename</a>
</nav>
```

# Sebenar-nya apa perbedaan Magic.JS dengan Framework Javascript lain... ?
magic.js kami perlakukan sebagai library dan bukan framework, magic.js tidak menolak framework yang sudah ada tapi magic.js akan berprilaku sebagai driver. Orang selalu mengistilahkan bahwa framework adalah alat atau kendaraan untuk membantu kita mencapai tujuan dalam pengembangan aplikasi dengan lebih cepat dan mudah.

Sekarang setelah kita tahu bahwa framework adalak kendaraan, maka untuk menjadi lebih mudah tentu saja kita butuh driver untuk mengendarai kendaraan tersebut, sehingga kita tidak perlu mempelajari hal-hal apapun terkait kendaraan yang kita gunakan tapi kita hanya perlu belajar menjadi bos yang bisa mengatur sang driver tadi.

Tidak perduli akhir-nya anda mau menggunakan kendaraan manapun, anda hanya perlu mendownload dan menggunakan driver yang sesuai. dengan cara ini kendaraan manapun yang akhirnya anda gunakan, cara kerja anda tidak akan berubah, anda hanya perlu mengerti satu bahasa yang dikuasai oleh driver sehingga anda bisa berkomunikasi dengan driver yang anda pilih.

## Keyword yang logis

Jika anda memperhatikan maka anda akan mengerti bahwa menggunakan magic.js tidak membuat anda perlu mempelajari terlalu banyak hal baru, karena kita benar-benar hanya memperkaya arsitektur native.

anda sudah mengenal attrtibute seperti name, style, role, href sekarang tinggal anda menggunakan sedikit penalaran maka anda akan terbiasa dengan penambahan attribute dari magic.js contoh:

```
addname nameadd
parent-style child-style
href-popup href-dialog href-dialog-ajax
```

Jika kita menggunakan istilah dalam bahasa indonesia maka kita akan tau dengan istilah awalan dan akhiran "kata kerja" begitulah dasar kami dalam penambahan attribute, kami mencoba membuat-nya se-logis dan sedekat mungkin denggan keyword sudah ada dan sudah sangat kita kenal.

# Penutup
Perlu anda ketahui, bahwa Senimandigital Framework tidak mengandalkan pengalaman dan keterampilan pengguna untuk merancang aplikasi yang mutakhir tapi lebih mengandalkan berbagai tool Desain Visual, attribute yang mungkin bagi anda terlihat unik, aneh dan tidak standar, sama sekali tidak perlu dihapal.
Karena yang menghapal-nya adalah tool kerja yang anda gunakan, kami menyediakan tool pengembangan khusus untuk menggunakan dan mengembangkan aplikasi menggunakan Senimandigital Framework.

Ada ribuan kode generator didalam tool pengembangan yang kami sediakan, dimana dengan itu memungkinkan anda membangun system informasi dalam waktu kurang dari satu
minggu. Kode generator hebat ini akan kami perkenalkan dengan nama "Backend Behavior" dan "Frontend Behavior".
