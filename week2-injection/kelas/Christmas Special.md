1. Endpoint product search `https://juice-shop.herokuapp.com/#/search?q=apple`. Untuk mendapatkan hidden product christmas special dapat menggunakan sql injection pada payload `apple')) UNION SELECT * FROM PRODUCTS WHERE deletedAt IS NOT NULL--`
   <img width="1226" height="940" alt="image" src="https://github.com/user-attachments/assets/dc215978-1a53-4f4a-8c68-9408bdb4db14" />

2. Product ID untuk christmas special berhasil didapatkan. ID = 10 <br />
   <img width="1888" height="1116" alt="image" src="https://github.com/user-attachments/assets/941d5241-55f5-4b47-a8d1-f462bdd493c7" /> <br />

3. Modify request pada burpsuite agar product id 10 ditambahkan ke cart
   <img width="708" height="568" alt="image" src="https://github.com/user-attachments/assets/3aafd37a-9826-4bf4-80bf-1232a0f9cd21" />
