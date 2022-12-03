# PRAKTIKUM 7
## Latihan 1

- Ubahlah kode di bawah ini  menjadi menggunakan fungsi lambda 
```
import math

def a(x):
return x**2

def b(x, y):
return math.sqrt(x**2 + y**2)

def c(*args):
return sum(args)/len(args)

def d(s):
return "".join(set(s))
```
![gambar1](gambar/gambargg2.png)

# TUGAS PRAKTIKUM 

- Buat program sederhana dengan menggunakan fungsi yang akan menampilkan daftar nilai mahasiswa, Dengan ketentuan:
- Fungsi - Tambah() untuk menambah data 
- Fungsi - Tampilkan() untuk menampilkn data
- Fungsi - Hapus(nama) untuk menghapus data berdasarkan nama
- Fungsi - Ubah (nama) untuk mengubah data berdasarkan nama
- Buat flowchart dengan penjelasan README.md

# Daftar nilai menggunakan fungsi

- Langkah awal sebelum menggunakan fungsi kita harus membuat dictionary kosong terlebih dahulu 
```
data = {}
```
- Fungsi untuk menambahkan data 
```
def tambah(*t):
    print("Tambah Data")
    nama = input("Nama           : ")
    nim = int(input("NIM            : "))
    uts = int(input("Nilai UTS      : "))
    uas = int(input("Nilai UAS      : "))
    tugas = int(input("Nilai Tugas    : "))
    akhir = tugas*30/100 + uts*35/100 + uas*35/100
    data[nama] = nim, uts, uas, tugas, akhir
    return
```
![gambar1](gambar/gambargg5.png)

- Fungsi untuk menampilan data 
```
def tampilkan(*l):
    if data.items():
        print("="*78)
        print("|                               Daftar Mahasiswa                             |")
        print("="*78)
        print("|No. | Nama            |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
        print("="*78)
        i = 0
        for z in data.items():
            i += 1
            print("| {no:2d} | {0:15s} | {1:15d} | {2:5d} | {3:5d} | {4:7d} | {5:7.2f} |"
                    .format(z[0][:13], z[1][0], z[1][1], z[1][2], z[1][3], z[1][4], no=i))
        print("=" * 78)
    else:
        print("="*78)
        print("|                               Daftar Mahasiswa                             |")
        print("="*78)
        print("|No. | Nama            |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
        print("="*78)
        print("|                                TIDAK ADA DATA                              |")
        print("="*78)
    return
```
![gambar1](gambar/gambargg7.png)

- Fungsi untuk menghapus data berdasarkan nama
```
def hapus(*nama):
    print("Hapus Data")
    nama = input("Masukkan Nama  : ")
    if nama in data.keys():
        del data[nama]
    else:
        print("Nama {0} Tidak Ditemukan".format(nama))
    return
```
![gambar1](gambar/gambargg13.png)

- Fungsi untuk mengubah data berdasarkan nama
```
def ubah(*nama):
    print("Ubah Data")
    nama = input("Masukkan Nama  : ")
    if nama in data.keys():
        nim = int(input("NIM            : "))
        uts = int(input("Nilai UTS      : "))
        uas = int(input("Nilai UAS      : "))
        tugas = int(input("Nilai Tugas    : "))
        akhir = tugas * 30 / 100 + uts * 35 / 100 + uas * 35 / 100
        data[nama] = nim, uts, uas, tugas, akhir
    else:
        print("Nama {0} tidak ditemukan".format(nama))
    return
```
![gambar1](gambar/gambargg11.png)

# FLOWCHART PRAKTIKUM 7

![gambar1](gambar/gambar1.png)
