---
layout: post
title: Cara Mengarahkan Domain Lama ke Domain Baru
---
Hal ini dilakukan ketika kamu ingin mengarahkan website dari domain lama ke domain baru secara menyeluruh.
> Sebagai contoh,<br/>
Domain lama: domainlama(dot)com<br/>
Ingin diarahkan ke domain baru : domainbaru(dot)com
Yang harus kamu lakukan yaitu:
1. Persiapkan `domain baru`.
2. Jika sudah, silakan buat `file .htaccess` di folder public_html.
3. Apabila file htaccess telah siap, silakan klik `Edit` kemudian tuliskan dengan kode berikut,

![_.htaccess](https://www.domainesia.com/asset/uploads/2017/05/4-1-920x380.jpg)

RewriteEngine On<br/>
RewriteCond %{HTTP_HOST} domainlama.com$<br/>
RewriteRule ^(.*) https://domainbaru.com/ [R=301,L]

Jangan lupa klik `Save Changes`.
