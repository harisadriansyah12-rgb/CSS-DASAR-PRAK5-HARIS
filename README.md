---

# 🌐 Praktikum 5: Javascript

---

**Mata Kuliah:** Pemrograman Web1

**Dosen Pengampu:** Agung Nugroho, S.Kom., M.Kom.

**Nama:** haris adriansyah

**NIM:** 312410286

**Kelas:** TI.2A.A.4

---

# Praktikum 5 – JavaScript

## Tujuan

Mempelajari dasar pemrograman JavaScript, meliputi cara menulis script di dalam HTML, penggunaan alert, prompt, function, operator aritmatika, kondisi, perulangan, serta manipulasi elemen form dan HTML DOM.

---

## 1. Pengenalan JavaScript

Contoh penggunaan **document.write** dan **console.log** untuk menampilkan teks di halaman dan di konsol.

```html
<!DOCTYPE html>
<html>
<head>
    <title>Mengenal JavaScript</title>
</head>
<body>
    <h1>Pengenalan JavaScript</h1>
    <p>Contoh document.write dan console.log</p>

    <script>
        document.write("Hello World<br>");
        console.log("hello world");
    </script>
</body>
</html>
```

**Penjelasan:**

* `document.write()` menulis teks langsung ke halaman web.
* `console.log()` menampilkan teks ke konsol (bisa dilihat lewat Inspect → Console).

---

## 2. JavaScript Dasar

### a. Pemakaian Alert sebagai Property Window

```html
<html>
<head>
    <title>alert box</title>
</head>
<body>
<script language="javascript">
<!--
    window.alert("ini merupakan pesan untuk anda");
//-->
</script>
</body>
</html>
```

**Penjelasan:**
Menampilkan pesan ke pengguna melalui pop-up alert box.

---

### b. Pemakaian Method dalam Objek

```html
<html>
<head>
    <title>skrip javascript</title>
</head>
<body>
    percobaan memakai javascript:<br>
<script language="javascript">
<!--
    document.write("selamat mencoba javascript<br>");
    document.write("semoga sukses!");
//-->
</script>
</body>
</html>
```

**Penjelasan:**

* `document.write()` digunakan untuk menulis teks secara langsung di halaman web.
* Teks dapat digabung dengan tag HTML seperti `<br>` untuk ganti baris.

---

### c. Pemakaian Prompt

```html
<html>
<head>
    <title>pemasukan data</title>
</head>
<body>
<script language="javascript">
<!--
    var nama = prompt("siapa nama anda?", "masukkan nama anda");
    document.write("hai, " + nama);
//-->
</script>
</body>
</html>
```

**Penjelasan:**
`prompt()` meminta input teks dari pengguna, lalu hasilnya ditampilkan dengan `document.write()`.

---

### d. Pembuatan Fungsi dan Cara Pemanggilannya

```html
<html>
<head>
    <title>contoh program javascript</title>
<script language="javascript">
    function pesan() {
        alert("memanggil javascript lewat body onload");
    }
</script>
</head>
<body onload=pesan()>
</body>
</html>
```

**Penjelasan:**
Fungsi `pesan()` akan dijalankan otomatis saat halaman dimuat (`onload`).

---

## 3. Dasar Pemrograman di JavaScript

### a. Operasi Dasar Aritmatika

```html
<html>
<head>
    <title>contoh program javascript</title>
<script language="javascript">
    function test(val1, val2) {
        document.write("<br>perkalian : val1*val2 = " + val1 * val2 + "<br>");
        document.write("pembagian : val1/val2 = " + val1 / val2 + "<br>");
        document.write("penjumlahan : val1+val2 = " + (val1 + val2) + "<br>");
        document.write("pengurangan : val1-val2 = " + (val1 - val2) + "<br>");
        document.write("modulus : val1%val2 = " + (val1 % val2) + "<br>");
    }
</script>
</head>
<body>
    <input type="button" name="button1" value="arithmetic" onclick="test(9,4)">
</body>
</html>
```

