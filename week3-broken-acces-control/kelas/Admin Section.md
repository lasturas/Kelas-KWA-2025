# Soal - Admin Section  

Source soal : https://demo.owasp-juice.shop/#/score-board?categories=Broken%20Access%20Control  

## Deskripsi Soal 
---

## Penyelesaian 
1. Akses soal dan login sebagai admin terlebih dahulu dengan cara yang sama seperti pada tantangan Login Admin pada Week 2  
email: `admin@juice-sh.op' --` --> ' untuk menutup string, dan -- untuk mengomentari kode setelah login agar terabaikan  
password: (bisa diisi apa saja)
<img width="578" height="528" alt="image" src="https://github.com/user-attachments/assets/59d69dcc-1f9f-4285-99b2-6180f9176789" />

2. Setelah berhasil login sebagai admin, cek pada bagian kiri atas (icon hamburger) untuk melihat tentang website lebih lanjut. Ternyata ditemuka bahwa website menggunakan Angular  
<img width="304" height="186" alt="image" src="https://github.com/user-attachments/assets/2b6be3a1-1a28-4efe-89c9-1d03a830e9ff" />  

3. Dengan hint ini maka kita bisa mencoba membuka akses menuju administrasi pada toko dengan cara menambahkan payload `/administration` pada URL
<img width="567" height="355" alt="image" src="https://github.com/user-attachments/assets/36e16933-e827-48d6-a881-9ea1b4e1b61f" />


4. Klik enter dan terlihat bahwa kita berhasil memasukin bagian administrasi toko  
<img width="1852" height="941" alt="image" src="https://github.com/user-attachments/assets/052af200-0a74-435e-841c-d93768314dbd" />


## Hasil 
---  
> ---
> - Penggunaan tabel dual (FROM dual) wajib ada dalam sintaks SELECT di Oracle
> - Mengetahui tabel sistem v$version dan kolom banner untuk mengekstrak informasi yang diminta
