# pertemuan-10
NAMA : AGIL TRI ISWARA
KELAS :IE.23.C12
MATKUL :PROGRAM KOMPUTER 

#program phyton 



data_mahasiswa = {}

def hitung_nilai_akhir(tugas, uts, uas):
    return (tugas * 0.3) + (uts * 0.35) + (uas * 0.35)

def tampilkan_data():
    if not data_mahasiswa:
        print("\nDaftar Nilai")
        print("="*57)
        print("| NO |  NIM  |   NAMA   | TUGAS |  UTS  |  UAS  | AKHIR |")
        print("="*57)
        print("|                    TIDAK ADA DATA                     |")
        print("="*57)
    else:
        print("\nDaftar Nilai")
        print("="*57)
        print("| NO |  NIM  |   NAMA   | TUGAS |  UTS  |  UAS  | AKHIR |")
        print("="*57)
        for i, (nim, data) in enumerate(data_mahasiswa.items(), start=1):
            print(f"| {i:<2} | {nim:<5} | {data['nama']:<8} | {data['tugas']:<5} | {data['uts']:<5} | {data['uas']:<5} | {data['akhir']:<0.2f} |")
        print("="*57)

def tambah_data():
    nim = input("NIM: ")
    nama = input("Nama: ")
    tugas = float(input("Nilai Tugas: "))
    uts = float(input("Nilai UTS: "))
    uas = float(input("Nilai UAS: "))
    nilai_akhir = hitung_nilai_akhir(tugas, uts, uas)
    data_mahasiswa[nim] = {"nama": nama, "tugas": tugas, "uts": uts, "uas": uas, "akhir": nilai_akhir}
    print("Data berhasil ditambahkan!")

def ubah_data():
    nim = input("Masukkan NIM mahasiswa yang akan diubah: ")
    if nim in data_mahasiswa:
        print("Masukkan data baru:")
        nama = input("Nama: ")
        tugas = float(input("Nilai Tugas: "))
        uts = float(input("Nilai UTS: "))
        uas = float(input("Nilai UAS: "))
        nilai_akhir = hitung_nilai_akhir(tugas, uts, uas)
        data_mahasiswa[nim] = {"nama": nama, "tugas": tugas, "uts": uts, "uas": uas, "akhir": nilai_akhir}
        print("Data berhasil diubah!")
    else:
        print("Data tidak ditemukan!")

def hapus_data():
    nim = input("Masukkan NIM mahasiswa yang akan dihapus: ")
    if nim in data_mahasiswa:
        del data_mahasiswa[nim]
        print("Data berhasil dihapus!")
    else:
        print("Data tidak ditemukan!")

def cari_data():
    nim = input("Masukkan NIM yang dicari: ")
    if nim in data_mahasiswa:
        data = data_mahasiswa[nim]
        print("\nData Mahasiswa")
        print(f"NIM: {nim}")
        print(f"Nama: {data['nama']}")
        print(f"Nilai Tugas: {data['tugas']}")
        print(f"Nilai UTS: {data['uts']}")
        print(f"Nilai UAS: {data['uas']}")
        print(f"Nilai Akhir: {data['akhir']:.2f}")
    else:
        print("Data tidak ditemukan!")

while True:
    print("\nProgram Input Nilai")
    print("===================")
    print("[(L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar]")
    pilihan = input("Pilih menu: ").lower()

    if pilihan == "l":
        tampilkan_data()
    elif pilihan == "t":
        tambah_data()
    elif pilihan == "u":
        ubah_data()
    elif pilihan == "h":
        hapus_data()
    elif pilihan == "c":
        cari_data()
    elif pilihan == "k":
        print("Program selesai. Terima kasih!")
        break
    else:
        print("Pilihan tidak valid! Silakan coba lagi.")

#tampilan screen shot aplikasi 
![PERTEMUAN 10 SS PHYTON](https://github.com/user-attachments/assets/d374e324-ba7e-4284-9d9a-e97904ea244e)






![pertemuan 10 ss ](https://github.com/user-attachments/assets/32818eb3-7a2f-4273-ac73-916dad2be8ce)








![pertemuan10 ss phyton](https://github.com/user-attachments/assets/2894c029-85c0-46dc-8018-a183196b94c1)














![ss komputer pertemuan 10](https://github.com/user-attachments/assets/3afb5513-50ce-4053-9804-0d7cc7c1701e)














![pertemuan 10 ss](https://github.com/user-attachments/assets/5ec682e7-edc9-4231-8833-d236b0bf8a99)













#FLOW CHART
![flow chart pertemuan 10 praktikum 7_page-0001](https://github.com/user-attachments/assets/79bc5bc7-1df5-4ac7-9140-7bccbddc407d)




















        
