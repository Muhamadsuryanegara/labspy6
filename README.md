# labspy6
Nama: Muhamad Suryanegara 
TI.21.A.1
312110447

## Latihan 1
- Ubahlah kode dibawah ini menjadi fungsi menggunakan *lambda*

```bash
import math
def a(x):
    return x**2
def b(x, y)
    return math.sqrt(x**2 + y**2)  
def c(*args):
    return sum(args)/len(args)
def d(s):
    return "".join(set(s))
```

### Penjelasan
- Untuk memperluas daftar fungsi matematika gunakan `import math`

- Fungsi lambda yang menggunakan variabel a-d
```baSH
def a(x):
    return x**2
    a = lambda x : x ** 2
print(a(2))
def b(x, y):
    return math.sqrt(x**2 + y**2)
    b = lambda x, y : x ** 2  + y ** 2
print(b(2, 2))
def c(*args):
    return sum(args)/len(args)
    c = lambda *args : sum(args)/len(args)
print(c(5, -1, 8, 19))
def d(s):
    return "".join(set(s))
    d = lambda s: "".join(set(s))
print(d("Jenab"))
```

### Output
![Screenshot (99)](https://user-images.githubusercontent.com/92678339/145719504-2ad0c1c2-4b9a-4889-9e9a-eff03f2f1c0e.png)
![Screenshot (100)](https://user-images.githubusercontent.com/92678339/145719518-916b0ef0-771e-4b2a-bc8e-6982e1ebdd0a.png)

## Praktikum
  Buat program sederhana dengan mengaplikasikan penggunaan fungsi yang akan menampilkan daftar nilai mahasiswa, dengan ketentuan:
 - Fungsi *tambah()* untuk menambah data
 - Fungsi *tampilkan()* untuk menampilkan data
 - Fungsi *hapus(nama)* untuk menghapus data berdasarkan nama
 - Fungsi *ubah(nama)* untuk mengubah data berdasarkan nama
 - Buatlah flowchart dan penjelasan programnya pada README.md

### Penjelasan
  Buatlah dictionary yang akan diinput dengan data
```bash
x = {}
```

  Membuat perulangan dan keterangan untuk pilihan menu
```bash
while True:
    header="PROGRAM INPUT NILAI MAHASISWA"
    print(header.center(97,"="))
    print()
    print("[ (L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar")
    c = input("Masukkan Pilihan: ")
```

- Menambahkan data yang akan diinput kemudian masuk ke dalam dictionary
```bash
if c == 'T' or c == 't':
        print("TAMBAH DATA")
        nim = int(input("Masukkan NIM\t\t: "))
        nama = input("Masukkan Nama\t\t: ")
        tugas = int(input("Masukkan Nilai Tugas\t: "))
        uts = int(input("Masukkan Nilai UTS\t: "))
        uas = int(input("Masukkan Nilai UAS\t: "))
        akhir = tugas*.3 + uts*.35 + uas*.35
        x[nama] = nim, uts, uas, tugas, akhir
```

Output Menambahkan Data


- Jika ingin menampilkan data dapat menggunakan
```py
elif c == 'C' or c == 'c':
        print("CARI DATA")
        nama = input("Masukkan Nama : ")
        if nama in x.keys():
            print("="*73)
            print("|                             Daftar Mahasiswa                          |")
            print("="*73)
            print("| Nama            |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
            print("="*73)
            print("| {0:15s} | {1:15d} | {2:5d} | {3:5d} | {4:7d} | {5:7.2f} |"
                  .format(nama, nim, uts, uas, tugas, akhir))
            print("="*73)
        else:
            print("Nama {0} Tidak Ditemukan".format(nama))

```

Mengubah data dapat menggunakan 
```py
elif c == 'U' or c == 'u':
        print("UBAH DATA")
        print("Cari Data Mahasiswa Menggunakan Nama")
        nama = input("Masukkan Nama Mahasiswa: ")
        if nama in x.keys():
            nim = int(input("Masukkan NIM yang benar\t\t: "))
            tugas = int(input("Masukkan Nilai Tugas yang benar\t: "))
            uts = int(input("Masukkan Nilai UTS yang benar\t: "))
            uas = int(input("Masukkan Nilai UAS yang benar\t: "))
            akhir = tugas*.3 + uts*.35 + uas*.35
            x[nama] = nim, uts, uas, tugas, akhir
        else:
            print("Nama {0} tidak ditemukan".format(nama))
```

- Menghapus data dapat menggunakan
```py
elif c == 'h' or c == 'H':
        print("HAPUS DATA")
        nama = input("Masukkan Nama untuk menghapus: ")
        if nama in x.keys():
            del x[nama]
        else:
            print("Nama {0} Tidak Ditemukan".format(nama))

```

- Mencari data dapat menggunakan
```py
 elif c == 'C' or c == 'c':
        print("CARI DATA")
        nama = input("Masukkan Nama : ")
        if nama in x.keys():
            print("="*73)
            print("|                             Daftar Mahasiswa                          |")
            print("="*73)
            print("| Nama            |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
            print("="*73)
            print("| {0:15s} | {1:15d} | {2:5d} | {3:5d} | {4:7d} | {5:7.2f} |"
                  .format(nama, nim, uts, uas, tugas, akhir))
            print("="*73)
        else:
            print("Nama {0} Tidak Ditemukan".format(nama))
```

- Jika sudah selesai input pilih menu 'K' untuk memberhentikan program
```py
elif c. lower() == 'k':
        break
```
### output
![Screenshot (102)](https://user-images.githubusercontent.com/92678339/145719619-ef075730-e202-4ae4-8c0f-3416d630d46b.png)
![Screenshot (98)](https://user-images.githubusercontent.com/92678339/145718684-097cb381-91af-48e3-b703-a3fd4b0ea286.png)

### flowchart
![png](https://user-images.githubusercontent.com/92736847/145682224-31098e61-3ef2-4f3f-872a-6326e133a49d.png)