**Penjelasan:**
Menampilkan hasil operasi aritmatika sederhana menggunakan dua nilai (`9` dan `4`).

---

### b. Seleksi Kondisi (if...else)

```html
<html>
<head>
    <title>contoh if-else</title>
</head>
<body>
<script language="javascript">
<!--
    var nilai = prompt("nilai (0-100): ", 0);
    var hasil = "";
    if (nilai >= 60)
        hasil = "lulus";
    else
        hasil = "tidak lulus";
    document.write("hasil: " + hasil);
//-->
</script>
</body>
</html>
```

**Penjelasan:**
Membandingkan nilai input pengguna dan menampilkan hasil lulus atau tidak lulus.

---

### c. Penggunaan Operator Switch untuk Seleksi Kondisi

```html
<html>
<head>
    <title>contoh program javascript</title>
<script language="javascript">
    function test() {
        val = window.prompt("input nilai (1-5):");
        switch (val) {
            case "1": document.write("bilangan satu"); break;
            case "2": document.write("bilangan dua"); break;
            case "3": document.write("bilangan tiga"); break;
            case "4": document.write("bilangan empat"); break;
            case "5": document.write("bilangan lima"); break;
            default: document.write("bilangan lainnya");
        }
    }
</script>
</head>
<body>
    <input type="button" name="button1" value="switch" onclick="test()">
</body>
</html>
```

**Penjelasan:**
`switch` digunakan untuk menyeleksi kondisi berdasarkan nilai tertentu.

---

## 4. Pembuatan Form

### a. Form Input

```html
<html>
<head>
<script language="javascript">
    function test() {
        var val1 = document.kirim.T1.value;
        if (val1 % 2 == 0)
            document.kirim.T2.value = "bilangan genap";
        else
            document.kirim.T2.value = "bilangan ganjil";
    }
</script>
</head>
<body>
<form method="POST" name="kirim">
    <p>BIL <input type="text" name="T1" size="20"></p>
    <p>MERUPAKAN BIL <input type="text" name="T2" size="20"></p>
    <p><input type="button" value="TEBAK" name="B1" onclick="test()"></p>
</form>
</body>
</html>
```

**Penjelasan:**
Script mengambil nilai input dari `T1`, mengecek apakah bilangan genap atau ganjil, lalu menampilkan hasil di `T2`.

---

### b. Form Button

```html
<html>
<head>
    <title>objek document</title>
<script language="javascript">
<!--
    function ubahWarnaLB(warna) {
        document.bgColor = warna;
    }
    function ubahWarnaLD(warna) {
        document.fgColor = warna;
    }
//-->
</script>
</head>
<body>
<input type="button" value="Latar Belakang Hijau" onClick="ubahWarnaLB('GREEN')">
<input type="button" value="Latar Belakang Putih" onClick="ubahWarnaLB('WHITE')">
<input type="button" value="Teks Kuning" onClick="ubahWarnaLD('YELLOW')">
<input type="button" value="Teks Biru" onClick="ubahWarnaLD('BLUE')">

<script language="javascript">
    document.write("Dimodifikasi terakhir pada " + document.lastModified);
</script>
</body>
</html>
```

**Penjelasan:**

* Mengubah warna latar belakang (`bgColor`) dan warna teks (`fgColor`).
* `document.lastModified` menampilkan tanggal terakhir file diubah.

---

## 5. HTML DOM

### Pilihan Menggunakan CheckBox dengan Perhitungan Otomatis

