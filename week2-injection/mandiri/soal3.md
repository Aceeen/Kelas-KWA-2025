Sumber Soal :
Portswigger Lab SQL injection attack, querying the database type and version on Oracle
https://portswigger.net/web-security/sql-injection/examining-the-database/lab-querying-database-version-oracle <br />

 This lab contains a SQL injection vulnerability in the product category filter. You can use a UNION attack to retrieve the results from an injected query.
To solve the lab, display the database version string. <br />

1. Menentukan jumlah kolom database
 <img width="1850" height="988" alt="image" src="https://github.com/user-attachments/assets/dc4249d0-b980-4754-9298-fb9ada55f275" /> <br />
 Ketika dicoba dengan 3 kolom, response internal server error yang berarti jumlah kolom adalah 2 <br />
<img width="1482" height="374" alt="image" src="https://github.com/user-attachments/assets/98b6c124-2b78-421f-ac38-8cf4cd36119e" />

2. Menentukan tipe data dalam kolom <br />
`' UNION SELECT 'a', 'a' from DUAL--`
<img width="1466" height="738" alt="image" src="https://github.com/user-attachments/assets/6389c241-5427-456c-8b61-7cbf79a61001" /> <br />
response success

3. Output versi database <br />
dengan menggunakan sql injection `' UNION SELECT banner, NULL from v$version--` pada database union
<img width="1405" height="746" alt="image" src="https://github.com/user-attachments/assets/198be1bb-3b90-4acf-9013-3aa5e9f976d1" />

