# SQLiLite Write-up:

Sumber: 
* https://play.picoctf.org/practice/challenge/304?category=1&page=1&search=sql
* https://github.com/payloadbox/sql-injection-payload-list

## Langkah pengerjaan:
* Masuk ke halaman login
<img width="946" height="811" alt="image" src="https://github.com/user-attachments/assets/e359a5db-d510-40c4-bab2-3564b0068944" />

* Setelah kita di halaman login, masukkan payload `admin' or '1'='1`
<img width="1918" height="754" alt="image" src="https://github.com/user-attachments/assets/5436c1e4-e366-4f04-9087-6004fa0235cc" />

* Tapi kita masih belum menemukan flag
<img width="917" height="230" alt="image" src="https://github.com/user-attachments/assets/61be9d3c-824f-4255-b556-8141f3bbd244" />

* Jika kita view page source kita akan menemuka flag
<img width="1433" height="193" alt="image" src="https://github.com/user-attachments/assets/655dd024-c8a2-4c7a-9baf-40e91d28cd93" />
