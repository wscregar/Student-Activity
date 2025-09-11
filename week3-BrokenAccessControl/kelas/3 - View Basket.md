# View Basket Write-up:

Sumber: https://youtu.be/rsj2MEZcRA8?si=Ipq6UsEj05Uf-8Kk

## Langkah pengerjaan
* Sebelum memulai harus login dahulu agar bisa mengakses basket
<img width="1911" height="795" alt="image" src="https://github.com/user-attachments/assets/85e30739-4a1d-4964-a28b-06ecd54f287a" />

* Buka aplikasi burp suite dan masuk ke fitur proxy lalu copy link basket ke browser burp `https://juice-shop.herokuapp.com/#/basket`
<img width="1898" height="956" alt="image" src="https://github.com/user-attachments/assets/4bdd6f09-3989-4380-852c-787e787e7677" />

* Intercept link basket dan cari directory `/rest/basket/NaN HTTP/1.1` dan ganti NaN menjadi angka untuk mengganti user sehingga basket juga berganti
<img width="1380" height="894" alt="image" src="https://github.com/user-attachments/assets/bd2309a5-8a5f-490f-9b99-1bde0e797306" />

* Jika view basket belum berubah memalui cara sebelumnya, coba akses inspect
<img width="1902" height="994" alt="image" src="https://github.com/user-attachments/assets/5e276481-6c6b-4432-b9c5-ac6571f8e934" />

* lalu pergi ke application/session storage. disana kita bisa mengganti value pada bid
<img width="1914" height="993" alt="image" src="https://github.com/user-attachments/assets/eab0b7ae-0f9c-4c54-a4f8-f74b8e93172a" />

* Setelah value diubah menjadi 1 atau 5 maka kita bisa melihat basket user lain
### Basket user 1:
<img width="1912" height="1007" alt="image" src="https://github.com/user-attachments/assets/b03a50d0-be23-4eed-935c-c76e4369352a" />
### Basket user 5:
<img width="1919" height="1004" alt="image" src="https://github.com/user-attachments/assets/d14ff8b5-e7db-476e-a030-8f78edbaed8c" />
