# Git and SSH Keygen
Git adalah sebuah version control management. version control memungkinkan kita untuk memperbaharui suatu dokumen, tetapi jika ada kesalahan atau error kita bsia kembali ke versi sebelumnya.

## Fork Repository App Backend
 * Pertama login kedalam akun github kita
 * Kemudian buka repository backend yang akan difork `https://github.com/sgnd/dumbflix-backend`
 * lalu setelah berada didalam repository backend pilih fork pada kakan atas sebelah watch 

    ![gambar fork 1](assets/fork1.png)

 * Setelah itu kita bisa cek didaftar repositori kita bahwa repository App Backend tadi sudah terfork dan berada direpository kita

     ![gambar fork 2](assets/fork2.png)


## SSH Keygen For Git
 * Untuk install Git kita bisa gunakan perintah `sudo apt install git -y`

    ![gambar 1](assets/git1.png)

 * Git config adalah perintah untuk pengaturan configurasi git dengan memasukkan username dan email yang terdaftar digithub.

    `git config --global user.name "nama github"`

    `git config --global user.email "email github"`

    ![gambar 2](assets/git2.png)

 * Untuk membuat sebuah keygen kita bisa memasukkan perintah `ssh-keygen`

    ![gambar 3](assets/git17.png)

 * Jika sudah kita bisa cek di direk tori /.ssh `cd ~/.ssh`kemudian `ls`

    ![gambar 4](assets/git18.png)

 * Kemudian buka isi dari file id_rsa.pub `cat id_rsa.pub`
 * Jika sudah copy isinya
 * Setelah itu buka menu setting di github kita
 * Kemudian pilih ssh and gpg keys
 * Lalu add ssh key dan masukkan ssh key kedalam key dan beri nama

    ![gambar 5](assets/git19.png)

 * Terakhir cek apakah ssh sudah berhasil terhubung dengan github `ssh -T git@github.com`

    ![gambar 6](assets/git20.png)

## Perintah dasar git

 * Git clone dari repository github `https://github.com/sgnd/dumbflix-backend.git`

    `git clone https://github.com/sgnd/dumbflix-backend.git`

    ![gambar 7](assets/git21.png)

 * Git init adalah perintah untuk menginisialisasi sebuah repositori lokal

    `git init`

    ![gambar 8](assets/git3.png)

 * Git status adalah perintah untuk mengecek status 

    `git status`

    ![gambar 9](assets/git4.png)

 * Git add adalah perintah untuk menandai file yang akan dipush kerepositori

    `git add nama file`

    ![gambar 10](assets/git5.png)

 * Git reset adalah perintah untuk membatalkan penandaan file

    `git reset nama file`

    ![gambar 11](assets/git6.png)

 * Git commit adalah perintah untuk melakukan commit pada perubahan ke head

    `git commit -m "first commit"`

    ![gambar 12](assets/git7.png)

 * Git remote adalah perintah untuk menghubungkan user dengan remote repository.
  - Sebelumnya kita buat sebuah repository di github kita

    `git remote add nama-remote git@github.com:Bimosatria-code/example.git`

    ![gambar 13](assets/git8.png)

    ![gambar 14](assets/git10.png)


 * Git push adalah perintah untuk mengupload data dari repository lokal ke repository github.

    `git push nama-remote nama-branch`

    ![gambar 15](assets/git11.png)

  - jika sudah bisa kita lihat direpository git kita dan refresh

    ![gambar 16](assets/git12.png)

 * Git branch adalah perintah untuk membuat percabangan.

    `git branch`

    `git branch nama-yang diinginkan`

    ![gambar 17](assets/git13.png)

 * Git checkout adalah perintah untuk berpindah branch

    `git checkout nama-branch`

    ![gambar 18](assets/git14.png)  


 * Git pull adalah perintah untuk mengupdate perubahan yang terjadi di website git

    `git pull nama-remote nama-branch`

    ![gambar 19](assets/git15.png)

 * Git merge adalah perintah untuk menyatukan dan menggabungkan percabangan.

    `git merge branch-aktif branch-tujuan`

    ![gambar 20](assets/git16.png)




