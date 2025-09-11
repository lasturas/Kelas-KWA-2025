# Soal - Reflected XSS into HTML context with nothing encoded  

Source soal : https://portswigger.net/web-security/cross-site-scripting/reflected/lab-html-context-nothing-encoded  

## Deskripsi Soal 
Menemukan dan mengeksploitasi kerentanan Reflected Cross-Site Scripting (XSS) yang sederhana pada fungsionalitas pencarian. Tujuannya adalah untuk melakukan serangan XSS yang berhasil memanggil fungsi JavaScript alert()  


## Penyelesaian 
1. Akses lab      
<img width="1537" height="787" alt="image" src="https://github.com/user-attachments/assets/a29e3119-d622-4461-8265-c954e83dc1fb" />


2. Memasukkan payload XSS sederhanan `<script>alert(1)</script>` langsung ke dalam kotak Search di halaman utama dengan tujuan memanggil fungsi alert()  
<img width="996" height="274" alt="image" src="https://github.com/user-attachments/assets/10295496-6a90-4908-8333-71881f20a898" />  


3. Setelah menekan tombol search maka akan muncul pop up notifikasi `alert` dan notifikasi berhasil menyelesaikan tantangan 
<img width="683" height="282" alt="image" src="https://github.com/user-attachments/assets/2b1e6e6f-8c14-465d-9e9c-e72bca4f0a81" />  
<img width="1509" height="595" alt="image" src="https://github.com/user-attachments/assets/909cf4cc-b897-472d-87e8-493e61e433dd" />  



## Hasil 
Berhasil memanggil fungsil alert() dengan menggunakan payload XSS sederhana   
> Serangan ini berhasil karena aplikasi web mengambil input dari kotak pencarian dan menempatkannya langsung ke dalam kode HTML halaman respons tanpa melakukan output encoding. Karakter khusus seperti < dan > tidak diubah menjadi entitas HTML (&lt; dan &gt;). Akibatnya, browser menginterpretasikan payload <script>alert(1)</script> sebagai tag HTML yang sah dan mengeksekusi kode JavaScript yang ada di dalamnya

