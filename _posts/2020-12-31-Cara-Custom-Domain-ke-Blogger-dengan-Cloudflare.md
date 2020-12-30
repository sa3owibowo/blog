---
layout: post
title:  Cara Custom Domain ke Blogger dengan Cloudflare
---
Adapun langkah- langkah dalam custom domain ke blogger melalui cloudflare yaitu,

**1. Mendaftar Cloudflare**<br/>
Langkah awal untuk memasang custom domain Blogger dengan Cloudflare adalah membuat akun di websitenya. Buka alamat berikut dan lakukan registrasi seperti biasa.
<pre><code>https://www.cloudflare.com</code></pre>
Gratis kok, ikuti saja semua langkahnya.

**2. Melakukan Pengaturan di Akun Blogspot**<br/>
Langkah selanjutnya, buka tab baru pada browser, ketikkan www.blogger.com. Kemudian login menggunakan akun blogger anda. Untuk melakukan custom domain ke blogger, klik pada tab `Settings` dan cek pada bagian `Publishing`. Silakan klik tulisan `custom domain`.

![_custom domain](https://www.domainesia.com/asset/uploads/2019/05/Screen-Shot-2020-09-02-at-9.46.03-AM.png)

Tuliskan `nama domain` yang ingin dilakukan custom domain. Misalnya www.satriowibowo.com. Pastikan menggunakan `www` ya. Lalu klik `Save`.

![_custom domain](https://www.domainesia.com/asset/uploads/2016/04/Screen-Shot-2020-09-02-at-9.46.21-PM-e1599062157516.png)

Maka akan ada error dari pihak blogspot. Mengapa itu bisa terjadi? Hal ini dikarenakan domain yang anda tuliskan belum ada sinkronisasi dari pihak blogger dan domain. Namun tenang saja! Jangan panik ya. Untuk melakukan sinkronisasi, terdapat **host unik** dan **record unik dari google** yang harus di masukkan ke pengaturan domain.

![_custom domain](https://www.domainesia.com/asset/uploads/2016/04/Screen-Shot-2020-09-02-at-10.46.24-PM-1-e1599062143528.png)

**3. Menambahkan CNAME Record**<br/>
Buka https://www.cloudflare.com tadi lagi, kemudian tambahkan record pada CNAME. Pada kolom Host, masukkan nama domain anda dan pada kolom kedua isikan ghs.google.com. Kemudian klik `Save Changes`.

![_custom domain](https://www.domainesia.com/asset/uploads/2018/01/Selection_245.png)

Masukkan **host unik** dan **record unik dari google.** Jangan lupa untuk memilih tipe `CNAME record`. **Ingat, setiap akun memiliki host unik dan record unik yang berbeda. Jadi, pastikan copy paste sesuai dengan yang tertera di akun blogger anda!**

![_custom domain](https://www.domainesia.com/asset/uploads/2018/01/Selection_246.png)
Catatan: **Pastikan anda telah menambahkan 4 A record yang berisi 4 IP address dari blogger dan 2 CNAME record!**

**4. Menambahkan A Record**<br/>
Nah, step ini merupakan hal yang penting karena anda harus mengarahkan IP Address Blogspot/ Blogger ke domain yang anda miliki. Masukkan A record lalu isikan hostname dan IP address dari blogger. Adapun IP address dari blogger/ blogger sendiri yaitu,

> 216.239.32.21<br/>
216.239.34.21<br/>
216.239.36.21<br/>
216.239.38.21

Isikan satu persatu IP Address Blogspot tersebut. Jangan lupa klik `Save Changes`.

![_custom domain](https://www.domainesia.com/asset/uploads/2018/01/Selection_244.png)

**4. Memasukkan Kembali Domain/ URL Pihak Ketiga**<br/>
Setelah pengaturan tadi anda tambahkan semua, hal selanjutnya yaitu silahkan login ke blogger.com lagi. coba reload browser atau coba tuliskan domain kembali dan klik `Save`. Bila masih tidak bisa, mohon bersabar karena mungkin Blogger masih dalam **proses propagasi** dengan DNS Anda yang dapat memakan waktu hingga 24 jam. **Jika lebih dari 24 jam juga belum bisa dilakukan, maka mungkin terdapat kesalahan pada pengaturan Anda** dan silakan coba lagi untuk yang kedua kali.

![_custom domain](https://www.domainesia.com/asset/uploads/2016/04/Screen-Shot-2020-09-02-at-9.46.21-PM-1-e1599101932541.png)

Jika proses `Simpan` sudah berhasil, maka Anda akan melihat halaman Settings di Blogger berisi nama domain dan nama blog lama. Misalnya www.satriowibowo.com dan dibawahnya terdapat nama blog lama berupa xxxx.blogspot.com. Agar alamat blogger bisa langsung terarah, silakan aktifkan `Redirect domain` dan jangan lupa centang bagian **Alihkan domain.com ke www.domain.com** lalu kil `Simpan`. Custom domain anda sudah berhasil dilakukan.

**5. Menunggu Proses Resolving DNS dan Update Konfigurasi**<br/>
Reminder, untuk proses custom domain ke Blogspot di Cloudflare ini memerlukan waktu **kurang lebih 24 jam** untuk resolving DNS dan update konfigurasi.
