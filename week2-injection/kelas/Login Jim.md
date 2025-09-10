# Soal - Login Jim 

Source soal : [https://demo.owasp-juice.shop/#/score-board?categories=Injection](https://demo.owasp-juice.shop/#/score-board?categories=Injection)

## Deskripsi Soal 
Mencoba untuk login sebagai Jim tanpa mengetahui email dan password milik Jim 

## Penyelesaian 
1. Untuk informasi mengenail email Jim dapat ditemukan pada bagian pencarian produk dengan nama Green Smoothie pada reviews
<img width="698" height="603" alt="image" src="https://github.com/user-attachments/assets/4e540263-a49b-41a6-9b8d-770de38c5682" />  

2. Mengisi bagian email dengan 'jim@juice-sh.op' --'. Penambahan tanda petik 1 (') dan min (--) untuk membuat command yang nantinya membuat query dan kode selanjutnya menjadi komen sehingga tidak bisa dieksekusi. Untuk password bisa diisi apapun   
<img width="536" height="513" alt="image" src="https://github.com/user-attachments/assets/fd265880-e8da-4b5c-b6c4-d361dcc661af" />  


3.  Klik login dan ternyata berhasil masuk sebagai Jim
<img width="390" height="342" alt="image" src="https://github.com/user-attachments/assets/5284006c-fe85-4e48-8a6e-90cdf0d45213" />

 
## Hasil 
Berhasil login sebagai Jim tanpa mengetahui email dan password asli milik Jim
