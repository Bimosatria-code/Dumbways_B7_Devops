# Reverse Proxy
    Pada Pembahasan ini kita akan membahas langkah- langkah reverse proxy dengan server dari AWS kita, berikut langkah-langkahnya:

 * pertama tama masuk keserver kita `ssh -i Dumbwayskeypair.pem ubuntu@35.175.30.82`

    ![gambar 1](assets/proxy1.png)

 * Kemudian Update dan Upgrade terlebih dahulu `sudo apt update` & `sudo apt upgrade -y`

    ![gambar 2](assets/proxy2.png)

    ![gambar 3](assets/proxy3.png)

 * Lalu jika sudah selesai kita install Nginx `sudo apt install nginx`

    ![gambar 4](assets/proxy4.png)

 * Setelah installasi selesai kita cek status nginx `sudo systemctl status nginx`

    ![gambar 5](assets/proxy5.png)

 * Kemudian kita masuk kedalam direktori /etc/nginx `cd /etc/nginx`
 * Lalu buat direktori dumbflix dan kita masuk kedalam direktori dumbflix 

    ![gambar 6](assets/proxy6.png)

 * Lalu buat file didalam direktori dumbflix dengan perintah `sudo nano bimo.onlinecamp.id`
 * Didalamnya kita bisa isikan seperti gambar dibawah

    ![gambar 7](assets/proxy7.png)

 * Setelah selesai kita bisa klik `ctrl + x` lalu tekan `y` dan `enter`
 * Kemudian mundur satu direktori
 * Lalu kita edit file nginx.conf `sudo nano nginx.conf` ini berguna untuk memberi akses lokasi kepada direktori dan file yang barusan kita buat

    ![gambar 8](assets/proxy8.png)
 
 * Setelah selesai kita bisa klik `ctrl + x` lalu tekan `y` dan `enter`
 * kemudian kita cek apakah ada kesalahan atau tidak dalam set confignya dengan `sudo nginx -t`

    ![gambar 9](assets/proxy9.png)

 * Lalu reload nginx `sudo systemctl reload nginx`
 * Kemudian arahkan domain dengan ip publik server yg dipakai untuk reverse proxy `35.175.30.82`

    ![gambar 10](assets/proxy10.png)

* Jika sudah kita bisa akses dibrowser dengan `http://bimo.onlinecamp.id`/

    ![gambar 11](assets/proxy11.png)