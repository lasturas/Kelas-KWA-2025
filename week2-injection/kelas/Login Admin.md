# Soal - Login Admin 
---
Source soal : https://demo.owasp-juice.shop/#/score-board?categories=Injection

## Deskripsi Soal 
Mencoba untuk login menggunakan akun admin 

## Penyelesaian 
1. Membuka halaman login
  <img width="563" height="482" alt="Screenshot 2025-09-10 215606" src="https://github.com/user-attachments/assets/4148609a-3dea-4ea1-ae20-1b4168963d0e" />   

2. Mengisi bagian email dengan 'admin@juice-sh.op' --'. Penambahan tanda petik 1 (') dan min (--) untuk membuat command yang nantinya membuat query dan kode selanjutnya menjadi komen sehingga tidak bisa dieksekusi. Untuk password bisa diisi apapun   
<img width="573" height="541" alt="Screenshot 2025-09-10 214936" src="https://github.com/user-attachments/assets/f4a6b87d-c466-4ce6-8ecd-f657b25178f1" />   

3.  Klik login dan ternyata berhasil masuk sebagai admin
   <img width="445" height="375" alt="Screenshot 2025-09-10 214952" src="https://github.com/user-attachments/assets/db7bc003-29c5-49e3-84b0-a172542c0320" />   


## Hasil 
Berhasil login sebagai admin tanpa mengetahui email dan password asli milik admin
