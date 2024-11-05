# labpy03
# Tugas Praktikum 3

# Latihan 1 
1. Tampilkan n bilangan acak yang lebih kecil dari 0.5.
2. nilai n diisi pada saat runtime
3. anda bisa menggunakan kombinasi while dan for untuk menyelesaikannya
4. gunakan fungsi random() yang dapat diimport terlebih dahulu

       from random import random

        def generate_random_numbers():
        n = int(input("Masukkan angka n: "))
        count = 1
    
        while count <= n:
        value = random()
        if value < 0.5:
            print(f"data ke: {count} => {value}")
            count += 1
            
        print("END")

        # Menjalankan program
        generate_random_numbers()

PROSES INPUT DAN HASIL OUTPUT 
![latihan 1 py](https://github.com/user-attachments/assets/a855f776-a4ab-47f8-9467-87829bde36e6)

PENJELASAN PROGRAM NILAI RANDOM : 
1. From random import random berfungsi untuk mengimpor fungsi random dari modul random yang akan menghasilkan angka acak dalam rentang [0.0, 1.0]
2. generate_random_numbers berfungsi untuk menghasilkan dan mencetak angka acak berdasarkan apa yang di input ( pada percobaan diatas menggunakan angka 5 )
3. count = 1 digunakan untuk mencari jumlah angka acak yang dihasilkan yang dimulai dari 1
4. value = random berfungsi menghasilkan angka acak antara 0.0 dan 1.0
5. if value < 0.5 berfungsi memeriksa angka acak yang dihasilkan kurang dari 0.5. Jika ini terpenuhi, maka angka tersebut akan dicetak dengan format 'data ke: {count} >= {value}
6. count += 1 berfungsi untuk menambahkan 1 untuk melanjutkanke angka acak selanjutnya
7. Setelah selesai, program akan mencetak kata "END" 

FLOWCHART 


# Latihan 2 
Seorang pengusaha menginvestasikan uangnya untuk memulai usahanya dengan modal awal 100 juta, pada bulan pertama dan kedua belum mendapatkan laba. pada bulan ketiga baru mulai mendapatkan laba sebesar 1% dan pada bulan ke 5, pendapatan meningkat 5%, selanjutnya pada bulan ke 8 mengalami penurunan keuntungan sebesar 2%, sehingga laba menjadi 3%. 
Hitung total keuntungan selama 8 bulan berjalan usahanya.

    modal_awal = 100000000
    laba_bulanan = []
    total_laba = 0

    for bulan in range(1, 9):
    laba = 0
    
    if bulan <= 2:  # Bulan 1-2: belum ada laba
        laba = 0
    elif bulan <= 4:  # Bulan 3-4: laba 1%
        laba = modal_awal * 0.01
    elif bulan <= 7:  # Bulan 5-7: laba 5%
        laba = modal_awal * 0.05
    else:  # Bulan 8: laba 2%
        laba = modal_awal * 0.02
    
    laba_bulanan.append(laba)
    total_laba += laba

    # Menampilkan laba per bulan
    for bulan, laba in enumerate(laba_bulanan, 1):
    print(f"laba bulan ke- {bulan} sebesar: {laba}")
  
    # Menampilkan total laba
    print(f"Total laba adalah: {total_laba}")

PROSES INPUT 

![kode 1 laba](https://github.com/user-attachments/assets/c81bb0e5-d35a-4233-b704-99a767c573b9)
![kode 2 laba](https://github.com/user-attachments/assets/255889c8-4029-4eae-be2e-07a88da87b21)

HASIL OUTPUT
![hasil laba](https://github.com/user-attachments/assets/b76cd24a-559f-443f-9b79-8ac768d9dd7d)

PENJELASAN PROGRAM LABA : 
1. Menetapkan modal awal, membuat list untuk menyimpan laba yang dihasilkan setiap bulan dan variabel akan menyimpan total laba yang diperoleh
2. Menggunakan loop untuk mengulang dari bulan 1 hingga bulan 8
3. Menghitung laba berdasarkan bulan dengan menggunakan 'if bulan <= bulan'
4. Menyimpan laba bulanan
5. Menampilkan laba perbulan
6. Yang terakhir adalah menampilkan total





