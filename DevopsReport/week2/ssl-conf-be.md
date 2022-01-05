# SSL Configuration App Backend

 * Kita akan memakai api yg minggu lalu
 * Kemudian masuk ke server aws yg menjadi gateway

     ![gambar 1](assets/sslbe1.png)

 * Setelah itu masuk kedalam direktorinya `cd .cloudflare/`
 * Setelah kita bisa cek file api.key `sudo cat api.key`

     ![gambar 2](assets/sslbe2.png)

 * Karena kita sudah menginstall certbot kita bisa langsung saja jalankan certbot `sudo certbot`
 * Dan kita pilih saja nomer `2. api.bimo.onlinecamp.id`

     ![gambar 3](assets/sslbe3.png)

 * Jika prosesnya sudah selesai kita cek sertifikasinya dengan masuk ke `cd /etc/nginx/dumbflix`
 * Lalu kita bisa melihatnya dengan `cat api.bimo.onlinecamp.id` atau `sudo nano api.bimo.onlinecamp.id`

     ![gambar 4](assets/sslbe4.png)
 
 * Setelah itu kita masukkan perintah `sudo nginx -t` untuk mengecek apakah konfigurasinya berhasil atau ada kesalahan

     ![gambar 5](assets/sslbe5.png)

 * Terakhir kita bisa akses dibrowser dengan `https://bimo.onlinecamp.id`

     ![gambar 6](assets/sslbe6.png)