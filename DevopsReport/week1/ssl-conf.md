# SSL Configuration AWS

 * pertama tama masuk ke Dashboard Cloudflare
 * Klik profile
 * setelah itu pilih API TOKENs

     ![gambar 1](assets/ssl1.png)

 * Kemudian pilih view di Global Api Key

     ![gambar 2](assets/ssl2.png)

 * Masukkan password kita dan centang im human
 * setelah itu copy api key kita
 * Kemudian masuk ke server aws yg menjadi gateway lalu buat folder `sudo mkdir .cloudflare`
 * Setelah itu masuk kedalam direktorinya `cd .cloudflare/`
 * Setelah masuk kita buat file `sudo nano api.key`
 * Didalamnya kita masukkan email dan apikey kita

     ![gambar 3](assets/ssl3.png)

 * Kemudian setelah selesai keluar `ctrl + x` lalu `y` tekan `enter`
 * setelah itu masukkan perintah `sudo chmod 400 api.key`
 * Setelah selesai kita installasi Certbot agar untuk mensertifikasi
 * Masukkan perintah `sudo snap install core; sudo snap refresh core`
 * lalu masukkan `sudo snap install --classic certbot`
 * lalu masukkan `sudo ls -s /snap/bin/certbot /usr/bin/certbot
 * Kemudian masukkan perintah `sudo certbot` disini kita akan diminta memasukkan email dan memilih file mana yg akan kita aktifkan httpsnya

     ![gambar 4](assets/ssl4.png)
     ![gambar 5](assets/ssl5.png)

 * Jika prosesnya sudah selesai kita cek sertifikasinya dengan masuk ke `cd /etc/nginx/dumbflix`
 * Lalu kita bisa melihatnya dengan `cat bimo.onlinecamp.id` atau `sudo nano bimo.onlinecamp.id`

     ![gambar 6](assets/ssl6.png)
 
 * Setelah itu kita masukkan perintah `sudo nginx -t` untuk mengecek apakah konfigurasinya berhasil atau ada kesalahan

     ![gambar 7](assets/ssl7.png)

 * Terakhir kita bisa akses dibrowser dengan `https://bimo.onlinecamp.id`

     ![gambar 8](assets/ssl8.png)