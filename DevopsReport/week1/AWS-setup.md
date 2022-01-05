# AWS Create & Setup Server
    Pada Pembahasan ini kita akan membahas bagaimana cara mengcreate dan mensetup server di AWS, berikut langkah-langkahnya:
  
## Create server for gateway

 * pertama tama buka AWS Educate dan login.

    ![gambar 1](assets/aws1.png)

 * lalu pilih myclassroom dan klik go to myclassroom

    ![gambar 2](assets/aws2.png)

 * Kemudian tekan Continue

    ![gambar 3](assets/aws3.png)

 * Lalu kita akan diarahkan ke `labs.vocareum.com` dan pilih aws console

    ![gambar 4](assets/aws4.png)

 * Kemudian kita pilih Launch a Virtual Machine With EC2

    ![gambar 5](assets/aws5.png)

 * Lalu selanjutnya search ubuntu dan kita pilih yang ubuntu 20.04 LTS dan tekan select

    ![gambar 6](assets/aws6.png)

 * Lalu pada step Choose an Instance Type pilih sesuai kebutuhan disini saya memilih t2 micro cpu 1 dan memory 1. Lalu next configure instance details

    ![gambar 7](assets/aws7.png)

 * kemudian pada step Configure Instance Details kita ubah dibagian Number of instance sesuai dengan berapa server yang ingin kita buat, lalu ubah juga Auto-assign public IP dengan disable supaya ketika server kita mati dan dijalankan kembali ip kita static/elastic tidak berubah. Lalu next add storage
 
    ![gambar 8](assets/aws8.png)

 * Lalu pada step Add Storage kita bisa ubah mau berapa size yg kita inginkan disini saya pilih defaultnya yaitu 8 dan klik add tags
 
    ![gambar 9](assets/aws9.png)

 * Lalu pada step Add tags kita bisa skip saja dan klik next configure security group
 
    ![gambar 10](assets/aws10.png)

 * Lalu pada step configure security group kita masukkan nama security group dan deskripsi. Kemudian kita add rule SSH, HTTP dan HTTPS lalu klik review and launch
 
    ![gambar 11](assets/aws11.png)

 * setelah itu kita bisa cek konfigurasi yg sudah kita masukkan di step review instance launch. jika sudah kita klik launch
 
    ![gambar 12](assets/aws12.png)

 * Kemudian akan muncul module untuk membuat key pair yg berguna untuk masuk keserver kita, disini kita bisa pilih create a new key pair lalu pilih rsa dan masukkan nama key pair kita lalu download key pair. Setelah terdownload kita pilih launch instance dan tunggu prosesnya
 
    ![gambar 13](assets/aws13.png)

 * Setelah proses selesai dan server kita sedah selesai dibuat kita masuk ke instance lalu edit nama server kita
 
    ![gambar 14](assets/aws14.png)

 * lalu kita set static ip dengan menggunakan elastic ip
 * kita masuk kepilihan elastic IPs lalu tekan allocate elastic ip address
 * lalu setelah itu pilih action dan associate
 
    ![gambar 15](assets/aws15.png)

    ![gambar 16](assets/aws16.png)

 * Kemudian pada bagian instance kita pilih server yang tadi kita buat lalu associate
 
    ![gambar 17](assets/aws17.png)

 * lalu kalian bisa kembali ke instances dan kalian bisa lihat elastic ip sudah kelihatan di server kalian tadi

    ![gambar 18](assets/aws18.png)

 * Kemudian buka terminal dan masuk server yang kita buat tadi
 * Setelah terminal terbuka kita masuk kedirektori tempat keypair kita terdownload
 * Kemudian masukkan perintah `sudo chmod 400 DumbwaysAWS.pem` untuk membuka lock pada keypair kita agar dapat digunakan
 * dan kita coba masuk server kita dengan perintah `ssh -i DumbwaysAWS.pem ubuntu@35.175.30.82`

    ![gambar 19](assets/aws19.png)


## Create Server For Apps

 * Pertama-tama kita klik launch instance  
 * Lalu selanjutnya search ubuntu dan kita pilih yang ubuntu 20.04 LTS dan tekan select

    ![gambar 20](assets/aws20.png)

 * Lalu pada step Choose an Instance Type pilih sesuai kebutuhan disini saya memilih t2 micro cpu 1 dan memory 1. Lalu next configure instance details

    ![gambar 21](assets/aws21.png)

 * kemudian pada step Configure Instance Details kita ubah dibagian Number of instance sesuai dengan berapa server yang ingin kita buat, lalu ubah juga Auto-assign public IP dengan disable supaya ketika server kita mati dan dijalankan kembali ip kita static/elastic tidak berubah. Lalu next add storage
 
    ![gambar 22](assets/aws22.png)

  * Lalu pada step Add Storage kita bisa skip saja pilih defaultnya storagenya 8, klik add tags
  * Lalu pada step Add Tags juga kita bisa skip saja, klik next configure security group
  * Lalu di Configure Security Group masukkan security group name dengan App-Frontend dan deskripsinya juga sama. Kemudian ad rule dan typenya dijadikan all traffic supaya bisa diakses dari semua port dan pilih `0.0.0.0/0`. lalu klik review and launch

    ![gambar 23](assets/aws23.png)

 * setelah itu kita bisa cek konfigurasi yg sudah kita masukkan di step review instance launch. jika sudah kita klik launch

    ![gambar 25](assets/aws25.png)

 * Kemudain akan muncule module untuk key pair, kita bisa pilih sama seperti sebelumnya saja
 * Lalu pilih launch saja
 * Selanjutnya setelah jadi kita ubah nama server kita dengan AppFrontend
 * Setelah itu kita allocate elastic ip untuk server app

    ![gambar 27](assets/aws27.png)

 * pilih action dan allocate elastic ip
 * setelah itu pada pilihan instance masukkan server app kita kemudian associate

    ![gambar 28](assets/aws28.png)

 * Kemudian kita bisa kembali ke instance untuk mengecek apakah sudah berhasil terbuat elastic ip untuk server app kita

    ![gambar 29](assets/aws29.png)

 * Terakhir kita buka terminal dan coba masuk kedalam server app kita dengan menggunakan ip server app kita, `ssh -i Dumbwayskeypair.pem ubuntu@3.220.105.51`

     ![gambar 30](assets/aws30.png)


