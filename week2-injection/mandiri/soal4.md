Sumber Soal:
Portswigger Lab SQL injection attack, querying the database type and version on MySQL and Microsoft
https://portswigger.net/web-security/sql-injection/examining-the-database/lab-querying-database-version-mysql-microsoft
<br />
 This lab contains a SQL injection vulnerability in the product category filter. You can use a UNION attack to retrieve the results from an injected query.
To solve the lab, display the database version string. 

1. Tentukan jumlah kolom yang ada `' order by 1#`
   <img width="1373" height="537" alt="image" src="https://github.com/user-attachments/assets/fea2887b-41b3-4dd1-8216-3a08a91895c6" /> <br />
   Ketika menggunakan order by 3 kolom, response error yang berarti hanya terdapat 2 kolom <br />
    <img width="1189" height="337" alt="image" src="https://github.com/user-attachments/assets/cc2b9032-6cce-4a7e-a827-ed15c4baeef4" />

2. Tentukan kolom yang isinya teks `' UNION SELECT 'a', 'a'#` <br />
    <img width="1472" height="883" alt="Screenshot 2025-09-11 114544" src="https://github.com/user-attachments/assets/24a1d3e0-4580-4adc-9654-a156a071803e" /> <br />
    Teks berhasil dioutput pada kedua kolom

3. Output versi database `' UNION SELECT @@version, NULL#` <br />
    <img width="1838" height="927" alt="image" src="https://github.com/user-attachments/assets/08b6b43a-80bc-4510-b761-f80b51bec6f8" /> <br />
    versi database berhasil dioutput.
