---
author: "Faruq 1935"
draft: false
date: 2023-01-25T00:32:34Z
description: ""
title: "Cara Mengganti dan Menambahkan Repository Di Debian 11"
slug: cara-mengganti-repository-di-debian-11
featured_image: "source.png"
cascade:
    banner: 
    -
    
tags:
    - linux
    - cli
    - debian

categories:
    -

bahasa:
    -

topik:


---

Hallo kawan sinauriyen kembali lagi bersama admin Faruq kali ini saya akan menuliskan cara mengganti/memperbaharui repository linux di Debian 11.
Repository perlu di ganti jika kita tidak menemukan aplikasi/alat yang mau kita install dan gunakan atau repository terasa lambat biasanya perlu diganti ke repository lokal, Oke langsung saja kita lakukan:

### **1. Menuju File Konfigurasi source.list ?**
&nbsp;&nbsp;&nbsp;&nbsp;
`Pastikan kalian login sebagai superuser (root) ya`,
Langsung saja kalian ketikan perintah :
```shell
nano /etc/apt/source.list
```
> nano adalah text editor yang kita pakai.
`/etc/apt/source.list` adalah letak file konfigurasi repository Debian

### **2. Menambah/Mengganti Repository Baru**
&nbsp;&nbsp;&nbsp;&nbsp;
Maka akan muncul tampilan seperti ini.
Kalian langsung bisa menambah repository baru di barisan paling belakang.

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/repository-debian11/source.list.png "source.list")
&nbsp;&nbsp;&nbsp;&nbsp;

Misalkan disini saya akan mengganti dengan miror repository lokal Indonesia :

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/repository-debian11/lokal.png "source.list")
&nbsp;&nbsp;&nbsp;&nbsp;

Untuk mematikan/uncomment repository yang sudah tidak digunakan tambahkan tanda pagar **`#`** diawal repository

#### **Contoh**:
&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/repository-debian11/repomati.png "source.list")
&nbsp;&nbsp;&nbsp;&nbsp;

Setelah selesai kalian bisa keluar dari nano dengan perintah `ctrl + x ` teakn `y` dan `enter`.

##### **Eitss jangan lupa...**
setelah melakukan penggantian atau penambahan repository kalian harus melakukan perintah :
```shell
apt-get update
```
> untuk memperbaharui konfigurasi repository.

### **3. Beberapa Daftar Repository lokal Indonesia**
Repository lokal Indonesia digunakan agar proses update dan upgrade lebih cepat.

##### Berikut Daftar Repository Indonesia:
***
**Data Utama Surabaya**
```shell
deb http://kartolo.sby.datautama.net.id/debian/ bullseye main contrib non-free
deb http://kartolo.sby.datautama.net.id/debian/ bullseye-updates main contrib non-free
deb http://kartolo.sby.datautama.net.id/debian-security/ bullseye/updates main contrib non-free 
```

**Mirror Unej**
```shell
deb http://mirror.unej.ac.id/debian/ bullseye main contrib non-free
deb http://mirror.unej.ac.id/debian/ bullseye-updates main contrib non-free
deb http://mirror.unej.ac.id/debian-security/ bullseye/updates main contrib non-free 
```

**Kambing UI**
```shell
deb http://kambing.ui.ac.id/debian/ bullseye main contrib non-free
deb http://kambing.ui.ac.id/debian/ bullseye-updates main contrib non-free
deb http://kambing.ui.ac.id/debian-security/ bullseye/updates main contrib non-free 
```

**Kebo VLSM**
```shell
deb http://kebo.vlsm.org/debian/ bullseye main contrib non-free
deb http://kebo.vlsm.org/debian/ bullseye-updates main contrib non-free
deb http://kebo.vlsm.org/debian-security/ bullseye/updates main contrib non-free 
```

#### **Penutupan**
Sekian Artikel kali ini semoga bisa membantu jika ada pertanyaan bisa tulis di kolom kometar ya barlaku juga ada kesalahan di artikel ini 😃
Sampai Jumpa lagi 👋👋👋