# Pertemuan 06 Nested Loop Python

**Nama:** Maspupatul Hasanah  
**NIM:** 2225250050  
**Kelas:** 3A  
**Mata Kuliah:** Algoritma dan Pemrograman  

## Tujuan

Pada Pertemuan 06, saya mempelajari penggunaan **nested loop** dalam Python untuk membentuk pola, mengolah pasangan data, melakukan akumulasi, dan pencacahan. Selain itu, saya mempraktikkan cara menjalankan serta menguji program menggunakan VS Code dan mengunggah hasil pekerjaan melalui GitHub.

Materi yang dipelajari meliputi:
- Nested loop
- Pola baris dan kolom
- Akumulasi
- Pencacahan dengan kondisi
- Tracing dua variabel kontrol
- Debugging nested loop
- Git dan GitHub

## Struktur Folder

```text
pertemuan-06-nested-loop-2225250050/
│
├── README.md
├── .gitignore
│
├── latihan/
│   ├── 01_pasangan_indeks.py
│   ├── 02_pola_segitiga.py
│   ├── 03_jumlah_per_baris.py
│   └── 04_hitung_pasangan.py
│
└── tugas/
    └── tabel_perkalian_dan_statistik.py
```

## Konsep Nested Loop

Nested loop adalah perulangan yang berada di dalam perulangan lainnya. Loop luar digunakan untuk mengatur kelompok atau baris, sedangkan loop dalam digunakan untuk memproses elemen pada setiap kelompok.

Contoh:

```python
for i in range(1, 4):
    for j in range(1, 3):
        print(i, j)
```

Jika loop luar berjalan sebanyak `m` kali dan loop dalam berjalan sebanyak `n` kali untuk setiap iterasi loop luar, maka badan loop dalam dijalankan sebanyak:

```text
m × n
```

## Latihan

### 1. Pasangan Indeks

Program `01_pasangan_indeks.py` digunakan untuk menampilkan seluruh pasangan `(i, j)` dengan:

- `i = 1 sampai 3`
- `j = 1 sampai 4`

Program juga menggunakan counter untuk menghitung banyak pasangan yang dihasilkan.

Hasil yang diharapkan:

```text
Banyak pasangan = 12
```

### 2. Pola Segitiga

Program `02_pola_segitiga.py` menerima nilai `n` dan menghasilkan pola bintang dengan jumlah simbol yang bertambah pada setiap baris.

Contoh untuk `n = 5`:

```text
*
* *
* * *
* * * *
* * * * *
```

### 3. Jumlah Per Baris

Program `03_jumlah_per_baris.py` menghitung nilai `i × j` untuk `i = 1 sampai 4` dan `j = 1 sampai 3`, kemudian menghitung jumlah setiap baris.

Hasil yang diharapkan:

```text
Jumlah baris 1 = 6
Jumlah baris 2 = 12
Jumlah baris 3 = 18
Jumlah baris 4 = 24
```

Pada program ini, `total_baris` diinisialisasi kembali pada setiap iterasi loop luar agar jumlah yang diperoleh merupakan jumlah untuk masing-masing baris.

### 4. Menghitung Pasangan

Program `04_hitung_pasangan.py` menghitung banyak pasangan `(i, j)` untuk `i` dan `j` dari `1 sampai n` yang memenuhi kondisi:

```text
i + j <= n
```

Program diuji menggunakan beberapa nilai `n`, yaitu:

- `n = 2`
- `n = 3`
- `n = 5`

## Tugas 3: Tabel Perkalian dan Statistik

File:

```text
tugas/tabel_perkalian_dan_statistik.py
```

Program menerima bilangan bulat positif `n` dan menggunakan nested loop untuk membuat tabel perkalian dari `1 sampai n`.

Program melakukan beberapa proses, yaitu:

1. Memvalidasi input `n`.
2. Membuat tabel perkalian `n × n`.
3. Menghitung jumlah setiap baris.
4. Menghitung total seluruh hasil perkalian.
5. Menghitung banyak hasil perkalian yang genap.

### Algoritma

