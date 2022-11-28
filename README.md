# Pratikum-5

# PENJELASAN PRATIKUM 5 " PROGRAM INPUT NILAI "

Penjelasan

1.Mendeklarasikan Dictonary kosong dengan synatax data = {}
2.Lalu membuat perulangan while dan untuk menginisialkan penambahan menu pilihan Tambah, Ubah, Hapus, Cari, Lihat, dan Keluar :

      while True:
    x = input("(T)ambah, (U)bah, (H)apus, (C)ari, (L)ihat, (K)eluar: ")

3.Menambahkan Data
Berikut adalah Syntax untuk menambahkan data dengan ketentuan jika kita mengetikkan T pada keyboard, maka akan melakukan penambahan data dan ditampung kedalam Dictonary data yang telah kita buat, dengan nama sebagai keys dan yang lainnya sbagai values.

    if x.lower() == 't':
        print("Tambah Data")
        nama = input("Nama           : ")
        nim = int(input("NIM            : "))
        uts = int(input("Nilai UTS      : "))
        uas = int(input("Nilai UAS      : "))
        tugas = int(input("Nilai Tugas    : "))
        n_akhir = tugas * 0.30 + uts * 0.35 + uas * 0.35
        data[nama] = nim, uts, uas, tugas, n_akhir

4.Mengubah Data

Jika input yang dimasukkan adalah U, di dalam kondisi ini terdapat input dan kondisi, dimana jika input nama ada didalam variabel data maka akan muncul beberapa pilihan untuk mengubah semua data atau data tertentu saja.

      elif x.lower() == 'u':
    print("Ubah Data")
    nama = input("Masukkan Nama   : ")
    if nama in data.keys():
        nim = int(input("NIM            : "))
        uts = int(input("Nilai UTS      : "))
        uas = int(input("Nilai UAS      : "))
        tugas = int(input("Nilai Tugas    : "))
        n_akhir = tugas*0.30 + uts*0.35 + uas*0.35
        data[nama] = nim, uts, uas, tugas, n_akhir
    else:
        print("Nama{0} Tidak Ditemukan".format(nama))

5.Menghapus Data

Sama seperti mengubah data yang dipilih.
Data yang dihapus adalah data yang di input dalam variabel nama dimana berisi (string) yang mewakili NIM, Nilai Tugas, UTS, UAS.

    elif x.lower() == 'h':
        print("Hapus Data")
        nama = input("Masukkan Nama  : ")
        if nama in data.keys():
            del data[nama]
        else:
            print("Nama {0} Tidak Ditemukan".format(nama))

6.Mencari Data

Perbandingan untuk mencari data yang akan diubah sama seperti cara mengubah data, hanya saja perintah ini digunakan untuk menampilkan data yang di input berdasarkan nama. Berikut kode yang digunakan.

      elif x.lower() == 'c':
    print("Cari Data")
    nama = input("Masukkan Nama : ")
    if nama in data.keys():
        print("=" * 73)
        print(
            "|                             Daftar Mahasiswa                          |")
        print("=" * 73)
        print(
            "| Nama            |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
        print("=" * 73)
        print("| {0:15s} | {1:15d} | {2:5d} | {3:5d} | {4:7d} | {5:7.2f} |"
              .format(nama, nim, uts, uas, tugas, n_akhir))
        print("=" * 73)
    else:
        print("Nama {0} Tidak Ditemukan".format(nama))

7.Melihat Data

Selanjutnya adalah kode yang digunakan untuk melihat input yang sudah dimasukkan.
Data dalam perulangan for di ambil dari variabel Dictionary data pada bagian value yang berbntuk list. variabel i = 0 digunakan untuk membuat nomer. Data yang akan ditambilkan adalah Nama, NIM, Nilai Tugas, UTS, UAS dan Nilai Akhir

      elif x.lower() == 'l':
    if data.items():
        print("=" * 78)
        print(
            "|                               Daftar Mahasiswa                             |")
        print("=" * 78)
        print(
            "|No. | Nama            |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
        print("=" * 78)
        i = 0
        for y in data.items():
            i += 1
            print("| {no:2d} | {0:15s} | {1:15d} | {2:5d} | {3:5d} | {4:7d} | {5:7.2f} |"
                  .format(y[0][:13], y[1][0], y[1][1], y[1][2], y[1][3], y[1][4], no=i))
            print("=" * 78)
    else:
        print("=" * 78)
        print(
            "|                               Daftar Mahasiswa                             |")
        print("=" * 78)
        print(
            "|No. | Nama            |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
        print("=" * 78)
        print(
            "|                                TIDAK ADA DATA                              |")
        print("=" * 78)

8.Keluar

Perulangan diatas adalah perulangan yang akan berjalan terus menerus dan akan berhenti jika kode berikut di eksekusi elif x.lower() == 'k':

A. Jika k di input dan lower() digunakan untuk mengkonversi input yang dimasukkan ke bentuk lower case dan input k digunakan berdasarkan perintah yang sudah dimasukan dalam keterangan pada fungsi input dibawah ini:

    elif x.lower() == 'k':
        break

    else:
        print("Pilih Menu Yang Tersedia")

B.Hasil Output
Apabila program dijalankan maka akan menghasilkan output sebagai berikut : 

- Diawali dengan langkah input : 
T ( untuk langkah Tambah) dan seterusnya.


   <img src="Program input Nilai.png">

# Dan berikut adalah tampilan dari flowchartnya :

   <img src="flow.png">


   ======= SELESAI =========
