# More SQLi Write-up:

Sumber: 
* https://play.picoctf.org/practice/challenge/358?category=1&page=1&search=sql
* https://github.com/payloadbox/sql-injection-payload-list

## Langkah pengerjaan:
* Masuk ke halaman login
<img width="1911" height="530" alt="image" src="https://github.com/user-attachments/assets/85bb7211-badf-47aa-9326-50e3a84d4641" />

* Setelah kita di halaman login, kita coba login dahulu. kita bisa lihat disini bahwa SQL disini mengecek password dahulu, sehingga kita bisa fokus masukkan payload kedalam password saja
<img width="736" height="102" alt="image" src="https://github.com/user-attachments/assets/81328012-dd06-42bd-82b3-c0427308f090" />

* Kita coba login dengan username `admin` dan password `' or 1=1--`
<img width="1915" height="517" alt="image" src="https://github.com/user-attachments/assets/27833243-28cc-480f-bd69-e468ee44c11a" />

* Setelah login kita menemukan tabel yang fitur search, kita bisa lihat bahwa search bar menggunakan SQLite rentan terhadap SQL injection
<img width="985" height="582" alt="image" src="https://github.com/user-attachments/assets/0f1e000a-ac0c-490d-b314-7d74e1fb5bee" />

<img width="920" height="685" alt="image" src="https://github.com/user-attachments/assets/6a318e4b-787a-42eb-b2ce-0671ea024af9" />

* Kita bisa gunakan command `' UNION SELECT name, sql, 'ww' FROM sqlite_master WHERE type='table'--` untuk mengakses struktur tabelnya
<img width="920" height="685" alt="image" src="https://github.com/user-attachments/assets/76a4a11f-448b-4529-8e1b-7c97391640d7" />

* Terakhir masuk ke dalam directory more_table menggunakan command `' UNION SELECT flag,NULL,NULL FROM more_table--` untuk menemukan flag
<img width="924" height="603" alt="image" src="https://github.com/user-attachments/assets/6119d6ec-e39a-4346-b28a-4c30ab2c7591" />
