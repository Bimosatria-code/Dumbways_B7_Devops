# Setup Network di VMWare
Pada pembahasan kali ini kita akan mensetup network server kita yg berjalan di VMWare. Berikut adalah langkah-langkah setup network di VMWare:

## Pertama 
### Langkah pertama kita install dulu net-tools terlebih dahulu agar kita bisa mengakses perintah-perintah untuk mensetup network.

![gambar 1](assets/setup1.png)

## Kedua 
### Kemudian kita bisa cek konfigurasi ip kita dengan perintah ifconfig.

![gambar 2](assets/setup2.png)

## Ketiga 
### Langkah berikutnya untuk mensetup kita masuk direktori /etc/netplan kemudian edit file 00-installer-config.yaml dengan perintah nano.

![gambar 3](assets/setup3.png)

## Keempat 
### Didalam file tersebut edit addresses ip sesuai dengan ip yg kita inginkan, kemudian setting juga gatewaynya dan pada nameservers addresses masukkan dns google yaitu 8.8.8.8 .

![gambar 4](assets/setup4.png)

## Kelima 
### Terakhir test ping ip yg sudah kita setup barusan dengan perintah ping kemudian ip yg sudah disetup.

![gambar 5](assets/setup5.png)

