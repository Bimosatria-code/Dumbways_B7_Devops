# Install App Frontend in Server App AWS
    Pada Pembahasan ini kita akan membahas langkah-langkah menginstall aplikasi frontend kedalam server app AWS, berikut langkah-langkahnya:

 * pertama tama masuk kedalam server apps AWS kita

     ![gambar 1](assets/awsapp.png)

 * Kemudian update dan upgrade terlebih dahulu `sudo apt update` `sudo apt upgrade`
 * Setelah itu kita clone app frontend kita `git clone https://github.com/sgnd/dumbflix-frontend.git`

     ![gambar 2](assets/awsapp1.png)

 * Setelah aplikasi terclone kita masuk kedalam direktori aplikasinya `cd dumbflix-frontend`
 * Kemudian install node js `curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash`

     ![gambar 3](assets/awsapp2.png)

 * Kemudian `exec bash` agar bisa mendeteksi nvm dan npm
 * Lalu `nvm install 14`
 * Lalu `nvm use 14`

     ![gambar 4](assets/awsapp3.png)

 * Setelah itu kita cek versinya `node -v` `npm -v`

     ![gambar 5](assets/awsapp4.png)

 * Jika sudah kita `npm install`

     ![gambar 6](assets/awsapp5.png)

 * Jika sudah kita akan menjalankan aplikasi dengan pm2
 * Mula-mula kita install dulu pm2nya `npm install pm2 -g`

     ![gambar 7](assets/awsapp6.png)

 * Setelah pm2 sudah terinstall buat ecosystemnya jalankan perintah `pm2 ecosystem simple`

     ![gambar 8](assets/awsapp7.png)

 * Kemudian langkah berikutnya edit file ecosystem.config.js dibagian nama dan scriptnya`sudo nano ecosystem.config.js`

     ![gambar 9](assets/awsapp8.png)

     ![gambar 10](assets/awsapp9.png)

 * lalu jika sudah diedit klik `ctrl + x` lalu `y` dan `enter`
 * Sekarang kita jalankan aplikasi dengan perintah `pm2 start ecosystem.config.js`

     ![gambar 11](assets/awsapp10.png)

 * Terakhir kita bisa akses dibrowser dengan ip serverapp kita dan portnya `3.220.105.51:3000` 

     ![gambar 12](assets/awsapp11.png)
