# Soal - Forged Feedback  

Source soal : https://demo.owasp-juice.shop/#/score-board?categories=Broken%20Access%20Control  

## Deskripsi Soal 
AAA  

## Penyelesaian 
1. Akses soal dan pastikan sudah login (boleh admin atau akun lain), lalu masuk menuju Customer Feedback   
<img width="358" height="293" alt="image" src="https://github.com/user-attachments/assets/5f8d8d0c-421a-4daf-8aa5-b81484bcc728" />

2. Nyalakan proxy pada Burp Suite dan kirimkan feedback seperti biasa  
<img width="542" height="699" alt="image" src="https://github.com/user-attachments/assets/7c032f2f-6cd0-4987-af6f-1948fcd26ccb" />

3. Cek pada bagian HTTP History pada Burp Suite dan cari URL `/api/Feedbacks` dan klik kanan lalu kirim menuju repeater  
<img width="1430" height="793" alt="image" src="https://github.com/user-attachments/assets/cb12e3cb-4225-48f1-a1d1-f570f2a13902" />

4. Pada repeater, cari request yang berisi "UserId" dan ubah value tersebut yang awalnya 1 menjadi angka lain untuk mengubah id pengirim feedback. Klik send dan akan muncul response yang mengirimkan feedback dengan UserID yang berbeda yang menandakan kita berhasil menyelesaikan tantangan    
<img width="1449" height="730" alt="image" src="https://github.com/user-attachments/assets/6bede4e6-f52d-449d-a4c3-d9a56d3a0b0e" />



## Hasil 
AAAAAAA  
> AAAAA
