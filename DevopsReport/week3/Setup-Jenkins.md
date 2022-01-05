# Setup Jenkins
    Pada Pembahasan ini kita akan membahas langkah-langkah mensetup jenkins, berikut langkah-langkahnya:

## Requirements

 * Install plugin Publish Over SSH
 * Multipass Instance
 * ssh key
 * System configuration

 ## Configure System in Jenkins

 * install plugin `Publish Over SSH`

    ![gambar 1](assets/jdk1.png)

 * Pada hamalan dashboard masuk ke manage jenkins
 * kemudian pilih configuration system
 * cari publish over ssh
 * copy paste key ssh yg dibuat diserver
 * masukkan nama server yg kita inginkan
 * masukkan hostname server dengan ip server kita
 * input username

    ![gambar 2](assets/jdk2.png)

 * test koneksi SSH keserver

## Create Job
 * Pertama-tama masuk ke server jenkins
 * Klik Create Job
 * Masukkan nama project kemudian pilih freestyle project

    ![gambar 3](assets/jdk3.png)

 * Isikan pada bagian source code management pilih Git
 * masukkan repository dan branch yang digunakan

    ![gambar 4](assets/jdk4.png)

 * Pada build trigger pilih ` Github hook trigger for GITScm polling`

    ![gambar 5](assets/jdk5.png)

 * Kemudian pada build pilih `send files or execute commands over ssh`
 * kemudian masukkan name
 * Setelah itu ceklis `verbose output in console` untuk bisa melihat log buildnya
 * Pada bagian transfer set isi source file, remote directory dan exec command
 * Setelah itu set Execution time jadi 0
 * Kemudian Apply and save
 * Build manual dengan build now

## Create Job
 * Login ke akun Github
 * masuk ke halaman repository kita kemudian pilih setting
 * Kemudian Pilih webhook
 * Pilih add webhook
 * Masukkan hostname server jenkins di playload URL

    ![gambar 6](assets/jdk6.png)

 * Pilih just the push event
 * Setelah itu add webhook 