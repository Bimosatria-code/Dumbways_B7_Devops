# Install Aplikasi Frontend dan Reverse Proxy
    Pada Pembahasan ini kita akan membahas bagaimana cara menginstall aplikasi kedalam linux server kita yang ada di VMWare dan membahas langkah-langkah pembuatan reverse proxy.

    Jadi apa itu reverse Proxy?

    Reverse Proxy adalah salah satu jenis Server Proxy yang bertanggungjawab dalam meneruskan request client ke server. Reverse Proxy terletak diantara client dan server.
    
    Jadi, request yang dilakukan client akan diteruskan oleh reverse proxy untuk mencapai ke server. Mudahnya, Reverse Proxy ini berada diantara client dan server yang bertugas untuk menjamin pertukaran data antara client dan server berjalan dengan lancar.

1. Frontend Dumbflix 
  
 * pertama tama kalian bisa buka terminal kalian lalu kalian bisa masuk ke server yang tadi sudah kalian buat. contoh punya saya disini adalah `ssh bimo@192.168.0.17` lalu masukan password kalian.

    ![gambar 1](assets/app1.png)

    ![gambar 2](assets/app2.png)


 * Kemudian setelah kita masuk kedalam server yang kita remote jalankan perintah `git clone https://github.com/sgnd/dumbflix-frontend.git` untuk mengclone aplikasi frontend yang akan kita gunakan.

    ![gambar 3](assets/app3.png)

 * Kemudian setelah aplikasi sudah berhasil kita clone kita install nodejs dengan perintah `curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash`

    ![gambar 4](assets/app4.png)

 * lalu masukkan perintah `exec bash`, perintah ini berguna ketika node dan npm kita tidak terdeteksi.

 * Kemudian install nodejs dengan `nvm install 14`

    ![gambar 5](assets/app5.png)

 * Lalu kita bisa cek version node js dan npm dengan perintah `node -v` lalu `npm -v`

    ![gambar 6](assets/app6.png)

 * Jika semua sudah dipastikan terinstall masuk ke direktori yang kita klone `dumbflix-frontend`

 * Kemudian jalankan perintah `npm install`

    ![gambar 7](assets/app7.png)

    ![gambar 8](assets/app8.png)

 * Setelah prosesnya selesai kita bisa coba jalankan aplikasi dengan perintah `npm start`

    ![gambar 9](assets/app9.png)

    ![gambar 10](assets/app10.png)

 * Jika aplikasi sudah running kita bisa jalankan dibrowser dengan memasukkan ip kita dan portnya yaitu port 3000 `192.168.0.17:3000`

    ![gambar 11](assets/app11.png)


 2. Reverse Proxy  
  
 * pertama-tama kita install nginx `sudo apt install nginx`.

 * Jika sudah kita cek statusnya dengan `sudo systemctl status nginx`

    ![gambar 12](assets/app12.png)

 * Kemudian kita masuk ke direktori /etc/nginx dengan perintah `cd /etc/nginx`

 * Lalu setelah masuk kita buat direktori Dumbflix `sudo mkdir Dumbflix`
    
    ![gambar 13](assets/app13.png)

 * Lalu kita masuk kedalam direktori Dumbflix dan membuat sebuah file yang berisi konfigurasi reverse proxy dengan perintah `sudo nano dumbflix.xyz`

    ![gambar 14](assets/app14.png)

 * Jika konfigurasi sudah dibuat klik `ctrl + x` lalu tekan `y` dan `enter`
 
 * Langkah selanjutnya adalah kita edit file nginx.conf yang berada di /etc/nginx dengan perintah `sudo nano nginx.conf` disini kita masukkan lokasi direktori yang kita buat tadi include /etc/nginx/Dumbflix/*; dan bintang diakhir adalah untuk mendeteksi semua file didalam direktori tersebut
    
    ![gambar 15](assets/app15.png)

 * setelah itu klik `ctrl + x` lalu tekan `y` dan `enter`

 * Lalu masukkan perintah `sudo nginx -t` untuk mengecek apakah konfigurasi terdapat masalah atau tidak

    ![gambar 16](assets/app16.png)

 * Kemudian reload nginx `sudo systemctl reload nginx`

    ![gambar 17](assets/app17.png)

 * Jika sudah selesai kita buat virtual host, kita pindah keserver lokal kita dan masukkan perintah `sudo nano /etc/hosts` kemudian masukkan password

    ![gambar 18](assets/app18.png)

 * Didalamnya kita bisa isikan alamat ip server dan nama domain yg tadi sudah kita set didalam konfigurasi reverse proxy

    ![gambar 19](assets/app19.png)

 * Kemudian setelah kita set virtual host dilokal kita, kita kembali keserver dan masuk direktori aplikasi kita dan jalankan `npm start`

    ![gambar 20](assets/app20.png)

 * Terakhir setelah aplikasi dirunning kita bisa akses dibrowser dengan domain `dumbflix.xyz`

    ![gambar 21](assets/app21.png)