1. Membaca nilai `n`.
2. Jika `n <= 0`, meminta input kembali sampai mendapatkan nilai positif.
3. Menginisialisasi `total_semua = 0`.
4. Menginisialisasi `count_genap = 0`.
5. Melakukan perulangan `i` dari `1 sampai n`.
6. Menginisialisasi `total_baris = 0` pada setiap baris.
7. Melakukan perulangan `j` dari `1 sampai n`.
8. Menghitung `hasil = i * j`.
9. Menambahkan `hasil` ke `total_baris`.
10. Menambahkan `hasil` ke `total_semua`.
11. Jika `hasil` genap, menambah `count_genap`.
12. Setelah loop dalam selesai, menampilkan jumlah baris.
13. Setelah seluruh loop selesai, menampilkan total keseluruhan dan banyak hasil genap.

## Cara Menjalankan

Pastikan berada pada folder utama repository, kemudian jalankan program dengan perintah:

```bash
python tugas/tabel_perkalian_dan_statistik.py
```

Untuk menjalankan latihan, contohnya:

```bash
python latihan/01_pasangan_indeks.py
```

atau:

```bash
python latihan/02_pola_segitiga.py
```

## Hasil Pengujian

### Tugas 3

| Input `n` | Jumlah Pasangan | Total Semua | Banyak Hasil Genap |
|---|---:|---:|---:|
| 1 | 1 | 1 | 0 |
| 2 | 4 | 9 | 3 |
| 3 | 9 | 36 | 5 |

Hasil program dibandingkan dengan hasil perhitungan manual untuk memastikan bahwa nested loop, akumulasi, dan pencacahan telah berjalan dengan benar.

## Analisis Efisiensi

Pada Tugas 3, loop luar berjalan sebanyak `n` kali dan loop dalam juga berjalan sebanyak `n` kali untuk setiap iterasi loop luar.

Dengan demikian, pernyataan:

```python
hasil = i * j
```

dieksekusi sebanyak:

```text
n × n = n²
```

kali.

Contohnya:

- `n = 1` → `1² = 1` kali
- `n = 2` → `2² = 4` kali
- `n = 3` → `3² = 9` kali

Semakin besar nilai `n`, semakin banyak iterasi yang dilakukan oleh nested loop.

## Refleksi

Pada pertemuan ini saya memahami bahwa nested loop digunakan ketika suatu proses membutuhkan lebih dari satu tingkat perulangan. Saya juga memahami bahwa posisi inisialisasi akumulator sangat penting.

`total_baris` harus diinisialisasi di dalam loop luar karena nilainya harus kembali menjadi `0` pada setiap baris. Sementara itu, `total_semua` harus diinisialisasi sebelum kedua loop karena digunakan untuk menghitung keseluruhan hasil perkalian.

Saya juga belajar menggunakan counter untuk menghitung banyak data yang memenuhi kondisi tertentu. Selain itu, tracing nilai `i` dan `j` membantu dalam memahami urutan eksekusi dan menemukan kesalahan pada nested loop.

Kesalahan yang perlu diperhatikan adalah kesalahan indentasi, kesalahan batas `range`, serta kesalahan dalam menentukan lokasi inisialisasi akumulator atau counter.

## Git dan GitHub

Perubahan program dikelola menggunakan Git dan diunggah ke GitHub menggunakan `push`.

Beberapa commit yang digunakan:

```bash
git add latihan
git commit -m "feat: menyelesaikan latihan pola dan nested loop"

git add tugas/tabel_perkalian_dan_statistik.py
git commit -m "feat: menyelesaikan tugas 3 akumulasi dan pencacahan"

git add README.md
git commit -m "docs: menambahkan hasil uji analisis dan refleksi"

git push
```

Repository digunakan untuk menyimpan kode program, dokumentasi, hasil pengujian, dan riwayat perkembangan pekerjaan.

## Kesimpulan

Pertemuan 06 memberikan pemahaman tentang penggunaan nested loop dalam Python. Nested loop dapat digunakan untuk membentuk pola, menghasilkan pasangan data, menghitung akumulasi per baris maupun keseluruhan, serta melakukan pencacahan berdasarkan kondisi.

Melalui latihan dan Tugas 3, saya dapat memahami hubungan antara loop luar dan loop dalam, melakukan tracing, menguji program dengan beberapa test case, serta mengelola hasil pekerjaan menggunakan Git dan GitHub.