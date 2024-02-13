---
title: Dokumentasi Python (Bahasa Indonesia)
tags: Pemrograman Python
date: 2024-02-13 06:58:00 +08:00
---

![python](https://www.ntuclearninghub.com/documents/51786/4216795/Python-Symbol.png/369e410e-a90f-f887-c2dc-61f7ef761476?t=1679043970578)

### Pendahuluan

Python adalah bahasa pemrograman tingkat tinggi dan terinterpretasi yang populer karena kesederhanaannya dan mudah dibaca. Dokumentasi ini akan memberikan gambaran umum tentang bahasa pemrograman Python, dimulai dari konsep dasar hingga fitur canggih. Baik Anda baru memulai di dunia programmer atau telah memiliki pengalaman, semua konten ini dirancang untuk menjadi panduan bagi Anda.

#### Instalasi Python

Sebelum memulai, pastikan Anda sudah menginstal Python di komputer Anda. Untuk informasi instalasi lebih lanjut, kunjungi website resmi Python: <https://www.python.org/>. Pastikan versi Python yang Anda gunakan sesuai dengan kebutuhan proyek Anda. Selama ini, rekomendasi untuk digunakan adalah Python 3.x.
<!--more-->

#### Cara Menjalankan Kode Python

Setelah Python terinstall, Anda dapat mengetik perintah berikut di terminal atau command prompt untuk melakukan verifikasi instalasi:
```
python --version
```
atau
```csharp
py --version
```
Untuk mengeksekusi script Python, jalankan perintah berikut:
```bash
python nama_file.py
```
atau
```csharp
py nama_file.py
```
Ganti `nama_file.py` dengan nama file script Python yang ingin Anda jalankan.

#### Komentar dan Penafian

Dokumen ini merupakan hasil tugas  saya selaku pelajar ilmu komputer. Semua konten disini dipetik dari referensi resmi sehingga tidak ada plagiasi apapun. Jika terdapat kesalahan ataupun masukan penambahan, silakan hubungi saya di mhmmdriann@gmail.com. Terima kasih.

---

### Bagian 1: Konsep Dasar Python

#### Variabel
Variabel adalah wadah tempat kita menyimpan data. Di Python, variabel didefinisikan dengan cara langsung asignasinya ke suatu nilai. Misalnya:
```python
nama = "John Doe"
umur = 25
tinggi_badan = 170.5
```
Anda bebas menggunakan huruf besar atau kecil, serta karakter spesial (kecuali spasi). Namun, harus diawali oleh huruf atau underscore (_).

#### Tipe Data
Terdapat beberapa tipe data dasar di Python, antara lain:

- **string**: teks yang dicantumkan di dalam tanda petik satu ('') atau tanda petik dua ("")
- **integer**: bilangan bulat tanpa koma
- **float**: bilangan desimal
- **boolean**: nilai benar (True) atau salah (False)
- **list**: koleksi item yang dikelompokkan dalam kurung siku [] dan dipisahkan koma
- **tuple**: koleksi item yang dikelompokkan dalam kurung () dan dipisahkan koma; tidak dapat diubah setelah dideklarasikan
- **dictionary**: koleksi pasangan key-value yang dikelompokkan dalam kurung kurawal {}
- **set**: koleksi item unik yang dipisahkan koma dan dikelompokkan dalam kurung kurawal {}; tidak mempertahankan urutan items

Berikut contoh tiap tipe data:
```python
# string
nama = "John Doe"

# integer
umur = 25

# float
tinggi_badan = 170.5

# boolean
sudah_menikah = False

# list
daftar_buah = ["apel", "mangga", "pisang"]

# tuple
data_diri = ("John Doe", 25, True)

# dictionary
identitas = {
    "nama": "John Doe",
    "umur": 25,
    "status": True
}

# set
hobi = {"renang", "memancing", "main game"}
```
#### Operator
Ada beberapa operator yang dapat digunakan di Python, antara lain:

| Operator | Deskripsi                         | Contoh           | Hasil   |
|----------|------------------------------------|------------------|---------|
| `+`      | Penjumlahan                       | `1 + 2`          | `3`     |
| `-`      | Pengurangan                       | `5 - 4`          | `1`     |
| `*`      | Perkalian                         | `6 * 8`          | `48`    |
| `/`      | Pembagian                         | `9 / 4`          | `2.25`  |
| `//`     | Pembulatan bagi kebilangan terdekat| `11 // 4`        | `2`     |
| `%`      | Modulus                            | `12 % 5`         | `2`     |
| `**`     | Eksponensial                      | `2 ** 3`         | `8`     |
| `==`     | Sama dengan                       | `5 == 5`         | `True`  |
| `!=`     | Tidak sama dengan                | `5 != 4`         | `True`  |
| `<`      | Kurang dari                       | `3 < 4`          | `True`  |
| `>`      | Lebih dari                         | `6 > 3`          | `True`  |
| `<=`     | Kurang dari sama dengan          | `4 <= 4`         | `True`  |
| `>=`     | Lebih dari sama dengan           | `10 >= 9`        | `True`  |
| `and`    | Logika AND                         | `True and False`  | `False` |
| `or`     | Logika OR                          | `True or False`  | `True`  |
| `not`    | Negasi logika                      | `not True`       | `False` |

#### Input dan Output
Untuk menerima input dari user, gunakan fungsi `input()`. Berikut contoh input dan output:
```python
print("Masukkan nama Anda: ")
nama = input() # User mengetik "John Doe"
print(f"Halo, {nama}")
```
Hasil:
```arduino
Masukkan nama Anda: John Doe
Halo, John Doe
```
Jika Anda ingin menerima input numerik, perlu dilakukan casting ke tipe data yang diinginkan. Contoh:
```python
print("Masukkan usia Anda: ")
umur = int(input()) # User mengetik "25"
print(f"Usia Anda adalah {umur} tahun.")
```
Hasil:
```arduino
Masukkan usia Anda: 25
Usia Anda adalah 25 tahun.
```
#### Kontrol Aliran
Di Python, terdapat beberapa struktur kontrol aliran, antara lain:

- If else statement
- For loop
- While loop

##### If Else Statement
Struktur if else statement mirip dengan bahasa pemrograman lainnya. Berikut contoh if else statement:
```python
nilai = 85
if nilai >= 80:
    print("Nilai Anda A")
elif nilai >= 70:
    print("Nilai Anda B")
else:
    print("Nilai Anda C")
```
Hasil:
```makefile
Nilai Anda A
```
##### For Loop
For loop digunakan untuk iterasi atau melakukan perulangan sesuai dengan rentang atau koleksi items. Berikut contoh for loop:
```python
for i in range(5):
    print(i)
```
Hasil:
```csharp
0
1
2
3
4
```
##### While Loop
While loop digunakan untuk melakukan perulangan selama kondisi tertentu true. Berikut contoh while loop:
```go
i = 0
while i < 5:
    print(i)
    i += 1
```
Hasil:
```csharp
0
1
2
3
4
```
---

### Bagian 2: Fungsionalitas Lanjutan Python

#### Fungsi
Fungsi adalah blok kode yang dapat digunakan berulang kali. Functions didefinisikan dengan keyword `def`, followed by function name, parentheses `()`, dan colon `:`. Arguments dituliskan didalam parentheses. Berikut contoh definisi fungsi:
```python
def hitung_luas_persegi(sisi):
    luas = sisi * sisi
    return luas
```
Untuk memanggil fungsi, cukup tuliskan nama fungsinya, lalu ikuti dengan parameter yang sesuai. Contoh:
```python
hasil = hitung_luas_persegi(5)
print(f"Luas persegi dengan sisi 5 adalah {hasil}")
```
Hasil:
```makefile
Luas persegi dengan sisi 5 adalah 25
```
#### Class Dan Objek
Python merupakan bahasa pemograman objek oriented. Setiap class merepresentasikan template untuk membuat object. Object sendiri mewakili instance dari class. Sebelum membuat class, mari kita pelajari attribute dan method.

Method adalah fungsi yang terhubung dengan class. Mari lihat contoh class, attribut, dan method:

```python
class Mahasiswa:
    universitas = 'Universitas XYZ' # Attribut class

    def __init__(self, nama, npm): # Method constructor
        self.nama = nama # Atribute instance
        self.npm = npm

    def cetak_info(self): # Method
        print(f'Nama: {self.nama}, NPM: {self.npm}')

mahasiswa1 = Mahasiswa('John Doe', '12345678')
mahasiswa1.cetak_info()
```
Hasil:
```vbnet
Nama: John Doe, NPM: 12345678
```
Dalam contoh di atas, `Mahasiswa` adalah class, `universitas`, `nama`, dan `npm` adalah attribut, sedangkan `__init__` dan `cetak_info` adalah method.

#### Exception Handling
Exception handling adalah teknik untuk mengatur hal-hal yang tidak diinginkan saat eksekusi program. Dalam Python, exception handlings didefinisikan dengan `try` dan `except`. Berikut contoh exception handling:

```python
try:
    x = 10 / 0
except ZeroDivisionError as e:
    print(f'Terjadi error: {e}')

try:
    with open('file.txt', 'r') as f:
        content = f.read()
except FileNotFoundError as e:
    print(f'File tidak ditemukan: {e}')
```
Hasil:
```makefile
Terjadi error: division by zero
File tidak ditemukan: [Errno 2] No such file or directory: 'file.txt'
```
Dalam contoh di atas, kami mencoba melakukan bagi nol dan membaca file yang tidak ada. Hal ini akan menghasilkan exception. Namun, dengan menggunakan except, kita bisa menangani exception tersebut.

#### Mengimpor Modul
Modul adalah file Python yang berisi kode yang dapat digunakan lagi di file lain. Untuk mengimport modul, gunakan perintah `import`. Berikut contoh import modul:

```python
# Import modul math
import math

# Gunakan fungsi pi dari modul math
pi = math.pi

# Gunakan fungsi sqrt dari modul math
hasil = math.sqrt(16)

print(f'Pi: {pi}')
print(f'Akar Kuadrat dari 16: {hasil}')
```
Hasil:
```yaml
Pi: 3.141592653589793
Akar Kuadrat dari 16: 4.0
```
Kita juga dapat menggunakan perintah `from ... import ...` untuk mengimpor fungsi atau variable tertentu. Contoh:

```python
# Import fungsi sqrt dari modul math
from math import sqrt

# Gunakan fungsi sqrt
hasil = sqrt(25)

print(f'Akar Kuadrat dari 25: {hasil}')
```
Hasil:
```csharp
Akar Kuadrat dari 25: 5.0
```
#### Generator
Generator adalah fungsi yang bereturn value secara dinamis. Saat generator dieksekusi, ia akan membuat objek generator yang dapat digunakan untuk mendapatkan nilai berikutnya. Berikut contoh generator:

```python
def fibonacci():
    a, b = 0, 1
    yield a
    while True:
        a, b = b, a + b
        yield b

gen_fibo = fibonacci()

for i in range(10):
    next(gen_fibo)
```
Hasil:
```go
0
1
1
2
3
5
8
13
21
34
```
Dalam contoh di atas, kami mendefinisikan fungsi genertor `fibonacci` yang bereturn angka Fibonacci. Setelah itu, kami membuat objek generator `gen\_fibo` dengan menggunakan perintah `next(gen\_fibo)` kami dapat mendapatkan nilai berikutnya.

---

### Bagian 3: Framework & Library Python

#### Flask
Flask adalah framework micro web server written in Python. Flask memungkinkan kita untuk membuat aplikasi web ringan dan fleksibel. Untuk memulai project Flask, install terlebih dahulu Flask menggunakan pip:

```shell
$ pip install flask
```
Buat file app.py dan tambahkan kode berikut:

```python
from flask import Flask, render_template
app = Flask(__name__)

@app.route('/')
def home():
    return render_template('home.html')

if __name__ == '__main__':
    app.run()
```
Buat folder templates dan tambahkan file home.html:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Halaman Utama</title>
</head>
<body>
    <h1>Selamat Datang Ke Website Kami!</h1>
</body>
</html>
```
Jalankan aplikasi Flask dengan perintah berikut:

```shell
$ export FLASK_APP=app.py
$ flask run
```
Hasil:
```csharp
 * Debugger is active!
 * Debugger PIN: XXXX-XXXX-XXXX
 * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
```
Klik link http://127.0.0.1:5000/ untuk melihat hasil.

#### Scrapy
Scrapy adalah framework crawler dan scraping yang ditulis dalam bahasa pemrogaman Python. Scrapy diciptakan untuk mengumpulkan data dari internet. Untuk mulai menggunakan Scrapy, install terlebih dahulu Scrapy menggunakan pip:

```shell
$ pip install scrapy
```
Buat folder project Scrapy dan jalankan perintah berikut:

```shell
$ cd myproject
$ scrapy startproject myspider
```
Buat folder spiders dan buat file spider.py:

```python
import scrapy
from ..items import MyItem

class SpiderClass(scrapy.Spider):
    name = 'myspider'
    allowed_domains = ['example.com']
    start_urls = ['http://www.example.com']

    def parse(self, response):
        myitem = MyItem()
        myitem['judul'] = response.css('.title::text').extract()
        myitem['deskripsi'] = response.css('.description::text').extract()
        yield myitem
```
Buat file items.py:

```python
import scrapy

class MyItem(scrapy.Item):
    judul = scrapy.Field()
    deskripsi = scrapy.Field()
```
Jalankan spider dengan perintah berikut:

```shell
$ scrapy crawl myspider
```
Hasil:
```markdown
...
[scrapy.core.engine] DEBUG: Crawled (200) <GET https://www.example.com> (referer: None)
[scrapy.core.scraper] DEBUG: Scraped from <200 https://www.example.com>
{'judul': ['Contoh Judul'], 'deskripsi': ['Contoh Deskripsi']}
...
```
Data yang telah di-scraping akan tersimpan dalam bentuk JSON.

#### Pandas
Pandas adalah library data analisis yang sangat populer dalam bahasa pemrograman Python. Pandas memungkinkan kita untuk melakukan operasi dataframe dan seri. Install terlebih dahulu Pandas menggunakan pip:

```shell
$ pip install pandas
```
Buat file main.py dan tambahkan kode berikut:

```python
import pandas as pd

data = {'Nama': ['John', 'Anna', 'Peter'],
        'Umur': [25, 22, 28],
        'Negara': ['Amerika Serikat', 'Finlandia', 'Inggris']}
df = pd.DataFrame(data)

print(df)
```
Hasil:
```lua
    Nama  Umur         Negara
0   John   25  Amerika Serikat
1   Anna   22       Finlandia
2 Peter   28         Inggris
```
Dalam contoh di atas, kami membuat data frame dari dictionary `data`. Kemudian, kami mencetak data frame tersebut menggunakan metode `print()`.

---

### Referensi

1. Python Software Foundation. (2021). Welcome to Python.org. Retrieved March 15, 2023, from <https://docs.python.org/3/tutorial/index.html>
2. Real Python. (2021). Real Python - Learn Python Programming. Retrieved March 15, 2023, from <https://realpython.com/>
3. Flask Documentation. (2021). Flask Web Development — The Full-Stack Web Developer’s Guide to Developing Web Applications Using Python — Scott Wingo 2nd Edition. Retrieved March 15, 2023, from <https://flask.palletsprojects.com/en/2.1.x/>
4. Scrapy Tutorial. (2021). Official Scrapy Tutorial. Retrieved March 15, 2023, from <https://doc.scrapy.org/en/latest/intro/tutorial.html>
5. McKinney, Wes. (2018). Python for Data Analysis: Data Wrangling with Pandas, NumPy, and IPython. O'Reilly Media. ISBN: 978-1-491-95766-0. Retrieved March 15, 2023, from <https://pandas.pydata.org/pandas-docs/stable/>