1. Mencoba mengetes kerentanan login Page terhadap SQL injection dengan menggunakan karakter spesial sql ' <br />
<img width="1859" height="965" alt="1-1" src="https://github.com/user-attachments/assets/bc22c30c-e644-4f46-93b0-37bde9cc0339" />
<br />

Pada response terlihat error message SQLITE_ERROR yang menandakan bahwa login page rentan terhadap SQL injection
<br />
2. Menggunakan ' OR true-- agar command setelahnya tidak dieksekusi <br />
<img width="1915" height="958" alt="1-2" src="https://github.com/user-attachments/assets/c419617b-3ebb-4fde-8a2d-f96c08b892da" />
<br />

3. Berhasil log in sebagai admin<br />
<img width="1827" height="1027" alt="1-3" src="https://github.com/user-attachments/assets/32d5cea0-7ceb-47fd-9b6d-bf57b2922122" />

