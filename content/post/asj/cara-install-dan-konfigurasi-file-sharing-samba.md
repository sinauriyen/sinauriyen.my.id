---
author: "Faruq 1935"
draft: false
date: 2022-09-13T20:05:31+07:00
description: ""
title: "Cara Install Dan Konfigurasi File Sharing Samba Di Debian"
slug: cara-install-dan-konfigurasi-file-sharing-samba-di-debian
featured_image: "sambasinauriyen.png"
cascade:
    banner: 
tags:
    - server
    - linux
    - virtualbox
    - administrasi-sistem-jaringan

categories:
    - administrasi-sistem-jaringan

bahasa:
    -

topik:


---

### **Pengenalan file sharing SAMBA**
&nbsp;&nbsp;&nbsp;&nbsp;Samba adalah implementasi sumber terbuka dari protokol jaringan SMB/CIFS yang digunakan di lingkungan Windows untuk layanan bersama seperti akses file dan printer serta Active Directory. Samba juga dapat digunakan untuk membuat berbagi file lintas platform dalam konfigurasi yang disebut server standalone.

### **Keunggulan file sharing SAMBA**
&nbsp;&nbsp;&nbsp;&nbsp;Gratis atau free. Tersedia untuk berbagai macam platform. Mudah dikonfigurasi oleh administrator. Sudah terhubung langsung dengan jaringan dan jarang ditemui masalah dalam penggunaannya di jaringan.

Oke mungkin cukup penjelasan tentang file sharing SAMBA ya walaupun cuma sedikit :D

### **1. Menginstall file sharing SAMBA di Debian**

&nbsp;&nbsp;&nbsp;&nbsp;Sebelum menginstall package apapun biasakan update :

```shell
    apt update
```

Karena Operating sistem yang saya pakai Debian maka pakai `apt` ini juga bisa dipkai di Ubuntu dan turunan Debian yang lain:

```shell
    apt install samba -y
```

### **2. Konfigurasi file SAMBA**

&nbsp;&nbsp;&nbsp;&nbsp;Setelah berhasil di install kalian perlu mengkonfigurasi file SAMBA terlebih dahulu letaknya
ada di `/etc/samba/smb.conf`

lakukan backup terlebih dahulu file konfigurasi SAMBA supaya jika ada yang bermasalah bisa ambil dari file backup :

```shell
    cp /etc/samba/smb.conf /etc/samba/smb.conf-bak
```
Stelah di backup edit file :

```shell
    nano /etc/samba/smb.conf
```

![b](/assets/img/samba-configuration/samba-1.png "smb-conf")
&nbsp;&nbsp;&nbsp;&nbsp;

Kedmudian tambahkan konfigurasi baru di baris paling akhir :

```shell
[user-faruq]
path = /share/faruq
writeable = yes
browseable = yes
guest ok = no
security = user
```

Penjelasan syntax di atas : 

* `path` - Ini adalah letak file yang akan dibagikan di sistem file.
* `writeable` - Ini menetapkan apakah pengguna dapat menulis/menambahkan file diserver.
* `browseable` - Ini menetapkan apakah pengguna lain dapat melihat yang dapat dibagikan atau tidak.
  Mengaktifkan opsi ini hanya memungkinkan pengguna lain dari server Samba untuk melihat keberadaan share. Itu tidak memberikan izin baca atau tulis apa pun.
* `guest ok` - Jika `yes` Ini membuat izin kepada user tamu untuk bisa mengakses tapa password.
* `security` - Ini menempatkan password user untuk mengakses file.


**Jadinya seperti ini :**

![b](/assets/img/samba-configuration/samba-2.png "smb-conf")
&nbsp;&nbsp;&nbsp;&nbsp;

Setelah selesai simpan dan keluar **ctrl + x** lalu tekan **y** dan **enter**.

Untuk mengetes konfigurasi benar atau tidak laukan :

```shell
testparm
```
**Jika konfigurasi benar maka akan menampilkan seperti ini :**

![b](/assets/img/samba-configuration/samba-3.png "smb-conf")
&nbsp;&nbsp;&nbsp;&nbsp;

### **3. Membuat File Untuk Bisa Dibagikan**

&nbsp;&nbsp;&nbsp;&nbsp;Oh ya ini jangan lupa setelah itu buat file path `/home/faruq` :

```shell
mkdir /share
mkdir /share/faruq
chmod 777 /share/faruq
```
> * mkdir - untuk membuat file 
> * chmod 777 - membuat akses keseluruh user

### **4. Menambahkan User Baru File &nbsp;&nbsp;&nbsp;&nbsp;Sharing SAMBA**

&nbsp;&nbsp;&nbsp;&nbsp;Gunakan nama sesuka hati :
```shell
adduser --no-create-home user-faruq
smbpasswd -a user-faruq
```
>`adduser --no-create-home` - Artinya user-faruq directory home tidak akan dibuatkan


![b](/assets/img/samba-configuration/samba-4.png "smb-conf")
&nbsp;&nbsp;&nbsp;&nbsp;

![b](/assets/img/samba-configuration/samba-5.png "smb-conf")
>Masukan password yang mudah di ingat

### **5. Merestart konfigurasi File Sharing &nbsp;&nbsp;&nbsp;&nbsp;SAMBA**

&nbsp;&nbsp;&nbsp;&nbsp;Nah sudah selesai menginstall dan mengkonfigurasi file sharing SAMBA tinggal kita restart deh :

```shell
systemctl restart smbd.service
systemctl status smbd.service
```
![b](/assets/img/samba-configuration/samba-6.png "smb-conf")
&nbsp;&nbsp;&nbsp;&nbsp;

### **6. Melakukan Pengujian Di Client &nbsp;&nbsp;&nbsp;&nbsp;Terminal Linux**

&nbsp;&nbsp;&nbsp;&nbsp;Nah di sini saya akan menguji di Debian 11 XFCE.

Saya menggunakan thunar file manager pengelola file default di XCFE dan memiliki  fungsionalitas bawaan untuk mengakses share Samba.

Setelah membuka thunar file manager, lakukan langkah-langkah berikut :

1. Pilih Browse Network

![b](/assets/img/samba-configuration/samba-7.png "smb-conf")
&nbsp;&nbsp;&nbsp;&nbsp;

2. Ketikan di kolom pencarian network


```shell
smb://ip_address_server
```
![b](/assets/img/samba-configuration/samba-8.png "smb-conf")
&nbsp;&nbsp;&nbsp;&nbsp;

3. Mengakses file 

> Pilih Register User => isikan username dan password
![b](/assets/img/samba-configuration/samba-9.png "smb-conf")
&nbsp;&nbsp;&nbsp;&nbsp;

> Membuat folder 
![b](/assets/img/samba-configuration/samba-10.png "smb-conf")
&nbsp;&nbsp;&nbsp;&nbsp;

> Bisa membuat folder tanpa ada larangan
![b](/assets/img/samba-configuration/samba-11.png "smb-conf")
&nbsp;&nbsp;&nbsp;&nbsp;

Sudah selesai kita mengkonfigurasi file sharing samba, kalian juga bisa menambahkan
user baru agar cuma bisa menyalin file saja ya itu PR kalian :D