# AUTH
 ## Basic Auth Prometheus
 * Login server nginx
 * Install apache2-utils `sudo apt install apache2-utils`

     ![gambar 1](assets/auth1.png)

 * Buat direktori auth `sudo mkdir -f /etc/nginx/auth`
 * Buat password file `htpasswd -c /etc/nginx/auth/.htpasswd username
 * Kemudian isikan password
 * Buka reverse proxy prometheus dan edit

     ![gambar 2](assets/auth2.png)

 * Test config `sudo nginx -t`
 * Buka prometheus di browser

     ![gambar 3](assets/auth3.png)