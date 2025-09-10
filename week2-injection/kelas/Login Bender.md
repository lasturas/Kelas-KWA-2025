# Soal - Login Bender 

Source soal : https://demo.owasp-juice.shop/#/score-board?categories=Injection

## Deskripsi Soal 
Mencoba untuk login sebagai Bender menggunakan akun Bender 

## Penyelesaian 
1. Mencari informasi mengenai email Bender. Email ini dapat ditemukan pada bagian About Us, pada Customer Feedback   
<img width="1339" height="601" alt="image" src="https://github.com/user-attachments/assets/53f3348e-17be-46f2-a081-78f94c455ab1" />  

Atau bisa juga ditemukan pada Pencarian semua produk, pada produk OWASP Juice Shop "King of the Hill" Facemask, di bagian reviews  
<img width="699" height="636" alt="image" src="https://github.com/user-attachments/assets/1037a1b6-3e2e-495b-8020-1233b42250c2" />  


2. Mengisi bagian email dengan 'bender@juice-sh.op' --'. Penambahan tanda petik 1 (') dan min (--) untuk membuat command yang nantinya membuat query dan kode selanjutnya menjadi komen sehingga tidak bisa dieksekusi. Untuk password bisa diisi apapun   
<img width="565" height="520" alt="image" src="https://github.com/user-attachments/assets/6a370461-d1dd-4fff-9ab8-2256d8db7af5" />  

3.  Klik login dan ternyata berhasil masuk sebagai Bender
<img width="448" height="345" alt="image" src="https://github.com/user-attachments/assets/95b85c6c-b5dd-4c9a-9f4a-dab3a2ffd7e0" />  


## Hasil 
Berhasil login sebagai Bender tanpa mengetahui email dan password asli milik Bender
