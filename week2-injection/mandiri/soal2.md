Sumber Soal :
Portswigger Lab SQL injection vulnerability allowing login bypass
https://portswigger.net/web-security/sql-injection/lab-login-bypass <br />


perform a SQL injection attack that logs in to the application as the administrator user. 

1. Ketika dicoba input karakter sql ' pada login page, terjadi internal server error message yang berarti web app rentan terhadap sql injection <br />
<img width="995" height="255" alt="image" src="https://github.com/user-attachments/assets/16520e1a-9c3c-43ec-9b49-acdda3c47dae" />

2. Ketika menggunakan payload `administrator'--` penyerang berhasil log in. Payload ini membuat penyerang dapat log in dengan username administrator tanpa perlu adanya password sebab pengecekan password diabaikan. <br />
<img width="1848" height="969" alt="image" src="https://github.com/user-attachments/assets/a2e71498-a611-49f7-840b-97c74f9d49d4" /> <br />
<img width="1595" height="844" alt="image" src="https://github.com/user-attachments/assets/4333666c-557b-4fbf-a652-2643f23bc486" />