```html
<html>
<head>
    <title>Daftar Menu</title>
<script>
function hitung(ele) {
    total = document.getElementById('total').value;
    total = (total ? parseInt(total) : 0);
    var harga = 0;

    if (ele.checked)
        harga = ele.value;
    else
        harga = -ele.value;

    total += parseInt(harga);
    document.getElementById('total').value = total;
}
</script>
</head>
<body>
<h1>Daftar Menu Makanan</h1>
<label><input type="checkbox" value="5000" id="menu1" onclick="hitung(this);"> Ayam Goreng Rp. 5.000</label><br>
<label><input type="checkbox" value="500" id="menu2" onclick="hitung(this);"> Tempe Goreng Rp. 500</label><br>
<label><input type="checkbox" value="2500" id="menu3" onclick="hitung(this);"> Telur Dadar Rp. 2.500</label><br>
<strong>Total Bayar: Rp. <input id="total" type="text" /></strong>
</body>
</html>
```

**Penjelasan:**

* Menggunakan `getElementById()` untuk mengakses elemen input berdasarkan ID-nya.
* Setiap kali checkbox diklik, fungsi `hitung()` akan menambah atau mengurangi total harga sesuai pilihan pengguna.

---

Oke, berikut README untuk **bagian “Pertanyaan dan Tugas” serta “Laporan Praktikum”** dari **materi Lab5Web**, dibuat rapi dan sesuai format laporan GitHub — **tidak digabung dengan README sebelumnya**, jadi bisa kamu pakai langsung di repo baru `Lab5Web`.

---

# **Praktikum 5 - JavaScript**

## **Pertanyaan dan Tugas**

### **1. Buat script untuk melakukan validasi pada isian form**

Berikut contoh implementasi validasi form menggunakan JavaScript.
Validasi dilakukan untuk memastikan semua input telah diisi dan format email sesuai.

#### **Kode Program (`form_validasi.html`):**

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <title>Validasi Form</title>
    <script>
        function validasiForm() {
            var nama = document.forms["formData"]["nama"].value;
            var email = document.forms["formData"]["email"].value;
            var password = document.forms["formData"]["password"].value;

            if (nama == "" || email == "" || password == "") {
                alert("Semua field wajib diisi!");
                return false;
            }

            var polaEmail = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            if (!polaEmail.test(email)) {
                alert("Format email tidak valid!");
                return false;
            }

            alert("Data berhasil dikirim!");
            return true;
        }
    </script>
</head>
<body>
    <h2>Form Pendaftaran</h2>
    <form name="formData" onsubmit="return validasiForm()">
        <p>Nama: <input type="text" name="nama"></p>
        <p>Email: <input type="text" name="email"></p>
        <p>Password: <input type="password" name="password"></p>
        <input type="submit" value="Kirim">
    </form>
</body>
</html>
```

#### **Penjelasan:**

1. **Input validation:**
   Script mengecek apakah semua input (nama, email, password) sudah diisi.
2. **Email format check:**
   Menggunakan pola regex `/^[^\s@]+@[^\s@]+\.[^\s@]+$/` untuk memeriksa format email.
3. **Alert messages:**

   * Jika ada field kosong → muncul alert *“Semua field wajib diisi!”*
   * Jika format email salah → muncul alert *“Format email tidak valid!”*
   * Jika semua benar → muncul alert *“Data berhasil dikirim!”*

#### **Hasil Tampilan di Browser:**

Form akan menampilkan 3 field (Nama, Email, Password) dan tombol **Kirim**.
Saat tombol ditekan, JavaScript akan menampilkan alert sesuai kondisi input.

---

<img width="1526" height="467" alt="Screenshot 2025-10-24 102956" src="https://github.com/user-attachments/assets/ecf45bf6-1b71-4b01-8be4-24513612d534" />


---

### **Kesimpulan:**

Melalui praktikum ini, mahasiswa dapat memahami dasar-dasar JavaScript meliputi:

* Penulisan kode JavaScript di dalam HTML
* Penggunaan fungsi `alert()`, `prompt()`, `document.write()`, `if`, `switch`, `function`
* Validasi form input menggunakan JavaScript
* Menampilkan hasil di browser dan console

---
