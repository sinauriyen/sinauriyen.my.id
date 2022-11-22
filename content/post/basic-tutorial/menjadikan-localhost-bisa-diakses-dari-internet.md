---
author: "Faruq 1935"
draft: false
date: 2022-11-21T06:10:24Z
description: ""
title: "Menjadikan Localhost Bisa Diakses Dari Internet"
slug: menjadikan-localhost-bisa-diakses-dari-internet
featured_image: "ngrok.png"
cascade:
    banner: 

tags: 
   - linux
   - ngrok


categories:
    - basic-tutorial

bahasa:
    - Indonesia

topik:


---

### **`Pendahuluan`**

Salam sehat, kali saya akan membagikan cara menjadikan aplikasi localhost bisa diakses dari internet menggunakan **`ngrok`**

 #### **ngrok itu apa si ?**
Dari dokumetasi ngorok itu adalah proxy reverse yang membuat tunnel aman dari titik akhir publik ke layanan web yang berjalan secara lokal. ngrok menangkap dan menganalisis semua lalu lintas di tunnel untuk pemeriksaan dan pemutaran ulang nanti. 

 #### **ngrok bisa buat apa aja ?**
 
* Mengekspos layanan http apa pun di belakang NAT atau firewall ke internet di subdomain ngrok.com
* Mengekspos layanan tcp apa pun di belakang NAT atau firewall ke internet di port acak ngrok.com
* Periksa semua permintaan/respons http yang dikirimkan melalui terowongan
* Putar ulang setiap permintaan yang dikirimkan melalui terowongan

 #### **ngrok berfungsi untuk ?**
 
* Berbagi sementara situs web yang hanya berjalan di mesin pengembangan Anda
* Demo aplikasi di hackathon tanpa menerapkan
* Mengembangkan layanan apa pun yang menggunakan webhook (panggilan balik HTTP) dengan memungkinkan Anda memutar ulang permintaan tersebut
* Men-debug dan memahami layanan web apa pun dengan memeriksa lalu lintas HTTP
* Menjalankan layanan jaringan pada mesin yang di-firewall dari internet

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/ngrok/ngrok-banner.png "bootable-rufus")
&nbsp;&nbsp;&nbsp;&nbsp;

Oke langsung saja, cara install ngrok.

Pertama ya kalian pergi ke website [ngrok.com  ](https://ngrok.com "link Download")
kalian sign up terlebih dahulu di website ngroknya bisa menggunakan akun google atau github.
Setelah login kalian download ngrok di [ngrok download](https://ngrok.com/download "link Download") pilih sesuai Operating sistem kalian dan arsitektur processor kalian.

setelah kalian download lakukan perintah ini untuk Operating sistem linux: 

```shell
    sudo tar xvzf ~/Downloads/ngrok-v3-stable-linux-amd64.tgz 
```
Sesudah di ekstrak kalian ubah permission dan pindahkan ke /usr/bin file ngrok:

```shell
    chmod +x ngrok
    sudo mv ngrok /usr/bin
```

Atau kalian bisa install lewat apt khusus keturunan Debian:

```shell
    curl -s https://ngrok-agent.s3.amazonaws.com/ngrok.asc | sudo tee /etc/apt/trusted.gpg.d/ngrok.asc >/dev/null && echo "deb https://ngrok-agent.s3.amazonaws.com buster main" | sudo tee /etc/apt/sources.list.d/ngrok.list && sudo apt update && sudo apt install ngrok
```

Kemudian kalian connect kan ke akun ngrok kalian dengan perintah:
```shell
    ngrok config add-authtoken <token akun kalian>
```
> bisa didapat di dashboard ngrok.com setelah login

nah terus cara memakainya gimana ?
kalian bisa ketik:
```shell
    ngrok help
```
Jika output muncul seperti ini berarti kalian berhasil install ngrok:

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/ngrok/ngrok-help.jpg "bootable-rufus")
&nbsp;&nbsp;&nbsp;&nbsp;

Kemudian jika kalian ingin lokal network ( misal localhost port 1313 ) bisa diakses dari internet massukan perintah:
```shell
    ngrok http 1313
```
> Catatan: Service port 1313 harus dijalankan terlebih dahulu sebelum memasukan perintah diatas

#### **`Selamat localhost kalian bisa diakses dari internet`**

Kalian akan mendapatkan alamat forwarding yang bisa kalian akses dari browser: 

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/ngrok/ngrok-online.jpg "bootable-rufus")
&nbsp;&nbsp;&nbsp;&nbsp;

tampilan di browser:

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/ngrok/ngrok-final.jpg "bootable-rufus")
&nbsp;&nbsp;&nbsp;&nbsp;

oke selesai kalian juga bisa membuat server Minecraft sendiri loh dari ngrok ini karena ngrok juga support protokol **`TCP`**