## NAMA  : ADINDA AULIA NABILA PUTRI

## NIM   : 312410309

## KELAS : TI.24.A.4



## LATIHAN 

  ![Screenshot (85)](https://github.com/user-attachments/assets/c1d7de0a-64e8-4660-86d3-f3cc7107a8a2)

```PYTHON
import math

a = lambda x: x**2
b = lambda x, y: math.sqrt(x**2 + y**2)
c = lambda *args: sum(args)/len(agrs) if args else 0
d = lambda s: "".joint(set(s))

print("lambda a(5):", a(5))
print("lambda b(3, 4):", b(3, 4))
print("lambda c(1, 2, 3, 4, 5):", c(1, 2, 3, 4, 5))
print("lambda d('hello adinda'):, d("adinda))
````



Berikut code dan hasil dari program tersebut 

![code](https://github.com/user-attachments/assets/8ba3c407-8ee3-4be0-a6ef-b66a3a64ccd8)

![Screenshot (88)](https://github.com/user-attachments/assets/ff4ae514-7eed-498e-8ee3-5c48d1e104b7)




# TUGAS PRAKTIKUM 

![Screenshot (86)](https://github.com/user-attachments/assets/4dc911c2-bb77-469b-b65d-1df3020cf591)

```PYTHON
def tambah():
    """Menambahkan data mahasiswa baru ke dalam daftar."""
    nama = input("Masukkan nama mahasiswa: ")
    if not nama.strip():
        print("Nama tidak boleh kosong.")
        return
    try:
        nilai = int(input("Masukkan nilai mahasiswa: "))
    except ValueError:
        print("Nilai harus berupa angka.")
        return
    daftar_mahasiswa[nama] = nilai
    print("Data mahasiswa berhasil ditambahkan.")

def tampilkan():
    """Menampilkan semua data mahasiswa."""
    if not daftar_mahasiswa:
        print("Daftar mahasiswa kosong.")
    else:
        print("Daftar Mahasiswa:")
        for nama, nilai in daftar_mahasiswa.items():
            print(f"{nama}: {nilai}")

def hapus(nama):
    """Menghapus data mahasiswa berdasarkan nama."""
    if nama in daftar_mahasiswa:
        del daftar_mahasiswa[nama]
        print(f"Data mahasiswa {nama} berhasil dihapus.")
    else:
        print(f"Data mahasiswa {nama} tidak ditemukan.")

def ubah(nama):
    """Mengubah data mahasiswa berdasarkan nama."""
    if nama in daftar_mahasiswa:
        try:
            nilai_baru = int(input(f"Masukkan nilai baru untuk {nama}: "))
            daftar_mahasiswa[nama] = nilai_baru
            print(f"Data mahasiswa {nama} berhasil diubah.")
        except ValueError:
            print("Nilai harus berupa angka.")
    else:
        print(f"Data mahasiswa {nama} tidak ditemukan.")

daftar_mahasiswa = {}

if __name__ == "__main__":
    while True:
        print("\nMenu:")
        print("1. Tambah data")
        print("2. Tampilkan data")
        print("3. Hapus data")
        print("4. Ubah data")
        print("5. Keluar")

        pilihan = input("Pilih menu (1-5): ")

        if pilihan == '1':
            tambah()
        elif pilihan == '2':
            tampilkan()
        elif pilihan == '3':
            nama = input("Masukkan nama mahasiswa yang ingin dihapus: ")
            hapus(nama)
        elif pilihan == '4':
            nama = input("Masukkan nama mahasiswa yang ingin diubah: ")
            ubah(nama)
        elif pilihan == '5':
            print("Terima kasih!")
            break
        else:
            print("Pilihan tidak valid.")
````


```PYTHON
def tambah():
    """Menambahkan data mahasiswa baru ke dalam daftar."""
    nama = input("Masukkan nama mahasiswa: ")
    if not nama.strip():
        print("Nama tidak boleh kosong.")
        return
    try:
        nilai = int(input("Masukkan nilai mahasiswa: "))
    except ValueError:
        print("Nilai harus berupa angka.")
        return
    daftar_mahasiswa[nama] = nilai
    print("Data mahasiswa berhasil ditambahkan.")
````
def tambah() memungkinkan pengguna menambah data mahasiswa baru seperti meminta input nama, nilai. try-except untuk mencoba mengonversi nilai yang dimasukkan menjadi integer. jika gagal, maka program mencetak pesan kesalahan, dan jika semua input valid, data mahasiswa ditambahkan kedalam distionary daftar_mahasiswa, dan program mencetak pesan konfirmasi.




```PYTHON
def tampilkan():
    """Menampilkan semua data mahasiswa."""
    if not daftar_mahasiswa:
        print("Daftar mahasiswa kosong.")
    else:
        print("Daftar Mahasiswa:")
        for nama, nilai in daftar_mahasiswa.items():
            print(f"{nama}: {nilai}")
````
def tampilkan(), menampilkan seluruh data mahasiswa yang tersimpan, jika tidak ada data/kosong, mencetak "Daftar Mahasiswa:" dan menggunakan loop untuk mencetak setiap nama mahasiswa.





```PYTHON
def hapus(nama):
    """Menghapus data mahasiswa berdasarkan nama."""
    if nama in daftar_mahasiswa:
        del daftar_mahasiswa[nama]
        print(f"Data mahasiswa {nama} berhasil dihapus.")
    else:
        print(f"Data mahasiswa {nama} tidak ditemukan.")
````
def hapus(nama), digunakan untuk menghapus data mahasiswa berdasarkan nama, jika ada data mahasiswa yang dihapus menggunakan del, maka mencetak pesan konfirmasi bahwa data berhasil dihapus. jika tidak ada maka mencetak pesan mahasiswa tidak ditemukan.




```PYTHON
def ubah(nama):
    """Mengubah data mahasiswa berdasarkan nama."""
    if nama in daftar_mahasiswa:
        try:
            nilai_baru = int(input(f"Masukkan nilai baru untuk {nama}: "))
            daftar_mahasiswa[nama] = nilai_baru
            print(f"Data mahasiswa {nama} berhasil diubah.")
        except ValueError:
            print("Nilai harus berupa angka.")
    else:
        print(f"Data mahasiswa {nama} tidak ditemukan.")
````
def ubah(nama), mengubah nilai mahasiswa dengan nama tertentu, memeriksa nama mahasiswa apakah ada dalam daftar_mahasiswa, jika ada maka pengguna meminta untuk memasukkan nilai baru dan mencoba mengonversinya menjadi integer. 





```PYTHON
 print("\nMenu:")
        print("1. Tambah data")
        print("2. Tampilkan data")
        print("3. Hapus data")
        print("4. Ubah data")
        print("5. Keluar")
````
Program mencetak menu dengan lima opsi yang dapat dipilih pengguna tersebut 
1. untuk menambah data mahasiswa baru
2. untuk menampilkan semua data mahasiswa yang telah dimasukkan
3. menghapus data mahasiswa berdasarkan nama
4. mengubah nilai mahasiswa berdasarkan nama
5. keluar dari program





```PYTHON
pilihan = input("Pilih menu (1-5): ")

        if pilihan == '1':
            tambah()
        elif pilihan == '2':
            tampilkan()        
````
Program meminta input untuk memilih salah satu menu(1-5). jika pengguna memilih 1, maka fungsi akan tambah(), tetapi jika pengguna memilih 2, maka fungsi akan tampilkan().




```PYTHON
 elif pilihan == '3':
            nama = input("Masukkan nama mahasiswa yang ingin dihapus: ")
            hapus(nama)
        elif pilihan == '4':
            nama = input("Masukkan nama mahasiswa yang ingin diubah: ")
            ubah(nama)
        elif pilihan == '5':
            print("Terima kasih!")
            break
````
Jika pengguna memilih 3, maka program akan meminta input nama mahasiswa yang ingin dihapus, jika pengguna memilih 4, maka program akan meminta input nama mahasiswa yang ingin diubah, tetapi jika pengguna memilih 5, maka program akan mencetak pesan "terima kasih!" dan keluar dari loop utama dengan menggunakan break. 






Berikut hasil dan code dari program tersebut 

   ![code 2](https://github.com/user-attachments/assets/01d00bff-eecf-4b34-940b-977ce8ded9e0)


  ![Screenshot (89)](https://github.com/user-attachments/assets/78bbb8b5-8bb4-4b50-a6b0-dc6129e8369d)




