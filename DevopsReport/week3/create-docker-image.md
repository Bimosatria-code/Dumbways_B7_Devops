# Create Docker Image
    Pada Pembahasan ini kita akan membahas Pembuatan docker image untuk App Frontend dan App backend, berikut langkah-langkahnya:

# Create Docker Image App Frontend

 * Pertama-tama kita masuk keserver Tempat App Frontend 
 * Lalu didalam direktori dumbflix-frontend saya buat Dockerfile `sudo nano Dockerfile`
 * Lalu masukkan konfigurasi perintah untuk membuat image

    ![gambar 1](assets/image1.png)

 * Kemudian langkah selanjutnya build imagenya `sudo docker build -t bimsatpratams/dumbflix-frontend:1.0 .`

     ![gambar 2](assets/image2.png)

 * Setelah itu tunggu proses build selesai
 * Jika sudah selesai kita cek hasil build images dengan perintah `sudo docker images`

     ![gambar 3](assets/image3.png)

 * Setelah itu kita push images yang sudah dibuat ke repository docker.hub kita `sudo docker push bimsatpratams/dumbflix-frontend:1.0`

     ![gambar 4](assets/image4.png)

 * Kemudian tunggu sampai proses selesai dan jika sudah kita bisa cek di akun docker.hub kita

     ![gambar 5](assets/image5.png)


# Create Docker Image App Backend

 * Pertama-tama kita masuk keserver Tempat App Backend
 * Lalu didalam direktori dumbflix-backend saya buat Dockerfile `sudo nano Dockerfile`
 * Lalu masukkan konfigurasi perintah untuk membuat image

    ![gambar 6](assets/image6.png)

 * Kemudian langkah selanjutnya build imagenya `sudo docker build -t bimsatpratams/dumbflix-backend:1.0 .`

     ![gambar 7](assets/image7.png)

 * Setelah itu tunggu proses build selesai
 * Jika sudah selesai kita cek hasil build images dengan perintah `sudo docker images`

     ![gambar 8](assets/image8.png)

 * Setelah itu kita push images yang sudah dibuat ke repository docker.hub kita `sudo docker push bimsatpratams/dumbflix-backend:1.0`

     ![gambar 9](assets/image9.png)

 * Kemudian tunggu sampai proses selesai dan jika sudah kita bisa cek di akun docker.hub kita

     ![gambar 10](assets/image10.png)
