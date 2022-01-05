# Installasi Linux Ubuntu Server di VMWare
Berikut adalah proses installasi Ubuntu Server di VMWare:

## Pertama 
### Siapkan aplikasi Virtual Box dan iso file ubuntu yg sudah didownload. Kemudian buka aplikasi VMWare dan Pilih Create a New Virtual Machine 

## Kedua 
### Kemudian akan muncul module dan browse lokasi tempat file iso ubuntu server kita berada,lalu klik next.

![gambar 1](assets/vm1.png)

## Ketiga 
### Lalu akan muncul form lalu isikan fullname, username kemudian password dan ulangi password. Jika sudah klik next.

![gambar 2](assets/vm3.png)

## Keempat 
### Kemudian pada virtual machine name isikan nama virtual machine yg kita inginkan dan pilih lokasi virtual machine kita nanti ditempatkan, lalu klik next.

![gambar 3](assets/vm4.png)

## Kelima 
### Kemudian pilih split virtual disk into multiple files dan isikan disk size sesuai yg kita butuhkan, lalu klik next.

![gambar 4](assets/vm5.png)

## Keenam 
### Selanjutnya kita costumize hardware disini kita setting network adaptor ke bridged supaya kita bisa terhubung dengan jaringan internet yg terhubung ke laptop kita dan kita set memory sesuai kebutuhan juga processor ubah menjadi 1 supaya ringan, lalu klik next.

![gambar 5](assets/vm6.png)

## Ketujuh 
### Kembali dan klik finish.

![gambar 6](assets/vm7.png)

## Kedelapan 
### Kemudian vmware akan memproses dan setelah itu akan muncul tampilan untuk memilih bahasa apa yang akan digunakan, disini saya memilih english lalu klik done.

![gambar 7](assets/vm8.png)

## Kesembilan 
### Di bagian installer update available kita pilih continue without updating. lalu tekan enter.

![gambar 8](assets/vm9.png)

## Kesepuluh 
### Kemudian pada Keyboard Configuration pilih sesuai yg kamu inginkan, tapi disarankan memilih English(US) pada bagian Layout dan variant. lalu pilih done dan enter.

![gambar 9](assets/vm10.png)

## Kesebelas 
### Kemudian pada bagian Network Connection kita bisa setup ip kita sendiri, pilih enp0se3 lalu pilih manual dan isikan ip wifi atau modem kita, lalu isi ip yg ingin kita custom, lalu isi gateway sesuai default gateway milik wifi kita lalu save. dan jika sudah klik done.

![gambar 10](assets/vm11.png)

![gambar 11](assets/vm12.png)

## Keduabelas 
### Kemudian pada Configuration proxy skip dan klik done

![gambar 12](assets/vm13.png)

## Ketigabelas 
### Lalu skip lagi pada bagian configure ubuntu archive mirror. lalu klik done.

![gambar 13](assets/vm14.png)

## Keempatbelas 
### lalu pilih custom storage layout dan klik done.

![gambar 14](assets/vm15.png)

## Kelimabelas 
### Kemudian kita buat partisinya partisi pertama kita buat untuk swap 2Gb setelah selesai klik create

![gambar 15](assets/vm16.png)

## Keenambelas 
### Kemudian kita buat partisinya partisi kedua kita buat sisanya untuk root ext4 setelah selesai klik create. Lalu setelah semua partisi  dibuat klik done dan ketika muncul module pilih continue.

![gambar 16](assets/vm17.png)

## Ketujuhbelas 
### Setelah itu isikan nama, nama server, username dan password. Ini semua berguna ketika nanti kita akan akses masuk kedalam ubuntu server. klik done

![gambar 17](assets/vm18.png)

## Kedelapanbelas 
### Kemudian di SSH Setup kita klik install OpenSSH Server, lalu klik done.

![gambar 18](assets/vm19.png)

## Kesembilanbelas
### Setelah itu kita akan masuk kepilihan Featured Server snaps, disini kita skip dan klik done.

![gambar 19](assets/vm20.png)

## Keduapuluh
### Lalu kita tunggu proses installasi sedang berjalan,setelah installasi selesai kita pilih reboot now.

![gambar 20](assets/vm21.png)

## Keduapuluhsatu
### Setelah direboot selesai kita akan diminta untuk login dan masukkan username dan password kita dan proses instalasi selesai kita bisa menggunakan ubuntu server kita.

![gambar 21](assets/vm22.png)