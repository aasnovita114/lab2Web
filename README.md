<table>
  <tr>
    <th colspan="2">DATA MAHASISWA</th>
  </tr>
  <tr>
    <td>Nama</td>
    <td>Aas Novitasari</td>
  </tr>
  <tr>
    <td>NIM</td>
    <td>312210167</td>
  </tr>
  <tr>
    <td>Kelas</td>
    <td>TI.22.A1</td>
  </tr>
</table>

# <p align="center">Praktikum2 : CSS Dasar</p>

# Langkah 1
## Membuat Dokumen HTML
- Buka VS Code dan buat file HTML baru. Setelah itu buat struktur HTML
  
Disini sudah terdapat file Dokumen HTML yang belom terdapat file css nya
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>CSS Dasar</title>
</head>
<body>
<header>
<h1>CSS Internal dan <i>Inline CSS</i></h1>
</header>
<nav>
<a href="lab2_css_dasar.html">CSS Dasar</a>
<a href="lab2_css_eksternal.html">CSS Eksternal</a>
<a href="lab1_tag_dasar.html">HTML Dasar</a>
</nav>
<!-- CSS ID Selector -->
<div id="intro">
<h1>Hello World</h1>
<p>Kami sedang belajar HTML dan CSS dasar, pada mata kuliah <b>Pemrograman
Web</b> di <i>Universitas Pelita Bangsa</i>. Pelajaran pertama yang kami dapat
adalah membuat tampilan web sederhana dalam rangka mengenal tag-tag dasar HTML
dan CSS.</p>
<!-- CSS Class Selector -->
<a class="button btn-primary" href="#intro">Informasi selengkapnya.</a>
</div>
</body>
</html>

- Maka hasilnya akan seperti berikut
![image](https://github.com/aasnovita114/lab2Web/assets/116045324/111fa73c-b19f-408e-9429-1ee744cd68e8)


# Langkah 2

## Mendeklarasikan CSS Internal
```
<head>
<title>CSS Dasar</title>
<style>
body {
font-family:'Open Sans', sans-serif;
}
header {
min-height: 80px;
border-bottom:1px solid #77CCEF;
}
h1 {
font-size: 24px;
color: #0F189F;
text-align: center;
padding: 20px 10px;
}
h1 i {
color:#6d6a6b;
}
</style>
</head>
```

> - Maka hasilnya akan seperti berikut :

![image](https://github.com/aasnovita114/lab2Web/assets/116045324/5ec44057-5fa6-476a-b9c7-bdacd22ed5a2)

### 3. Menambahkan Inline CSS
> - Menambahkan Inline CSS, kemudian tambahkan deklarasi inline CSS pada tag `<p>`
```
<p style="text-align: center; color: #ccd8e4;">
```
> - Maka hasilnya akan seperti berikut :

![image](https://github.com/aasnovita114/lab2Web/assets/116045324/07ee6074-fe30-4d8e-beb2-ca34a80e61f7)

### 4. Membuat CSS Eksternal
> - Membuat CSS Eksternal dengan membuat file baru dengan nama **style_eksternal.css** kemudian buat deklarasi css seperti berikut ini.
```
nav {
background: #20A759;
color:#fff;
padding: 10px;
}
nav a {
color: #fff;
text-decoration: none;
padding:10px 20px;
}
nav .active,
nav a:hover {
background: #0B6B3A;
}
```
> - Kemudian tambahkan <link untuk merujuk File CSS yang telah dibuat pada bagian `<head>`
```
<head>
<!-- menyisipkan css eksternal -->
<link rel="stylesheet" href="style_eksternal.css" type="text/css">
</head>
```
> - Maka hasilnya akan seperti berikut :

![273381998-5f78a0cf-48c6-4342-b203-07c23198b1fc](https://github.com/aasnovita114/lab2Web/assets/116045324/a1e0f1a3-813a-418d-a8d9-a996a96f39d4)


> - CSS ekternal adalah CSS yang file di tempatkan di luar file HTML dengan menambahkan link dalam HTML agar tertaut dengan file CSS

### 5. Menambahkan CSS Selector
> - Selanjutnya menambahkan CSS Selector menggunkan ID dan class Selector pada file **style_eksternal.css** dan menambahkan kode seperti berikut :
```
/* ID Selector */
#intro {
background: #418fb1;
border: 1px solid #099249;
min-height: 100px;
padding: 10px;
}
#intro h1 {
text-align: left;
border: 0;
color: #fff;
}
/* Class Selector */
.button {
padding: 15px 20px;
background: #bebcbd;
color: #fff;
display: inline-block;
margin: 10px;
text-decoration: none;
}
.btn-primary {
background: #E42A42;
}
```
> - Maka hasilnya akan seperti berikut :
![image](https://github.com/aasnovita114/lab2Web/assets/116045324/eb8c4e35-ccaf-4d8a-a138-3d127b29a1f3)

### 6. MeLakukan validasi dokumen css dengan mengakses https://jigsaw.w3.org/css-validator/
![image](https://github.com/aasnovita114/lab2Web/assets/116045324/248b73ae-c937-4260-8478-5de59d48f0ac)
![image](https://github.com/aasnovita114/lab2Web/assets/116045324/58354ae3-90e1-4a46-b5a7-3e96f10b9747)

## Pertanyaan dan Tugas 

1. Lakukan eksperimen dengan mengubah dan menambah properti dan nilai pada kode CSS dengan mengacu pada CSS Cheat Sheet yang diberikan pada file terpisah dari modul ini.
> Jawaban :
![image](https://github.com/aasnovita114/lab2Web/assets/116045324/781727ef-a180-4306-9621-72d6203fdfed)

![image](https://github.com/aasnovita114/lab2Web/assets/116045324/5413dd11-ce7e-4a83-8752-b06d7e6c4cdd)

2. Apa perbedaan pendeklarasian CSS elemen `h1 {...}` dengan `#intro h1 {...}?` berikan penjelasannya!
> Jawaban :

- `h1 {...}` : Deklarasi ini akan merubah semua elemen "h1".

- `#intro h1 {...}` : Deklarasi ini lebih spesifik, maksud nya adalah pendeklarasian yang mengacu kepada pemberian atribut pada elemen "h1" dengan menambahkan id "intro".
  
3. Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada elemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya!
> Jawaban :

![image](https://github.com/aasnovita114/lab2Web/assets/116045324/661ed556-128b-4b0d-974e-78810bb3c599)
4. Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebut terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya!
> Jawaban :

```
( <p id="paragraf-1" class="text-paragraf"> )
```
- Yang terpanggil di browser adalah **ID** karena **ID** bersifat unik berbeda dengan **Class**. **Class** bisa digunakan banyak sementara **ID** hanya tertentu saja itu kenapa **ID** unik dan yang terpanggil di browser adalah **ID**.
![image](https://github.com/aasnovita114/lab2Web/assets/116045324/6fe3c6ee-20ff-4b7a-8367-7fd4617822db)

## Terima kasih ##












