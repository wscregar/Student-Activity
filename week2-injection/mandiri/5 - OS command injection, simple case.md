# OS command injection, simple case Write-up:

Sumber: https://portswigger.net/web-security/os-command-injection/lab-simple

## Langkah pengerjaan
* Sama seperti tugas mandiri 3 & 4, kita siapkan burp suite di mode intercept dan buka lab di portswigger
<img width="1779" height="964" alt="image" src="https://github.com/user-attachments/assets/01d2f671-fcbf-447b-9beb-68127931101f" />

* Cek salah satu stok barang yang ada di toko
<img width="982" height="938" alt="image" src="https://github.com/user-attachments/assets/8b6b8a66-7256-4819-8be7-44471bc0f766" />

* Setelah itu nyalakan intercept dan cek lagi stok barang yang berbeda lokasi dan kita bisa lihat terdapat kerentanan pada pemeriksa stok produk `productId=1&storeId=1` 
<img width="1776" height="969" alt="image" src="https://github.com/user-attachments/assets/60a10abe-d6d9-490a-90ac-fa2161ad4b31" />

* Kita bisa memasukkan `command injection` pada kerentanan tersebut. tambahkan `1|whoami` setelah productId=1&storeId=1, lalu forward. Bisa dilihat stok berubah menjadi `peter-J485Ea
` menandakan command injection berhasil
<img width="1781" height="949" alt="image" src="https://github.com/user-attachments/assets/71d52e94-f6b4-43c2-89e0-95918265f599" />
