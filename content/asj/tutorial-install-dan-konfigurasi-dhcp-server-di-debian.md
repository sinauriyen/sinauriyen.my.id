---
author: "Faruq 1935"
draft: false
date: 2022-07-30T07:55:43+07:00
description: ""
title: "Tutorial Install Dan Konfigurasi DHCP Server Debian Virtualbox"
slug: tutorial-install-dan-konfigurasi-dhcp-server-debian-virtualbox
featured_image: "dhcp.png"
cascade:
    banner: pin.png

tags:
    - dhcp-server
    - debian
    - virtualbox
    - linux

categories:
    - administrasi sistem-jaringan

bahasa:
    -

topik:
    -

---

DHCP(Dynamic Host Configuration Protocol) server adalah layanan pendistribusian alamat IP ke komputer client secara otomatis
## **Beberapa fungsi DHCP server**
1. Mengelola dan mendistribusi alamat ip
2. Mencegah IP conflict
3. Memperbaharui alamat IP secara otomatis
4. Mendukung penggunaan kembali alamat IP
   
Mungkin sedikit penjelasan tentang DHCP server diatas, oke langsung saja kita konfigurasi.

### **1. Menambahkan network adapter**
&nbsp;&nbsp;&nbsp;&nbsp;Karena kita menggunakan virtualbox maka harus menembahkan network adapter dulu di mesin virtual kita.

![b](/assets/img/dhcp-server/network-interface.png "network-interface")
&nbsp;&nbsp;&nbsp;&nbsp;

### **2. Menambahkan network interface**
&nbsp;&nbsp;&nbsp;&nbsp;Settelah masuk ke debian ketikan perintah            
* `nano /etc/network/interface` 

![b](/assets/img/dhcp-server/awal-net-inter.png "awal-net-inter")
* kemudian kalian tambahkan di bawah baris `iface enp0s3 inet dhcp`
* ketikan perintah seperti di bawah ini 
```python
    auto enp0s8
    iface enp0s8 inet static
            address 192.168.2.1
            netmask 255.255.255.0
```
![b](/assets/img/dhcp-server/hasil-network-interface.png "hasil-network-interfacetting")

Untuk keluar dari text editor nano tekan secara bersama **ctrl + x** lalu tekan **y** dan **enter**               
Selanjutnya kita perlu menghidupkan network interface yang sudah ditambahkan tadi dengan perintah:
* `ifup enp0s8`
* `ifup enp0s3`

Cek IP dengan perintah `ip a` 

![b](/assets/img/dhcp-server/ip-a.png "ip-a")
&nbsp;&nbsp;&nbsp;&nbsp;

### **3. Menginstall package DHCP server**
&nbsp;&nbsp;&nbsp;&nbsp;Sebelum menginstall package isc-dhcp-server tambahkan repository di `/etc/apt/sources.list`
dengan perintah `nano /etc/apt/sources.list` lalu tambahkan di baris paling akhir
* `deb http://ftp.us.debian.org/debian/ bullseye main contrib non-free`
* `deb-src http://ftp.us.debian.org/debian/ bullseye main contrib non-free`

![b](/assets/img/dhcp-server/source-list.png "source-list")
&nbsp;&nbsp;&nbsp;&nbsp; 

> Kemudian simpan keluar **ctrl + x** lalu tekan **y** dan **enter**.

Perintah untuk menginstall DHCP server
* `apt update && apt install isc-dhcp-server`

![b](/assets/img/dhcp-server/isc-dhcp-server-i.png "isc-dhcp-server-i")
&nbsp;&nbsp;&nbsp;&nbsp; 

### **4. Mengkonfigurasi DHCP server**
&nbsp;&nbsp;&nbsp;&nbsp;Langkah selanjutnya kita rubah konfigurasi isc-dhcp-server di file dengan mengetikan perintah
`nano /etc/dhcp/dhcpd.conf`

![b](/assets/img/dhcp-server/dhcp-conf.png "dhcp-conf")
&nbsp;&nbsp;&nbsp;&nbsp;

- kemuidan cari dan ubah di baris 50 sampai 58 atau secroll ke bawah sampai menemukan tulisan berikut :
  
![b](/assets/img/dhcp-server/dhcp-conf1.png "dhcp-conf1")
&nbsp;&nbsp;&nbsp;&nbsp;

- ikuti konfigurasi seperti di bawah :

![b](/assets/img/dhcp-server/dhcp-conf2.png "dhcp-conf2")
&nbsp;&nbsp;&nbsp;&nbsp;

> Cermati gambar, teliti dalam menghapus tanda pagar.

* setelah selesai simpan dan keluar **ctrl + x** lalu tekan **y** dan **enter**

Kita arahkan ke interface mana dhcp server akan menuju, pergi ke file `/etc/default/isc-dhcp-server` dengan perintah :
* `nano /etc/default/isc-dhcp-server`

![b](/assets/img/dhcp-server/dhcp-conf3.png "dhcp-conf3")
&nbsp;&nbsp;&nbsp;&nbsp;

> Ubah dibagian INTERFACEv4="" menjadi `INTERFACEv4="enp0s8"` karena kita mau mengarahkan dhcp server ke interface enp0s8, setelah itu simpan keluar.

### **5. Melakukan service restart dan status DHCP server**
&nbsp;&nbsp;&nbsp;&nbsp;Lakukan perintah untuk merestart DHCP server dan mengetahui status DHCP server sebagai berikut :
* `service isc-dhcp-server restart`
* `service isc-dhcp-server status`

![b](/assets/img/dhcp-server/dhcp-conf4.png "dhcp-conf4")
&nbsp;&nbsp;&nbsp;&nbsp;

### **6. Melakukan pengujian di client OS Windows 7**

&nbsp;&nbsp;&nbsp;&nbsp;Sebelum pengujian di clien Windows 7 virtualbox ubah dulu network adapter di setting seperti yang sudah di tambahkan di server Debian tadi

![b](/assets/img/dhcp-server/pengujian.png "pengujian")
&nbsp;&nbsp;&nbsp;&nbsp;

Kalian bisa pergi ke **Network and internet >> Network Coneections** pilih local area network atau aapter yang tersedia klik kanan pada adapter network kemudian status >> details

![b](/assets/img/dhcp-server/pengujian2.png "pengujian2")
&nbsp;&nbsp;&nbsp;&nbsp;

> Bisa dilihat di client Windows 7 mendaoatkan ip dari range 192.168.2.2 - 192.168.2.100

Cukup segitu penjelasan tentang DHCP server dan juga konfigurasinya di Debian kalau ada yang ingin di tanyakan silahkan bisa tulis di kolom komentar di bawah untuk kurang lebihnya saya minta maaf.

Sekian