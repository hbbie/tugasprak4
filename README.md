# tugasprak4
# Tugas Pertemuan 9
# Biodata
Nama  :Dhani Naufal Habibie
NIM   :312410300
Kelas :TI.24.A.4

Mata Kuliah   :Bahasa Pemrograman
Dosen Pengampu:Agung Nugroho, M.Kom

![image](https://github.com/user-attachments/assets/cb42ba27-4641-4684-b2d4-b6a2c7019348)


# Kodingan Program
# List untuk menyimpan data mahasiswa
data_mahasiswa = []

# Perulangan untuk menambahkan data
while True:
    # Meminta input data mahasiswa
    nama = input("Nama: ")
    nim = input("NIM: ")
    tugas = float(input("Nilai Tugas: "))
    uts = float(input("Nilai UTS: "))
    uas = float(input("Nilai UAS: "))
    
    # Menghitung nilai akhir
    nilai_akhir = (tugas * 0.30) + (uts * 0.35) + (uas * 0.35)
    
    # Menyimpan data ke dalam list
    data_mahasiswa.append({
        "Nama": nama,
        "NIM": nim,
        "Nilai Tugas": tugas,
        "Nilai UTS": uts,
        "Nilai UAS": uas,
        "Nilai Akhir": nilai_akhir
    })
    
    # Menanyakan apakah ingin menambah data lagi
    tambah_data = input("Tambah data (y/t)? ")
    if tambah_data.lower() == 't':
        break

# Menampilkan daftar data mahasiswa dalam bentuk tabel
print("\n" + "="*55)
print("| No |     Nama      |   NIM   | Tugas | UTS | UAS | Akhir |")
print("="*55)
for i, mahasiswa in enumerate(data_mahasiswa, start=1):
    print(f"| {i:<2} | {mahasiswa['Nama']:<12} | {mahasiswa['NIM']:<6} |"
          f" {mahasiswa['Nilai Tugas']:<5} | {mahasiswa['Nilai UTS']:<3} |"
          f" {mahasiswa['Nilai UAS']:<3} | {mahasiswa['Nilai Akhir']:<5.2f} |")
print("="*55)


# Berikut adalah penjelasan untuk setiap bagian kode program:

---

### 1. **`data_mahasiswa = []`**
   - **Fungsi:** Membuat sebuah list kosong yang akan digunakan untuk menyimpan data mahasiswa.
   - **Penjelasan:** Semua data mahasiswa (nama, NIM, nilai, dll.) akan disimpan sebagai dictionary di dalam list ini.

---

### 2. **`while True:`**
   - **Fungsi:** Membuat perulangan tak terbatas hingga pengguna memutuskan untuk berhenti (menginput `'t'`).
   - **Penjelasan:** Perulangan ini memungkinkan pengguna untuk terus menambahkan data mahasiswa tanpa batasan jumlah hingga dihentikan manual.

---

### 3. **Meminta Input Data Mahasiswa**
   ```python
   nama = input("Nama: ")
   nim = input("NIM: ")
   tugas = float(input("Nilai Tugas: "))
   uts = float(input("Nilai UTS: "))
   uas = float(input("Nilai UAS: "))
   ```
   - **Fungsi:**
     - Mengambil input dari pengguna berupa nama, NIM, nilai tugas, nilai UTS, dan nilai UAS.
     - `float()` digunakan agar nilai tugas, UTS, dan UAS bisa dihitung sebagai angka desimal.
   - **Penjelasan:** Data yang diinputkan akan digunakan untuk perhitungan nilai akhir dan disimpan dalam list.

---

### 4. **Menghitung Nilai Akhir**
   ```python
   nilai_akhir = (tugas * 0.30) + (uts * 0.35) + (uas * 0.35)
   ```
   - **Fungsi:** Menghitung nilai akhir berdasarkan bobot masing-masing komponen:
     - Tugas: 30%
     - UTS: 35%
     - UAS: 35%
   - **Penjelasan:** Hasil perhitungan disimpan dalam variabel `nilai_akhir` untuk setiap mahasiswa.

---

### 5. **Menyimpan Data ke List**
   ```python
   data_mahasiswa.append({
       "Nama": nama,
       "NIM": nim,
       "Nilai Tugas": tugas,
       "Nilai UTS": uts,
       "Nilai UAS": uas,
       "Nilai Akhir": nilai_akhir
   })
   ```
   - **Fungsi:** Menambahkan dictionary berisi data lengkap mahasiswa ke dalam list `data_mahasiswa`.
   - **Penjelasan:** Struktur dictionary mempermudah pengorganisasian data dengan label (`Nama`, `NIM`, dll.).

---

### 6. **Menanyakan Apakah Ingin Menambah Data Lagi**
   ```python
   tambah_data = input("Tambah data (y/t)? ")
   if tambah_data.lower() == 't':
       break
   ```
   - **Fungsi:**
     - Meminta konfirmasi pengguna apakah ingin menambahkan data lagi.
     - Jika input adalah `'t'`, perulangan akan berhenti (`break`).
   - **Penjelasan:** `tambah_data.lower()` memastikan input tidak case-sensitive (baik `'T'` maupun `'t'` akan dihentikan).

---

### 7. **Menampilkan Data Mahasiswa dalam Bentuk Tabel**
   ```python
   print("\n" + "="*55)
   print("| No |     Nama      |   NIM   | Tugas | UTS | UAS | Akhir |")
   print("="*55)
   ```
   - **Fungsi:** Menampilkan header tabel dengan format yang rapi.
   - **Penjelasan:** 
     - `"\n"` untuk memberikan jarak sebelum tabel.
     - `("="*55)` membuat garis horizontal sepanjang 55 karakter.

---

### 8. **Perulangan untuk Menampilkan Setiap Mahasiswa**
   ```python
   for i, mahasiswa in enumerate(data_mahasiswa, start=1):
       print(f"| {i:<2} | {mahasiswa['Nama']:<12} | {mahasiswa['NIM']:<6} |"
             f" {mahasiswa['Nilai Tugas']:<5} | {mahasiswa['Nilai UTS']:<3} |"
             f" {mahasiswa['Nilai UAS']:<3} | {mahasiswa['Nilai Akhir']:<5.2f} |")
   ```
   - **Fungsi:** Menampilkan setiap data mahasiswa dalam bentuk tabel.
   - **Penjelasan:** 
     - `enumerate(data_mahasiswa, start=1)` memberikan nomor urut (`No`) untuk setiap mahasiswa.
     - Format `{:<12}`, `{:<5}`, dll., mengatur lebar kolom agar data terlihat rapi.
     - `{:<5.2f}` memastikan nilai akhir ditampilkan dengan dua angka di belakang desimal.

---

### 9. **Menutup Tabel dengan Garis Horizontal**
   ```python
   print("="*55)
   ```
   - **Fungsi:** Membuat garis penutup tabel.
   - **Penjelasan:** Memastikan tampilan tabel terlihat rapi dan terorganisasi.

--- 

Program ini dirancang untuk mengelola data mahasiswa, menghitung nilai akhir berdasarkan bobot tertentu, dan menampilkannya dalam format tabel yang mudah dibaca.

# HASIL PROGRAM
![image](https://github.com/user-attachments/assets/0c17a29e-033b-4491-b4f9-75a2e9644569)


# FLOWCHART

# Flowchart
![image](https://github.com/user-attachments/assets/36afe717-4fea-466b-b51a-93ea6b740b26)


# Penjelasan Flow Chart
Pertama mulai
kedua kita akan melist data data mahasiswa
ketiga masukkan nama
keempat masukan nim
kelima masukan nilai tugas
keenam masukkan nilai uts
ketujuh masukkan nilai uas
kedelapan menghitung nilai akhir (nilai tugas * 0.30)(nilai uts * 0.35)(nilai uas * 0.35)jika sudah lanjut
kesembilan tambahkan ke list data
kesepuluh ada dua pilihan jika ingin menambahkan data pilih iya dan kita akan kembali ke langkah ke tiga jika tidak tampilkan tabel data dan terakhir selesai

