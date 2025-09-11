Sumber soal :
Portswigger Lab : SQL injection vulnerability in WHERE clause allowing retrieval of hidden data
https://portswigger.net/web-security/sql-injection/lab-retrieve-hidden-data

Perform a SQL injection attack that causes the application to display one or more unreleased products. 
1. Payload kategori produk seperti berikut
   ```
   academy.net/filter?category=Tech+gifts
   ```
   <img width="1652" height="1046" alt="image" src="https://github.com/user-attachments/assets/35363f4b-8872-47fd-a1ac-e1c778d4f84e" /> <br />
   Dapat disimpulkan bahwa command sql pada backend web app seperti
   ```
    SELECT * FROM products WHERE category = 'Pets' AND release = 1
   ```
2. Ketika payload diinjeksi dengan karakter sql ', dapat dilihat bahwa web app rentan terhadap sql injection <br />
    <img width="1719" height="941" alt="image" src="https://github.com/user-attachments/assets/250687e4-7a61-46d7-9a5b-e07d4658e19d" /> <br />

3. Dengan memodifikasi command SQL agar categorynya ditampilkan dengan `'or1=1--`, semua produk berhasil ditampilkan. <br />
   <img width="1796" height="1053" alt="image" src="https://github.com/user-attachments/assets/2511259c-df3b-4a52-8de2-efc9ad1ba19c" />

