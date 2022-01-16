# Webserver
## Setup Nginx Reverse Proxy
 * Pertama masuk keserver reverse proxy dan install nginx dengan menggunakan ansible

    ![gambar 1](assets/nginx1.png)

 * Setelah terinstall kita buat folder final
 * Kemudian kita buat file

   `bimo.onlinecamp.id`
   `api.bimo.onlinecamp.id`
   `jenkins.bimo.onlinecamp.id`
   `prometheus.bimo.onlinecamp.id`
   `monitoring.onlinecamp.id`

 * Buat config app frontend untuk file `bimo.onlinecamp.id`

    ![gambar 2](assets/nginx2.png)

 * simpan

 * Buat config app backend untuk file `api.bimo.onlinecamp.id`

    ![gambar 3](assets/nginx3.png)

 * simpan

 * Buat config jenkins untuk file `jenkins.bimo.onlinecamp.id`

    ![gambar 4](assets/nginx4.png)

 * simpan

 * Buat config prometheus untuk file `prometheus.bimo.onlinecamp.id`

    ![gambar 5](assets/nginx5.png)

 * simpan

 * Buat config monitoring untuk file `monitoring.bimo.onlinecamp.id`

    ![gambar 6](assets/nginx6.png)

 * simpan

 * Kemudian include folder final kedalam nginx.conf
 
    ![gambar 7](assets/nginx7.png)

 * Terakhir test apakah konfig sucsess dengan `sudo nginx -t`